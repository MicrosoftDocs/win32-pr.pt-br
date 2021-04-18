---
description: Representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: Classe CIM_Service (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778764"
---
# <a name="cim_service-class-hyper-v-management"></a><span data-ttu-id="90c0d-103">Classe CIM_Service (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="90c0d-103">CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="90c0d-104">Representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software.</span><span class="sxs-lookup"><span data-stu-id="90c0d-104">Represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="90c0d-105">Um serviço é um objeto de finalidade geral para configurar e gerenciar a implementação da funcionalidade; Ela não é a funcionalidade propriamente dita.</span><span class="sxs-lookup"><span data-stu-id="90c0d-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c0d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90c0d-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a><span data-ttu-id="90c0d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="90c0d-107">Members</span></span>

<span data-ttu-id="90c0d-108">A classe de **\_ serviço CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="90c0d-108">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="90c0d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="90c0d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="90c0d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90c0d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="90c0d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="90c0d-111">Methods</span></span>

<span data-ttu-id="90c0d-112">A classe de **\_ serviço CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="90c0d-112">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="90c0d-113">Método</span><span class="sxs-lookup"><span data-stu-id="90c0d-113">Method</span></span>                                           | <span data-ttu-id="90c0d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="90c0d-114">Description</span></span>                    |
|:-------------------------------------------------|:-------------------------------|
| [<span data-ttu-id="90c0d-115">**StartService**</span><span class="sxs-lookup"><span data-stu-id="90c0d-115">**StartService**</span></span>](cim-service-startservice.md) | <span data-ttu-id="90c0d-116">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="90c0d-116">Starts the service.</span></span><br/> |
| [<span data-ttu-id="90c0d-117">**StopService**</span><span class="sxs-lookup"><span data-stu-id="90c0d-117">**StopService**</span></span>](cim-service-stopservice.md)   | <span data-ttu-id="90c0d-118">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="90c0d-118">Stops the service.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="90c0d-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90c0d-119">Properties</span></span>

<span data-ttu-id="90c0d-120">A classe de **\_ serviço CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="90c0d-120">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90c0d-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="90c0d-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90c0d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90c0d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-124">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="90c0d-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-125">O nome da classe usada para criar uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="90c0d-125">The class name used to create an instance of this class.</span></span> <span data-ttu-id="90c0d-126">**CreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="90c0d-126">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="90c0d-127">**Nome**</span><span class="sxs-lookup"><span data-stu-id="90c0d-127">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90c0d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90c0d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-130">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="90c0d-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-131">Um identificador exclusivo do serviço que indica a funcionalidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="90c0d-131">A unique identifier of the service that indicates the functionality of the service.</span></span>

</dd> <dt>

<span data-ttu-id="90c0d-132">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="90c0d-132">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90c0d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="90c0d-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-135">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="90c0d-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-136">Informações de contato para o proprietário principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="90c0d-136">Contact information for the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="90c0d-137">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="90c0d-137">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90c0d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="90c0d-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-140">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações gerais do DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="90c0d-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-141">O nome do proprietário principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="90c0d-141">The name of the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="90c0d-142">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="90c0d-142">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="90c0d-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90c0d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-145">**true** se o serviço tiver sido iniciado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="90c0d-145">**true** if the service has been started; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="90c0d-146">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="90c0d-146">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90c0d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90c0d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-149">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (**" \_ serviço CIM**.**EnabledDefault**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="90c0d-149">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Service**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-150">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="90c0d-150">This property is deprecated.</span></span> <span data-ttu-id="90c0d-151">Em vez disso, use a propriedade **EnabledDefault** que é herdada do [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="90c0d-151">Instead, use the **EnabledDefault** property that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="90c0d-152">Descrição preterida: indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="90c0d-152">Deprecated description: Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

 

<dt>



 <span data-ttu-id="90c0d-153">("Automático")</span><span class="sxs-lookup"><span data-stu-id="90c0d-153">("Automatic")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="90c0d-154">("Manual")</span><span class="sxs-lookup"><span data-stu-id="90c0d-154">("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="90c0d-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="90c0d-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90c0d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90c0d-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-158">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="90c0d-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-159">O nome da classe usada para criar uma instância do sistema que contém o serviço.</span><span class="sxs-lookup"><span data-stu-id="90c0d-159">The class name used to create an instance of the system that contains the service.</span></span> <span data-ttu-id="90c0d-160">**SystemCreationClassName** é combinado com outras propriedades de chave dessa classe para identificar exclusivamente as instâncias dessa classe e suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="90c0d-160">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="90c0d-161">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="90c0d-161">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90c0d-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90c0d-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90c0d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90c0d-164">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="90c0d-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="90c0d-165">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="90c0d-165">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90c0d-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90c0d-166">Requirements</span></span>



| <span data-ttu-id="90c0d-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="90c0d-167">Requirement</span></span> | <span data-ttu-id="90c0d-168">Valor</span><span class="sxs-lookup"><span data-stu-id="90c0d-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90c0d-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90c0d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="90c0d-170">Windows 8</span><span class="sxs-lookup"><span data-stu-id="90c0d-170">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="90c0d-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90c0d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="90c0d-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90c0d-172">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="90c0d-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="90c0d-173">Namespace</span></span><br/>                | <span data-ttu-id="90c0d-174">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="90c0d-174">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="90c0d-175">MOF</span><span class="sxs-lookup"><span data-stu-id="90c0d-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90c0d-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90c0d-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90c0d-177">DLL</span><span class="sxs-lookup"><span data-stu-id="90c0d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c0d-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90c0d-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90c0d-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="90c0d-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c0d-180">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="90c0d-180">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

