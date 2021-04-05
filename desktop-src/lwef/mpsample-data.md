---
title: Estrutura de MPSAMPLE_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada de envio de exemplo.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSAMPLE_DATA
- Ponteiro de estrutura de PMPSAMPLE_DATA recursos de ambiente herdados do Windows
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
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086428"
---
# <a name="mpsample_data-structure"></a>\_Estrutura de dados MPSAMPLE

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





