---
title: Estrutura de MPEXPIRATION_DATA (MpClient. h)
description: Notificação de status de expiração do produto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPEXPIRATION_DATA
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPEXPIRATION_DATA
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f270b7d433e6de7cd1eb3e7a3cfc88c9cb85c6087c20371ac804ec61d949d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976026"
---
# <a name="mpexpiration_data-structure"></a>\_Estrutura de dados MPEXPIRATION

Notificação de status de expiração do produto.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Motivo**
</dt> <dd>

Tipo: **\_ \_ motivo de expiração do MP**

</dd> <dd>

Motivo da expiração. Esse é um dos seguintes valores possíveis:



| Valor                                                                                                                                                                                                                                | Significado                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <dt>**MP \_ 0 de \_ desconhecido expirado**</dt> <dt></dt> </dl> | Desconhecido.<br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <dt>**MP \_ \_Avaliação expirada**</dt> <dt>1</dt> </dl>          | Período.<br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <dt>**MP \_ \_Wat 2 expirado**</dt> <dt></dt> </dl>             | Wat.<br/>        |



 

</dd> <dt>

**State**
</dt> <dd>

Tipo: **\_ \_ \_ relatório de estado de expiração do PG**

</dd> <dd>

Estado de expiração. Esse é um dos seguintes valores possíveis:



| Valor                                                                                                                                                                                                                                                                      | Significado                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <dt>**MP \_ Relatório de estado de EXPIRAção \_ \_ \_ desconhecido**</dt> <dt>0</dt> </dl> | Estado desconhecido.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <dt>**MP \_ Relatório de \_ estado expirado \_ \_ válido**</dt> <dt>1</dt> </dl>       | Sem expiração.<br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <dt>**MP \_ \_ \_ \_ Aviso de expiração do relatório de estado**</dt> <dt>2</dt> </dl> | Quase vencido.<br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <dt>**MP \_ EXPIRAr \_ \_ relatório de \_ estado**</dt> expirado <dt>3</dt> </dl> | Vencer.<br/>       |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





