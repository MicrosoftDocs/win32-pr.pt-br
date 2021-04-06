---
description: Exporta uma máquina virtual, ou um instantâneo de uma máquina virtual, para um arquivo.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Método ExportSystemDefinition da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646684"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a5c57-103">Método ExportSystemDefinition da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="a5c57-103">ExportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a5c57-104">Exporta uma máquina virtual, ou um instantâneo de uma máquina virtual, para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5c57-104">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span> <span data-ttu-id="a5c57-105">A máquina virtual deve estar no estado "desligado" ou "salvo" para ser exportada.</span><span class="sxs-lookup"><span data-stu-id="a5c57-105">The virtual machine must be in the "powered off" or "saved" state to be exported.</span></span> <span data-ttu-id="a5c57-106">A máquina virtual, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.</span><span class="sxs-lookup"><span data-stu-id="a5c57-106">The virtual machine, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c57-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5c57-107">Syntax</span></span>


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a5c57-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5c57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c57-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5c57-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c57-110">Uma referência a um [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual a ser exportada.</span><span class="sxs-lookup"><span data-stu-id="a5c57-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="a5c57-111">*ExportDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5c57-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c57-112">O caminho totalmente qualificado do diretório no qual a máquina virtual deve ser exportada.</span><span class="sxs-lookup"><span data-stu-id="a5c57-112">The fully qualified path of the directory to which the virtual machine is to be exported.</span></span> <span data-ttu-id="a5c57-113">Se a propriedade **CreateVmExportSubdirectory** da classe [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) no parâmetro *ExportSettingData* for definida como **true**, esse diretório poderá ser reutilizado para exportar várias máquinas virtuais e esse método colocará cada definição de máquina virtual em um subdiretório separado sob esse caminho.</span><span class="sxs-lookup"><span data-stu-id="a5c57-113">If the **CreateVmExportSubdirectory** property of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class in the *ExportSettingData* parameter is set to **True**, then this directory can be reused for exporting multiple virtual machines and this method places each virtual machine definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="a5c57-114">*ExportSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5c57-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c57-115">Uma instância inserida da classe [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) que representa as configurações da operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="a5c57-115">An embedded instance of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="a5c57-116">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a5c57-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c57-117">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a5c57-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c57-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5c57-118">Return value</span></span>

<span data-ttu-id="a5c57-119">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5c57-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a5c57-120">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a5c57-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a5c57-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-122">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="a5c57-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-123">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a5c57-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-124">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="a5c57-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-125">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a5c57-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-126">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="a5c57-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-127">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a5c57-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-128">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a5c57-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-129">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="a5c57-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-130">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a5c57-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-131">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="a5c57-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a5c57-132">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a5c57-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a5c57-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5c57-133">Requirements</span></span>



| <span data-ttu-id="a5c57-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c57-134">Requirement</span></span> | <span data-ttu-id="a5c57-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a5c57-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c57-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5c57-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c57-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a5c57-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a5c57-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5c57-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c57-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a5c57-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5c57-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5c57-140">Namespace</span></span><br/>                | <span data-ttu-id="a5c57-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a5c57-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a5c57-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a5c57-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5c57-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5c57-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5c57-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a5c57-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5c57-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5c57-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5c57-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5c57-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c57-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a5c57-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

