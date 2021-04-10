---
description: Interfaces do codificador
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces do codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170306"
---
# <a name="encoder-interfaces"></a>Interfaces do codificador


As tabelas a seguir mostram as interfaces implementadas pelos codificadores do Windows Imaging Component (WIC) e o diagrama de classe mostra a hierarquia de herança.

Interfaces do codificador Container-Level



| Interface                                                                                       | Responsabilidades                             | Implementação                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Serviços de nível de contêiner                     | Obrigatório                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Notificação de progresso & suporte ao cancelamento | Recomendadas                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Serviços de serialização de metadados              | Opcional (necessário apenas para formatos que dão suporte a metadados em nível de contêiner) |



 

Interfaces do codificador Frame-Level



| Interface                                                       | Responsabilidades                | Implementação |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Serviços de nível de quadro            | Obrigatório       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Serviços de serialização de metadados | Obrigatório       |



 

![hierarquia de herança da interface do codificador WIC](graphics/wicencoderinterfaces.png)

Você observará que as interfaces do codificador são quase imagens espelhadas das interfaces do decodificador e que a maioria dos métodos nessas interfaces correspondem aos métodos nas interfaces do decodificador relacionadas. Agora que você está familiarizado com a implementação de um decodificador habilitado por WIC, a implementação de um codificador habilitado para WIC também parecerá familiar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando um codificador de WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Implementando IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



