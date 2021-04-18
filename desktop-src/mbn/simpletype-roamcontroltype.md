---
description: Descreve como o perfil controla o roaming.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simples de roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784678"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Tipo simples de roamControlType

Descreve como o perfil controla o roaming.

Há dois Estados de registro de roaming possíveis:

-   Parceiro: registrado em uma rede afiliada de forma bem associada à rede doméstica
-   Não parceiro: registrado em uma rede que não está fortemente afiliada com a rede doméstica

O significado preciso de "parceiro" varia de acordo com a rede, mas representa uma relação mais próxima com taxas mais favoráveis do que um não parceiro. Esse pode ser o caso se um operador com base em regiões tiver uma organização de negócios para usar a rede de acesso de rádio de outra operadora fora de sua área inicial. Ele também pode representar a diferença entre o roaming em uma região (por exemplo, a UE) e fora dele.

Observe que [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) é um atributo mais expressivo do que **roamControlType**, e um perfil deve usar **roamControlType** ou **roamApplicabilityType**, mas não ambos. (Se um perfil usar ambos, ambos serão aplicados. O resultado é a interseção dos dois.)

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O tipo simples **roamControlType** define os valores a seguir.

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
<td>AllRoamAllowed</td>
<td><p>O roaming é permitido em redes de parceiros e não parceiros.</p></td>
</tr>
<tr class="even">
<td>PartnerRoamAllowed</td>
<td><p>O roaming só é permitido em redes de parceiros.</p></td>
</tr>
<tr class="odd">
<td>NoRoamAllowed</td>
<td><p>Nenhum roaming é permitido.</p></td>
</tr>
</tbody>
</table>

 

 



