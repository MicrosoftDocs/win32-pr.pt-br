---
title: Tipo simples de processTokenSidType
description: Define os valores possíveis para o elemento ProcessTokenSidType (PrincipalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Agendador de Tarefas tipo simples de processTokenSidType
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369464"
---
# <a name="processtokensidtype-simple-type"></a>Tipo simples de processTokenSidType

Define os valores possíveis para o elemento [**ProcessTokenSidType (PrincipalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .

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

O tipo simples **processTokenSidType** define os valores a seguir.



| Valor        | Descrição                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nenhum         | As tarefas são executadas em um processo que não contém um SID de token de processo (nenhuma alteração será feita na lista de grupos de tokens de processo).<br/> |
| Irrestrito | Um SID de tarefa será derivado do caminho completo da tarefa e será adicionado à lista de grupos de tokens de processo.<br/>                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 





