---
description: Altera a taxa de quadros de um fluxo de vídeo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: DSP do Conversor de Taxa de Quadros (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca4a728f37caa43ee99a0d293d5113e9c26cfb1dcfe51f399482fb614283737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600486"
---
# <a name="frame-rate-converter-dsp"></a>DSP do Conversor de Taxa de Quadros

Altera a taxa de quadros de um fluxo de vídeo.

## <a name="clsid"></a>CLSID

CLSID \_ CFrameRateConvertDmo

## <a name="interfaces"></a>Interfaces

-   **Imediaobject**
-   **IMFTransform**
-   **Ipropertystore**

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

-   [MFPKEY \_ CONV \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ CONV \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Comentários

Esse DSP altera a taxa de quadros repetindo ou soltando quadros.

Por padrão, o DSP obtém as taxas de quadros dos tipos de mídia. Opcionalmente, você pode especificar as taxas de quadros definindo as propriedades MFPKEY \_ CONV \_ INPUTFRAMERATE e MFPKEY \_ CONV \_ OUTPUTFRAMERATE. Esses valores substituem a taxa de quadros determinada no tipo de mídia. No entanto, se você estiver usando esse DSP no pipeline Media Foundation, não deverá definir essas propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




