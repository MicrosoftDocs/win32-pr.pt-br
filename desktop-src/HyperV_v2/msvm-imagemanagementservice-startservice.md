---
description: Inicia o serviço.
ms.assetid: d1e11947-4f48-404f-a359-627a3b7716fd
title: Método StartService da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd13a4eb39477d9d22fc687b095a8f6fbbc68c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775729"
---
# <a name="startservice-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="dab2a-103">Método StartService da classe Msvm \_ imagens</span><span class="sxs-lookup"><span data-stu-id="dab2a-103">StartService method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="dab2a-104">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="dab2a-104">Starts the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dab2a-105">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="dab2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dab2a-106">Parameters</span></span>

<span data-ttu-id="dab2a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dab2a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dab2a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dab2a-108">Return value</span></span>

<span data-ttu-id="dab2a-109">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="dab2a-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="dab2a-110">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="dab2a-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dab2a-111">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="dab2a-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dab2a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dab2a-112">Requirements</span></span>



| <span data-ttu-id="dab2a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dab2a-113">Requirement</span></span> | <span data-ttu-id="dab2a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="dab2a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab2a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dab2a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dab2a-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dab2a-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="dab2a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dab2a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dab2a-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dab2a-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="dab2a-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="dab2a-119">Namespace</span></span><br/>                | <span data-ttu-id="dab2a-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dab2a-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dab2a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="dab2a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dab2a-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dab2a-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dab2a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dab2a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dab2a-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dab2a-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dab2a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dab2a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab2a-126">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="dab2a-126">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




