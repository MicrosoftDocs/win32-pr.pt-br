---
title: Tipo simples de sessionStateChangeType
description: Define valores para o tipo de Terminal Server alteração de estado de sessão que você pode usar para disparar uma tarefa a ser iniciada.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- Agendador de Tarefas tipo simples de sessionStateChangeType
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a67334b2e8d51404a0e5e78a7d2b3e49908cd1c6ce74f499e66272d2db9be910
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099806"
---
# <a name="sessionstatechangetype-simple-type"></a>Tipo simples de sessionStateChangeType

Define valores para o tipo de Terminal Server alteração de estado de sessão que você pode usar para disparar uma tarefa a ser iniciada.

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O tipo simples **sessionStateChangeType** define os valores a seguir.



| Valor             | Descrição                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConsoleConnect    | Terminal Server alteração de estado da conexão do console. Por exemplo, quando você se conecta a uma sessão de usuário no computador local, alternando os usuários no computador. <br/>                            |
| ConsoleDisconnect | Alteração do estado de desconexão do Console Terminal Server. Por exemplo, quando você se desconecta a uma sessão de usuário no computador local, alternando os usuários no computador. <br/>                      |
| RemoteConnect     | Terminal Server alteração de estado da conexão remota. Por exemplo, quando um usuário se conecta a uma sessão de usuário usando o programa Conexão de Área de Trabalho Remota de um computador remoto. <br/>            |
| RemoteDisconnect  | Terminal Server alteração de estado de desconexão remota. Por exemplo, quando um usuário se desconecta de uma sessão de usuário enquanto usa o programa de Conexão de Área de Trabalho Remota de um computador remoto. <br/> |
| SessionLock       | Alteração de estado bloqueado da sessão de Terminal Server. Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é bloqueado. <br/>                                                       |
| SessionUnlock     | Alteração de estado desbloqueado da sessão de Terminal Server. Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é desbloqueado.<br/>                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





