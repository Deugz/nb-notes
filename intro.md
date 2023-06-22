% Thesaurus script (need to be in the head)

<script src='https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.js'></script>
<script type="text/javascript" src="https://vocabs.ardc.edu.au/apps/assets/vocab_widget/js/vocab_widget_v2.js"></script>
<link rel="stylesheet" type="text/css" href="https://vocabs.ardc.edu.au/apps/assets/vocab_widget/css/vocab_widget_v2.css" />
<script type="text/javascript" src="https://vocabs.ardc.edu.au/assets/core/lib/qtip2/jquery.qtip.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/qtip2/2.2.1/basic/jquery.qtip.min.css" media="screen" />


# Notes

Transcend my own work, whole problematic (exhaustive overview)

- Planet formation
- Amorphous Ice


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

