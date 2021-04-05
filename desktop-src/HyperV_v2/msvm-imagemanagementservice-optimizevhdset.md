---
description: Otimiza um arquivo de conjunto VHD para usar menos espaço em disco.
ms.assetid: 2d2f4531-5d2d-4334-bcc2-d3d3c15b1f46
title: Método OptimizeVHDSet da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.OptimizeVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c360dcd8acf0a4721b8921cd2ca914c34002d078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827297"
---
# <a name="optimizevhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="30f43-103">Método OptimizeVHDSet da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="30f43-103">OptimizeVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="30f43-104">Otimiza um arquivo de conjunto VHD para usar menos espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="30f43-104">Optimizes a VHD Set file to use less disk space.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30f43-105">Syntax</span></span>


```mof
uint32 OptimizeVHDSet(
  [in]  string              VHDSetPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="30f43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30f43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f43-107">*VHDSetPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30f43-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30f43-108">Um caminho totalmente qualificado que especifica o local do arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="30f43-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="30f43-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="30f43-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30f43-110">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="30f43-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f43-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30f43-111">Return value</span></span>

<span data-ttu-id="30f43-112">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="30f43-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="30f43-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="30f43-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="30f43-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="30f43-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="30f43-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="30f43-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="30f43-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="30f43-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="30f43-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="30f43-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="30f43-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="30f43-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="30f43-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="30f43-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="30f43-126">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="30f43-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="30f43-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f43-127">Requirements</span></span>



| <span data-ttu-id="30f43-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f43-128">Requirement</span></span> | <span data-ttu-id="30f43-129">Valor</span><span class="sxs-lookup"><span data-stu-id="30f43-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f43-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30f43-130">Minimum supported client</span></span><br/> | <span data-ttu-id="30f43-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="30f43-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="30f43-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30f43-132">Minimum supported server</span></span><br/> | <span data-ttu-id="30f43-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="30f43-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="30f43-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="30f43-134">Namespace</span></span><br/>                | <span data-ttu-id="30f43-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="30f43-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="30f43-136">MOF</span><span class="sxs-lookup"><span data-stu-id="30f43-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30f43-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30f43-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30f43-138">DLL</span><span class="sxs-lookup"><span data-stu-id="30f43-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30f43-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30f43-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30f43-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="30f43-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f43-141">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="30f43-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




