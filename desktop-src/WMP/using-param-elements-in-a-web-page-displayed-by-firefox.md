---
title: Usando elementos PARAM em uma página da Web exibida pelo Firefox
description: Usando elementos PARAM em uma página da Web exibida pelo Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Windows Media Player elementos PARAM no elemento OBJECT
- Windows Media Player modelo de objeto, elementos PARAM no elemento OBJECT
- modelo de objeto, elementos PARAM no elemento OBJECT
- Windows Media Player Elementos Mobile,PARAM no elemento OBJECT
- Windows Media Player ActiveX controle, elementos PARAM no elemento OBJECT
- Windows Media Player Controle ActiveX dispositivo móvel, elementos PARAM no elemento OBJECT
- ActiveX controle, elementos PARAM no elemento OBJECT
- incorporação, páginas da Web
- Incorporação de página da Web, elementos PARAM no elemento OBJECT
- Elementos PARAM no elemento OBJECT
- Windows Media Player, Firefox
- Windows Media Player modelo de objeto, Firefox
- modelo de objeto, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX controle, Firefox
- Windows Media Player Controle de ActiveX móvel, Firefox
- ActiveX controle,Firefox
- Elementos Firefox,PARAM no elemento OBJECT
- Incorporação de página da Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767b9b0d5e4367a17f07f68600ff8e9cac488ca9e4c950165d84677fd7d03956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117301"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Usando elementos PARAM em uma página da Web exibida pelo Firefox

Você pode usar elementos PARAM dentro de um elemento OBJECT para definir o estado inicial do controle Player. Por exemplo, os elementos PARAM no exemplo a seguir especificam que o controle deve reproduzir seattle.wmv automaticamente.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



A maioria dos elementos PARAM pode ser interpretada por Internet Explorer e pelo Firefox. No entanto, há alguns elementos PARAM que o plug-in firefox não dá suporte. Para obter informações sobre quais elementos PARAM têm suporte pelo plug-in firefox, consulte [Elementos PARAM em um elemento OBJECT](param-elements-in-an-object-element.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o controle Windows Media Player com Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




