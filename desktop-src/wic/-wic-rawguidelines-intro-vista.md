---
description: Formatos de imagem BRUTOs no Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formatos de imagem BRUTOs no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170861"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formatos de imagem BRUTOs no Windows Vista

O Windows Vista Explorer, a Galeria de fotos do Windows Vista, a Galeria de fotos do Windows Live e o Visualizador de fotos do Azure 7 usam o Windows Imaging Component (WIC) e, portanto, oferecem suporte a formatos de imagem BRUTOs quando os codecs apropriados são instalados no computador.

Como o WIC é uma arquitetura de geração de imagens extensível, qualquer aplicativo de WIC pode consumir novos formatos de imagem assim que novos codecs são instalados no sistema. Isso torna o WIC ideal como uma solução Plug and Play para os formatos de imagem BRUTOs que as câmeras digitais produzem. Por meio do WIC, os aplicativos do Windows podem obter suporte para novos modelos de câmera sempre que os codecs atualizados são disponibilizados (idealmente na caixa com novas câmeras). Os autores de codecs podem dar suporte a esses cenários implementando interfaces WIC comuns a todos os tipos de imagem, conforme descrito em mais detalhes neste documento.

Hoje, a maioria dos aplicativos de consumidor básicos não tem conhecimento especial sobre formatos de imagem BRUTOs e não expõe uma interface do usuário para ajustar as configurações de processamento bruto.

No entanto, para dar suporte a aplicativos de geração de imagens especializados, os autores de codec BRUTOs também devem implementar a interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Essa interface expõe recursos especiais para imagens BRUTAs, como a capacidade de fazer ajustes de imagem comuns e processar (desenvolver) imagens BRUTAs em espaços de cores RGB (vermelho-verde-azul) especificados.

Várias outras interfaces de WIC são importantes para que os autores de codecs BRUTOs implementem. Eles são discutidos mais detalhadamente nesta série de tópicos.

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

 

 



