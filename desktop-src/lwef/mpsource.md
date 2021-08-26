---
title: Enumeração MPSOURCE (MpClient.h)
description: Possível categoria de origem.
ms.assetid: 1AD12D67-C74B-481A-AC9B-D119AABDB6E9
keywords:
- Recursos de ambiente herdado da enumeração MPSOURCE Windows ambiente
- Ponteiro de enumeração PMPSOURCE Herdado Windows ambiente
topic_type:
- apiref
api_name:
- MPSOURCE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59eb014ab78645d78cd2942c37477d9a19d2572826859be77c6f5ecddfcb1bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961096"
---
# <a name="mpsource-enumeration"></a>Enumeração MPSOURCE

Possível categoria de origem.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPSOURCE { 
  MPSOURCE_UNKNOWN             = 0,
  MPSOURCE_USER                = 1,
  MPSOURCE_SYSTEM              = 2,
  MPSOURCE_REALTIME            = 3,
  MPSOURCE_IOAV                = 4,
  MPSOURCE_NIS                 = 5,
  MPSOURCE_BHO                 = 6,
  MPSOURCE_IEPROTECT           = 6,
  MPSOURCE_ELAM                = 7,
  MPSOURCE_LOCAL_ATTESTATION   = 8,
  MPSOURCE_REMOTE_ATTESTATION  = 9,
  MPSOURCE_AMSI                = 10,
  MP_SOURCE_MAXVALUE           = 10
} MPSOURCE, *PMPSOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPSOURCE_UNKNOWN"></span><span id="mpsource_unknown"></span>**MPSOURCE \_ DESCONHECIDO**
</dt> <dd>

Origem desconhecida.

</dd> <dt>

<span id="MPSOURCE_USER"></span><span id="mpsource_user"></span>**USUÁRIO DO \_ MPSOURCE**
</dt> <dd>

Iniciado pelo usuário.

</dd> <dt>

<span id="MPSOURCE_SYSTEM"></span><span id="mpsource_system"></span>**SISTEMA \_ MPSOURCE**
</dt> <dd>

iniciado pelo sistema.

</dd> <dt>

<span id="MPSOURCE_REALTIME"></span><span id="mpsource_realtime"></span>**MPSOURCE \_ REALTIME**
</dt> <dd>

Componente em tempo real iniciado.

</dd> <dt>

<span id="MPSOURCE_IOAV"></span><span id="mpsource_ioav"></span>**MPSOURCE \_ IOAV**
</dt> <dd>

Downloads do IE e Outlook Express Attachments iniciados.

</dd> <dt>

<span id="MPSOURCE_NIS"></span><span id="mpsource_nis"></span>**MPSOURCE \_ NIS**
</dt> <dd>

Sistema de inspeção de rede.

</dd> <dt>

<span id="MPSOURCE_BHO"></span><span id="mpsource_bho"></span>**MPSOURCE \_ BHO**
</dt> <dd>

BHO – script Web (preterido).

</dd> <dt>

<span id="MPSOURCE_IEPROTECT"></span><span id="mpsource_ieprotect"></span>**MPSOURCE \_ IEPROTECT**
</dt> <dd>

IE – IExtensionValidation.

</dd> <dt>

<span id="MPSOURCE_ELAM"></span><span id="mpsource_elam"></span>**MPSOURCE \_ ELAM**
</dt> <dd>

ELAM

</dd> <dt>

<span id="MPSOURCE_LOCAL_ATTESTATION"></span><span id="mpsource_local_attestation"></span>**ATESTADO LOCAL \_ DO \_ MPSOURCE**
</dt> <dd>

Atestado local.

</dd> <dt>

<span id="MPSOURCE_REMOTE_ATTESTATION"></span><span id="mpsource_remote_attestation"></span>**ATESTADO REMOTO DO \_ \_ MPSOURCE**
</dt> <dd>

Atestado remoto.

</dd> <dt>

<span id="MPSOURCE_AMSI"></span><span id="mpsource_amsi"></span>**MPSOURCE \_ AMSI**
</dt> <dd>

AMSI

</dd> <dt>

<span id="MP_SOURCE_MAXVALUE"></span><span id="mp_source_maxvalue"></span>**VALOR MÁXIMO \_ \_ DA ORIGEM DO MP**
</dt> <dd>

Valor máximo possível.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





