---
title: Elementos PARAM em um elemento OBJECT
description: Elementos PARAM em um elemento OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Windows Media Player, elementos PARAM no elemento OBJECT
- Modelo de objeto do Windows Media Player, elementos PARAM no elemento OBJECT
- modelo de objeto, elementos PARAM no elemento OBJECT
- Windows Media Player Mobile, elementos PARAM no elemento OBJECT
- Controle ActiveX do Windows Media Player, elementos PARAM no elemento OBJECT
- Controle ActiveX móvel do Windows Media Player, elementos PARAM no elemento OBJECT
- Controle ActiveX, elementos PARAM no elemento OBJECT
- inserindo, páginas da Web
- Inserção de página da Web, elementos PARAM no elemento OBJECT
- Elementos PARAM no elemento OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "103823083"
---
# <a name="param-elements-in-an-object-element"></a>Elementos PARAM em um elemento OBJECT

O Windows Media Player usa o elemento PARAM para definir condições de inicialização específicas para o controle. O elemento PARAM é inserido dentro do elemento OBJECT.

Por exemplo, se você quiser definir se a propriedade **AutoStart** é true, você incorporaria o elemento param dentro do elemento Object.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



Você pode ter tantos elementos PARAM em um elemento OBJECT quanto desejar. PARAM tem dois atributos, Name e Value. Ambos os atributos devem ser definidos.

Os atributos de parâmetro com suporte variam ligeiramente entre navegadores e tipos de MIME. A tabela a seguir mostra os atributos com suporte nos navegadores do Internet Explorer e Firefox. O tipo MIME preferencial para o navegador Firefox é application/x-MS-WMP. no entanto, há vários outros tipos MIME que você pode usar para inserir o controle do jogador em uma página da web hospedada pelo navegador Firefox. A quarta coluna da tabela mostra os atributos com suporte quando você usa um tipo MIME diferente de application/x-MS-WMP.



| Nome do parâmetro                                            | Internet Explorer | Firefox com tipo MIME application/x-MS-WMP | Firefox com qualquer outro tipo MIME |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Inicialização automática](settings-autostart.md)                   | sim               | sim                                         | sim                              |
| [Lance](settings-balance.md)                       | sim               | sim                                         | sim                              |
| [baseURL](settings-baseurl.md)                       | sim               | sim                                         | sim                              |
| [captioningID](closedcaption-captioningid.md)        | sim               | sim                                         | sim                              |
| [currentMarker](controls-currentmarker.md)           | sim               | sim                                         | sim                              |
| [currentPosition](controls-currentposition.md)       | sim               | sim                                         | sim                              |
| [DefaultFrame](settings-defaultframe.md)             | sim               | não                                          | não                               |
| [enableContextMenu](player-enablecontextmenu.md)     | sim               | sim                                         | sim                              |
| [habilitado](player-enabled.md)                         | sim               | sim                                         | sim                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | sim               | sim                                         | não                               |
| **Nome do arquivo**                                          | não                | sim                                         | sim                              |
| [Tela inteira](player-fullscreen.md)                   | sim               | não                                          | não                               |
| [invokeURLs](settings-invokeurls.md)                 | sim               | não                                          | não                               |
| [Muta](settings-mute.md)                             | sim               | sim                                         | sim                              |
| [playCount](settings-playcount.md)                   | sim               | sim                                         | não                               |
| [frequência](settings-rate.md)                             | sim               | sim                                         | sim                              |
| [SAMIFileName](closedcaption-samifilename.md)        | sim               | sim                                         | sim                              |
| [SAMILang](closedcaption-samilang.md)                | sim               | sim                                         | sim                              |
| [SAMIstyle](closedcaption-samistyle.md)              | sim               | sim                                         | sim                              |
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

[**Usando o controle do Windows Media Player em uma página da Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




