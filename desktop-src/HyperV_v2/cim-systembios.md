---
description: Associa um BIOS a um sistema de computador.
ms.assetid: a06af789-75c8-4d58-8a25-572dcf1091e2
title: Classe CIM_SystemBIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemBIOS
- CIM_SystemBIOS.GroupComponent
- CIM_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: faa3130544fdb97bdf216fa266bc9e8cfe1815bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010835"
---
# <a name="cim_systembios-class"></a><span data-ttu-id="20235-103">\_Classe CIM SystemBIOS</span><span class="sxs-lookup"><span data-stu-id="20235-103">CIM\_SystemBIOS class</span></span>

<span data-ttu-id="20235-104">Associa um BIOS a um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="20235-104">Associates a BIOS with a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="20235-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20235-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_SystemBIOS : CIM_SystemComponent
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_BIOSElement    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="20235-106">Membros</span><span class="sxs-lookup"><span data-stu-id="20235-106">Members</span></span>

<span data-ttu-id="20235-107">A classe **CIM \_ SystemBIOS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20235-107">The **CIM\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="20235-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20235-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20235-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20235-109">Properties</span></span>

<span data-ttu-id="20235-110">A classe **CIM \_ SystemBIOS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="20235-110">The **CIM\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20235-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="20235-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20235-112">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="20235-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="20235-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20235-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20235-114">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="20235-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="20235-115">O sistema de computador que inicializa a partir do BIOS.</span><span class="sxs-lookup"><span data-stu-id="20235-115">The computer system that boots from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="20235-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="20235-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20235-117">Tipo de dados: **CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="20235-117">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="20235-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20235-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20235-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="20235-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="20235-120">O BIOS.</span><span class="sxs-lookup"><span data-stu-id="20235-120">The BIOS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20235-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20235-121">Requirements</span></span>



| <span data-ttu-id="20235-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="20235-122">Requirement</span></span> | <span data-ttu-id="20235-123">Valor</span><span class="sxs-lookup"><span data-stu-id="20235-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20235-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20235-124">Minimum supported client</span></span><br/> | <span data-ttu-id="20235-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="20235-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="20235-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20235-126">Minimum supported server</span></span><br/> | <span data-ttu-id="20235-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20235-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="20235-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="20235-128">Namespace</span></span><br/>                | <span data-ttu-id="20235-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="20235-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="20235-130">MOF</span><span class="sxs-lookup"><span data-stu-id="20235-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20235-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20235-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20235-132">DLL</span><span class="sxs-lookup"><span data-stu-id="20235-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20235-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20235-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20235-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="20235-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20235-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="20235-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

