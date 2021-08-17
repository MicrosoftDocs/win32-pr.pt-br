---
description: O decodificador de vídeo DV Media Foundation é uma transformação Media Foundation que decodifica vídeo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Decodificador de vídeo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd91cf325d9ba715d75aae884e29665d05d449ca39f01c195f9b13e2e1f8c1fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064089"
---
# <a name="dv-video-decoder"></a>Decodificador de vídeo DV

O decodificador de vídeo DV Media Foundation é uma [transformação Media Foundation](media-foundation-transforms.md) que DECODIFICA vídeo DV.

O decodificador de vídeo DV dá suporte aos seguintes tipos de entrada:



| Subtype                 | Descrição                  |
|-------------------------|------------------------------|
| **MFVideoFormat \_ DVC**  | Vídeo de DVC/DV                 |
| **MFVideoFormat \_ DVHD** | HD-DVCR (1125-60 ou 1250-50) |
| **MFVideoFormat \_ DVSD** | SDL-DVCR (525-60 ou 625-50)  |
| **MFVideoFormat \_ DVSL** | SD-DVCR (525-60 ou 625-50)   |



 

Ele dá suporte a um único tipo de saída:



| Subtype             | Descrição |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | Vídeo do YUY2  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 




