# hide-youtube-related-videos
hide youtube related videos
 ```
     let relatedbtn = document.createElement('button')
    relatedbtn.style = 'background: brown; border: 0; padding: 5px 13px; cursor: pointer; color: white; border-radius: 4px; outline:none;'
    let relatedVideos = document.querySelector('#items > ytd-item-section-renderer')
    document.querySelector('#chips').appendChild(relatedbtn)
    document.querySelector('#chips').prepend(relatedbtn)

    relatedbtn.textContent = 'alternar'
    relatedVideos.dataset.toggle = 'hide'

    function toggleRelated(opt){
        if(opt == 'hide'){
            relatedVideos.style.visibility = 'hidden'
            relatedVideos.dataset.toggle = 'hide'

        }else if(opt == 'show'){
            relatedVideos.style.visibility = 'visible'
            relatedVideos.dataset.toggle = 'show'
        }

    }

    relatedbtn.onclick = function(){
        if(relatedVideos.dataset.toggle == 'show'){
            toggleRelated('hide')
        }else if(relatedVideos.dataset.toggle == 'hide'){
            toggleRelated('show')
        }
    }
 ```
