---
title: Método fileresource da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Define o tipo e o nome do grupo de recursos.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Método fileresource Serviços de Área de Trabalho Remota
- Método fileresource Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método setresourceobject
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824576"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="0be3d-106">Método fileresource da \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="0be3d-106">SetResourceGroup method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="0be3d-107">Define o tipo e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0be3d-107">Sets the resource group type and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be3d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0be3d-108">Syntax</span></span>


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a><span data-ttu-id="0be3d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0be3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be3d-110">*ResourceGroupName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0be3d-110">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be3d-111">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0be3d-111">Resource group name.</span></span> <span data-ttu-id="0be3d-112">Esse valor substitui a propriedade **ResourceGroupName** existente.</span><span class="sxs-lookup"><span data-stu-id="0be3d-112">This value replaces the existing **ResourceGroupName** property.</span></span>

</dd> <dt>

<span data-ttu-id="0be3d-113">*ResourceGroupType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0be3d-113">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be3d-114">Identifica o tipo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0be3d-114">Identifies the type of the resource group.</span></span> <span data-ttu-id="0be3d-115">Esse valor substitui a propriedade **ResourceGroupType** existente.</span><span class="sxs-lookup"><span data-stu-id="0be3d-115">This value replaces the existing **ResourceGroupType** property.</span></span>

<dt>

<span data-ttu-id="0be3d-116">RT</span><span class="sxs-lookup"><span data-stu-id="0be3d-116">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="0be3d-117">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0be3d-117">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="0be3d-118">CG</span><span class="sxs-lookup"><span data-stu-id="0be3d-118">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="0be3d-119">Grupo de computadores, conforme armazenado em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="0be3d-119">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="0be3d-120">OS</span><span class="sxs-lookup"><span data-stu-id="0be3d-120">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="0be3d-121">Todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="0be3d-121">All resources.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be3d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0be3d-122">Return value</span></span>

<span data-ttu-id="0be3d-123">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="0be3d-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0be3d-124">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0be3d-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0be3d-125">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0be3d-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0be3d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0be3d-126">Remarks</span></span>

<span data-ttu-id="0be3d-127">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="0be3d-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0be3d-128">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0be3d-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0be3d-129">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0be3d-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0be3d-130">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0be3d-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0be3d-131">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0be3d-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0be3d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be3d-132">Requirements</span></span>



| <span data-ttu-id="0be3d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be3d-133">Requirement</span></span> | <span data-ttu-id="0be3d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="0be3d-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be3d-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be3d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0be3d-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0be3d-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0be3d-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be3d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0be3d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0be3d-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0be3d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0be3d-139">Namespace</span></span><br/>                | <span data-ttu-id="0be3d-140">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="0be3d-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0be3d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="0be3d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0be3d-142"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0be3d-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0be3d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0be3d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0be3d-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0be3d-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0be3d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="0be3d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be3d-146">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="0be3d-146">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

