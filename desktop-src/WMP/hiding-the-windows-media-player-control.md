---
title: Ocultando o controle do Windows Media Player
description: Ocultando o controle do Windows Media Player
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- inserindo, páginas da Web
- Windows Media Player, ocultando o controle ActiveX
- Modelo de objeto do Windows Media Player, ocultando o controle ActiveX
- modelo de objeto, ocultando o controle ActiveX
- Windows Media Player Mobile, controle hidingActiveX
- Controle ActiveX do Windows Media Player, ocultando
- Controle ActiveX móvel do Windows Media Player, ocultando
- Controle ActiveX, ocultando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- Incorporação de página da Web, ocultando o controle ActiveX
- ocultando o controle ActiveX do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292553"
---
# <a name="hiding-the-windows-media-player-control"></a>Ocultando o controle do Windows Media Player

O objeto ActiveX do Windows Media Player é inserido em uma página da Web usando o elemento OBJECT. Ao contrário das versões anteriores, o elemento OBJECT que define o Windows Media Player deve ser colocado na seção BODY de uma página da Web, entre as marcas <BODY> e </BODY> . Colocar o objeto ActiveX do Windows Media Player na seção de cabeçalho de uma página da Web para ocultar a interface do usuário pode produzir resultados inesperados.

Se você colocar o controle ActiveX do Windows Media Player na seção corpo de uma página da Web, a interface do usuário de controle será exibida. Se você não quiser que ele seja exibido e deseja criar sua própria interface do usuário, defina os atributos Height e Width do elemento OBJECT como zero.

O controle também pode ser invisível definindo o *Player*. Propriedade **UIMODE** como "invisível". Isso pode ser feito usando uma marca PARAM, conforme discutido na próxima seção. Nesse caso, o espaço é reservado para o controle usando altura e largura, mas nada é exibido no espaço reservado até que **UIMODE** seja alterado para algo diferente de "invisível".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o controle do Windows Media Player em uma página da Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




