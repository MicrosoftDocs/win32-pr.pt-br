---
description: Implementando um codificador de WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementando um codificador de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170456"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implementando um codificador de WIC-Enabled

## <a name="introduction"></a>Introdução

A implementação de um codificador do Windows Imaging Component (WIC) requer a escrita de duas classes, como também é verdadeira para implementar um decodificador de WIC. As interfaces dessas classes correspondem diretamente às responsabilidades do codificador descritas na seção [codificação](-wic-howwicworks.md) de como o Windows Imaging Component funciona.

Uma das classes fornece serviços de nível de contêiner e gerencia a serialização dos quadros de imagem individuais dentro do contêiner. Essa classe implementa a interface [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) . Se o formato de imagem der suporte a metadados em nível de contêiner, você também deverá implementar a interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) nessa classe.

A outra classe fornece serviços de nível de quadro e faz a codificação real dos bits de imagem para cada quadro no contêiner. Ele também itera nos blocos de metadados de cada quadro e solicita os gravadores de metadados apropriados para serializar os blocos. Essa classe implementa a interface **IWICBitmapFrameEncode** e a interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) . Essa classe deve ter um membro IStream que a classe de nível de contêiner inicialize na instanciação, na qual o método **Commit** serializará os dados do quadro.

Em alguns casos, como formatos brutos, o autor do codec pode não querer que os aplicativos sejam capazes de codificar ou recodificar no formato bruto, pois a finalidade de um arquivo bruto é conter os dados do sensor exatamente como vieram da câmera. Nos casos em que o autor do codec não deseja habilitar a codificação, ainda é necessário implementar um codificador rudimentar apenas para habilitar a adição de metadados. Nesse caso, o codificador precisa dar suporte apenas a esses métodos necessários para gravar metadados e pode copiar os bits da imagem intocados do decodificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Interfaces do codificador](-wic-encoderinterfaces.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



