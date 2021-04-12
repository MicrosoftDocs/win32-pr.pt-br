---
description: Define códigos de erro de chave de mídia para o mecanismo de mídia.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Enumeração de MF_MEDIA_ENGINE_KEYERR
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
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297918"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>\_ \_ Enumeração KEYERR do mecanismo de mídia MF \_

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

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ desconhecido**
</dt> <dd>

Ocorreu um erro desconhecido.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_cliente MF MEDIAENGINE \_ KEYERR \_**
</dt> <dd>

Ocorreu um erro com o cliente.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_serviço MEDIAENGINE \_ KEYERR \_ MF**
</dt> <dd>

Ocorreu um erro com o serviço.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_saída de \_ KEYERR \_ MEDIAENGINE MF**
</dt> <dd>

Ocorreu um erro com a saída.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE** 
</dt> <dd>

Ocorreu um erro relacionado a uma alteração de hardware.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_MEDIAENGINE MF \_ KEYERR \_ domínio**
</dt> <dd>

Ocorreu um erro com o domínio.

</dd> </dl>

## <a name="remarks"></a>Comentários

**MF \_ O \_ mecanismo \_ de mídia KEYERR** é usado com o parâmetro de *código* de [**IMFMediaKeySessionNotify:: keyerror**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) e o valor de *código* retornado de [**IMFMediaKeySession:: GetError**](imfmediakeysession-geterror.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




