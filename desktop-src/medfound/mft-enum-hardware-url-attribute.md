---
description: Contém o link simbólico para uma transformação de Media Foundation baseada em hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Atributo MFT_ENUM_HARDWARE_URL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165294"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>\_Atributo de \_ atributo de URL de hardware de enumeração de \_ MFT \_

Contém o link simbólico para uma transformação de Media Foundation baseada em hardware (MFT).

## <a name="data-type"></a>Tipo de dados

**WCHAR \** _

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Esse atributo tem suporte de MFTs baseadas em hardware. O valor do atributo é o link simbólico para o driver de dispositivo. Esse atributo também é definido nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alocados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando esses ponteiros representam MFTs baseadas em hardware.

O link simbólico deve ser considerado uma cadeia de caracteres opaca. Para obter o nome de exibição de um dispositivo, consulte o atributo [ \_ \_ nome amigável de MFT](mft-friendly-name-attribute.md) .

O MFTs de software não deve ter esse atributo definido.

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

[MFTs de hardware](hardware-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




