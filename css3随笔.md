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
    
