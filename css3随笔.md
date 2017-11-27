## 多行省略
    
    overflow : hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical
    

## 单行省略
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    
    
## 0.5px border
    div{
       border:1px solid black;
    }
    
    @media (-webkit-min-device-pixel-ratio: 2){
     div{
        border-width:0.5px;
     }
    }

## flex均分
       .parent{
            display: -webkit-flex;
	      	-webkit-flex-direction: row;
	      	display: flex;
	      	flex-direction: row;
	    }
        
        .children{
            -webkit-flex: 1;
      		flex: 1;
        }
	
	// flex子元素上下左右距中
	.parent{
	    justify-content: center;
            align-items: center;
	}
        
##  硬件加速 will-change:contents;
        
## 无线的滚动
    
    overflow-x: scroll;
    overflow-scrolling: touch;
    -webkit-overflow-scrolling: touch;
    
## png透明 1px http://png-pixel.com/
  data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR42mNkYAAAAAYAAjCB0C8AAAAASUVORK5CYII=  
  
  
  
