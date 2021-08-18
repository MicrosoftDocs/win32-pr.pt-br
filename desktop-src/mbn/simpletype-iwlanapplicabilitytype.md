---
description: Enumeração que descreve o tipo de conexão de rede em que um perfil é aplicável.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simples iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ede1e4c360bfd88fa8ca0eb3494a9400f4dfc2a1eb70f7857156caabf7b469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035744"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo simples iwlanApplicabilityType

Enumeração que descreve o tipo de conexão de rede em que um perfil é aplicável.

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

O **tipo simples iwlanApplicabilityType** define os valores a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CellularOnly</td>
<td><p>O perfil é válido somente para conexões de rede celular.</p></td>
</tr>
<tr class="even">
<td>CellularAndIwlan</td>
<td><p>O perfil é válido para conexões de celular Wi-Fi descarregadas.</p></td>
</tr>
<tr class="odd">
<td>IwlanOnly</td>
<td><p>O perfil é válido para Wi-Fi somente conexões descarregadas.</p></td>
</tr>
</tbody>
</table>

 

 



