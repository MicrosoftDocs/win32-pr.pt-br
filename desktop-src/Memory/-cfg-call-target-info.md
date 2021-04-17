---
description: Representa informações sobre destinos de chamada para a proteção de fluxo de controle (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Estrutura de CFG_CALL_TARGET_INFO (Ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775552"
---
# <a name="cfg_call_target_info-structure"></a>CFG \_ chamar \_ estrutura de informações de destino \_

Representa informações sobre destinos de chamada para a proteção de fluxo de controle (CFG).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Deslocamento**
</dt> <dd>

Deslocamento relativo a um endereço virtual (inicial) fornecido. Esse deslocamento deve ser alinhado em 16 bytes.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Sinalizadores que descrevem a operação a ser executada no endereço. Se o destino da chamada de cfg for definido como **\_ \_ \_ válido** , o endereço será marcado como válido para cfg. Caso contrário, ele será marcado como um destino de chamada inválido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Ntmmapi. h</dt> </dl> |



 

 




