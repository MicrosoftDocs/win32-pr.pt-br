---
description: Contém sinalizadores para um objeto de ativação Media Foundation transformação (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: MF_TRANSFORM_FLAGS_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54d8775cb58980e0b5b4a8557ae4a3e8082b045eb3e87330841f75dfd057774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739224"
---
# <a name="mf_transform_flags_attribute-attribute"></a>Atributo MF \_ TRANSFORM \_ FLAGS \_ Attribute

Contém sinalizadores para um objeto de ativação Media Foundation transformação (MFT).

## <a name="data-type"></a>Tipo de dados

**UINT32**

O valor é um **OR** bit a bit de sinalizadores da [**\_ enumeração MFT \_ ENUM \_ FLAG.**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag)

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo é definido nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela [**função MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) O atributo contém sinalizadores que descrevem o MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 
