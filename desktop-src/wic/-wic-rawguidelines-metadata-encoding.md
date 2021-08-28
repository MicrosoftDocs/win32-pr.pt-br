---
description: Codificação
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codificação (Windows de imagens)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b3d6eef499379bbdc668e70d5d0ec4326b390372da910934a6e7c7f547d177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964645"
---
# <a name="encoding-windows-imaging-component"></a>Codificação (Windows de imagens)

O autor do codificador deve fazer o seguinte:

-   Implemente [**interfaces IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) [**e IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
-   Implemente [**IWICMetadataBlockWriter no**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) codificador de quadro. Se o codec for compatível com metadados no nível do contêiner, essa interface deverá ser implementada no codificador no nível do contêiner, bem como no codificador de quadro.
-   Se o formato de contêiner contiver implicitamente quaisquer blocos de metadados obrigatórios, insinue um autor de metadados para cada bloco desse tipo. Por exemplo, o formato TIFF requer um dispositivo de interface (IFD) para cada quadro, portanto, o autor IFD sempre deve ser exposto.
-   Implemente suporte para gerenciar a coleção de autores de metadados. O bloqueador gerencia quaisquer requisitos de pedido ou restrições de contêiner nos tipos de blocos de metadados que podem ser codificados. O bloqueador deve verificar se os novos autores de metadados podem ser inseridos no formato de contêiner.
-   Ao codificar o fluxo de imagem, chame [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para serializar o conteúdo de cada autor de metadados no fluxo. Se o bloco de metadados contiver metadados "críticos", o codificador deverá definir os itens de metadados críticos antes de pedir ao autor de metadados para serializar o conteúdo.
-   Verifique se há manipuladores de metadados desconhecidos para garantir que os blocos de metadados redundantes não estão presentes. Isso é importante porque, ao preservar metadados em um cenário de decodificação ou codificação, blocos desconhecidos podem ser uma duplicata de blocos de metadados obrigatórios.

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

 

 



