# Basic parameterized case
Simple parameterized case for openscad

**Example**

``` 
// Render options
case_part        = "case_all";
render_mode      = "normal";

// Board values
dim_board        = [60,30,2];
space_top        = 7;
space_bottom     = 3;
space_bscrew     = 1;

// Board Screw values
dia_bscrew       = 3.2;
loc_bscrews      = [[3.5,3.5],
                    [dim_board[0]-3.5,3.5],
                    [dim_board[0]-3.5,dim_board[1]-3.5],
                    [3.5,dim_board[1]-3.5]];                    

// Case Screw values
dia_cscrew       = 3;
dia_chead        = 5.5;
height_chead     = 2.5;
                    
// Case values
wall_frame       = 1.2;
rim              = 1;
mki              = 2;
                  
// ports
cuts             = [[[0,0],[5,3],"front","sqr_indent"],       
                    [[0,0],[5,3],"back","sqr_indent"],
                    [[0,0],[5,3],"left","sqr"],
                    [[0,0],[5,3],"right","sqr"],
                    [[0,0],[5,3],"top","sqr"],
                    [[0,0],[5,3],"bottom","sqr_indent"],
                    ];

case(part=case_part,
     render_mode=render_mode,
     
     wall_frame=wall_frame,
     rim=rim,
     mki=mki,
     port_length=wall_frame+rim,
          
     dim_board=dim_board,
     cuts=cuts,
     space_top=space_top,
     space_bottom=space_bottom,
     space_bscrew=space_bscrew,

     dia_cscrew=dia_cscrew,
     dia_chead=dia_chead,
     height_chead=height_chead,
     
     dia_bscrew=dia_bscrew,
     loc_bscrews=loc_bscrews);
```
