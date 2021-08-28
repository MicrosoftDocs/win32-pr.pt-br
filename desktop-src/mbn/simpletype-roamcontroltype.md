---
description: Descreve como o perfil controla o roaming.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simples de roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19243625c07afae49011638a37734a5515e626d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480232"
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


| Valor | Descrição | 
|-------|-------------|
| AllRoamAllowed | <p>O roaming é permitido em redes de parceiros e não parceiros.</p> | 
| PartnerRoamAllowed | <p>O roaming só é permitido em redes de parceiros.</p> | 
| NoRoamAllowed | <p>Nenhum roaming é permitido.</p> | 


 

 



