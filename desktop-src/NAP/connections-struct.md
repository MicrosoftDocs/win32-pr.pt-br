---
title: Estrutura de conexões (NapEnforcementClient.h)
description: Contém informações sobre a lista de conexões mantidas por um executor.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- NAP da estrutura de conexões
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91e2dc404ff50c7edc3ba80a3c772ac6be762c1fe49575d8503a783e83bbef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800143"
---
# <a name="connections-structure"></a>Estrutura de conexões

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **estrutura connections** contém informações sobre a lista de conexões mantidas por um executor.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a>Membros

<dl> <dt>

**contagem**
</dt> <dd>

O número de conexões ativas atualmente mantidas por um executor dentro do intervalo 0 (zero) para [**maxConnectionCountPerEnforcer**](nap-type-constants.md).

</dd> <dt>

**localNetworkGateways**
</dt> <dd>

Um ponteiro COM para uma lista de interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) que representam conexões de cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência nap](nap-reference.md)
</dt> <dt>

[Estruturas NAP](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





