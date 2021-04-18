---
description: Representa o estado da porta PCI Express.
ms.assetid: 15d670ee-940a-4737-b2cd-e89dd8a63a5c
title: Classe Msvm_PciExpress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PciExpress
- Msvm_PciExpress.DeviceInstancePath
- Msvm_PciExpress.LocationPath
- Msvm_PciExpress.FunctionNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7534d09c9c0f3825ca462c342747caa17c8de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778586"
---
# <a name="msvm_pciexpress-class"></a><span data-ttu-id="88553-103">\_Classe Msvm PciExpress</span><span class="sxs-lookup"><span data-stu-id="88553-103">Msvm\_PciExpress class</span></span>

<span data-ttu-id="88553-104">Representa o estado da porta PCI Express.</span><span class="sxs-lookup"><span data-stu-id="88553-104">Represents the state of the PCI Express port.</span></span>

<span data-ttu-id="88553-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="88553-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="88553-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88553-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PciExpress : CIM_LogicalDevice
{
  string DeviceInstancePath;
  string LocationPath;
  uint16 FunctionNumber;
};
```

## <a name="members"></a><span data-ttu-id="88553-107">Membros</span><span class="sxs-lookup"><span data-stu-id="88553-107">Members</span></span>

<span data-ttu-id="88553-108">A classe **Msvm \_ PciExpress** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="88553-108">The **Msvm\_PciExpress** class has these types of members:</span></span>

-   [<span data-ttu-id="88553-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88553-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88553-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88553-110">Properties</span></span>

<span data-ttu-id="88553-111">A classe **Msvm \_ PciExpress** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="88553-111">The **Msvm\_PciExpress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88553-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="88553-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88553-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88553-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88553-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88553-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88553-115">Uma cadeia de caracteres que contém o caminho da instância do dispositivo que identifica o dispositivo PCI Express virtual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88553-115">A string containing the device instance path that identifies the device virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="88553-116">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="88553-116">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88553-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="88553-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88553-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88553-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88553-119">O número da função do dispositivo PCI Express virtual.</span><span class="sxs-lookup"><span data-stu-id="88553-119">The function number of the virtual PCI Express device.</span></span>

</dd> <dt>

<span data-ttu-id="88553-120">**LocationPath**</span><span class="sxs-lookup"><span data-stu-id="88553-120">**LocationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88553-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="88553-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88553-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88553-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88553-123">Uma cadeia de caracteres que contém o caminho do local do dispositivo que identifica o dispositivo virtual PCI Express do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88553-123">A string containing the device location path that identifies the device virtual PCI Express device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88553-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88553-124">Requirements</span></span>



| <span data-ttu-id="88553-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="88553-125">Requirement</span></span> | <span data-ttu-id="88553-126">Valor</span><span class="sxs-lookup"><span data-stu-id="88553-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88553-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88553-127">Minimum supported client</span></span><br/> | <span data-ttu-id="88553-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="88553-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="88553-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88553-129">Minimum supported server</span></span><br/> | <span data-ttu-id="88553-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="88553-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="88553-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="88553-131">Namespace</span></span><br/>                | <span data-ttu-id="88553-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="88553-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="88553-133">MOF</span><span class="sxs-lookup"><span data-stu-id="88553-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88553-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88553-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="88553-135">DLL</span><span class="sxs-lookup"><span data-stu-id="88553-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88553-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="88553-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="88553-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="88553-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88553-138">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="88553-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




