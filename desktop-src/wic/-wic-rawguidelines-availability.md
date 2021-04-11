---
description: Disponibilidade de codec e suporte de plataforma
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilidade de codec e suporte de plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170863"
---
# <a name="codec-availability-and-platform-support"></a>Disponibilidade de codec e suporte de plataforma

A Microsoft recomenda que os fornecedores de câmera incluam os codecs de WIC (Windows Imaging Component) atualizados na distribuição de software com novas câmeras e que o codec atualizado seja instalado com a instalação de software do fornecedor padrão Windows 7, Windows Vista e Windows XP. Os fornecedores de câmera também devem fornecer o último codec do WIC como um download de seus sites de suporte.

## <a name="codec-discovery"></a>Descoberta de codec

A Microsoft está fazendo o seguinte para ajudar a apontar os usuários para sites de fornecedores para downloads de codec:

-   No Windows Explorer, se um usuário clicar duas vezes em um arquivo não reconhecido (o caso padrão quando um arquivo bruto estiver no computador, mas o codec ainda não estiver instalado), uma caixa de diálogo relatará que o arquivo não é reconhecido e perguntará se o usuário deseja encontrar um programa que entenda o arquivo. A Microsoft mantém um serviço de redirecionamento existente para encaminhar os usuários aos sites de fornecedores que podem fornecer o programa para entender o arquivo. Esse recurso existe no Windows XP e no Windows Vista.
-   A Galeria de fotos do Windows, a Galeria de fotos do Windows Live e o Visualizador de fotos do Windows 7 reconhecem um conjunto de extensões de arquivo como arquivos BRUTOs. Se os arquivos desse conjunto forem encontrados em pastas que qualquer um desses aplicativos estão olhando e um codec para o arquivo ainda não estiver instalado, uma caixa de diálogo será exibida, conforme descrito no parágrafo anterior.

Para obter mais informações sobre a descoberta de codecs, consulte disponibilidade de codec e suporte de plataforma.

## <a name="windows-xp-platform-support"></a>Suporte à plataforma Windows XP

A Microsoft lançou o Windows XP SP3 com o WIC e um instalador de WIC autônomo para o Windows XP SP2. Eles usam codecs WIC para habilitar o suporte para miniaturas e visualizações nessas plataformas. Portanto, é importante que o download e a instalação do codec tenham suporte e testados no Windows 7, no Windows Vista e no Windows XP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



