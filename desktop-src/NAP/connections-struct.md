---
title: Estrutura de conexões (NapEnforcementClient. h)
description: Contém informações sobre a lista de conexões mantidas por um aplicador.
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
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919214"
---
# <a name="connections-structure"></a>Estrutura de conexões

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A estrutura **conexões** contém informações sobre a lista de conexões mantidas por um aplicador.

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

O número de conexões ativas atualmente mantidas por um aplicador dentro do intervalo de 0 (zero) a [**maxConnectionCountPerEnforcer**](nap-type-constants.md).

</dd> <dt>

**connections**
</dt> <dd>

Um ponteiro COM para uma lista de interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) que representam conexões de cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de NAP](nap-reference.md)
</dt> <dt>

[Estruturas de NAP](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





