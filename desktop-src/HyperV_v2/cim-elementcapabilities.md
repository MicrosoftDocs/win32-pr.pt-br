---
description: Representa uma associação entre um elemento gerenciado e seus recursos.
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: Classe CIM_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782368"
---
# <a name="cim_elementcapabilities-class"></a><span data-ttu-id="9e6a2-103">\_Classe CIM ElementCapabilities</span><span class="sxs-lookup"><span data-stu-id="9e6a2-103">CIM\_ElementCapabilities class</span></span>

<span data-ttu-id="9e6a2-104">Representa uma associação entre um elemento gerenciado e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="9e6a2-104">Represents an association between a managed element and its capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e6a2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="9e6a2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9e6a2-106">Members</span></span>

<span data-ttu-id="9e6a2-107">A classe **CIM \_ ElementCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9e6a2-107">The **CIM\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="9e6a2-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9e6a2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e6a2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9e6a2-109">Properties</span></span>

<span data-ttu-id="9e6a2-110">A classe **CIM \_ ElementCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9e6a2-110">The **CIM\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e6a2-111">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="9e6a2-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6a2-112">Tipo de dados **: \_ recursos CIM**</span><span class="sxs-lookup"><span data-stu-id="9e6a2-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="9e6a2-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e6a2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6a2-114">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9e6a2-115">Os recursos associados ao elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9e6a2-115">The capabilities associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="9e6a2-116">**Características**</span><span class="sxs-lookup"><span data-stu-id="9e6a2-116">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6a2-117">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e6a2-117">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9e6a2-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e6a2-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e6a2-119">Um conjunto de informações descritivas sobre os recursos.</span><span class="sxs-lookup"><span data-stu-id="9e6a2-119">A set of descriptive information about the capabilities.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="9e6a2-120">**Padrão** (2)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-120">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

<span data-ttu-id="9e6a2-121">**Atual** (3)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-121">**Current** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9e6a2-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="9e6a2-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-123">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e6a2-124">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="9e6a2-124">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6a2-125">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="9e6a2-125">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="9e6a2-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e6a2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6a2-127">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="9e6a2-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9e6a2-128">O elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9e6a2-128">The managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e6a2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e6a2-129">Requirements</span></span>



| <span data-ttu-id="9e6a2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e6a2-130">Requirement</span></span> | <span data-ttu-id="9e6a2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9e6a2-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6a2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e6a2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6a2-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9e6a2-133">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9e6a2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e6a2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6a2-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e6a2-135">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9e6a2-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e6a2-136">Namespace</span></span><br/>                | <span data-ttu-id="9e6a2-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9e6a2-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9e6a2-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9e6a2-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e6a2-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e6a2-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e6a2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9e6a2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e6a2-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e6a2-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

