---
description: Converte um arquivo de disco rígido virtual criando um novo arquivo de conjunto de VHD junto com o disco rígido virtual existente.
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Método ConvertVirtualHardDiskToVHDSet da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6113a14f321ff7319f8be15767621db3a7e833de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922697"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="a6e7a-103">Método ConvertVirtualHardDiskToVHDSet da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="a6e7a-103">ConvertVirtualHardDiskToVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="a6e7a-104">Converte um arquivo de disco rígido virtual criando um novo arquivo de conjunto de VHD junto com o disco rígido virtual existente.</span><span class="sxs-lookup"><span data-stu-id="a6e7a-104">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e7a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6e7a-105">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a6e7a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6e7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e7a-107">*VirtualHardDiskPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6e7a-107">*VirtualHardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6e7a-108">Cadeia de caracteres que contém o caminho para o arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="a6e7a-108">String containing the path to the virtual hard disk file.</span></span> <span data-ttu-id="a6e7a-109">O novo arquivo de conjunto VHD terá o mesmo nome de arquivo, mas com o. Extensão de VHDS.</span><span class="sxs-lookup"><span data-stu-id="a6e7a-109">The new VHD Set file will have the same filename but with the .VHDS extension.</span></span>

</dd> <dt>

<span data-ttu-id="a6e7a-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a6e7a-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6e7a-111">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="a6e7a-111">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e7a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6e7a-112">Return value</span></span>

<span data-ttu-id="a6e7a-113">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a6e7a-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="a6e7a-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a6e7a-127">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="a6e7a-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a6e7a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6e7a-128">Requirements</span></span>



| <span data-ttu-id="a6e7a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6e7a-129">Requirement</span></span> | <span data-ttu-id="a6e7a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a6e7a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e7a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6e7a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a6e7a-132">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a6e7a-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a6e7a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6e7a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a6e7a-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a6e7a-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a6e7a-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6e7a-135">Namespace</span></span><br/>                | <span data-ttu-id="a6e7a-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a6e7a-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a6e7a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a6e7a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6e7a-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6e7a-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6e7a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a6e7a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6e7a-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6e7a-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a6e7a-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6e7a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6e7a-142">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="a6e7a-142">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




