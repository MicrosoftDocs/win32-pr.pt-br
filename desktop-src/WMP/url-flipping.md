---
title: Invertia de URL
description: Invertia de URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Windows Media Player apresentações baseadas na Web
- Windows Media Player modelo de objeto, apresentações baseadas na Web
- modelo de objeto, apresentações baseadas na Web
- Windows Media Player Apresentações móveis baseadas na Web
- Windows Media Player ActiveX controle, apresentações baseadas na Web
- Windows Media Player Controle ActiveX dispositivo móvel, apresentações baseadas na Web
- ActiveX controle, apresentações baseadas na Web
- Windows Media Player, invertindo URL
- Windows Media Player de objeto, inverter URL
- modelo de objeto, inverter URL
- Windows Media Player Móvel, invertindo URL
- Windows Media Player ActiveX controle, invertindo URL
- Windows Media Player Controle de ActiveX móvel, invertindo URL
- ActiveX controle, invertia de URL
- Apresentações baseadas na Web, invertia de URL
- criando apresentações baseadas na Web, invertindo URL
- Invertia de URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4471045506447b93621578f27e2f156bb214016b3fa8ec114a689b919314d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134519"
---
# <a name="url-flipping"></a>Invertia de URL

O uso de páginas da Web para apresentação de slides é chamado de invertida de URL e é tratado automaticamente pelo Windows Media Player quando encontra comandos de script de URL inseridos no fluxo de mídia digital que ele está tocando. Você pode especificar um quadro de destino para suas páginas em cada comando de script ou especificá-lo definindo a **propriedade Configurações.defaultFrame.** Você pode definir essa propriedade no código de script ou usando um elemento PARAM dentro do elemento OBJECT que incorpora o Windows Media Player controle.

Você é livre para lidar com os comandos de script de URL em seu código JScript da mesma forma que lidaria com comandos de script personalizados. Se você quiser que Windows Media Player controle de configuração ignore os comandos de script de URL para que você possa lidar totalmente com eles por conta própria, de definir o *Configurações*. **Propriedade invokeURLs** como false no código de script ou usando um elemento PARAM conforme descrito anteriormente.

O exemplo a seguir ilustra um quadro típico para invertimento de URL. Primeiro, crie uma página que descreva o quadro:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



Em seguida, crie o arquivo player.html referenciado no quadro usando o código a seguir (supõe-se que o arquivo video.wmv exista no mesmo diretório que os arquivos HTML):


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



Se suas páginas da Web são pequenas o suficiente para serem carregadas rapidamente, essa configuração pode ser suficiente para suas necessidades. Se, por outro lado, suas páginas da Web são complexas, o streaming de mídias rich pode ser mais eficaz, dependendo da velocidade de conexão do seu público-alvo.

> [!Note]  
> A invertia de URL não funciona corretamente com páginas exibidas no Netscape Navigator. Em vez de aparecer no quadro especificado por **defaultFrame,** cada comando de script de URL recebido no Navegador exibe a URL em uma nova janela do navegador.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando Web-Based apresentações**](creating-web-based-presentations.md)
</dt> <dt>

[**Usando script para controlar a invertia de URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




