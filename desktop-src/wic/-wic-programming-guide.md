---
title: Guia de programação do WIC
description: Descreve como usar as APIs do WIC.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370730"
---
# <a name="wic-programming-guide"></a>Guia de programação do WIC

Esta seção contém tópicos conceituais que descrevem como usar as APIs do Windows Imaging Component (WIC).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                 | Descrição                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)<br/> | O WIC fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem.<br/>                                                                                                                       |
| [Visão geral da API do WIC](-wic-api.md)<br/>                                           | O WIC fornece uma API baseada em Component Object Model (COM) para uso em C e C++.<br/>                                                                                                                            |
| [Decodificando imagens digitais](-wic-decoder-portal.md)<br/>                         | Esta seção contém tópicos conceituais e de instruções que descrevem os decodificadores de bitmap do WIC que são usados na decodificação de imagens digitais.<br/>                                                                            |
| [Usando dados de imagem](-wic-bitmapsources-portal.md)<br/>                          | Esta seção contém tópicos conceituais e de instruções que descrevem as fontes de bitmap do WIC e como manipulá-las.<br/>                                                                                            |
| [Dados da imagem de codificação](encoding-bitmaps-to-digital-images.md)<br/>              | Esta seção contém tópicos conceituais e de instruções que descrevem codificadores de bitmaps do WIC que são usados para codificar imagens digitais.<br/>                                                                              |
| [Codecs nativos do WIC](native-wic-codecs.md)<br/>                                 | Esta seção contém informações sobre os codecs de imagens nativas disponíveis no WIC.<br/>                                                                                                                        |
| [Processando metadados de imagem](-wic-metadata-portal.md)<br/>                      | Esta seção contém tópicos conceituais que descrevem o sistema de metadados do WIC.<br/>                                                                                                                             |
| [Suporte a JPEG YCbCr](jpeg-ycbcr-support.md)<br/>                               | A partir do Windows 8.1, o codec JPEG do [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) dá suporte à leitura e gravação de dados de imagem em seu formulário YC<sub>b</sub>C<sub>r</sub> nativo. <br/> |
| [Gerenciamento de cores](-wic-colormanagement.md)<br/>                               | O WIC simplifica o gerenciamento de cores, fornecendo a interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) e a interface [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) .<br/>          |
| [Desenvolvimento de componentes](-wic-component-development.md)<br/>                    | O WIC é uma plataforma extensível que fornece uma API de nível baixo para imagens digitais.<br/>                                                                                                                          |



 

## <a name="see-also"></a>Consulte Também

[Referência do WIC](-wic-codec-reference.md)


[Exemplos de WIC](-wic-samples.md)


 

 




