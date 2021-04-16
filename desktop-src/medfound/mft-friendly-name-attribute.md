---
description: Contém o nome de exibição para uma transformação de Media Foundation baseada em hardware (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: Atributo MFT_FRIENDLY_NAME_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752351"
---
# <a name="mft_friendly_name_attribute-attribute"></a>\_Atributo de \_ atributo de nome amigável de MFT \_

Contém o nome de exibição para uma transformação de Media Foundation baseada em hardware (MFT).

## <a name="data-type"></a>Tipo de dados

**WCHAR \** _

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Esse atributo tem suporte de MFTs baseadas em hardware. Ele também é definido nos ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) alocados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando esses ponteiros representam MFTs baseadas em hardware.

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

 

 




