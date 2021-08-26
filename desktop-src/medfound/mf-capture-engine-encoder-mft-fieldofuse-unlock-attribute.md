---
description: Permite que o mecanismo de captura use um codificador com restrições de campo de uso.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Atributo MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f2fb9d85c68adbc726fa4b36f2ea960a33e68c4dff836fac0370c8e9e4e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060816"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_FIELDOFUSE de \_ \_ atributo de \_ \_ \_ desbloqueio \_ do mecanismo de captura do MF MFT

Permite que o mecanismo de captura use um codificador com restrições de campo de uso.

## <a name="data-type"></a>Tipo de dados

**IUnknown\***

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementado pelo chamador. Espera-se que a implementação dessa interface do chamador execute um handshake com o codificador, conforme descrito em [campo de restrições de uso](field-of-use-restrictions.md). Microsoft Media Foundation não define o handshake — normalmente, ele envolveria algum tipo de troca de criptografia.

Internamente, o mecanismo de captura define o ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) no codificador definindo o atributo [atributo de \_ \_ desbloqueio \_ de MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) do codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




