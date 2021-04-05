---
title: Tipo simples de Logontype
description: Define os valores possíveis do elemento Logontype.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- tipo simples de Logontype Agendador de Tarefas
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086067"
---
# <a name="logontype-simple-type"></a>Tipo simples de Logontype

Define os valores possíveis do elemento [**Logontype**](taskschedulerschema-logontype-principaltype-element.md) .

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

O tipo simples de **Logontype** define os valores a seguir.



| Valor                      | Descrição                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4U                        | O usuário deve fazer logon usando um logon S4U (serviço para usuário). Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.<br/>                                                                                                                                                          |
| Senha                   | O usuário deve fazer logon usando uma senha.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | O usuário já deve estar conectado. A tarefa será executada somente em uma sessão interativa existente.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | Não está mais em uso; atualmente idêntica à senha.<br/> **Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista e Windows server 2008:** A tarefa será executada em uma sessão interativa existente ou o usuário deverá fazer logon usando uma senha.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos simples de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





