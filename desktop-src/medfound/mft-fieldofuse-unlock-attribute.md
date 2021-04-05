---
description: Contém um ponteiro IMFFieldOfUseMFTUnlock, que pode ser usado para desbloquear uma Media Foundation transformação (MFT). A interface IMFFieldOfUseMFTUnlock é usada para desbloquear uma MFT que tem restrições de campo de uso.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Atributo MFT_FIELDOFUSE_UNLOCK_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661824"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>\_Atributo de \_ atributo de desbloqueio de MFT FIELDOFUSE \_

Contém um ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que pode ser usado para desbloquear uma Media Foundation transformação (MFT). A interface **IMFFieldOfUseMFTUnlock** é usada para desbloquear uma MFT que tem restrições de campo de uso.

## <a name="data-type"></a>Tipo de dados

**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ armazenado como _*IUnknown \**_

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

Para obter mais informações sobre esse atributo, consulte [campo de restrições de uso](field-of-use-restrictions.md).

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

[Campo de restrições de uso](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




