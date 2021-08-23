---
description: Contém um ponteiro IMFFieldOfUseMFTUnlock, que pode ser usado para desbloquear uma transformação Media Foundation (MFT). A interface IMFFieldOfUseMFTUnlock é usada para desbloquear uma MFT que tem restrições de campo de uso.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476ae7ffdc6de506b4dbc2f49ec7a6b19b01affafd53f0c9495f9f5c396c5caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973065"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>Atributo MFT \_ FIELDOFUSE \_ UNLOCK \_

Contém um [**ponteiro IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que pode ser usado para desbloquear uma transformação Media Foundation (MFT). A interface **IMFFieldOfUseMFTUnlock** é usada para desbloquear uma MFT que tem restrições de campo de uso.

## <a name="data-type"></a>Tipo de dados

**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) \* *_ armazenado como _* Iunknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

Para obter mais informações sobre esse atributo, consulte [Restrições de campo de uso.](field-of-use-restrictions.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Restrições de campo de uso](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




