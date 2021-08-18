---
description: representa informações sobre destinos de chamada para Control Flow Guard (CFG).
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
ms.openlocfilehash: e3bd7d351e890a968f2fa01ddffa6c8e3be16164d78393894055f55660c516bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040276"
---
# <a name="cfg_call_target_info-structure"></a>CFG \_ chamar \_ estrutura de informações de destino \_

representa informações sobre destinos de chamada para Control Flow Guard (CFG).

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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Ntmmapi. h</dt> </dl> |



 

 




