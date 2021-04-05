---
description: O roamApplicabilityType descreve as condições de roaming para as quais um perfil móvel se aplica.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simples de roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827082"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo simples de roamApplicabilityType

O roamApplicabilityType descreve as condições de roaming para as quais um perfil móvel se aplica.

Esse é um atributo mais expressivo do que [**roamControlType**](simpletype-roamcontroltype.md), e um perfil deve usar **roamControlType** ou **roamApplicabilityType**, mas não ambos. (Se um perfil usar ambos, ambos serão aplicados. O resultado é a interseção dos dois.)

Use esse atributo para diferenciar entre vários perfis com condições de roaming não associadas, para especificar diferentes atributos de perfil para, por exemplo, Home versus roaming.

Há três Estados de registro iniciais/móveis possíveis:

-   Página inicial: registrado na rede doméstica
-   Parceiro: registrado em uma rede afiliada de forma bem associada à rede doméstica
-   Não parceiro: registrado em uma rede que não está fortemente afiliada com a rede doméstica

O significado preciso de "parceiro" varia de acordo com a rede, mas representa uma relação mais próxima com taxas mais favoráveis do que um não parceiro. Esse pode ser o caso se um operador com base em regiões tiver uma organização de negócios para usar a rede de acesso de rádio de outra operadora fora de sua área inicial. Ele também pode representar a diferença entre o roaming em uma região (por exemplo, a UE) e fora dele.

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O tipo simples **roamApplicabilityType** define os valores a seguir.

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
<td>NonPartnerOnly</td>
<td><p>Este perfil é usado somente quando estiver em roaming em uma rede que não seja de parceiro</p></td>
</tr>
<tr class="even">
<td>PartnerOnly</td>
<td><p>Este perfil é usado somente quando estiver em roaming em uma rede de parceiros</p></td>
</tr>
<tr class="odd">
<td>HomeOnly</td>
<td><p>Este perfil é usado somente quando estiver na rede doméstica</p></td>
</tr>
<tr class="even">
<td>HomeAndPartner</td>
<td><p>Este perfil é usado somente quando em casa ou em uma rede de parceiros</p></td>
</tr>
<tr class="odd">
<td>PartnerAndNonpartner</td>
<td><p>Este perfil é usado quando não está em casa (roaming em qualquer rede)</p></td>
</tr>
<tr class="even">
<td>Em roaming</td>
<td><p>Este perfil é usado em todas as redes</p></td>
</tr>
</tbody>
</table>

 

 



