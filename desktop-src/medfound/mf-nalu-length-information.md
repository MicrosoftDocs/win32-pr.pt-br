---
description: Indica os comprimentos de NALUs no exemplo. Esse é um BLOB MF definido em amostras de entrada compactadas para o decodificador H.264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: MF_NALU_LENGTH_INFORMATION atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2020c0086247adda742ce2613045bb3a2004c3b8c13c7cdcb04a0ff3997cf0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104412"
---
# <a name="mf_nalu_length_information-attribute"></a>Atributo MF \_ NALU \_ LENGTH \_ INFORMATION

Indica os comprimentos de NALUs no exemplo. Esse é um **BLOB** MF definido em amostras de entrada compactadas para o decodificador H.264.

## <a name="data-type"></a>Tipo de dados

**Blob**

## <a name="remarks"></a>Comentários

Para que esse atributo seja definido, a mídia deve ser do tipo MEDIASUBTYPE H264 e o atributo MF NALU LENGTH SET deve ser definido no tipo de mídia de entrada \_ MEDIASUBTYPE [ \_ \_ \_ ](mf-nalu-length-set.md) \_ H264.

Definir INFORMAÇÕES DE COMPRIMENTO DE NALU do MF como um BLOB na amostra de entrada, com uma \_ \_ \_ DWORD para cada NALU no exemplo.  Por exemplo, se houver AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), fatia IDR 2 (60 k), deverá haver 5 DWORDs com valores 9, 25, 10, 50 k, 60 k no **BLOB**.

Aqui, um código que define o **BLOB**, em que **rgdwNALULengthInfo** é uma matriz do tipo DWORD e **uiNaluLengthIdx** são os comprimentos NALU válidos definidos para o **BLOB**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




