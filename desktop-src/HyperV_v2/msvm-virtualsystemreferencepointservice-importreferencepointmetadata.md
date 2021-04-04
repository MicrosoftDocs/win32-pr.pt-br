---
description: Importa os metadados do ponto de referência do sistema virtual.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Método ImportReferencePointMetadata da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930194"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="5e6a6-103">Método ImportReferencePointMetadata da \_ classe VirtualSystemReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="5e6a6-103">ImportReferencePointMetadata method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="5e6a6-104">Importa os metadados do ponto de referência do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5e6a6-104">Imports reference point metadata of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e6a6-105">Syntax</span></span>


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5e6a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e6a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e6a6-107">*AffectedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e6a6-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6a6-108">Uma referência a um [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que descreve o sistema afetado.</span><span class="sxs-lookup"><span data-stu-id="5e6a6-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) describing the affected system.</span></span>

</dd> <dt>

<span data-ttu-id="5e6a6-109">*ConfigFilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e6a6-109">*ConfigFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6a6-110">O caminho totalmente qualificado do arquivo de configuração de onde os metadados do ponto de referência serão importados.</span><span class="sxs-lookup"><span data-stu-id="5e6a6-110">The fully-qualified path of the config file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="5e6a6-111">*RuntimeStateFilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e6a6-111">*RuntimeStateFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6a6-112">O caminho totalmente qualificado do arquivo de estado de tempo de execução de onde os metadados do ponto de referência serão importados.</span><span class="sxs-lookup"><span data-stu-id="5e6a6-112">The fully-qualified path of the runtime state file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="5e6a6-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5e6a6-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e6a6-114">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="5e6a6-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="5e6a6-115">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="5e6a6-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e6a6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e6a6-116">Return value</span></span>

<span data-ttu-id="5e6a6-117">Retorna 0 (sem erro) ou uma das seguintes mensagens de erro:</span><span class="sxs-lookup"><span data-stu-id="5e6a6-117">Returns either 0 (no error) or one of the following error messages:</span></span>

<dl> <dt>

<span data-ttu-id="5e6a6-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5e6a6-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5e6a6-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5e6a6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e6a6-131">Requirements</span></span>



| <span data-ttu-id="5e6a6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e6a6-132">Requirement</span></span> | <span data-ttu-id="5e6a6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5e6a6-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6a6-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e6a6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e6a6-135">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="5e6a6-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5e6a6-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e6a6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e6a6-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5e6a6-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5e6a6-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e6a6-138">Namespace</span></span><br/>                | <span data-ttu-id="5e6a6-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5e6a6-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5e6a6-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5e6a6-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e6a6-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e6a6-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e6a6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5e6a6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e6a6-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e6a6-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e6a6-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e6a6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6a6-145">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="5e6a6-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




