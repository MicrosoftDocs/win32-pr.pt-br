---
description: Habilita uma GPU física para virtualização.
ms.assetid: 700cb46b-97f1-40cf-88d2-64242f4bd2c6
title: Método EnableGPUForVirtualization da classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.EnableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cf21424e9af8398cd435dce409bccde03543a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768511"
---
# <a name="enablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="5659c-103">Método EnableGPUForVirtualization da \_ classe Synthetic3DService Msvm</span><span class="sxs-lookup"><span data-stu-id="5659c-103">EnableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="5659c-104">Habilita uma GPU física para virtualização.</span><span class="sxs-lookup"><span data-stu-id="5659c-104">Enables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="5659c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5659c-105">Syntax</span></span>


```mof
uint32 EnableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5659c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5659c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5659c-107">*PhysicalGPU* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5659c-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5659c-108">Uma referência a uma instância da classe [**Msvm \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) que representa a GPU física a ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="5659c-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="5659c-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5659c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5659c-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5659c-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5659c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5659c-111">Return value</span></span>

<span data-ttu-id="5659c-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5659c-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5659c-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5659c-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5659c-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5659c-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5659c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5659c-115">Requirements</span></span>



| <span data-ttu-id="5659c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5659c-116">Requirement</span></span> | <span data-ttu-id="5659c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5659c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5659c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5659c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5659c-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5659c-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5659c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5659c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5659c-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5659c-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5659c-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="5659c-122">Namespace</span></span><br/>                | <span data-ttu-id="5659c-123">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5659c-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5659c-124">MOF</span><span class="sxs-lookup"><span data-stu-id="5659c-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5659c-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5659c-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5659c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5659c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5659c-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5659c-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5659c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5659c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5659c-129">**Msvm \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="5659c-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

