---
description: O ritmo do serviço no estado parado.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Método StopService da classe CIM_Service (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827261"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="ea60d-103">Método StopService da classe CIM_Service (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ea60d-103">StopService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="ea60d-104">O ritmo do serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="ea60d-104">Paces the service in the stopped state.</span></span>

> [!Note]
>
> <span data-ttu-id="ea60d-105">A semântica desse método se sobrepõe ao método **RequestStateChange** herdado do [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ea60d-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="ea60d-106">Esse método é mantido porque foi amplamente implementado, e sua semântica simples de "parada" é conveniente de usar.</span><span class="sxs-lookup"><span data-stu-id="ea60d-106">This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ea60d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea60d-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="ea60d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea60d-108">Parameters</span></span>

<span data-ttu-id="ea60d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ea60d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea60d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea60d-110">Return value</span></span>

<span data-ttu-id="ea60d-111">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="ea60d-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea60d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea60d-112">Requirements</span></span>



| <span data-ttu-id="ea60d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea60d-113">Requirement</span></span> | <span data-ttu-id="ea60d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ea60d-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea60d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea60d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ea60d-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ea60d-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ea60d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea60d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ea60d-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ea60d-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ea60d-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea60d-119">Namespace</span></span><br/>                | <span data-ttu-id="ea60d-120">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ea60d-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ea60d-121">MOF</span><span class="sxs-lookup"><span data-stu-id="ea60d-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea60d-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea60d-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea60d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ea60d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea60d-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea60d-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea60d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea60d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea60d-126">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="ea60d-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




