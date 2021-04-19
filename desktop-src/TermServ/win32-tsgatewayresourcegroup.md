---
title: Classe Win32_TSGatewayResourceGroup
description: Descreve um grupo de recursos, que mapeia um conjunto de recursos (nomes de computador) para uma única entidade.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayResourceGroup classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810968"
---
# <a name="win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="9d0e9-105">\_Classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9d0e9-105">Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="9d0e9-106">Descreve um grupo de recursos, que mapeia um conjunto de recursos (nomes de computador) para uma única entidade.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-106">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d0e9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d0e9-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a><span data-ttu-id="9d0e9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9d0e9-108">Members</span></span>

<span data-ttu-id="9d0e9-109">A classe **Win32 \_ TSGatewayResourceGroup** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9d0e9-109">The **Win32\_TSGatewayResourceGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="9d0e9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d0e9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9d0e9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d0e9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9d0e9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d0e9-112">Methods</span></span>

<span data-ttu-id="9d0e9-113">A classe **Win32 \_ TSGatewayResourceGroup** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-113">The **Win32\_TSGatewayResourceGroup** class has these methods.</span></span>



| <span data-ttu-id="9d0e9-114">Método</span><span class="sxs-lookup"><span data-stu-id="9d0e9-114">Method</span></span>                                                                  | <span data-ttu-id="9d0e9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d0e9-115">Description</span></span>                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d0e9-116">**Addresources**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-116">**AddResources**</span></span>](addresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="9d0e9-117">Adiciona recursos à propriedade **Resources** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-117">Adds resources to the **Resources** property for this resource group.</span></span><br/>      |
| [<span data-ttu-id="9d0e9-118">**Criar**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-118">**Create**</span></span>](create-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="9d0e9-119">Cria um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-119">Creates a resource group.</span></span><br/>                                                  |
| [<span data-ttu-id="9d0e9-120">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-120">**Delete**</span></span>](delete-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="9d0e9-121">Exclui este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-121">Deletes this resource group.</span></span><br/>                                               |
| [<span data-ttu-id="9d0e9-122">**RemoveResources**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-122">**RemoveResources**</span></span>](removeresources-win32-tsgatewayresourcegroup.md) | <span data-ttu-id="9d0e9-123">Exclui recursos da propriedade **Resources** para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-123">Deletes resources from the **Resources** property for this resource group.</span></span><br/> |
| [<span data-ttu-id="9d0e9-124">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-124">**SetDescription**</span></span>](setdescription-win32-tsgatewayresourcegroup.md)   | <span data-ttu-id="9d0e9-125">Define a propriedade **Description** para esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-125">Sets the **Description** property for this resource group.</span></span><br/>                 |
| [<span data-ttu-id="9d0e9-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-126">**SetName**</span></span>](setname-win32-tsgatewayresourcegroup.md)                 | <span data-ttu-id="9d0e9-127">Define a propriedade **Name** para esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-127">Sets the **Name** property for this resource group.</span></span><br/>                        |
| [<span data-ttu-id="9d0e9-128">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-128">**SetResources**</span></span>](setresources-win32-tsgatewayresourcegroup.md)       | <span data-ttu-id="9d0e9-129">Define a propriedade **Resources** para esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-129">Sets the **Resources** property for this resource group.</span></span><br/>                   |
| [<span data-ttu-id="9d0e9-130">**Cumulativo**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-130">**Update**</span></span>](update-win32-tsgatewayresourcegroup.md)                   | <span data-ttu-id="9d0e9-131">Atualiza este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-131">Updates this resource group.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="9d0e9-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d0e9-132">Properties</span></span>

<span data-ttu-id="9d0e9-133">A classe **Win32 \_ TSGatewayResourceGroup** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-133">The **Win32\_TSGatewayResourceGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d0e9-134">**AssociatedRAPs**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-134">**AssociatedRAPs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d0e9-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d0e9-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d0e9-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d0e9-137">Lista separada por ponto-e-vírgula de Serviços de Área de Trabalho Remota RD RAPs (políticas de autorização de recursos) que estão associadas a esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-137">Semicolon-separated list of Remote Desktop Services resource authorization policies (RD RAPs) that are associated with this resource group.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e9-138">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d0e9-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d0e9-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d0e9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d0e9-141">Descrição do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-141">Description of the resource group.</span></span> <span data-ttu-id="9d0e9-142">Essa propriedade pode ser alterada com o método [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0e9-142">This property can be changed with the [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e9-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d0e9-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d0e9-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d0e9-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d0e9-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d0e9-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d0e9-147">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-147">Name of the resource group.</span></span> <span data-ttu-id="9d0e9-148">Essa propriedade pode ser alterada com o método [**SetName**](setname-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0e9-148">This property can be changed with the [**SetName**](setname-win32-tsgatewayresourcegroup.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e9-149">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-149">**Resources**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d0e9-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d0e9-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d0e9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d0e9-152">Lista de recursos separados por ponto e vírgula neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-152">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="9d0e9-153">Um " \* " significa todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-153">An "\*" means all resources.</span></span> <span data-ttu-id="9d0e9-154">Essa propriedade pode ser alterada com os métodos [**Setresources**](setresources-win32-tsgatewayresourcegroup.md), [**addresources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)e [**Update**](update-win32-tsgatewayresourcegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0e9-154">This property can be changed with the [**SetResources**](setresources-win32-tsgatewayresourcegroup.md), [**AddResources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md), and [**Update**](update-win32-tsgatewayresourcegroup.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d0e9-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d0e9-155">Remarks</span></span>

<span data-ttu-id="9d0e9-156">Você deve ser um membro do grupo Administradores para usar essa classe.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-156">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="9d0e9-157">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9d0e9-157">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9d0e9-158">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-158">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9d0e9-159">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9d0e9-159">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9d0e9-160">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9d0e9-160">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d0e9-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d0e9-161">Requirements</span></span>



| <span data-ttu-id="9d0e9-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d0e9-162">Requirement</span></span> | <span data-ttu-id="9d0e9-163">Valor</span><span class="sxs-lookup"><span data-stu-id="9d0e9-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0e9-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d0e9-164">Minimum supported client</span></span><br/> | <span data-ttu-id="9d0e9-165">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9d0e9-165">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9d0e9-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d0e9-166">Minimum supported server</span></span><br/> | <span data-ttu-id="9d0e9-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d0e9-167">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9d0e9-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d0e9-168">Namespace</span></span><br/>                | <span data-ttu-id="9d0e9-169">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9d0e9-169">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9d0e9-170">MOF</span><span class="sxs-lookup"><span data-stu-id="9d0e9-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d0e9-171"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d0e9-171"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d0e9-172">DLL</span><span class="sxs-lookup"><span data-stu-id="9d0e9-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d0e9-173"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d0e9-173"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9d0e9-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d0e9-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d0e9-175">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-175">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="9d0e9-176">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-176">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="9d0e9-177">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-177">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="9d0e9-178">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-178">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="9d0e9-179">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-179">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="9d0e9-180">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="9d0e9-180">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

