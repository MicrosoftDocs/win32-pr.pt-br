---
title: Ocultando o Windows Media Player controle
description: Ocultando o Windows Media Player controle
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, incorporando ActiveX controle
- Windows Media Player modelo de objeto, incorporando ActiveX controle
- modelo de objeto, incorporando ActiveX controle
- Windows Media Player Mobile, incorporando ActiveX controle
- Windows Media Player ActiveX controle,incorporação
- Windows Media Player Controle ActiveX dispositivo móvel, incorporação
- ActiveX controle,incorporação
- Windows Media Player ActiveX, páginas da Web
- Windows Media Player Controle ActiveX dispositivo móvel, páginas da Web
- ActiveX, páginas da Web
- incorporação, páginas da Web
- Windows Media Player, ocultando ActiveX controle
- Windows Media Player modelo de objeto, ocultando ActiveX controle
- modelo de objeto, ocultando ActiveX controle
- Windows Media Player Móvel, ocultando o controleActiveX
- Windows Media Player ActiveX controle, ocultando
- Windows Media Player Controle de ActiveX móvel, ocultando
- ActiveX controle,ocultando
- Windows Media Player ActiveX, páginas da Web
- Windows Media Player Controle ActiveX dispositivo móvel, páginas da Web
- ActiveX, páginas da Web
- Incorporação de página da Web, ocultando ActiveX controle
- ocultando Windows Media Player ActiveX controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb0b29bbbc1b2eb978c5bd9f29a58aa02bf629d5c6befe9f1dc68bbc92d280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339177"
---
# <a name="hiding-the-windows-media-player-control"></a>Ocultando o Windows Media Player controle

O Windows Media Player ActiveX objeto é inserido em uma página da Web usando o elemento OBJECT. Ao contrário de versões anteriores, o elemento OBJECT que define Windows Media Player deve ser colocado na seção BODY de uma página da Web, entre o <BODY> e </BODY> Tags. Colocar o Windows Media Player ActiveX na seção HEAD de uma página da Web para ocultar a interface do usuário pode produzir resultados inesperados.

Se você colocar o Windows Media Player ActiveX na seção CORPO de uma página da Web, a interface do usuário do controle será exibida. Se você não quiser que ele seja exibido e desejar criar sua própria interface do usuário, de definir os atributos de altura e largura do elemento OBJECT como zero.

O controle também pode ficar invisível definindo o *Player*. **Propriedade uiMode** para "invisível". Isso pode ser feito usando uma marca PARAM, conforme discutido na próxima seção. Nesse caso, o espaço é reservado para o controle usando altura e largura, mas nada é exibido no espaço reservado até que **uiMode** seja alterado para algo diferente de "invisível".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Windows Media Player controle em uma página da Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




