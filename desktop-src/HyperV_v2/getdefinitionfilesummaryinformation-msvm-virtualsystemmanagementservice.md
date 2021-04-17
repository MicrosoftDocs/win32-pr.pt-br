---
description: Retorna informações de resumo da máquina virtual para os arquivos de definição de máquina virtual especificados.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Método GetDefinitionFileSummaryInformation da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775738"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="eaa85-103">Método GetDefinitionFileSummaryInformation da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="eaa85-103">GetDefinitionFileSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="eaa85-104">Retorna informações de resumo da máquina virtual para os arquivos de definição de máquina virtual especificados.</span><span class="sxs-lookup"><span data-stu-id="eaa85-104">Returns virtual machine summary information for the specified virtual machine definition files.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa85-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaa85-105">Syntax</span></span>


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="eaa85-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaa85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa85-107">*DefinitionFiles* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eaa85-107">*DefinitionFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaa85-108">Uma matriz de caminhos para arquivos de configuração XML para os quais retornar informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="eaa85-108">An array of paths to XML configuration files for which to return summary information.</span></span>

</dd> <dt>

<span data-ttu-id="eaa85-109">*SummaryInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eaa85-109">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaa85-110">Uma matriz de instâncias do [**Msvm \_ SummaryInformationBase**](msvm-summaryinformation.md) que contém as informações solicitadas para as máquinas virtuais e/ou os instantâneos especificados na matriz *DefinitionFiles* .</span><span class="sxs-lookup"><span data-stu-id="eaa85-110">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformation.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *DefinitionFiles* array.</span></span> <span data-ttu-id="eaa85-111">Somente as propriedades **Name**, **ElementName**, **CreationTime** e **Notes** são retornadas, todas as outras propriedades serão **nulas**.</span><span class="sxs-lookup"><span data-stu-id="eaa85-111">Only the **Name**, **ElementName**, **CreationTime**, and **Notes** properties are returned, all other properties will be **Null**.</span></span>

> [!Note]  

 

<span data-ttu-id="eaa85-112">Antes do Windows 10, a versão 1703, DataType era [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="eaa85-112">Prior to Windows 10, version 1703, datatype was [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa85-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eaa85-113">Return value</span></span>

<span data-ttu-id="eaa85-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eaa85-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="eaa85-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="eaa85-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="eaa85-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="eaa85-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="eaa85-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="eaa85-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="eaa85-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="eaa85-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="eaa85-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="eaa85-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="eaa85-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="eaa85-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="eaa85-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="eaa85-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="eaa85-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eaa85-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaa85-128">Requirements</span></span>



| <span data-ttu-id="eaa85-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaa85-129">Requirement</span></span> | <span data-ttu-id="eaa85-130">Valor</span><span class="sxs-lookup"><span data-stu-id="eaa85-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa85-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaa85-131">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa85-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eaa85-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eaa85-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaa85-133">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa85-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eaa85-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eaa85-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="eaa85-135">Namespace</span></span><br/>                | <span data-ttu-id="eaa85-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="eaa85-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eaa85-137">MOF</span><span class="sxs-lookup"><span data-stu-id="eaa85-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaa85-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaa85-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaa85-139">DLL</span><span class="sxs-lookup"><span data-stu-id="eaa85-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaa85-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eaa85-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eaa85-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaa85-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa85-142">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="eaa85-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




