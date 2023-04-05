# EditREADME

# App.js code

import './App.css';
import Collapsible from './components/Collapsible';


function App() {
  return (
    <div className="App">

      <Collapsible className='name' label = 'Banner with Images'>
        <h1>This is collapsible</h1>
        <a href='./Collapsible.js'> 
        <img title='Royal Enfiled' src='https://wallpapers.com/images/featured/7jd7dnumdmtmc6ze.jpg' alt='Royal Enfiled'></img></a>
        <p>Royal Enfield was a brand name under which <strong>The Enfield Cycle Company Limited of Redditch </strong> , Worcestershire sold motorcycles, bicycles, lawnmowers and stationary engines which they had manufactured. Enfield Cycle Company also used the brand name "Enfield" without the "Royal".</p>

        <a href='./Collapsible.js'> 
        <img title='Yamaha' src='https://wallpaperaccess.com/full/1766860.jpg' alt='Yamaha'></img></a>

        <p><strong>Yamaha Motor Co., Ltd.</strong>  is a Japanese multinational manufacturer of motorcycles, marine products such as boats and outboard motors, and other motorized products. The company was established in 1955 upon separation from Yamaha Corporation</p>
        
      </Collapsible>
      <Collapsible label = 'Banner with List'>

      
        <ol>
          <a href='./Collapsible.js'>
          <li><img title='Thar' src='https://imgd-ct.aeplcdn.com/1056x660/n/cw/ec/40087/thar-exterior-right-rear-three-quarter.jpeg?q=75' alt='Thar'></img>MAHINDRA THAR</li></a>
          <p> The Thar was first introduced in 2010 as a modernized version of the Mahindra Legend, which was based on the Mahindra MM540, a vehicle that was in production in India since the 1980s. The Mahindra Thar was designed to be a rugged, reliable, and affordable off-road vehicle that could handle the rough terrain found in many parts of India. The Thar's design is based on the iconic Jeep CJ series, which Mahindra had been producing under license since the 1940s.</p>


          <a href='./Collapsible.js'>
            <li><img title='BMW' src='https://img5.goodfon.com/wallpaper/nbig/6/17/kerem-cayci-by-kerem-cayci-bmw-m850i-bmw-m850i-bmw-m-850i-fu.jpg' alt='BMW'></img> BMW</li>
          </a>
          <p><strong>Bayerische Motoren Werke AG, abbreviated as BMW</strong>is a German multinational manufacturer of luxury vehicles and motorcycles headquartered in Munich, Bavaria. The corporation was founded in 1916 as a manufacturer of aircraft engines, which it produced from 1917 until 1918 and again from 1933 to 1945.</p>

        </ol> 


      </Collapsible>
      <Collapsible label= 'Banner with Input Types' >

      <label>Choose date</label>
        <input type='date'></input>
        <br></br>

        <label>Choose Time</label>
        <input type='time'></input>
        <br></br>

        <label>Choose Multiple Files</label>
        <input type='file' multiple></input>
        <br></br>

        <label>Choose COlor</label>
        <input type='color'></input>
        
        <br></br>

        
      </Collapsible>
   
    </div>
  );
}

export default App;




# component

import React, { useState } from 'react'

function Collapsible(props) {

    const [isOpen, setIsOpen] = useState (false);

  return (
    <div className='collapsible'>
        <button className='togg' onClick={() => setIsOpen(!isOpen)}>
            {props.label} 
        </button>
        {isOpen && <div className='content'>{props.children}</div> } 

    </div>
  )
}

export default Collapsible

# App.CSS



*{
  font-family: sans-serif;
}

.collapsible{
  background-color:#75E6DA ;
  
}

.togg{
  padding: 10px;
  width: 100%;
  padding: 10px;
  margin-bottom: 10px;
  margin-top: 10px;
   font-size: 1.3rem;
  font-family: sans-serif;
  background-color: #189AB4;
}

img{
  display: inline-block;
  width: 40%;
  padding: 10px;
  border-radius: 40px;
}

input{
  margin: 20px;
  padding: 20px;
}


h1{
  background-color: #189AB4;
  text-align: center;
}

p{
  text-align: justify;
  padding: 10px;
  background-color: #189AB4;
}
