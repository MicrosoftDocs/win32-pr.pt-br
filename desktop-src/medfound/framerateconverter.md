---
description: Altera a taxa de quadros de um fluxo de vídeo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Conversor de taxa de quadros DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646582"
---
# <a name="frame-rate-converter-dsp"></a>Conversor de taxa de quadros DSP

Altera a taxa de quadros de um fluxo de vídeo.

## <a name="clsid"></a>CLSID

\_CFRAMERATECONVERTDMO CLSID

## <a name="interfaces"></a>Interfaces

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>Formatos

-   ARGB 32
-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   IYUV
-   UYVY
-   Y211
-   Y411
-   Y41P
-   YUY2
-   YUYV
-   YV12
-   YVYU

## <a name="properties"></a>Propriedades

-   [MFPKEY \_ convu \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ convu \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Comentários

Esse DSP altera a taxa de quadros repetindo ou soltando quadros.

Por padrão, o DSP Obtém as taxas de quadros dos tipos de mídia. Opcionalmente, você pode especificar as taxas de quadros definindo as \_ Propriedades MFPKEY CONV \_ INPUTFRAMERATE e MFPKEY \_ CONV \_ OUTPUTFRAMERATE. Esses valores substituem a taxa de quadros fornecida no tipo de mídia. No entanto, se você estiver usando esse DSP dentro do pipeline de Media Foundation, não deverá definir essas propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




