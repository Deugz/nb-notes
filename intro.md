% Thesaurus script (need to be in the head)

<script src='https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.js'></script>
<script type="text/javascript" src="https://vocabs.ardc.edu.au/apps/assets/vocab_widget/js/vocab_widget_v2.js"></script>
<link rel="stylesheet" type="text/css" href="https://vocabs.ardc.edu.au/apps/assets/vocab_widget/css/vocab_widget_v2.css" />
<script type="text/javascript" src="https://vocabs.ardc.edu.au/assets/core/lib/qtip2/jquery.qtip.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/qtip2/2.2.1/basic/jquery.qtip.min.css" media="screen" />

```{image} _static/Images/Title-nb-notes.png
:width: 100%

```

<br>
<br>



Transcend my own work, whole problematic (exhaustive overview)

- Planet formation
- Amorphous Ice


```{note}

rethink the sections

```

- [Gallery to include](https://codepen.io/GreenSock/pen/JjeRNGz)

## Tags

I use the Unified Astronomy thesaurus to link the different pages and improve their discoverability

- [Source](https://vocabs.ardc.edu.au/viewById/119)

<input type="text" id="the-unified-astronomy-thesaurus" name="the-unified-astronomy-thesaurus" value="" size="80" autocomplete="off">
<script>
$("#the-unified-astronomy-thesaurus").qtip({
    content:{text:'<div class="subject_chooser"></div>'},
    prerender:true,
    position:{
        my:'center left',
        at: 'center right',
        viewport:$(window)
    },
    show: {event: 'click',ready:false},
    hide: {event: 'unfocus'},
    events: {
        render: function(event, api) {
            var widget = $(".subject_chooser", this).vocab_widget({mode:'tree',
                repository:'http://vocabs.ardc.edu.au/repository/api/lda/aas/the-unified-astronomy-thesaurus/5-0-0',
                endpoint:'https://vocabs.ardc.edu.au/apps/vocab_widget/proxy/' ,
                display_count:false});
            widget.on('treeselect.vocab.ands', function(event) {
                var target = $(event.target);
                var data = target.data('vocab');
                $("#the-unified-astronomy-thesaurus").val(data.label);
            });
            api.elements.content.find('.hasTooltip').qtip('repopsition');
            api.elements.content.find('.hasTooltip').qtip('update');
        }
    },
    style: {classes: 'qtip-bootstrap ui-tooltip-shadow ui-tooltip-bootstrap ui-tooltip-large'}
});
</script>


```{note}

Would be good to create a knowledge graph (interactif ?) with the full thesaurus

```


# Comments



:::::::{div} full-width

::::::{grid} 3

:::::{grid-item-card}
:class-header: bg-light
:columns: 5

**Notes**
^^^

<br>

<blockquote class="trello-card"> 
  <a href="https://trello.com/c/WTiMvieA/3-intromd">Trello Card</a>
</blockquote>
<script src="https://p.trellocdn.com/embed.min.js"></script>


:::::



:::::{grid-item-card}
:class-header: bg-light
:columns: 4
**Page**
^^^

<br>

- Author:  Vincent Deguin;
- Status:  &#9989; <span class="hovertext" data-hover="To be Reviewed">🔎</span>
- Reviewed: <span class="hovertext" data-hover="Insert here who has done what">&#x274C;</span>
- Updated: 28/05/2023



   
:::::

:::::{grid-item-card}
:class-header: bg-light
:columns: 3
<span style="float: right">![flag alt >](_static/Svg_icons/coins-money-svgrepo-com.svg)</span>**Help** 
^^^

<br>

<script type='text/javascript' src='https://storage.ko-fi.com/cdn/widget/Widget_2.js'></script><script type='text/javascript'>kofiwidget2.init('Buy me a coffee', '#317315', 'O4O6EZO78');kofiwidget2.draw();</script> 

<br>
<br>

or

<br>

![flag alt >](_static/Svg_icons/patreon-svgrepo-com.svg) [Patreon](https://www.patreon.com/Science_for_the_People) 

:::::
::::::
:::::::


***

::::{div} full-width

- ![GitHub last commit](https://img.shields.io/github/last-commit/Deugz/nb-notes?color=green&style=plastic) - ![GitHub repo size](https://img.shields.io/github/repo-size/Deugz/nb-notes?color=yellow&style=plastic) - ![GitHub contributors](https://img.shields.io/github/contributors/Deugz/nb-notes?color=red&style=plastic) - ![visitors](https://page-views.glitch.me/badge?page_id=https://deugz.github.io/nb-notes/_build/html/intro.html) - ![watchers](https://img.shields.io/github/watchers/Deugz/nb-notes?style=social) - ![stars](https://img.shields.io/github/stars/Deugz/nb-notes?style=social)
      
::::


***

<script src="https://utteranc.es/client.js"
        repo="Deugz/nb-notes"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>


