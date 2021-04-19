---
description: Associa o Msvm \_ BootSourceSettingData ao VirtualSystemSettingData Msvm geral \_ .
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Classe Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778752"
---
# <a name="msvm_bootsourcecomponent-class"></a><span data-ttu-id="1dc06-103">\_Classe Msvm BootSourceComponent</span><span class="sxs-lookup"><span data-stu-id="1dc06-103">Msvm\_BootSourceComponent class</span></span>

<span data-ttu-id="1dc06-104">Associa o [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md) ao [**\_ VirtualSystemSettingData Msvm**](msvm-virtualsystemsettingdata.md)geral.</span><span class="sxs-lookup"><span data-stu-id="1dc06-104">Associates the [**Msvm\_BootSourceSettingData**](msvm-bootsourcesettingdata.md) to the overall [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span></span> <span data-ttu-id="1dc06-105">Essa classe deriva do [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="1dc06-105">This class derives from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

<span data-ttu-id="1dc06-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1dc06-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc06-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dc06-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1dc06-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1dc06-108">Members</span></span>

<span data-ttu-id="1dc06-109">A classe **Msvm \_ BootSourceComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1dc06-109">The **Msvm\_BootSourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="1dc06-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1dc06-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1dc06-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1dc06-111">Properties</span></span>

<span data-ttu-id="1dc06-112">A classe **Msvm \_ BootSourceComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1dc06-112">The **Msvm\_BootSourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1dc06-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1dc06-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc06-114">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="1dc06-114">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="1dc06-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1dc06-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dc06-116">Referência ao elemento pai na associação.</span><span class="sxs-lookup"><span data-stu-id="1dc06-116">Reference to the parent element in the association.</span></span> <span data-ttu-id="1dc06-117">Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="1dc06-117">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dc06-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1dc06-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dc06-119">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="1dc06-119">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="1dc06-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1dc06-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dc06-121">Referência ao elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="1dc06-121">Reference to the child element in the association.</span></span> <span data-ttu-id="1dc06-122">Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="1dc06-122">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1dc06-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc06-123">Requirements</span></span>



| <span data-ttu-id="1dc06-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc06-124">Requirement</span></span> | <span data-ttu-id="1dc06-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1dc06-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc06-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc06-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc06-127">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1dc06-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1dc06-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc06-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc06-129">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="1dc06-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1dc06-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1dc06-130">Namespace</span></span><br/>                | <span data-ttu-id="1dc06-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1dc06-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1dc06-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1dc06-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dc06-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1dc06-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dc06-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1dc06-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dc06-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1dc06-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1dc06-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dc06-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc06-137">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="1dc06-137">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="1dc06-138">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="1dc06-138">**CIM\_Component**</span></span>](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[<span data-ttu-id="1dc06-139">**Msvm \_ BootSourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="1dc06-139">**Msvm\_BootSourceSettingData**</span></span>](msvm-bootsourcesettingdata.md)
</dt> <dt>

[<span data-ttu-id="1dc06-140">**Msvm \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="1dc06-140">**Msvm\_VirtualSystemSettingData**</span></span>](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

