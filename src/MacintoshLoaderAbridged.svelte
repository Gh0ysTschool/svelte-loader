script
    

style
   
    spinner-size  75px !default
    spinner-color  #69717d !default
    overlay-color  black !default

    absolute-center()
        position  absolute
        left  0
        right  0
        top  0
        bottom  0
        margin  auto
    

    .overlay 
        background  rgba( overlay-color,.9)
        absolute-center()
    
        
    .spinner 
        font-size   spinner-size
        position  relative
        display  inline-block
        width  1em
        height  1em

        .center 
            absolute-center()
    
    

    .spinner-blade 
        position  absolute
        left  .4629em
        bottom  0
        width  .074em
        height  .2777em
        border-radius  .5em
        background-color  transparent
        transform-origin  center -.2222em
        animation  spinner-fade 1s infinite linear


        for i in 1 2 3 4 5 6 7 8 9 10 11 12 
            :nth-child(i) 
                animation-delay  .083 * (i-1)
                transform  rotate(30deg * (i-1))
            
    @keyframes spinner-fade 
        0% 
            background-color   spinner-color
        100% 
            background-color  transparent
    
    
.overlay
    .spinner.center
        for i in [...Array(12).keys]
            .spinner-blade