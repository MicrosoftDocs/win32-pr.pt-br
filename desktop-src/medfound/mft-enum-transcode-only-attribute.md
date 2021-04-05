---
description: Especifica se um decodificador é otimizado para transcodificação em vez de para reprodução.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Atributo MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370682"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>\_Atributo de \_ \_ atributo somente TRANScodificação de MFT \_

Especifica se um decodificador é otimizado para transcodificação em vez de para reprodução.

Atualmente, esse atributo se aplica somente a decodificadores baseados em hardware que usam o mini-driver AVStream. O atributo é armazenado no registro sob as informações de recursos do decodificador. Para obter mais informações, consulte a documentação de [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).

Normalmente, os aplicativos não usam esse atributo.

## <a name="data-type"></a>Tipo de dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Se essa entrada de registro estiver presente e igual a 1, a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ignorará o decodificador, a menos que o chamador tenha especificado o sinalizador de **enumeração de MFT de \_ \_ \_ transcodificação \_ somente** no **MFTEnumEx**.

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

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
