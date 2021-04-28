---
description: Método StartService da classe Msvm_CollectionManagementService – interrompe o serviço.
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
ms.openlocfilehash: 18f58ae22cee06c439b6238df4c2a147405f7aca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112134"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="4b887-103">Método StartService da classe Msvm \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="4b887-103">StartService method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="4b887-104">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="4b887-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b887-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b887-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="4b887-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b887-106">Parameters</span></span>

<span data-ttu-id="4b887-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b887-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b887-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4b887-108">Return value</span></span>

<span data-ttu-id="4b887-109">Retornará 0 se for bem-sucedido; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4b887-109">Returns 0 if successful; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b887-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="4b887-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4b887-111">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="4b887-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4b887-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b887-112">Requirements</span></span>



| <span data-ttu-id="4b887-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b887-113">Requirement</span></span> | <span data-ttu-id="4b887-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4b887-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b887-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b887-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4b887-116">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4b887-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4b887-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b887-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4b887-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4b887-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4b887-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b887-119">Namespace</span></span><br/>                | <span data-ttu-id="4b887-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4b887-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b887-121">MOF</span><span class="sxs-lookup"><span data-stu-id="4b887-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b887-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b887-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b887-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4b887-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b887-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b887-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b887-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4b887-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b887-126">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="4b887-126">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




