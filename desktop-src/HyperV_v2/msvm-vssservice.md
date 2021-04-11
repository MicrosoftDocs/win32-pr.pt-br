---
description: Representa o serviço VSS convidado. Ele é usado para consultar informações de cluster de convidado do host Hyper-V.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296203"
---
# <a name="msvm_vssservice-class"></a><span data-ttu-id="27fdf-104">\_Classe Msvm VssService</span><span class="sxs-lookup"><span data-stu-id="27fdf-104">Msvm\_VssService class</span></span>

<span data-ttu-id="27fdf-105">Representa o serviço VSS convidado.</span><span class="sxs-lookup"><span data-stu-id="27fdf-105">Represents the guest VSS service.</span></span> <span data-ttu-id="27fdf-106">Ele é usado para consultar informações de cluster de convidado do host Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="27fdf-106">It is used for querying guest cluster information from the Hyper-V host.</span></span>

<span data-ttu-id="27fdf-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="27fdf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27fdf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27fdf-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a><span data-ttu-id="27fdf-109">Membros</span><span class="sxs-lookup"><span data-stu-id="27fdf-109">Members</span></span>

<span data-ttu-id="27fdf-110">A classe **Msvm \_ VssService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="27fdf-110">The **Msvm\_VssService** class has these types of members:</span></span>

-   [<span data-ttu-id="27fdf-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="27fdf-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="27fdf-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="27fdf-112">Methods</span></span>

<span data-ttu-id="27fdf-113">A classe **Msvm \_ VssService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="27fdf-113">The **Msvm\_VssService** class has these methods.</span></span>



| <span data-ttu-id="27fdf-114">Método</span><span class="sxs-lookup"><span data-stu-id="27fdf-114">Method</span></span>                                                                               | <span data-ttu-id="27fdf-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="27fdf-115">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="27fdf-116">**QueryGuestClusterInformation**</span><span class="sxs-lookup"><span data-stu-id="27fdf-116">**QueryGuestClusterInformation**</span></span>](msvm-vssservice-queryguestclusterinformation.md) | <span data-ttu-id="27fdf-117">Consultando informações de cluster do host Hyper-V para o convidado.</span><span class="sxs-lookup"><span data-stu-id="27fdf-117">Querying cluster information from the Hyper-V host to the guest.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="27fdf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27fdf-118">Requirements</span></span>



| <span data-ttu-id="27fdf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="27fdf-119">Requirement</span></span> | <span data-ttu-id="27fdf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="27fdf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27fdf-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27fdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27fdf-122">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="27fdf-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="27fdf-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27fdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27fdf-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="27fdf-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="27fdf-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="27fdf-125">Namespace</span></span><br/>                | <span data-ttu-id="27fdf-126">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="27fdf-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="27fdf-127">MOF</span><span class="sxs-lookup"><span data-stu-id="27fdf-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27fdf-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27fdf-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="27fdf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="27fdf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27fdf-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27fdf-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="27fdf-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="27fdf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27fdf-132">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="27fdf-132">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




