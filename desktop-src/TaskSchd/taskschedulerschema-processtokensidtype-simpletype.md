---
title: Tipo simples processTokenSidType
description: Define os valores possíveis para o elemento ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- tipo simples processTokenSidType Agendador de Tarefas
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 505f8abe340af36c25792ec97a5a465a166eedb74921c800d2a568d10a5cce0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611898"
---
# <a name="processtokensidtype-simple-type"></a>Tipo simples processTokenSidType

Define os valores possíveis para o [**elemento ProcessTokenSidType (principalType).**](taskschedulerschema-processtokensidtype-principaltype-element.md)

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O **tipo simples processTokenSidType** define os valores a seguir.



| Valor        | Descrição                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nenhum         | As tarefas são executadas em um processo que não contém um SID de token de processo (nenhuma alteração será feita na lista de grupos de tokens de processo).<br/> |
| Irrestrito | Um SID de tarefa será derivado do caminho completo da tarefa e será adicionado à lista de grupos de tokens de processo.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



 

 





