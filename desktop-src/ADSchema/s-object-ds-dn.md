---
title: Sintaxe de objeto (DS-DN)
description: Cadeia de caracteres que contém um DN (nome distinto).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de objeto (DS-DN) do AD
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499874"
---
# <a name="objectds-dn-syntax"></a><span data-ttu-id="3ccb7-104">Sintaxe de objeto (DS-DN)</span><span class="sxs-lookup"><span data-stu-id="3ccb7-104">Object(DS-DN) syntax</span></span>

<span data-ttu-id="3ccb7-105">Cadeia de caracteres que contém um DN (nome distinto).</span><span class="sxs-lookup"><span data-stu-id="3ccb7-105">String that contains a distinguished name (DN).</span></span> <span data-ttu-id="3ccb7-106">Para atributos com essa sintaxe, Active Directory manipula valores de atributo como referências ao objeto identificado pelo DN e atualiza automaticamente o valor se o objeto for movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="3ccb7-106">For attributes with this syntax, Active Directory handles attribute values as references to the object identified by the DN and automatically updates the value if the object is moved or renamed.</span></span> <span data-ttu-id="3ccb7-107">Para consultas que incluem atributos de sintaxe de DN em um filtro, especifique nomes distintos completos.</span><span class="sxs-lookup"><span data-stu-id="3ccb7-107">For queries that include attributes of DN syntax in a filter, specify full distinguished names.</span></span> <span data-ttu-id="3ccb7-108">Não há suporte para caracteres curinga (por exemplo, CN = João \* ).</span><span class="sxs-lookup"><span data-stu-id="3ccb7-108">Wildcards (for example, cn=John\*) are not supported.</span></span>



| <span data-ttu-id="3ccb7-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3ccb7-109">Entry</span></span> | <span data-ttu-id="3ccb7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3ccb7-110">Value</span></span> |
|--------------|------------------------------------------------------------------------|
| <span data-ttu-id="3ccb7-111">Nome</span><span class="sxs-lookup"><span data-stu-id="3ccb7-111">Name</span></span>         | <span data-ttu-id="3ccb7-112">Objeto (DS-DN)</span><span class="sxs-lookup"><span data-stu-id="3ccb7-112">Object(DS-DN)</span></span>                                                          |
| <span data-ttu-id="3ccb7-113">ID da sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ccb7-113">Syntax ID</span></span>    | <span data-ttu-id="3ccb7-114">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="3ccb7-114">2.5.5.1</span></span>                                                                |
| <span data-ttu-id="3ccb7-115">ID DO OM</span><span class="sxs-lookup"><span data-stu-id="3ccb7-115">OM ID</span></span>        | <span data-ttu-id="3ccb7-116">127</span><span class="sxs-lookup"><span data-stu-id="3ccb7-116">127</span></span>                                                                    |
| <span data-ttu-id="3ccb7-117">Tipo de MAPI</span><span class="sxs-lookup"><span data-stu-id="3ccb7-117">MAPI Type</span></span>    | <span data-ttu-id="3ccb7-118">OBJECT</span><span class="sxs-lookup"><span data-stu-id="3ccb7-118">OBJECT</span></span>                                                                 |
| <span data-ttu-id="3ccb7-119">Tipo de ADS</span><span class="sxs-lookup"><span data-stu-id="3ccb7-119">ADS Type</span></span>     | <span data-ttu-id="3ccb7-120">\_cadeia de \_ caracteres DN ADSTYPE</span><span class="sxs-lookup"><span data-stu-id="3ccb7-120">ADSTYPE\_DN\_STRING</span></span>                                                    |
| <span data-ttu-id="3ccb7-121">Tipo de variante</span><span class="sxs-lookup"><span data-stu-id="3ccb7-121">Variant Type</span></span> | <span data-ttu-id="3ccb7-122">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="3ccb7-122">VT\_BSTR</span></span>                                                               |
| <span data-ttu-id="3ccb7-123">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="3ccb7-123">SDS Type</span></span>     | [<span data-ttu-id="3ccb7-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3ccb7-124">System.String</span></span>](/dotnet/api/system.string) |



## <a name="see-also"></a><span data-ttu-id="3ccb7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ccb7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ccb7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3ccb7-126">System.String</span></span>](/dotnet/api/system.string)
</dt> </dl>

 

 
