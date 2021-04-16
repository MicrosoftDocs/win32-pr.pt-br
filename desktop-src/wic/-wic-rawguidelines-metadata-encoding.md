---
description: Codificação
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codificação (Windows Imaging Component)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765046"
---
# <a name="encoding-windows-imaging-component"></a>Codificação (Windows Imaging Component)

O autor do codificador deve fazer o seguinte:

-   Implemente as interfaces [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .
-   Implemente [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) no codificador de quadros. Se o codec oferecer suporte a metadados em nível de contêiner, essa interface deverá ser implementada no codificador de nível de contêiner, bem como no codificador de quadros.
-   Se o formato do contêiner contiver implicitamente quaisquer blocos de metadados obrigatórios, crie uma instância de um gravador de metadados para cada bloco. Por exemplo, o formato TIFF requer um dispositivo de interface (IFD) para cada quadro, de modo que o gravador IFD sempre deve ser exposto.
-   Implemente o suporte para gerenciar a coleção de gravadores de metadados. O gravador de bloco gerencia quaisquer requisitos de pedido ou restrições de contêiner nos tipos de blocos de metadados que podem ser codificados. O gravador de bloco deve verificar se os novos gravadores de metadados podem ser inseridos dentro do formato de contêiner.
-   Ao codificar o fluxo de imagem, chame [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para serializar o conteúdo de cada gravador de metadados no fluxo. Se o bloco de metadados contiver metadados "críticos", o codificador deverá definir os itens de metadados críticos antes de solicitar que o gravador de metadados Serialize o conteúdo.
-   Verifique se há manipuladores de metadados desconhecidos para garantir que os blocos de metadados redundantes não estejam presentes. Isso é importante porque, enquanto preserva os metadados em um cenário de decodificação ou codificação, os blocos desconhecidos podem ser uma duplicata de blocos de metadados obrigatórios.

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

 

 



