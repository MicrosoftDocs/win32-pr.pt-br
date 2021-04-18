---
description: Define o status do Gerenciador de proteção de saída (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Enumeração de MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105812802"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>\_Enumeração de \_ status de OPM do mecanismo de mídia MF \_ \_

Define o status do [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**\_OPM do mecanismo de mídia MF \_ \_ \_ não \_ solicitado**
</dt> <dd>

Status padrão. Usado para retornar o status correto quando o conteúdo está desprotegido.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**\_OPM do mecanismo de mídia MF \_ \_ \_ estabelecido**
</dt> <dd>

OPM estabelecido com êxito.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ \_ VM com falha em OPM do mecanismo de mídia \_ MF**
</dt> <dd>

OPM falhou porque está sendo executado em uma VM (máquina virtual).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**o \_ mecanismo de mídia MF \_ \_ OPM \_ falhou em \_ BDA**
</dt> <dd>

OPM falhou porque não há driver de gráficos e o sistema está usando o adaptador de vídeo básico (BDA).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**o \_ Driver de mídia MF \_ \_ OPM \_ falhou \_ sem sinal \_**
</dt> <dd>

OPM falhou porque o driver de gráficos não é assinado por PE, voltando para distorção.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**\_falha em \_ OPM do mecanismo de mídia MF \_ \_**
</dt> <dd>

OPM falhou por outros motivos.

</dd> </dl>

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

 

 




