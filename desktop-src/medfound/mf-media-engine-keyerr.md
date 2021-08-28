---
description: Define códigos de erro de chave de mídia para o mecanismo de mídia.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: MF_MEDIA_ENGINE_KEYERR enumeração
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 5a3573f721f31ffbe3858c7d6fb3c713468bc347f04a1b5d85c5839a1e18511b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113926"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>\_ \_ Enumeração KEYERR do MECANISMO \_ DE MÍDIA MF

Define códigos de erro de chave de mídia para o mecanismo de mídia.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ UNKNOWN**
</dt> <dd>

Ocorreu um erro desconhecido.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**CLIENTE MF \_ MEDIAENGINE \_ KEYERR \_**
</dt> <dd>

Ocorreu um erro com o cliente.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**SERVIÇO MF \_ MEDIAENGINE \_ KEYERR \_**
</dt> <dd>

Ocorreu um erro com o serviço.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ OUTPUT**
</dt> <dd>

Ocorreu um erro com a saída.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE** 
</dt> <dd>

Ocorreu um erro relacionado a uma alteração de hardware.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**DOMÍNIO DO MF \_ MEDIAENGINE \_ KEYERR \_**
</dt> <dd>

Ocorreu um erro com o domínio.

</dd> </dl>

## <a name="remarks"></a>Comentários

**MF \_ MEDIA \_ ENGINE \_ KEYERR** é  usado com o parâmetro de código [**de IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) e o valor *de* código retornado de [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[enumerações Media Foundation dados](media-foundation-enumerations.md)
</dt> </dl>

 

 




