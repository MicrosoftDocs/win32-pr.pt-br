---
description: O decodificador de vídeo DV Media Foundation é uma transformação Media Foundation que decodifica vídeo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Decodificador de vídeo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646589"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 




