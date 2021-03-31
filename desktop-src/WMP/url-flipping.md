---
title: Inversão de URL
description: Inversão de URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Windows Media Player, apresentações baseadas na Web
- Modelo de objeto do Windows Media Player, apresentações baseadas na Web
- modelo de objeto, apresentações baseadas na Web
- Windows Media Player Mobile, apresentações baseadas na Web
- Controle ActiveX do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX móvel do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX, apresentações baseadas na Web
- Windows Media Player, inversão de URL
- Modelo de objeto do Windows Media Player, inversão de URL
- modelo de objeto, inversão de URL
- Windows Media Player Mobile, inversão de URL
- Controle ActiveX do Windows Media Player, inversão de URL
- Controle ActiveX móvel do Windows Media Player, inversão de URL
- Controle ActiveX, inversão de URL
- Apresentações baseadas na Web, inversão de URL
- Criando apresentações baseadas na Web, inversão de URL
- Inversão de URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "103637309"
---
# <a name="url-flipping"></a>Inversão de URL

O uso de páginas da Web para apresentações de slides é chamado de inversão de URL e é manipulado automaticamente pelo Windows Media Player quando ele encontra comandos de script de URL inseridos no fluxo de mídia digital que está sendo reproduzido. Você pode especificar um quadro de destino para suas páginas em cada comando de script ou pode especificá-lo definindo a propriedade **Settings. DefaultFrame** . Você pode definir essa propriedade no código do script ou usando um elemento PARAM dentro do elemento OBJECT que incorpora o controle do Windows Media Player.

Você está livre para lidar com os comandos de script de URL no código JScript, assim como faria com os comandos de script personalizados. Se você quiser que o controle do Windows Media Player ignore comandos de script de URL para que você possa tratá-los inteiramente por conta própria, defina as *configurações*. Propriedade **invokeURLs** como false no código de script ou usando um elemento param como descrito anteriormente.

O exemplo a seguir ilustra um conjunto de quadros típico para inversão de URL. Primeiro, crie uma página que descreva o conjunto de quadros:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Em seguida, crie o arquivo player.html referenciado no conjunto de quadros usando o seguinte código (o arquivo video. wmv deve existir no mesmo diretório que os arquivos HTML):


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



Se suas páginas da Web forem pequenas o suficiente para serem carregadas rapidamente, essa configuração poderá ser suficiente para suas necessidades. Se, por outro lado, suas páginas da Web forem complexas, o streaming de mídia avançado poderá ser mais eficaz, dependendo da velocidade de conexão de seu público.

> [!Note]  
> A inversão de URL não funciona corretamente com páginas exibidas no Netscape Navigator. Em vez de aparecer no quadro especificado por **DefaultFrame**, cada comando de script de URL recebido no navegador EXIBE a URL em uma nova janela do navegador.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando Web-Based apresentações**](creating-web-based-presentations.md)
</dt> <dt>

[**Usando o script para controlar a inversão de URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




