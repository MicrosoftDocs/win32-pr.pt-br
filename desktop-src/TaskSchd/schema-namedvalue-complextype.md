---
title: Tipo complexo nomeadovalue
description: Define um nome que está associado a um valor em um par de nome-valor.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- tipo complexo nomeadovalue Agendador de Tarefas
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918745"
---
# <a name="namedvalue-complex-type"></a>Tipo complexo nomeadovalue

Define um nome que está associado a um valor em um par de nome-valor.

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nome | Tipo                                                                    | Descrição                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| name | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica o nome que está associado a um valor em um par de nome-valor. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





