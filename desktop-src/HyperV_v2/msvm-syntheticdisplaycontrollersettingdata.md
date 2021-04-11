---
description: Descreve os dados de configuração para um controlador de vídeo sintético virtual.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Classe Msvm_SyntheticDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165249"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a><span data-ttu-id="5f415-103">\_Classe Msvm SyntheticDisplayControllerSettingData</span><span class="sxs-lookup"><span data-stu-id="5f415-103">Msvm\_SyntheticDisplayControllerSettingData class</span></span>

<span data-ttu-id="5f415-104">Descreve os dados de configuração para um controlador de vídeo sintético virtual.</span><span class="sxs-lookup"><span data-stu-id="5f415-104">Describes the setting data for a virtual synthetic display controller.</span></span>

<span data-ttu-id="5f415-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5f415-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f415-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f415-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="5f415-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5f415-107">Members</span></span>

<span data-ttu-id="5f415-108">A classe **Msvm \_ SyntheticDisplayControllerSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f415-108">The **Msvm\_SyntheticDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5f415-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f415-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f415-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f415-110">Properties</span></span>

<span data-ttu-id="5f415-111">A classe **Msvm \_ SyntheticDisplayControllerSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f415-111">The **Msvm\_SyntheticDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f415-112">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="5f415-112">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f415-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f415-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f415-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5f415-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f415-115">A resolução horizontal.</span><span class="sxs-lookup"><span data-stu-id="5f415-115">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="5f415-116">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="5f415-116">**ResolutionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f415-117">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="5f415-117">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5f415-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f415-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f415-119">O tipo de resolução.</span><span class="sxs-lookup"><span data-stu-id="5f415-119">The resolution type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f415-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5f415-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f415-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5f415-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="5f415-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (2)</span><span class="sxs-lookup"><span data-stu-id="5f415-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span data-ttu-id="5f415-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Único** (3)</span><span class="sxs-lookup"><span data-stu-id="5f415-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="5f415-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Padrão** (4)</span><span class="sxs-lookup"><span data-stu-id="5f415-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="5f415-125">Adicionado no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="5f415-125">Added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f415-126">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="5f415-126">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f415-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f415-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f415-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5f415-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5f415-129">A resolução vertical.</span><span class="sxs-lookup"><span data-stu-id="5f415-129">The vertical resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f415-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f415-130">Requirements</span></span>



| <span data-ttu-id="5f415-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f415-131">Requirement</span></span> | <span data-ttu-id="5f415-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5f415-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f415-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f415-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5f415-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5f415-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5f415-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f415-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5f415-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5f415-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5f415-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f415-137">Namespace</span></span><br/>                | <span data-ttu-id="5f415-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5f415-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5f415-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5f415-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f415-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f415-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f415-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5f415-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f415-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f415-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5f415-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f415-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f415-144">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="5f415-144">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




