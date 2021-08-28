---
description: Enumeração que descreve o tipo de conexão de rede onde um perfil é aplicável.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simples de iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529ae39c2b0e137825e7a80d41c43203b0a27de7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478952"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo simples de iwlanApplicabilityType

Enumeração que descreve o tipo de conexão de rede onde um perfil é aplicável.

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O tipo simples **iwlanApplicabilityType** define os valores a seguir.


| Valor | Descrição | 
|-------|-------------|
| CellularOnly | <p>O perfil é válido somente para conexões de rede celular.</p> | 
| CellularAndIwlan | <p>O perfil é válido para conexões de celular ou Wi-Fi descarregadas.</p> | 
| IwlanOnly | <p>O perfil é válido somente para conexões descarregadas Wi-Fi.</p> | 


 

 



