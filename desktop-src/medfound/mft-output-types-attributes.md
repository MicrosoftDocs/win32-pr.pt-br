---
description: Contém os tipos de saída registrados para uma Media Foundation transformação (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Atributo MFT_OUTPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786164"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




