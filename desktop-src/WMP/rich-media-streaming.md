---
title: Streaming de mídia avançada
description: Streaming de mídia avançada
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, apresentações baseadas na Web
- Modelo de objeto do Windows Media Player, apresentações baseadas na Web
- modelo de objeto, apresentações baseadas na Web
- Windows Media Player Mobile, apresentações baseadas na Web
- Controle ActiveX do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX móvel do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX, apresentações baseadas na Web
- Windows Media Player, streaming de mídia avançada
- Modelo de objeto do Windows Media Player, streaming de mídia avançada
- modelo de objeto, streaming de mídia avançada
- Windows Media Player Mobile, streaming de mídia avançada
- Controle ActiveX do Windows Media Player, streaming de mídia avançada
- Controle ActiveX móvel do Windows Media Player, streaming de mídia avançada
- Controle ActiveX, streaming de mídia avançada
- Apresentações baseadas na Web, streaming de mídia avançada
- Criando apresentações baseadas na Web, streaming de mídia avançado
- streaming de mídia avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636640"
---
# <a name="rich-media-streaming"></a>Streaming de mídia avançada

Páginas da Web complexas contêm muitos componentes diferentes que normalmente são transferidos separadamente. Em uma conexão lenta, essas páginas exibem uma peça por vez e podem levar vários minutos para serem exibidas completamente. Isso pode impedi-lo de sincronizar efetivamente páginas da Web com sua mídia digital. A solução para esse problema é streaming de mídia avançada, o que significa adicionar suas páginas da Web ao seu fluxo de mídia digital para que elas sejam entregues ao mesmo tempo que os dados de áudio ou vídeo.

O streaming de mídia avançada usa um layout simples de conjunto de quadros e se comporta exatamente como a inversão normal de URL. Assim como na inversão de URL, os comandos de script de URL inseridos em fluxos de mídia digital são usados para exibir o conteúdo no quadro de destino. Em vez de apontar para páginas na Web, no entanto, os comandos de script de URL são usados pelo Windows Media Player 9 Series ou posterior para acessar arquivos no cache do Internet Explorer em que o conteúdo HTML transmitido é colocado conforme ele é recebido. Assim como acontece com a inversão de URL normal, você pode escrever manipuladores de eventos que respondam a esses comandos de script de URL ou pode deixar o controle do Windows Media Player controlar tudo automaticamente.

> [!Note]  
> Qualquer conteúdo HTML entregue por meio de streaming de mídia avançada é reproduzido na zona de segurança da Internet e está sujeito às configurações de segurança do navegador do usuário.

 

Para obter mais informações sobre como criar apresentações de mídia avançadas, consulte o SDK do Windows Media Format 9 Series ou posterior e o SDK do Windows Media Encoder 9 Series.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando Web-Based apresentações**](creating-web-based-presentations.md)
</dt> <dt>

[**Usando o script para controlar a inversão de URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




