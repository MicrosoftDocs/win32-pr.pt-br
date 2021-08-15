---
title: MPSAMPLE_DATA estrutura (MpClient.h)
description: Dados de notificação passados para a função de retorno de chamada de envio de exemplo.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- MPSAMPLE_DATA estrutura herdada Windows recursos de ambiente
- PMPSAMPLE_DATA de estrutura herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafafd2ff7162dcb50bd5e2ea92cd56ab9f073332238dc0742845f9c48c5a588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747409"
---
# <a name="mpsample_data-structure"></a>Estrutura MPSAMPLE \_ DATA

Dados de notificação passados para a função de retorno de chamada de envio de exemplo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSampleIndex**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Índice do item de exemplo para o qual o status de envio é relatado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





