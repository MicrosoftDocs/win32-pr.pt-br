---
description: Exporta o ponto de referência do sistema virtual.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Método ExportReferencePoint da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105750838"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="3cfb6-103">Método ExportReferencePoint da \_ classe VirtualSystemReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="3cfb6-103">ExportReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="3cfb6-104">Exporta o ponto de referência do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-104">Exports the reference point of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cfb6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cfb6-105">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3cfb6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cfb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cfb6-107">*ReferencePoint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cfb6-107">*ReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfb6-108">Uma referência à instância [**de \_ VirtualSystemReferencePoint Msvm**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência a ser exportado.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="3cfb6-109">*ExportDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cfb6-109">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfb6-110">O caminho totalmente qualificado do diretório no qual o ponto de referência deve ser exportado.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-110">The fully-qualified path of the directory to which the reference point is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="3cfb6-111">*ExportSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cfb6-111">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfb6-112">Uma instância de [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) que representa as configurações da operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-112">An instance of [**Msvm\_VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="3cfb6-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3cfb6-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cfb6-114">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="3cfb6-115">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cfb6-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cfb6-116">Return value</span></span>

<span data-ttu-id="3cfb6-117">Em caso de sucesso, retorna um 0 (completo sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="3cfb6-117">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="3cfb6-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3cfb6-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3cfb6-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3cfb6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cfb6-131">Requirements</span></span>



| <span data-ttu-id="3cfb6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cfb6-132">Requirement</span></span> | <span data-ttu-id="3cfb6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3cfb6-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cfb6-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cfb6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3cfb6-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3cfb6-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3cfb6-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cfb6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3cfb6-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3cfb6-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3cfb6-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cfb6-138">Namespace</span></span><br/>                | <span data-ttu-id="3cfb6-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3cfb6-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3cfb6-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3cfb6-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cfb6-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cfb6-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cfb6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3cfb6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cfb6-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cfb6-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3cfb6-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cfb6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cfb6-145">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="3cfb6-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




