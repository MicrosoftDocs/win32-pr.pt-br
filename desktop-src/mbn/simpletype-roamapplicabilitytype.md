---
description: O roamApplicabilityType descreve as condições de roaming às quais um perfil de roaming se aplica.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simples roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2ce8f24e0987d5e8463838b33d4f2f2cf859da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474752"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo simples roamApplicabilityType

O roamApplicabilityType descreve as condições de roaming às quais um perfil de roaming se aplica.

Esse é um atributo mais expressiva do [**que roamControlType**](simpletype-roamcontroltype.md)e um perfil deve usar **roamControlType** ou **roamApplicabilityType**, mas não ambos. (Se um perfil usar ambos, ambos serão aplicados. O resultado é a interseção dos dois.)

Use esse atributo para diferenciar entre vários perfis com condições de roaming diferentes, para especificar atributos de perfil diferentes para, por exemplo, home versus roaming.

Há três possíveis estados de registro em casa/roam:

-   Página Base: registrada na rede base
-   Parceiro: registrado em uma rede estreitamente afiliado à rede base
-   Não parceiro: registrado em uma rede que não é estreitamente afiliado à rede base

O significado preciso de "parceiro" varia com base na rede, mas representa uma relação mais próxima com taxas mais favoráveis do que um não parceiro. Esse pode ser o caso se um operador baseado regionalmente tiver uma disposição comercial para usar a rede de acesso de rádio de outro operador fora de sua área base. Ele também pode representar a diferença entre roaming em uma região (por exemplo, UE) e fora dela.

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

O **tipo simples roamApplicabilityType** define os valores a seguir.


| Valor | Descrição | 
|-------|-------------|
| NonPartnerOnly | <p>Esse perfil é usado somente ao fazer roaming em uma rede não parceira</p> | 
| PartnerOnly | <p>Esse perfil é usado somente ao fazer roaming em uma rede de parceiros</p> | 
| HomeOnly | <p>Esse perfil é usado somente quando está na rede base</p> | 
| HomeAndPartner | <p>Esse perfil é usado somente quando está em casa ou em uma rede de parceiros</p> | 
| PartnerAndNonpartner | <p>Esse perfil é usado quando não está em casa (roaming em qualquer rede)</p> | 
| AllRoaming | <p>Esse perfil é usado em todas as redes</p> | 


 

 



