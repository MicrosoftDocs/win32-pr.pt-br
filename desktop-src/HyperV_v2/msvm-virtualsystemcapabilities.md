---
description: Descreve os recursos do Msvm ComputerSystem associado \_ .
ms.assetid: 7e3b51ba-f85d-4b83-abc6-a094d412eca1
title: Classe Msvm_VirtualSystemCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCapabilities
- Msvm_VirtualSystemCapabilities.InstanceID
- Msvm_VirtualSystemCapabilities.Caption
- Msvm_VirtualSystemCapabilities.Description
- Msvm_VirtualSystemCapabilities.ElementName
- Msvm_VirtualSystemCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemCapabilities.MaxElementNameLen
- Msvm_VirtualSystemCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9fbd9b747e85ec1c9a1b7754f99282a7d913994e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164293"
---
# <a name="msvm_virtualsystemcapabilities-class"></a><span data-ttu-id="66a5a-103">\_Classe Msvm VirtualSystemCapabilities</span><span class="sxs-lookup"><span data-stu-id="66a5a-103">Msvm\_VirtualSystemCapabilities class</span></span>

<span data-ttu-id="66a5a-104">Descreve os recursos do [**Msvm \_ ComputerSystem**](msvm-computersystem.md)associado.</span><span class="sxs-lookup"><span data-stu-id="66a5a-104">Describes the capabilities of the associated [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="66a5a-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="66a5a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a5a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66a5a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Capabilities";
  string  Description = "Defines Virtual System Capabilities";
  string  ElementName = "Hyper-V Virtual System Capabilities";
  boolean ElementNameEditSupported = True;
  unit16  MaxElementNameLen = 100;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="66a5a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="66a5a-107">Members</span></span>

<span data-ttu-id="66a5a-108">A classe **Msvm \_ VirtualSystemCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="66a5a-108">The **Msvm\_VirtualSystemCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="66a5a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="66a5a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66a5a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="66a5a-110">Properties</span></span>

<span data-ttu-id="66a5a-111">A classe **Msvm \_ VirtualSystemCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="66a5a-111">The **Msvm\_VirtualSystemCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66a5a-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="66a5a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="66a5a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="66a5a-115">A short description of the object.</span></span> <span data-ttu-id="66a5a-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66a5a-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66a5a-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="66a5a-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="66a5a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="66a5a-120">A description of the object.</span></span> <span data-ttu-id="66a5a-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66a5a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66a5a-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="66a5a-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="66a5a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="66a5a-125">A display name for the object.</span></span> <span data-ttu-id="66a5a-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66a5a-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66a5a-127">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="66a5a-127">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="66a5a-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-130">Indica se a propriedade **ElementName** pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="66a5a-130">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="66a5a-131">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="66a5a-131">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="66a5a-132">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="66a5a-132">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="66a5a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-135">Especifica as restrições em **ElementName**, expressas como uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="66a5a-135">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="66a5a-136">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="66a5a-136">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="66a5a-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="66a5a-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="66a5a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-140">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="66a5a-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-141">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="66a5a-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="66a5a-142">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="66a5a-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="66a5a-143">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="66a5a-143">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-144">Tipo de dados: **unit16**</span><span class="sxs-lookup"><span data-stu-id="66a5a-144">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-146">Qualificadores: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="66a5a-146">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-147">Especifica o comprimento máximo com suporte da propriedade **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="66a5a-147">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="66a5a-148">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="66a5a-148">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="66a5a-149">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="66a5a-149">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a5a-150">Tipo de dados: matriz **unit16**</span><span class="sxs-lookup"><span data-stu-id="66a5a-150">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="66a5a-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="66a5a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66a5a-152">Indica os possíveis Estados que podem ser solicitados ao usar o método **RequestStateChange** no elemento lógico habilitado.</span><span class="sxs-lookup"><span data-stu-id="66a5a-152">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="66a5a-153">Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="66a5a-153">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="66a5a-154">Valor</span><span class="sxs-lookup"><span data-stu-id="66a5a-154">Value</span></span>                                                                         | <span data-ttu-id="66a5a-155">Significado</span><span class="sxs-lookup"><span data-stu-id="66a5a-155">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="66a5a-156"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-156"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="66a5a-157">habilitado</span><span class="sxs-lookup"><span data-stu-id="66a5a-157">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="66a5a-158"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-158"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="66a5a-159">Desabilita</span><span class="sxs-lookup"><span data-stu-id="66a5a-159">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="66a5a-160"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-160"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="66a5a-161">Desligar</span><span class="sxs-lookup"><span data-stu-id="66a5a-161">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="66a5a-162"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-162"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="66a5a-163">Offline</span><span class="sxs-lookup"><span data-stu-id="66a5a-163">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="66a5a-164"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-164"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="66a5a-165">Teste</span><span class="sxs-lookup"><span data-stu-id="66a5a-165">Test</span></span><br/>      |
| <dl> <span data-ttu-id="66a5a-166"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-166"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="66a5a-167">Ferida</span><span class="sxs-lookup"><span data-stu-id="66a5a-167">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="66a5a-168"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-168"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="66a5a-169">Fechar</span><span class="sxs-lookup"><span data-stu-id="66a5a-169">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="66a5a-170"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-170"><dt>10</dt></span></span> </dl> | <span data-ttu-id="66a5a-171">Reboot</span><span class="sxs-lookup"><span data-stu-id="66a5a-171">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="66a5a-172"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-172"><dt>11</dt></span></span> </dl> | <span data-ttu-id="66a5a-173">Redefinir</span><span class="sxs-lookup"><span data-stu-id="66a5a-173">Reset</span></span><br/>     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66a5a-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a5a-174">Requirements</span></span>



| <span data-ttu-id="66a5a-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a5a-175">Requirement</span></span> | <span data-ttu-id="66a5a-176">Valor</span><span class="sxs-lookup"><span data-stu-id="66a5a-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a5a-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a5a-177">Minimum supported client</span></span><br/> | <span data-ttu-id="66a5a-178">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="66a5a-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="66a5a-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66a5a-179">Minimum supported server</span></span><br/> | <span data-ttu-id="66a5a-180">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="66a5a-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66a5a-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="66a5a-181">Namespace</span></span><br/>                | <span data-ttu-id="66a5a-182">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="66a5a-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="66a5a-183">MOF</span><span class="sxs-lookup"><span data-stu-id="66a5a-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66a5a-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66a5a-185">DLL</span><span class="sxs-lookup"><span data-stu-id="66a5a-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66a5a-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66a5a-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

