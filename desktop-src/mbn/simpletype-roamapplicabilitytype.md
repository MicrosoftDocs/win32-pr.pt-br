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
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span data-ttu-id="0c54f-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Tipo simples de roamApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="0c54f-103"><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>roamApplicabilityType Simple Type</span></span>

<span data-ttu-id="0c54f-104">O roamApplicabilityType descreve as condições de roaming para as quais um perfil móvel se aplica.</span><span class="sxs-lookup"><span data-stu-id="0c54f-104">The roamApplicabilityType describes the roaming conditions for which a roaming profile applies.</span></span>

<span data-ttu-id="0c54f-105">Esse é um atributo mais expressivo do que [**roamControlType**](simpletype-roamcontroltype.md), e um perfil deve usar **roamControlType** ou **roamApplicabilityType**, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="0c54f-105">This is a more expressive attribute than [**roamControlType**](simpletype-roamcontroltype.md), and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="0c54f-106">(Se um perfil usar ambos, ambos serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="0c54f-106">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="0c54f-107">O resultado é a interseção dos dois.)</span><span class="sxs-lookup"><span data-stu-id="0c54f-107">The result is the intersection of the two.)</span></span>

<span data-ttu-id="0c54f-108">Use esse atributo para diferenciar entre vários perfis com condições de roaming não associadas, para especificar diferentes atributos de perfil para, por exemplo, Home versus roaming.</span><span class="sxs-lookup"><span data-stu-id="0c54f-108">Use this attribute to differentiate between multiple profiles with disjoint roaming conditions, to specify different profile attributes for, for example, home versus roaming.</span></span>

<span data-ttu-id="0c54f-109">Há três Estados de registro iniciais/móveis possíveis:</span><span class="sxs-lookup"><span data-stu-id="0c54f-109">There are three possible home/roam registration states:</span></span>

-   <span data-ttu-id="0c54f-110">Página inicial: registrado na rede doméstica</span><span class="sxs-lookup"><span data-stu-id="0c54f-110">Home: registered on the home network</span></span>
-   <span data-ttu-id="0c54f-111">Parceiro: registrado em uma rede afiliada de forma bem associada à rede doméstica</span><span class="sxs-lookup"><span data-stu-id="0c54f-111">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="0c54f-112">Não parceiro: registrado em uma rede que não está fortemente afiliada com a rede doméstica</span><span class="sxs-lookup"><span data-stu-id="0c54f-112">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="0c54f-113">O significado preciso de "parceiro" varia de acordo com a rede, mas representa uma relação mais próxima com taxas mais favoráveis do que um não parceiro.</span><span class="sxs-lookup"><span data-stu-id="0c54f-113">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="0c54f-114">Esse pode ser o caso se um operador com base em regiões tiver uma organização de negócios para usar a rede de acesso de rádio de outra operadora fora de sua área inicial.</span><span class="sxs-lookup"><span data-stu-id="0c54f-114">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="0c54f-115">Ele também pode representar a diferença entre o roaming em uma região (por exemplo, a UE) e fora dele.</span><span class="sxs-lookup"><span data-stu-id="0c54f-115">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

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

## <a name="enumeration-values"></a><span data-ttu-id="0c54f-116">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="0c54f-116">Enumeration values</span></span>

<span data-ttu-id="0c54f-117">O tipo simples **roamApplicabilityType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c54f-117">The **roamApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c54f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0c54f-118">Value</span></span></th>
<th><span data-ttu-id="0c54f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c54f-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c54f-120">NonPartnerOnly</span><span class="sxs-lookup"><span data-stu-id="0c54f-120">NonPartnerOnly</span></span></td>
<td><p><span data-ttu-id="0c54f-121">Este perfil é usado somente quando estiver em roaming em uma rede que não seja de parceiro</span><span class="sxs-lookup"><span data-stu-id="0c54f-121">This profile is used only when roaming on a non-partner network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c54f-122">PartnerOnly</span><span class="sxs-lookup"><span data-stu-id="0c54f-122">PartnerOnly</span></span></td>
<td><p><span data-ttu-id="0c54f-123">Este perfil é usado somente quando estiver em roaming em uma rede de parceiros</span><span class="sxs-lookup"><span data-stu-id="0c54f-123">This profile is used only when roaming on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c54f-124">HomeOnly</span><span class="sxs-lookup"><span data-stu-id="0c54f-124">HomeOnly</span></span></td>
<td><p><span data-ttu-id="0c54f-125">Este perfil é usado somente quando estiver na rede doméstica</span><span class="sxs-lookup"><span data-stu-id="0c54f-125">This profile is used only when on the home network</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c54f-126">HomeAndPartner</span><span class="sxs-lookup"><span data-stu-id="0c54f-126">HomeAndPartner</span></span></td>
<td><p><span data-ttu-id="0c54f-127">Este perfil é usado somente quando em casa ou em uma rede de parceiros</span><span class="sxs-lookup"><span data-stu-id="0c54f-127">This profile is used only when at home or on a partner network</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c54f-128">PartnerAndNonpartner</span><span class="sxs-lookup"><span data-stu-id="0c54f-128">PartnerAndNonpartner</span></span></td>
<td><p><span data-ttu-id="0c54f-129">Este perfil é usado quando não está em casa (roaming em qualquer rede)</span><span class="sxs-lookup"><span data-stu-id="0c54f-129">This profile is used when not at home (roaming on any network)</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c54f-130">Em roaming</span><span class="sxs-lookup"><span data-stu-id="0c54f-130">AllRoaming</span></span></td>
<td><p><span data-ttu-id="0c54f-131">Este perfil é usado em todas as redes</span><span class="sxs-lookup"><span data-stu-id="0c54f-131">This profile is used on all networks</span></span></p></td>
</tr>
</tbody>
</table>

 

 



