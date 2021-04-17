---
description: Representa um serviço da plataforma Microsoft Windows Hyper-V.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Classe Msvm_VirtualizationComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812933"
---
# <a name="msvm_virtualizationcomponent-class"></a><span data-ttu-id="feb24-103">\_Classe Msvm VirtualizationComponent</span><span class="sxs-lookup"><span data-stu-id="feb24-103">Msvm\_VirtualizationComponent class</span></span>

<span data-ttu-id="feb24-104">Representa um serviço da plataforma Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="feb24-104">Represents a service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="feb24-105">A sintaxe a seguir é simplificada formato MOF código (MOF).</span><span class="sxs-lookup"><span data-stu-id="feb24-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb24-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="feb24-106">Syntax</span></span>

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="feb24-107">Membros</span><span class="sxs-lookup"><span data-stu-id="feb24-107">Members</span></span>

<span data-ttu-id="feb24-108">A classe **Msvm \_ VirtualizationComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="feb24-108">The **Msvm\_VirtualizationComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="feb24-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="feb24-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="feb24-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="feb24-110">Properties</span></span>

<span data-ttu-id="feb24-111">A classe **Msvm \_ VirtualizationComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="feb24-111">The **Msvm\_VirtualizationComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="feb24-112">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="feb24-112">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feb24-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="feb24-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feb24-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="feb24-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feb24-115">Um **GUID** que representa o identificador de classe do objeto com do serviço.</span><span class="sxs-lookup"><span data-stu-id="feb24-115">A **GUID** that represents the class identifier of the service's COM object.</span></span>

</dd> <dt>

<span data-ttu-id="feb24-116">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="feb24-116">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feb24-117">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="feb24-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="feb24-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="feb24-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feb24-119">Qualificadores: **experimental**</span><span class="sxs-lookup"><span data-stu-id="feb24-119">Qualifiers: **Experimental**</span></span>
</dt> </dl>

<span data-ttu-id="feb24-120">O contexto no qual o objeto recém-criado será executado.</span><span class="sxs-lookup"><span data-stu-id="feb24-120">The context in which the newly created object will run.</span></span> <span data-ttu-id="feb24-121">Esse valor é passado no parâmetro *dwClsContext* para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="feb24-121">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="feb24-122">Essa propriedade é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="feb24-122">This property is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="feb24-123">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="feb24-123">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feb24-124">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="feb24-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="feb24-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="feb24-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="feb24-126">**True** é que essa instância está habilitada e pode ser usada para concluir as solicitações do cliente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="feb24-126">**True** is this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="feb24-127">Essa propriedade é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="feb24-127">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="feb24-128">**Nome**</span><span class="sxs-lookup"><span data-stu-id="feb24-128">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="feb24-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="feb24-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="feb24-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="feb24-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="feb24-131">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="feb24-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="feb24-132">Uma cadeia de caracteres neutra em idioma que identifica exclusivamente o serviço.</span><span class="sxs-lookup"><span data-stu-id="feb24-132">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="feb24-133">O seguinte formato é sugerido para evitar conflitos de nomenclatura: " \| versão do componente do fornecedor \| ".</span><span class="sxs-lookup"><span data-stu-id="feb24-133">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="feb24-134">Por exemplo, esse nome representa a versão 1,0 do componente de porta de rede emulada da Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="feb24-134">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="feb24-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="feb24-135">Remarks</span></span>

<span data-ttu-id="feb24-136">O acesso à classe **Msvm \_ VirtualizationComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="feb24-136">Access to the **Msvm\_VirtualizationComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="feb24-137">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="feb24-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="feb24-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feb24-138">Requirements</span></span>



| <span data-ttu-id="feb24-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="feb24-139">Requirement</span></span> | <span data-ttu-id="feb24-140">Valor</span><span class="sxs-lookup"><span data-stu-id="feb24-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb24-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="feb24-141">Minimum supported client</span></span><br/> | <span data-ttu-id="feb24-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="feb24-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="feb24-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="feb24-143">Minimum supported server</span></span><br/> | <span data-ttu-id="feb24-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="feb24-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="feb24-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="feb24-145">End of client support</span></span><br/>    | <span data-ttu-id="feb24-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="feb24-146">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="feb24-147">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="feb24-147">End of server support</span></span><br/>    | <span data-ttu-id="feb24-148">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="feb24-148">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="feb24-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="feb24-149">Namespace</span></span><br/>                | <span data-ttu-id="feb24-150">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="feb24-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="feb24-151">MOF</span><span class="sxs-lookup"><span data-stu-id="feb24-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="feb24-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="feb24-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="feb24-153">DLL</span><span class="sxs-lookup"><span data-stu-id="feb24-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="feb24-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="feb24-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

