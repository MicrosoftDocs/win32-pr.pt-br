---
description: Contém os tipos de saída registrados para uma Media Foundation transformação (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Atributo MFT_OUTPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d244bc5184652d0ba1d89ebf4e1beaddb472bb1d6fa09c05d1edf99030fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462776"
---
# <a name="mft_output_types_attributes-attribute"></a>\_Atributo de \_ atributos de tipos de saída de MFT \_

Contém os tipos de saída registrados para uma Media Foundation transformação (MFT).

## <a name="data-type"></a>Tipo de dados

**MFT \_ Informações de tipo de registro armazenadas como byte \_ \_ \[ \]** **\[ \]**

## <a name="remarks"></a>Comentários

Esse atributo é definido nos ponteiros do [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Esse atributo contém uma matriz de estruturas de informações de tipo de registro de MFT que descrevem um ou mais formatos de saída com suporte pelo MFT. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) Esses valores são extraídos do registro e são destinados como uma dica ao aplicativo. O MFT pode dar suporte a formatos adicionais. Para definir o formato de saída real, você deve criar o MFT e chamar [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




