---
description: Decodificação
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Decodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829489"
---
# <a name="decoding"></a>Decodificação

Para dar suporte adequado aos metadados, os autores de decodificador devem fazer o seguinte:

-   Implemente as interfaces [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .
-   Implemente o [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) no decodificador de quadro. Se o codec oferecer suporte a metadados em nível de contêiner, essa interface deverá ser implementada no decodificador de nível de contêiner, bem como no decodificador de quadro.
-   Ao decodificar o fluxo de imagem, chame [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) para instanciar um leitor de metadados para cada bloco de metadados. (Quaisquer novos leitores de metadados implementados pelo codec devem ser registrados com o WIC.)

    O decodificador não deve criar leitores de metadados por conta própria, mas sim usar o WIC para criá-los com base nos blocos de metadados no fluxo. O decodificador deve fazer isso em todos os blocos que encontrar, mesmo que eles não sejam nativamente conhecidos pelo docodificador, pois os leitores de metadados futuros podem ser instalados no sistema que entenda como lidar com esses blocos de metadados.

-   Se não houver nenhum manipulador de metadados para um bloco, crie uma instância do leitor de metadados desconhecido usando as opções de criação de metadados.
-   Expor a coleção de leitores de metadados por meio da interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .

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

 

 



