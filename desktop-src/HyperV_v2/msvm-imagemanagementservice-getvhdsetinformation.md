---
description: Recupera informações sobre um arquivo de conjunto de VHD.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Método GetVHDSetInformation da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770216"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="e6d4b-103">Método GetVHDSetInformation da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="e6d4b-103">GetVHDSetInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="e6d4b-104">Recupera informações sobre um arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-104">Retrieves information about a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6d4b-105">Syntax</span></span>


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e6d4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d4b-107">*VHDSetPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6d4b-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d4b-108">Um caminho totalmente qualificado que especifica o local do arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="e6d4b-109">*AdditionalInformation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6d4b-109">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d4b-110">Uma matriz que especifica quais informações adicionais devem ser coletadas sobre o arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-110">An array specifying what additional information should be gathered about the VHD Set file.</span></span> <span data-ttu-id="e6d4b-111">Cada entrada na matriz é um tipo de informação adicional.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-111">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="e6d4b-112">Se esse parâmetro for nulo, nenhuma informação adicional será recuperada.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-112">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e6d4b-113">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-113">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e6d4b-114">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-114">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

<span data-ttu-id="e6d4b-115">**Caminhos** (2)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-115">**Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e6d4b-116">*Informações* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e6d4b-116">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d4b-117">Se for bem-sucedido, esse objeto conterá as informações para o arquivo de conjunto de VHD solicitado.</span><span class="sxs-lookup"><span data-stu-id="e6d4b-117">If successful, this object contains the information for the requested VHD Set file.</span></span> <span data-ttu-id="e6d4b-118">Esta é uma instância incorporada de [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md).</span><span class="sxs-lookup"><span data-stu-id="e6d4b-118">This is an embedded instance of [**Msvm\_VHDSetInformation**](msvm-vhdsetinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6d4b-119">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e6d4b-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d4b-120">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="e6d4b-120">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d4b-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6d4b-121">Return value</span></span>

<span data-ttu-id="e6d4b-122">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e6d4b-122">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e6d4b-123">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-125">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-126">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-127">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-128">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-129">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-130">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-131">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-132">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-133">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-134">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-135">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-135">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e6d4b-136">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="e6d4b-136">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e6d4b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d4b-137">Requirements</span></span>



| <span data-ttu-id="e6d4b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d4b-138">Requirement</span></span> | <span data-ttu-id="e6d4b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e6d4b-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d4b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6d4b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d4b-141">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e6d4b-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e6d4b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6d4b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d4b-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e6d4b-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e6d4b-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6d4b-144">Namespace</span></span><br/>                | <span data-ttu-id="e6d4b-145">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e6d4b-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e6d4b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="e6d4b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6d4b-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6d4b-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6d4b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d4b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6d4b-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e6d4b-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e6d4b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6d4b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d4b-151">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="e6d4b-151">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




