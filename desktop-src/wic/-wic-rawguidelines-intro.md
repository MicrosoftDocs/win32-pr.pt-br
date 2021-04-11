---
description: Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170860"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introdução (diretrizes do WIC para formatos de imagem bruta de câmera)

O Windows Imaging Component (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem. O WIC possibilita que os fornecedores de software e hardware desenvolvam codecs para que seus próprios formatos de imagem possam obter o mesmo suporte de plataforma que os formatos de imagem nativa, como TIFF (Tagged Image File Format), JPEG (conjunto de especialistas fotográfico) ou foto de HD.

O WIC fornece um único conjunto consistente de interfaces para todo o processamento de imagens, independentemente do formato da imagem. Portanto, qualquer aplicativo que usa o WIC recebe o suporte automático para novos formatos de imagem assim que o codec é instalado. O WIC também fornece uma estrutura de metadados extensíveis que possibilita que os aplicativos leiam e gravem seus próprios metadados proprietários diretamente nos arquivos de imagem, para que os metadados nunca sejam perdidos ou separados da imagem.

O WIC está incluído com o Windows Presentation Foundation (WPF) e é incorporado ao Windows Vista e versões posteriores do Windows. Ele também está disponível como um componente redistribuível autônomo para o Windows XP.

Essas diretrizes foram projetadas para ajudar os fabricantes de formato bruto em seu desenvolvimento de codecs de WIC.

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

 

 



