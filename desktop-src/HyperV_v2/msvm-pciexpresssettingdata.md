---
description: Representa o estado configurado de uma porta PCI Express.
ms.assetid: adb03dd7-5a47-47e6-a4e4-28224164150c
title: Classe Msvm_PciExpressSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpressSettingData
- Msvm_PciExpressSettingData.VirtualFunctions
- Msvm_PciExpressSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c092cbc119506c4c52bc0565cd969426feffc481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789800"
---
# <a name="msvm_pciexpresssettingdata-class"></a><span data-ttu-id="80c0f-103">\_Classe Msvm PciExpressSettingData</span><span class="sxs-lookup"><span data-stu-id="80c0f-103">Msvm\_PciExpressSettingData class</span></span>

<span data-ttu-id="80c0f-104">Representa o estado configurado de uma porta PCI Express.</span><span class="sxs-lookup"><span data-stu-id="80c0f-104">Represents the configured state of a PCI Express port.</span></span>

<span data-ttu-id="80c0f-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="80c0f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c0f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80c0f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpressSettingData : CIM_ResourceAllocationSettingData
{
  uint16 VirtualFunctions[];
  string VirtualSystemIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="80c0f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="80c0f-107">Members</span></span>

<span data-ttu-id="80c0f-108">A classe **Msvm \_ PciExpressSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="80c0f-108">The **Msvm\_PciExpressSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="80c0f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80c0f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80c0f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80c0f-110">Properties</span></span>

<span data-ttu-id="80c0f-111">A classe **Msvm \_ PciExpressSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="80c0f-111">The **Msvm\_PciExpressSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80c0f-112">**VirtualFunctions**</span><span class="sxs-lookup"><span data-stu-id="80c0f-112">**VirtualFunctions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c0f-113">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80c0f-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="80c0f-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80c0f-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80c0f-115">O número da função virtual a ser atribuída à VM.</span><span class="sxs-lookup"><span data-stu-id="80c0f-115">The virtual function number to assign to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="80c0f-116">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="80c0f-116">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c0f-117">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80c0f-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="80c0f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80c0f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80c0f-119">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="80c0f-119">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="80c0f-120">Uma matriz de cadeia de caracteres de forma livre de identificadores desse recurso apresentada ao sistema operacional do sistema de computador virtual.</span><span class="sxs-lookup"><span data-stu-id="80c0f-120">A free-form string array of identifiers of this resource presented to the virtual computer system's operating system.</span></span> <span data-ttu-id="80c0f-121">Os índices e valores por índice são definidos por recurso (ou seja, para cada valor de **ResourceType** enumerado).</span><span class="sxs-lookup"><span data-stu-id="80c0f-121">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="80c0f-122">Essa propriedade é definida como "GUID".</span><span class="sxs-lookup"><span data-stu-id="80c0f-122">This property is set to "GUID".</span></span>

<span data-ttu-id="80c0f-123">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) da classe SD.</span><span class="sxs-lookup"><span data-stu-id="80c0f-123">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the sd class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80c0f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c0f-124">Requirements</span></span>



| <span data-ttu-id="80c0f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c0f-125">Requirement</span></span> | <span data-ttu-id="80c0f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="80c0f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c0f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c0f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80c0f-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="80c0f-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="80c0f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c0f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80c0f-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="80c0f-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="80c0f-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="80c0f-131">Namespace</span></span><br/>                | <span data-ttu-id="80c0f-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="80c0f-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="80c0f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="80c0f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80c0f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80c0f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80c0f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="80c0f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80c0f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80c0f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80c0f-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="80c0f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c0f-138">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="80c0f-138">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

