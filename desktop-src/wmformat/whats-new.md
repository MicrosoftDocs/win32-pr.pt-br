---
title: o que há de novo (Windows Media Format 11 SDK)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows SDK do formato de mídia, o que há de novo
- Windows SDK do formato de mídia, recursos
- Windows SDK do formato de mídia, novos recursos
- Windows SDK do formato de mídia, APIs estendidas do cliente
- Windows SDK de formato de mídia, atualizações de DRM
- Windows SDK de formato de mídia, atualizações de codec
- Windows SDK do formato de mídia, imagens em miniatura
- DRM (gerenciamento de direitos digitais), novos recursos
- DRM (gerenciamento de direitos digitais), novos recursos
- imagens em miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1174078ce6fde94794cff32f4384de4a6c7b774dec2943fa91f2ec279d9d718e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963885"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>o que há de novo (Windows Media Format 11 SDK)

o SDK do formato de mídia 11 do Windows introduz novos recursos de DRM (gerenciamento de direitos digitais). As alterações a seguir foram feitas no SDK desde a versão 9,5.

## <a name="windows-media-drm-client-extended-apis"></a>Windows APIs estendidas do cliente DRM de mídia

o SDK do Windows Media Format 11 é fornecido com um novo conjunto de APIs DRM. Essas APIs são implementadas em sua própria biblioteca. muitos dos recursos DRM com suporte dos objetos do SDK do formato de mídia do Windows também são compatíveis com as APIs estendidas do cliente de DRM de mídia Windows. A principal diferença nas novas APIs é que elas não dependem de ter um arquivo ASF para funcionar. Em vez disso, as novas APIs lidam com o armazenamento de licença local diretamente, geralmente usando a ID de chave para identificar licenças.

para obter mais informações, consulte a documentação [Windows Media DRM Client extended APIs](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Codecs atualizados

o codec de perfil avançado do Windows Media Video 9 foi atualizado para produzir um fluxo de bits compactado compatível com o padrão SMPTE VC-1 publicado.

o codec Windows Media Audio 10 Professional também está incluído nesta versão do SDK. O novo codec de áudio apresenta qualidade aprimorada a taxas de bits mais baixas.

## <a name="thumbnail-right"></a>Miniatura à direita

Os aplicativos podem solicitar uma nova ação de DRM para ler do vídeo para criar uma imagem em miniatura. Isso permite que os aplicativos criem e exibam imagens em miniatura para arquivos de vídeo sem abrir o arquivo para reprodução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**sobre o SDK do formato de mídia Windows**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




