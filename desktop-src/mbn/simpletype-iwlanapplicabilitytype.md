---
description: Enumeração que descreve o tipo de conexão de rede onde um perfil é aplicável.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Tipo simples de iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501843"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span data-ttu-id="9d19c-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Tipo simples de iwlanApplicabilityType</span><span class="sxs-lookup"><span data-stu-id="9d19c-103"><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>iwlanApplicabilityType Simple Type</span></span>

<span data-ttu-id="9d19c-104">Enumeração que descreve o tipo de conexão de rede onde um perfil é aplicável.</span><span class="sxs-lookup"><span data-stu-id="9d19c-104">Enumeration that describes the kind of network connection where a profile is applicable.</span></span>

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

## <a name="enumeration-values"></a><span data-ttu-id="9d19c-105">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="9d19c-105">Enumeration values</span></span>

<span data-ttu-id="9d19c-106">O tipo simples **iwlanApplicabilityType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d19c-106">The **iwlanApplicabilityType** simple type defines the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d19c-107">Valor</span><span class="sxs-lookup"><span data-stu-id="9d19c-107">Value</span></span></th>
<th><span data-ttu-id="9d19c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d19c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d19c-109">CellularOnly</span><span class="sxs-lookup"><span data-stu-id="9d19c-109">CellularOnly</span></span></td>
<td><p><span data-ttu-id="9d19c-110">O perfil é válido somente para conexões de rede celular.</span><span class="sxs-lookup"><span data-stu-id="9d19c-110">Profile is valid for cellular network connections only.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d19c-111">CellularAndIwlan</span><span class="sxs-lookup"><span data-stu-id="9d19c-111">CellularAndIwlan</span></span></td>
<td><p><span data-ttu-id="9d19c-112">O perfil é válido para conexões de celular ou Wi-Fi descarregadas.</span><span class="sxs-lookup"><span data-stu-id="9d19c-112">Profile is valid for cellular or Wi-Fi offloaded connections.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d19c-113">IwlanOnly</span><span class="sxs-lookup"><span data-stu-id="9d19c-113">IwlanOnly</span></span></td>
<td><p><span data-ttu-id="9d19c-114">O perfil é válido somente para conexões descarregadas Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="9d19c-114">Profile is valid for Wi-Fi offloaded connections only.</span></span></p></td>
</tr>
</tbody>
</table>

 

 



