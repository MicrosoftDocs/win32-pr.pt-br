---
description: Interfaces do decodificador
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces do decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a52a0924f6302e45b10cb32a1d621db04967d33a3251ee39cce359e5030af5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393516"
---
# <a name="decoder-interfaces"></a>Interfaces do decodificador

as tabelas a seguir mostram as interfaces implementadas por decodificadores de WIC (Windows Imaging Component) e o diagrama de classe mostra a hierarquia de herança.

Interfaces de decodificador Container-Level



| Interface                                                                                       | Responsabilidades                             | Implementação                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Serviços de nível de contêiner                     | Obrigatório                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Notificação de progresso & suporte ao cancelamento | Recomendado                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Enumeração de metadados                         | Opcional (necessário apenas para formatos que dão suporte a metadados em nível de contêiner) |



 

Interfaces de decodificador Frame-Level



| Interface                                                           | Responsabilidades          | Implementação                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Serviços de nível de quadro      | Obrigatório                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Enumeração de metadados      | Obrigatório                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Transformações de decodificador nativo | Recomendado                   |
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

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



