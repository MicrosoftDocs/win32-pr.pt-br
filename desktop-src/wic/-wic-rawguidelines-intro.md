---
description: Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96da37d36fed6af0aef271471eb2a0e5dae44bef71dfe14a4da37eba3f658c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086859"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)

o Windows o componente de geração de imagens (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem. O WIC possibilita que os fornecedores de software e hardware desenvolvam codecs para que seus próprios formatos de imagem possam obter o mesmo suporte de plataforma que os formatos de imagem nativa, como TIFF (Tagged Image File Format), JPEG (conjunto de especialistas fotográfico) ou foto de HD.

O WIC fornece um único conjunto consistente de interfaces para todo o processamento de imagens, independentemente do formato da imagem. Portanto, qualquer aplicativo que usa o WIC recebe o suporte automático para novos formatos de imagem assim que o codec é instalado. O WIC também fornece uma estrutura de metadados extensíveis que possibilita que os aplicativos leiam e gravem seus próprios metadados proprietários diretamente nos arquivos de imagem, para que os metadados nunca sejam perdidos ou separados da imagem.

o WIC está incluído com o Windows Presentation Foundation (WPF) e é incorporado ao Windows Vista e versões Windows posteriores. ele também está disponível como um componente redistribuível autônomo para o Windows XP.

Essas diretrizes foram projetadas para ajudar os fabricantes de formato bruto em seu desenvolvimento de codecs de WIC.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Diretrizes do WIC para formatos de imagem bruta de câmera](-wic-rawguidelines.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



