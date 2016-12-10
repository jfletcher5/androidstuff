# androidstuff
beginner apps

Notes on Custom Methods: example below:

 - void if returning no value
      - if returning a value, you must have a 'return' piece of code somewhere in the method
      - 
{
public void savePlayer (View view){

        Log.i("test", "test");

        ListView listView = (ListView) findViewById(R.id.members);

        TextView playerName = (TextView) findViewById(R.id.nameInput);
        TextView playerAge = (TextView) findViewById(R.id.ageInput);
        pName = playerName.getText().toString();

        memberMap.put(pName, playerAge.getText().toString());

        Toast.makeText(getApplicationContext(), "New user added. Name: "+ pName + ". Age: "+memberMap.get(pName),         Toast.LENGTH_LONG).show();

        myList.add(pName);

        ListAdapter myAdapter = new ArrayAdapter(this, android.R.layout.simple_list_item_1, myList);

        listView.setAdapter(myAdapter);
    }
    
   }
