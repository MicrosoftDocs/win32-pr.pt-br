---
title: O que há de novo (SDK do Windows Media Format 11)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- SDK do Windows Media Format, o que há de novo
- SDK do Windows Media Format, recursos
- SDK do Windows Media Format, novos recursos
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, atualizações de DRM
- SDK do Windows Media Format, atualizações de codec
- SDK do Windows Media Format, imagens em miniatura
- DRM (gerenciamento de direitos digitais), novos recursos
- DRM (gerenciamento de direitos digitais), novos recursos
- imagens em miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644150"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>O que há de novo (SDK do Windows Media Format 11)

O SDK do Windows Media Format 11 introduz novos recursos de DRM (gerenciamento de direitos digitais). As alterações a seguir foram feitas no SDK desde a versão 9,5.

## <a name="windows-media-drm-client-extended-apis"></a>APIs estendidas do cliente DRM do Windows Media

O SDK do Windows Media Format 11 é fornecido com um novo conjunto de APIs DRM. Essas APIs são implementadas em sua própria biblioteca. Muitos dos recursos DRM com suporte dos objetos do Windows Media Format SDK também são suportados pelas APIs estendidas do cliente DRM do Windows Media. A principal diferença nas novas APIs é que elas não dependem de ter um arquivo ASF para funcionar. Em vez disso, as novas APIs lidam com o armazenamento de licença local diretamente, geralmente usando a ID de chave para identificar licenças.

Para obter mais informações, consulte a documentação de [APIs estendidas do cliente DRM do Windows Media](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Codecs atualizados

O codec de perfil avançado do Windows Media Video 9 foi atualizado para produzir um fluxo de bits compactado compatível com o padrão SMPTE VC-1 publicado.

O codec Windows Media Audio 10 Professional também está incluído nesta versão do SDK. O novo codec de áudio apresenta qualidade aprimorada a taxas de bits mais baixas.

## <a name="thumbnail-right"></a>Miniatura à direita

Os aplicativos podem solicitar uma nova ação de DRM para ler do vídeo para criar uma imagem em miniatura. Isso permite que os aplicativos criem e exibam imagens em miniatura para arquivos de vídeo sem abrir o arquivo para reprodução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o SDK do Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




