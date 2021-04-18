---
description: Define algoritmos para o processador de vídeo que é usado pelo \_ algoritmo do processador de vídeo MF \_ \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Enumeração de MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781236"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>\_Enumeração de \_ tipo de algoritmo do processador de vídeo MF \_ \_

Define algoritmos para o processador de vídeo que é usado pelo [ \_ algoritmo do \_ processador \_ de vídeo MF](mf-video-processor-algorithm.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_padrão de \_ algoritmo do processador de vídeo MF \_ \_**
</dt> <dd>

o modo padrão favorece um equilíbrio entre qualidade e velocidade

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_Algoritmo do processador de vídeo MF \_ \_ \_ MRF \_ CRF \_ 444**
</dt> <dd>

O processador de vídeo sempre será processado internamente no AYUV e usará filtros de alta qualidade.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                              |
| INSERI<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




