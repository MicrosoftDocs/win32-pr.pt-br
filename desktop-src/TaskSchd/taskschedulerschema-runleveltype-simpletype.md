---
title: Tipo simples de runLevelType
description: Define os valores possíveis para o elemento RunLevel (PrincipalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Agendador de Tarefas tipo simples de runLevelType
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754720"
---
# <a name="runleveltype-simple-type"></a><span data-ttu-id="1058d-104">Tipo simples de runLevelType</span><span class="sxs-lookup"><span data-stu-id="1058d-104">runLevelType Simple Type</span></span>

<span data-ttu-id="1058d-105">Define os valores possíveis para o elemento [**runlevel (PrincipalType)**](taskschedulerschema-runlevel-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1058d-105">Defines the possible values for the [**RunLevel (principalType)**](taskschedulerschema-runlevel-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="1058d-106">Valores de enumeração</span><span class="sxs-lookup"><span data-stu-id="1058d-106">Enumeration values</span></span>

<span data-ttu-id="1058d-107">O tipo simples **runLevelType** define os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1058d-107">The **runLevelType** simple type defines the following values.</span></span>



| <span data-ttu-id="1058d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1058d-108">Value</span></span>            | <span data-ttu-id="1058d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1058d-109">Description</span></span>                                               |
|------------------|-----------------------------------------------------------|
| <span data-ttu-id="1058d-110">LeastPrivilege</span><span class="sxs-lookup"><span data-stu-id="1058d-110">LeastPrivilege</span></span>   | <span data-ttu-id="1058d-111">As tarefas são executadas com os privilégios mínimos (LUA).</span><span class="sxs-lookup"><span data-stu-id="1058d-111">Tasks are run with the least privileges (LUA).</span></span><br/> |
| <span data-ttu-id="1058d-112">HighestAvailable</span><span class="sxs-lookup"><span data-stu-id="1058d-112">HighestAvailable</span></span> | <span data-ttu-id="1058d-113">As tarefas são executadas com os privilégios mais altos.</span><span class="sxs-lookup"><span data-stu-id="1058d-113">Tasks are run with the highest privileges.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="1058d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1058d-114">Requirements</span></span>



| <span data-ttu-id="1058d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1058d-115">Requirement</span></span> | <span data-ttu-id="1058d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1058d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1058d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1058d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1058d-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1058d-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1058d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1058d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1058d-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1058d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





