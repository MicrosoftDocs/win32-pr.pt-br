---
description: Implementando IWICBitmapCodecProgressNotification (codificador)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Implementando IWICBitmapCodecProgressNotification (codificador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829498"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a>Implementando IWICBitmapCodecProgressNotification (codificador)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Embora a interface [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) seja opcional, é recomendável que ela seja implementada na classe de codificador de nível de contêiner. Essa interface é discutida em mais detalhes na [implementação de IWICBitmapCodecProgressNotification (decodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md). A implementação é a mesma para o decodificador e o codificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Implementando IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Implementando IWICBitmapCodecProgressNotification (decodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



