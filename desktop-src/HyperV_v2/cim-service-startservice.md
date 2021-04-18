---
description: Coloca o serviço no estado iniciado.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Método StartService da classe CIM_Service (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b89f7fc789639fb45acbde61da4c7962650177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757820"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="7079c-103">Método StartService da classe CIM_Service (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="7079c-103">StartService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="7079c-104">Coloca o serviço no estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="7079c-104">Places the service in the started state.</span></span>

> [!Note]
>
> <span data-ttu-id="7079c-105">A semântica desse método se sobrepõe ao método **RequestStateChange** herdado do [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="7079c-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="7079c-106">Esse método é mantido porque foi amplamente implementado, e sua semântica simples de "início" é conveniente de usar.</span><span class="sxs-lookup"><span data-stu-id="7079c-106">This method is maintained because it has been widely implemented, and its simple "start" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7079c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7079c-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="7079c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7079c-108">Parameters</span></span>

<span data-ttu-id="7079c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7079c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7079c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7079c-110">Return value</span></span>

<span data-ttu-id="7079c-111">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7079c-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7079c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7079c-112">Requirements</span></span>



| <span data-ttu-id="7079c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7079c-113">Requirement</span></span> | <span data-ttu-id="7079c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7079c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7079c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7079c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7079c-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7079c-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7079c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7079c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7079c-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7079c-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7079c-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="7079c-119">Namespace</span></span><br/>                | <span data-ttu-id="7079c-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7079c-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7079c-121">MOF</span><span class="sxs-lookup"><span data-stu-id="7079c-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7079c-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7079c-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7079c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7079c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7079c-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7079c-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7079c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7079c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7079c-126">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="7079c-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




