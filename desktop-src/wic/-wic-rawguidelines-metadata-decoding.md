---
description: Decodificação
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Decodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bfef7fe219ae7ff05227bfba48b69188844dc2373bd1c3099737224758fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667323"
---
# <a name="decoding"></a>Decodificação

Para dar suporte corretamente aos metadados, os autores do decodificador devem fazer o seguinte:

-   Implemente [**interfaces IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) [**e IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
-   Implemente [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) no decodificador de quadro. Se o codec for compatível com metadados no nível do contêiner, essa interface deverá ser implementada no decodificador no nível do contêiner, bem como no decodificador de quadro.
-   Ao decodificar o fluxo de imagem, chame [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) para criar uma instanciência de um leitor de metadados para cada bloco de metadados. (Todos os novos leitores de metadados que o codec implementa devem ser registrados com o WIC.)

    O decodificador não deve criar leitores de metadados por conta própria, mas usar o WIC para criar com base nos blocos de metadados no fluxo. O decodificador deve fazer isso em todos os blocos encontrados, mesmo que eles não sejam na verdade conhecidos pelo docoder, porque leitores de metadados futuros podem ser instalados no sistema que entendem como lidar com esses blocos de metadados.

-   Se não houver nenhum manipulador de metadados para um bloco, insinue o leitor de metadados desconhecido usando as opções de criação de metadados.
-   Expor a coleção de leitores de metadados por meio da interface [**IWICMetadataBlockReader.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)

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

 

 



