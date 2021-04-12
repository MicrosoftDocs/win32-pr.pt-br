---
description: Interfaces do decodificador
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces do decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171525"
---
# <a name="decoder-interfaces"></a>Interfaces do decodificador

As tabelas a seguir mostram as interfaces implementadas pelos decodificadores do Windows Imaging Component (WIC) e o diagrama de classe mostra a hierarquia de herança.

Interfaces de decodificador Container-Level



| Interface                                                                                       | Responsabilidades                             | Implementação                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Serviços de nível de contêiner                     | Obrigatório                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Notificação de progresso & suporte ao cancelamento | Recomendadas                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Enumeração de metadados                         | Opcional (necessário apenas para formatos que dão suporte a metadados em nível de contêiner) |



 

Interfaces de decodificador Frame-Level



| Interface                                                           | Responsabilidades          | Implementação                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Serviços de nível de quadro      | Obrigatório                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Enumeração de metadados      | Obrigatório                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Transformações de decodificador nativo | Recomendadas                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Serviços de processamento bruto   | Necessário somente para formatos brutos |



 

![hierarquia de herança da interface do WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando um decodificador de WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



