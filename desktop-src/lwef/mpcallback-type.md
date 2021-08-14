---
title: MPCALLBACK_TYPE enumeração (MpClient.h)
description: Possíveis tipos de retorno de chamada.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE de enumeração herdada Windows recursos de ambiente
- PMPCALLBACK_TYPE de enumeração herdada Windows ambiente
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35c1d6e92acc7c789b5f6d85184ba74970e12bedcc5cd412fc378b8c8dfeb066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883550"
---
# <a name="mpcallback_type-enumeration"></a>Enumeração MPCALLBACK \_ TYPE

Possíveis tipos de retorno de chamada.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK \_ UNKNOWN**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**STATUS DE \_ MPCALLBACK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**AMEAÇA DE \_ MPCALLBACK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK \_ SCAN**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK \_ CLEAN**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK \_ PRECHECK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK \_ SIGUPDATE**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**EXEMPLO DE \_ MPCALLBACK**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK \_ RESERVADO**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**NOTIFICAÇÃO DE \_ CONFIGURAÇÃO MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK \_ FASTPATH**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**EXPIRAÇÃO DO \_ PRODUTO MPCALLBACK \_**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK \_ NIS \_ PRIVATE**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK \_ HEALTH**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK \_ ENDOFLIFE**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK \_ MALWARETOAST**
</dt> <dd></dd> <dt>

<span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





