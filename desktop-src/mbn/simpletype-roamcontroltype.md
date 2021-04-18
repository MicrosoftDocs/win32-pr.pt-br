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
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span data-ttu-id="d9580-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Tipo simples de roamControlType</span><span class="sxs-lookup"><span data-stu-id="d9580-103"><span id="WWAN_profile_v4.simpleType_roamControlType"></span>roamControlType Simple Type</span></span>

<span data-ttu-id="d9580-104">Descreve como o perfil controla o roaming.</span><span class="sxs-lookup"><span data-stu-id="d9580-104">Describes how the profile controls roaming.</span></span>

<span data-ttu-id="d9580-105">Há dois Estados de registro de roaming possíveis:</span><span class="sxs-lookup"><span data-stu-id="d9580-105">There are two possible roam registration states:</span></span>

-   <span data-ttu-id="d9580-106">Parceiro: registrado em uma rede afiliada de forma bem associada à rede doméstica</span><span class="sxs-lookup"><span data-stu-id="d9580-106">Partner: registered on a network closely affiliated with the home network</span></span>
-   <span data-ttu-id="d9580-107">Não parceiro: registrado em uma rede que não está fortemente afiliada com a rede doméstica</span><span class="sxs-lookup"><span data-stu-id="d9580-107">Non-partner: registered on a network that is not closely affiliated with the home network</span></span>

<span data-ttu-id="d9580-108">O significado preciso de "parceiro" varia de acordo com a rede, mas representa uma relação mais próxima com taxas mais favoráveis do que um não parceiro.</span><span class="sxs-lookup"><span data-stu-id="d9580-108">The precise meaning of "partner" varies based upon the network, but it represents a closer relationship with more favorable rates than a non-partner.</span></span> <span data-ttu-id="d9580-109">Esse pode ser o caso se um operador com base em regiões tiver uma organização de negócios para usar a rede de acesso de rádio de outra operadora fora de sua área inicial.</span><span class="sxs-lookup"><span data-stu-id="d9580-109">This could be the case if a regionally-based operator has a business arrangement to use another operator’s radio access network outside of its home area.</span></span> <span data-ttu-id="d9580-110">Ele também pode representar a diferença entre o roaming em uma região (por exemplo, a UE) e fora dele.</span><span class="sxs-lookup"><span data-stu-id="d9580-110">It could also represent the difference between roaming within a region (e.g., EU) and outside of it.</span></span>

<span data-ttu-id="d9580-111">Observe que [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) é um atributo mais expressivo do que **roamControlType**, e um perfil deve usar **roamControlType** ou **roamApplicabilityType**, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="d9580-111">Note that [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) is a more expressive attribute than **roamControlType**, and a profile should use either **roamControlType** or **roamApplicabilityType**, but not both.</span></span> <span data-ttu-id="d9580-112">(Se um perfil usar ambos, ambos serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="d9580-112">(If a profile uses both, then both are applied.</span></span> <span data-ttu-id="d9580-113">O resultado é a interseção dos dois.)</span><span class="sxs-lookup"><span data-stu-id="d9580-113">The result is the intersection of the two.)</span></span>

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

## <a name="enumeration-values"></a><span data-ttu-id="d9580-114">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="d9580-114">Enumeration values</span></span>

<span data-ttu-id="d9580-115">O tipo simples **roamControlType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9580-115">The **roamControlType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9580-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d9580-116">Value</span></span></th>
<th><span data-ttu-id="d9580-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9580-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9580-118">AllRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="d9580-118">AllRoamAllowed</span></span></td>
<td><p><span data-ttu-id="d9580-119">O roaming é permitido em redes de parceiros e não parceiros.</span><span class="sxs-lookup"><span data-stu-id="d9580-119">Roaming is allowed on Partner and Non-Partner networks.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9580-120">PartnerRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="d9580-120">PartnerRoamAllowed</span></span></td>
<td><p><span data-ttu-id="d9580-121">O roaming só é permitido em redes de parceiros.</span><span class="sxs-lookup"><span data-stu-id="d9580-121">Roaming is allowed only on Partner networks.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9580-122">NoRoamAllowed</span><span class="sxs-lookup"><span data-stu-id="d9580-122">NoRoamAllowed</span></span></td>
<td><p><span data-ttu-id="d9580-123">Nenhum roaming é permitido.</span><span class="sxs-lookup"><span data-stu-id="d9580-123">No roaming is allowed.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



