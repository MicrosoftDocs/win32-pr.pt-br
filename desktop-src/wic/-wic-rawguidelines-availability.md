---
description: Disponibilidade do Codec e suporte à plataforma
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilidade do Codec e suporte à plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5768cdbe149e87188bdd9d21f87508991feb841a70acacf5984ada408f5b58fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032320"
---
# <a name="codec-availability-and-platform-support"></a>Disponibilidade do Codec e suporte à plataforma

A Microsoft recomenda que os fornecedores de câmera incluam codecs WIC (Componente de Geração de Imagem) RAW atualizado Windows s na distribuição de software com novas câmeras e que o codec atualizado seja instalado com a instalação de software do fornecedor padrão Windows 7, Windows Vista e Windows XP. Os fornecedores de câmera também devem fornecer o codec mais recente do WIC como um download de seus sites de suporte.

## <a name="codec-discovery"></a>Descoberta de Codec

A Microsoft está fazendo o seguinte para ajudar a apontar os usuários para sites de fornecedores para downloads de codec:

-   No Windows Explorer, se um usuário clicar duas vezes em um arquivo que não é reconhecido (o caso padrão quando um arquivo RAW estiver no computador, mas o codec ainda não estiver instalado), uma caixa de diálogo informa que o arquivo não foi reconhecido e pergunta se o usuário deseja encontrar um programa que entenda o arquivo. A Microsoft mantém um serviço de redirecionamento existente para encaminhar usuários para sites de fornecedores que podem fornecer o programa para entender o arquivo. Essa instalação existe no Windows XP e no Windows Vista.
-   O Windows Galeria de Fotos, Windows Live Galeria de Fotos e o Windows 7 Visualizador de Fotos reconhecer um conjunto de extensões de arquivo como arquivos RAW. Se os arquivos desse conjunto são encontrados em pastas que qualquer um desses aplicativos estão observando e um codec para o arquivo ainda não está instalado, uma caixa de diálogo é exibida, conforme descrito no parágrafo anterior.

Para obter mais informações sobre a descoberta de codec, consulte Disponibilidade do Codec e Suporte à plataforma.

## <a name="windows-xp-platform-support"></a>Windows Suporte à plataforma XP

A Microsoft lançou Windows XP SP3 com WIC e um instalador autônomo do WIC para Windows XP SP2. Eles usam codecs WIC para habilitar o suporte para miniaturas e visualizações nessas plataformas. Portanto, é importante que o download e a instalação do codec sejam suportados e testados no Windows 7, Windows Vista e Windows XP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem RAW da câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



