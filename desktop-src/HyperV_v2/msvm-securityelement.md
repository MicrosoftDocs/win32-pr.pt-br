---
description: Representa as configurações de segurança de tempo de execução de um \_ sistema CIM.
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Classe Msvm_SecurityElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f0de0fe1a515db0e7b1d8d49b96b61500703480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922990"
---
# <a name="msvm_securityelement-class"></a><span data-ttu-id="1ab01-103">\_Classe Msvm SecurityElement</span><span class="sxs-lookup"><span data-stu-id="1ab01-103">Msvm\_SecurityElement class</span></span>

<span data-ttu-id="1ab01-104">Representa as configurações de segurança de tempo de execução de um [**\_ sistema CIM**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="1ab01-104">Represents the runtime security settings of a [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="1ab01-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1ab01-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab01-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ab01-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a><span data-ttu-id="1ab01-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1ab01-107">Members</span></span>

<span data-ttu-id="1ab01-108">A classe **Msvm \_ SecurityElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1ab01-108">The **Msvm\_SecurityElement** class has these types of members:</span></span>

-   [<span data-ttu-id="1ab01-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1ab01-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ab01-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1ab01-110">Properties</span></span>

<span data-ttu-id="1ab01-111">A classe **Msvm \_ SecurityElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1ab01-111">The **Msvm\_SecurityElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ab01-112">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ab01-112">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ab01-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ab01-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab01-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1ab01-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1ab01-116">O nome da classe ou da subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1ab01-116">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="1ab01-117">Quando usado com as outras propriedades de chave dessa classe, **CreationClassName** permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1ab01-117">When used with the other key properties of this class, **CreationClassName** allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="1ab01-118">**EncryptStateAndVmMigrationTrafficEnabled**</span><span class="sxs-lookup"><span data-stu-id="1ab01-118">**EncryptStateAndVmMigrationTrafficEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ab01-119">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1ab01-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab01-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ab01-121">Indica se a VM está atualmente tendo seu estado e o tráfego de migração criptografados.</span><span class="sxs-lookup"><span data-stu-id="1ab01-121">Indicates whether the VM is currently having its state and migration traffic encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="1ab01-122">**Blindado**</span><span class="sxs-lookup"><span data-stu-id="1ab01-122">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ab01-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1ab01-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab01-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ab01-125">Indica se a VM está blindada no momento.</span><span class="sxs-lookup"><span data-stu-id="1ab01-125">Indicates whether the VM is currently shielded.</span></span>

</dd> <dt>

<span data-ttu-id="1ab01-126">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ab01-126">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ab01-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ab01-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab01-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-129">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="1ab01-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="1ab01-130">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1ab01-130">The creation class name of the scoping system.</span></span>

</dd> <dt>

<span data-ttu-id="1ab01-131">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1ab01-131">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ab01-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ab01-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ab01-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ab01-134">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="1ab01-134">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="1ab01-135">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1ab01-135">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ab01-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ab01-136">Requirements</span></span>



| <span data-ttu-id="1ab01-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ab01-137">Requirement</span></span> | <span data-ttu-id="1ab01-138">Valor</span><span class="sxs-lookup"><span data-stu-id="1ab01-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab01-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ab01-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab01-140">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="1ab01-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1ab01-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ab01-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab01-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1ab01-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1ab01-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ab01-143">Namespace</span></span><br/>                | <span data-ttu-id="1ab01-144">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1ab01-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1ab01-145">MOF</span><span class="sxs-lookup"><span data-stu-id="1ab01-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ab01-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ab01-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ab01-147">DLL</span><span class="sxs-lookup"><span data-stu-id="1ab01-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ab01-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ab01-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ab01-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ab01-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab01-150">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1ab01-150">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

