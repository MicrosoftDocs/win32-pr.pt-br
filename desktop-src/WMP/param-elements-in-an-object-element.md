---
title: Elementos PARAM em um elemento OBJECT
description: Elementos PARAM em um elemento OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Windows Media Player, elementos PARAM no elemento OBJECT
- Windows Media Player modelo de objeto, elementos PARAM no elemento OBJECT
- modelo de objeto, elementos PARAM no elemento OBJECT
- Windows Media Player Elementos Mobile,PARAM no elemento OBJECT
- Windows Media Player ActiveX controle, elementos PARAM no elemento OBJECT
- Windows Media Player Controle ActiveX dispositivo móvel, elementos PARAM no elemento OBJECT
- ActiveX controle, elementos PARAM no elemento OBJECT
- incorporação, páginas da Web
- Incorporação de página da Web, elementos PARAM no elemento OBJECT
- Elementos PARAM no elemento OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da684a39739703038793abb2f4fdd32b924f35cdffc0c0f9d796fb7dbb5532b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054424"
---
# <a name="param-elements-in-an-object-element"></a>Elementos PARAM em um elemento OBJECT

Windows Media Player usa o elemento PARAM para definir condições de inicialização específicas para o controle. O elemento PARAM é inserido dentro do elemento OBJECT.

Por exemplo, se você quiser definir se a propriedade **autoStart** é True, você inseriria o elemento PARAM dentro do elemento OBJECT.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



Você pode ter quantos elementos PARAM em um elemento OBJECT quiser. O PARAM tem dois atributos, nome e valor. Ambos os atributos devem ser definidos.

Os atributos PARAM com suporte variam ligeiramente entre navegadores e tipos mime. A tabela a seguir mostra os atributos com suporte pelos navegadores Internet Explorer e Firefox. O tipo mime preferencial para o navegador Firefox é application/x-ms-wmp, no entanto, há vários outros tipos mime que você pode usar para inserir o controle Player em uma página da Web hospedada pelo navegador Firefox. A quarta coluna da tabela mostra os atributos com suporte quando você usa um tipo mime diferente de application/x-ms-wmp.



| Nome do PARAM                                            | Internet Explorer | Firefox com o tipo mime application/x-ms-wmp | Firefox com qualquer outro tipo mime |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Autostart](settings-autostart.md)                   | sim               | sim                                         | sim                              |
| [Equilíbrio](settings-balance.md)                       | sim               | sim                                         | sim                              |
| [Baseurl](settings-baseurl.md)                       | sim               | sim                                         | sim                              |
| [captioningID](closedcaption-captioningid.md)        | sim               | sim                                         | sim                              |
| [Currentmarker](controls-currentmarker.md)           | sim               | sim                                         | sim                              |
| [Currentposition](controls-currentposition.md)       | sim               | sim                                         | sim                              |
| [defaultFrame](settings-defaultframe.md)             | sim               | não                                          | não                               |
| [enableContextMenu](player-enablecontextmenu.md)     | sim               | sim                                         | sim                              |
| [Habilitado](player-enabled.md)                         | sim               | sim                                         | sim                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | sim               | sim                                         | não                               |
| **fileName**                                          | não                | sim                                         | sim                              |
| [Fullscreen](player-fullscreen.md)                   | sim               | não                                          | não                               |
| [Invokeurls](settings-invokeurls.md)                 | sim               | não                                          | não                               |
| [Mudo](settings-mute.md)                             | sim               | sim                                         | sim                              |
| [playCount](settings-playcount.md)                   | sim               | sim                                         | não                               |
| [Taxa](settings-rate.md)                             | sim               | sim                                         | sim                              |
| [SAMIFileName](closedcaption-samifilename.md)        | sim               | sim                                         | sim                              |
| [SAMILang](closedcaption-samilang.md)                | sim               | sim                                         | sim                              |
| [SAMIStyle](closedcaption-samistyle.md)              | sim               | sim                                         | sim                              |
| **ORIG**                                               | não                | sim                                         | sim                              |
| [stretchToFit](player-stretchtofit.md)               | sim               | sim                                         | não                               |
| [URL](player-url.md)                                 | sim               | sim                                         | sim                              |
| [volume](settings-volume.md)                         | sim               | sim                                         | sim                              |
| [windowlessVideo](player-windowlessvideo.md)         | sim               | sim                                         | sim                              |



 

> [!Note]  
> Os elementos **filename** e **src** param são suportados pelo plug-in do Firefox, mas não pelo Internet Explorer. Ambos executam a mesma função que o elemento param de **URL** .

 

Consulte a [referência de modelo de objeto para scripts](object-model-reference-for-scripting.md) para obter mais detalhes sobre os valores de cada atributo de nome.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**usando o controle de Windows Media Player em uma página da Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




