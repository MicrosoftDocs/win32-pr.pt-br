---
description: Permite que o mecanismo de captura use um decodificador com restrições de campo de uso.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: Atributo MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787700"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_FIELDOFUSE de \_ \_ atributo do \_ \_ \_ desbloqueio \_ do mecanismo de captura do MF MFT

Permite que o mecanismo de captura use um decodificador com restrições de campo de uso.

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [_ *IMFFieldOfUseMFTUnlock* *](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementado pelo chamador. Espera-se que a implementação dessa interface do chamador execute um handshake com o decodificador, conforme descrito em [campo de restrições de uso](field-of-use-restrictions.md). Microsoft Media Foundation não define o handshake — normalmente, ele envolveria algum tipo de troca de criptografia.

Internamente, o mecanismo de captura define o ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) no decodificador definindo o atributo [de \_ \_ \_ atributo de desbloqueio de MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) do decodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




