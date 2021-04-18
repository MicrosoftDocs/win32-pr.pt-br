---
description: Indica os comprimentos de NALUs no exemplo. Este é um BLOB MF que é definido em exemplos de entrada compactados para o decodificador H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Atributo MF_NALU_LENGTH_INFORMATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807268"
---
# <a name="mf_nalu_length_information-attribute"></a>\_Atributo de \_ informações de comprimento de MF NALU \_

Indica os comprimentos de NALUs no exemplo. Este é um **blob** MF que é definido em exemplos de entrada compactados para o decodificador H. 264.

## <a name="data-type"></a>Tipo de dados

**BLOB**

## <a name="remarks"></a>Comentários

Para que esse atributo seja definido, a mídia deve ser do tipo MEDIASUBTYPE \_ H264 e o atributo de [ \_ conjunto de \_ comprimento \_ MF NALU](mf-nalu-length-set.md) deve ser definido no tipo de mídia de entrada de MEDIASUBTYPE \_ H264.

Defina \_ informações de comprimento de NALU MF \_ \_ como um **blob** no exemplo de entrada, com um DWORD para cada NALU no exemplo. Por exemplo, se houver AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), fatia de IDR 2 (60 k), deverá haver 5 DWORDs com os valores 9, 25, 10, 50 k, 60 k no **blob**.

Aqui, um código que define o **blob**, em que **rgdwNALULengthInfo** é uma matriz do tipo DWORD e **UINALULENGTHIDX** é o comprimento de NALU válido definido para o **blob**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




