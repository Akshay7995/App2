![WhatsApp Image 2022-02-07 at 12 20 48 PM](https://user-images.githubusercontent.com/98075789/152739378-1890ec9a-19e6-45a4-90b9-e582d35be78c.jpeg)
![WhatsApp Image 2022-02-07 at 12 20 23 PM](https://user-images.githubusercontent.com/98075789/152739391-2a78879e-4738-43f1-a889-e6eca14c505e.jpeg)
![WhatsApp Image 2022-02-07 at 12 19 51 PM](https://user-images.githubusercontent.com/98075789/152739396-36469831-940e-48e1-b734-b33636e2cdbb.jpeg)
![WhatsApp Image 2022-02-07 at 12 19 30 PM](https://user-images.githubusercontent.com/98075789/152739408-5bf47d6d-28f6-4af5-a1b0-35c6a38d7681.jpeg)
import React from 'react';
import { useState } from 'react';
import { StyleSheet, Text, View,SafeAreaView ,ImageBackground,Image,TouchableOpacity,Button} from 'react-native';


import { ScrollView } from 'react-native';



const App = ()=> 
{
  const image= {uri:'src/images/back.png'}
    const[count,myCount]=useState(0);

 return (
     
      <View style={styles.container}>
        <ScrollView>
       
       <Text style={{textAlign:'center', marginTop:30,marginBottom:40,fontSize:20,padding:30,backgroundColor:'#ce9ffc'}}>COUNTER APPLICATION</Text>

       
       <TouchableOpacity
       style={styles.triangleShape}
       onPress={()=>{myCount(count+1)}}>
           <Text>press</Text>
     </TouchableOpacity>

     <Text style={{textAlign:'center', padding:30}}>{count}</Text>
   
     <TouchableOpacity
       style={styles.lowertriangle}
       onPress={()=>{myCount(count-1)}}>
           
     </TouchableOpacity>
     
     <TouchableOpacity title="reset" onPress={()=>{myCount(0)} 
      }  style={styles.reset}>
        
        
        <Text style={{fontSize:30}}>RESET</Text>
      </TouchableOpacity>

     
    </ScrollView>

    <Text style={styles.name}>Designed By ENUGURUAKSHAY</Text>    
   </View>
      
  );
   
 }

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#feb672',
    //alignItems: 'center',
    //justifyContent: 'center',
  },
  triangleShape: {
    marginLeft:110,
  width: 0,
  height: 0,
  borderBottomWidth: 120,
  borderLeftWidth: 60,
  borderRightWidth: 60,
  backgroundColor: 'transparent',
  borderLeftColor: 'transparent',
  borderRightColor: 'transparent',
  borderBottomColor: '#f42e78'
},
lowertriangle: {
  marginLeft:110,
  width: 0,
  height: 0,
  borderTopWidth: 120,
  borderRightWidth: 60,
  borderLeftWidth: 60,
  borderRightColor: 'transparent',
  borderBottomColor: 'transparent',
  borderLeftColor: 'transparent',
  borderTopColor: "#f42e78",
},

reset:
{
  alignItems:'center',
  marginTop:50,
  marginRight:30,
 
},
icon:
{
  alignItems:'center',
  marginTop:-30,
  marginLeft:320,
  
},

name:
{
  textAlign:'center',
  
}



  
});

export default App;
