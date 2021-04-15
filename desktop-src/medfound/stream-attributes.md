---
description: Atributos de fluxo
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Atributos de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502246"
---
# <a name="stream-attributes"></a>Atributos de fluxo

Os atributos a seguir se aplicam a fluxos de mídia. Para obter os atributos de um exemplo de mídia, use o método [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .



| Atributo                                                                                   | Descrição                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [MFStreamExtension \_ CameraExtrinsics](mfstreamextension-cameraextrinsics.md)               | A câmera é extrínsecos para o fluxo.         |
| [MFStreamExtension \_ PinholeCameraIntrinsics](mfstreamextension-pinholecameraintrinsics.md) | A câmera pinhole é intrínseca para o fluxo. |



 

Nem todo fluxo de mídia contém todos os atributos listados aqui. Em alguns casos, um atributo se aplica somente a determinados tipos de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> </dl>

 

 



