---
description: Representa um ponto de acesso a serviços (SAP), que é capaz de utilizar ou invocar um serviço. SAPs indicam que um serviço está disponível para outras entidades usarem.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: Classe CIM_ServiceAccessPoint (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782364"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a><span data-ttu-id="5ebd9-104">Classe CIM_ServiceAccessPoint (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="5ebd9-104">CIM_ServiceAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="5ebd9-105">Representa um ponto de acesso a serviços (SAP), que é capaz de utilizar ou invocar um serviço.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-105">Represents a service access point (SAP), which is able to utilize or invoke a service.</span></span> <span data-ttu-id="5ebd9-106">SAPs indicam que um serviço está disponível para outras entidades usarem.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-106">SAPs indicate that a service is available for other entities to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebd9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ebd9-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="5ebd9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5ebd9-108">Members</span></span>

<span data-ttu-id="5ebd9-109">A classe **CIM \_ ServiceAccessPoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5ebd9-109">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="5ebd9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ebd9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ebd9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ebd9-111">Properties</span></span>

<span data-ttu-id="5ebd9-112">A classe **CIM \_ ServiceAccessPoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-112">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ebd9-113">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-113">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebd9-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ebd9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-116">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5ebd9-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ebd9-117">O nome da classe usada para criar uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-117">The class name used to create an instance of this class.</span></span> <span data-ttu-id="5ebd9-118">**CreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-118">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd9-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebd9-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ebd9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-122">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5ebd9-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ebd9-123">O nome exclusivo do SAP que indica os recursos com suporte no SAP.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-123">The unique name of the SAP that indicates the features supported by the SAP.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd9-124">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-124">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebd9-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ebd9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-127">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="5ebd9-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="5ebd9-128">O nome da classe usada para criar uma instância do sistema que contém o SAP.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-128">The class name used to create an instance of the system that contains the SAP.</span></span> <span data-ttu-id="5ebd9-129">**SystemCreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-129">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="5ebd9-130">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-130">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ebd9-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ebd9-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ebd9-133">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="5ebd9-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="5ebd9-134">O nome do sistema que contém o SAP.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-134">The name of the system that contains the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ebd9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ebd9-135">Requirements</span></span>



| <span data-ttu-id="5ebd9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebd9-136">Requirement</span></span> | <span data-ttu-id="5ebd9-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5ebd9-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebd9-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebd9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebd9-139">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ebd9-139">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5ebd9-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebd9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebd9-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ebd9-141">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5ebd9-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ebd9-142">Namespace</span></span><br/>                | <span data-ttu-id="5ebd9-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5ebd9-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ebd9-144">MOF</span><span class="sxs-lookup"><span data-stu-id="5ebd9-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ebd9-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd9-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ebd9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5ebd9-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ebd9-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ebd9-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ebd9-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ebd9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebd9-149">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5ebd9-149">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

