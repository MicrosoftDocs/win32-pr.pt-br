---
description: Formatos de imagem RAW no Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formatos de imagem RAW no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88026e85780706ca2bd5f23f5ca43ec49ae614d4c65e42ec19367b01b3f43423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709854"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formatos de imagem RAW no Windows Vista

Windows O Vista Explorer , Windows Vista Galeria de Fotos, o Window Live Galeria de Fotos e o Windows 7 Visualizador de Fotos usam o WIC (componente de imagens do Windows) e, portanto, suportam formatos de imagem RAW quando codecs apropriados são instalados no computador.

Como o WIC é uma arquitetura extensível de geração de imagens, qualquer aplicativo WIC pode consumir novos formatos de imagem assim que novos codecs são instalados no sistema. Isso torna o WIC ideal como uma Plug and Play para os formatos de imagem RAW produzidos pelas câmeras digitais. Por meio do WIC, Windows aplicativos podem obter suporte para novos modelos de câmera sempre que codecs atualizados são disponibilizados (idealmente in-box com novas câmeras). Os autores de codec podem dar suporte a esses cenários implementando interfaces WIC comuns a todos os tipos de imagem, conforme descrito mais detalhadamente neste documento.

Atualmente, a maioria dos aplicativos de consumidor base não tem conhecimento especial sobre formatos de imagem RAW e não expõe uma interface do usuário para ajustar as configurações de processamento RAW.

No entanto, para dar suporte a aplicativos de imagens especializadas, os autores de codec RAW também devem implementar a interface [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Essa interface expõe recursos especiais para imagens RAW, como a capacidade de fazer ajustes comuns de imagem e processar (desenvolver) imagens RAW em espaços de cores RGB (azul-verde-vermelho) especificados.

Várias outras interfaces WIC são importantes para que os autores de codec RAW implementem. Eles são discutidos mais detalhadamente nesta série de tópicos.

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

 

 



