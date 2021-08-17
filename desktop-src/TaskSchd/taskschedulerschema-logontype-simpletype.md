---
title: tipo simples logonType
description: Define os valores possíveis do elemento LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- tipo simples logonType Agendador de Tarefas
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f40301957ec323b8abf7c09829bf3b551e2e1665a811409622d342784d86e54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758888"
---
# <a name="logontype-simple-type"></a>tipo simples logonType

Define os valores possíveis do [**elemento LogonType.**](taskschedulerschema-logontype-principaltype-element.md)

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O **tipo simples logonType** define os valores a seguir.



| Valor                      | Descrição                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4u                        | O usuário deve fazer logon usando um serviço para logon de usuário (S4U). Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.<br/>                                                                                                                                                          |
| Senha                   | O usuário deve fazer logoff usando uma senha.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | O usuário já deve estar conectado. A tarefa será executado somente em uma sessão interativa existente.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | Não está mais em uso; atualmente idêntico à Senha.<br/> **Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows Vista e Windows Server 2008:** A tarefa será executado em uma sessão interativa existente ou o usuário deverá fazer logon usando uma senha.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas tipos simples de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





