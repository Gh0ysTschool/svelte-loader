script
    

style
    .shawbrook-loader 
        width: 7rem
        height: 4rem
        display: flex
        justify-content: center
        background: linear-gradient(40deg,var(--clr0), #141414)
        box-shadow: black 1px 1px
    
    .shawbrook-loader-dot 
        position: absolute
        transform-origin: bottom
        width:1rem
        height: 2rem
        :after    
            content: ''
            position: absolute
            width: 1rem
            height: 1rem
            background: radial-gradient(var(--clr2), var(--clr2) 0.1rem, transparent 0.1rem)
            animation: 1.6s pulse infinite
        
    for i in 1 2 3 4 5 6 7 8

        .shawbrook-loader-dot
            :nth-child(i) 
                animation-delay:i*0.2s
                transform: rotate(i*45deg)

            :nth-child(1):after 
                animation-delay:calc(i*0.2s)
    
    @keyframes pulse
        0% transform: scale(1)
        40% transform: scale(2.4)
        100% transform: scale(1)

.shawbrook-loader
    for x in [...Array(8),keys]
        .shawbrook-loader-dot
