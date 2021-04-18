---
description: Interrompe o serviço.
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Método StartService da classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f76fa9e5069c2a9e19b83a8ab83136879c6657e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778592"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="58c79-103">Método StartService da classe Msvm \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="58c79-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="58c79-104">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="58c79-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c79-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58c79-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="58c79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58c79-106">Parameters</span></span>

<span data-ttu-id="58c79-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="58c79-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58c79-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58c79-108">Return value</span></span>

<span data-ttu-id="58c79-109">Retornará 0 se for bem-sucedido; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="58c79-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="58c79-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="58c79-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58c79-111">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="58c79-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="58c79-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58c79-112">Requirements</span></span>



| <span data-ttu-id="58c79-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="58c79-113">Requirement</span></span> | <span data-ttu-id="58c79-114">Valor</span><span class="sxs-lookup"><span data-stu-id="58c79-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c79-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58c79-115">Minimum supported client</span></span><br/> | <span data-ttu-id="58c79-116">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="58c79-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="58c79-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58c79-117">Minimum supported server</span></span><br/> | <span data-ttu-id="58c79-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="58c79-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="58c79-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="58c79-119">Namespace</span></span><br/>                | <span data-ttu-id="58c79-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="58c79-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="58c79-121">MOF</span><span class="sxs-lookup"><span data-stu-id="58c79-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58c79-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58c79-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58c79-123">DLL</span><span class="sxs-lookup"><span data-stu-id="58c79-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c79-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58c79-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58c79-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="58c79-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c79-126">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="58c79-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




