---
title: Método RemoveUserGroupNames da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Remove os nomes de grupo de usuários especificados dos grupos de usuários existentes na propriedade usergroupnames.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveUserGroupNames
- Método RemoveUserGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753520"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="5ca3d-106">Método RemoveUserGroupNames da classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="5ca3d-106">RemoveUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="5ca3d-107">Remove os nomes de grupo de usuários especificados dos grupos de usuários existentes na propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="5ca3d-107">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca3d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ca3d-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="5ca3d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ca3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca3d-110">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ca3d-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca3d-111">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="5ca3d-111">Semicolon-separated list of user group names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca3d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ca3d-112">Return value</span></span>

<span data-ttu-id="5ca3d-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="5ca3d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5ca3d-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5ca3d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5ca3d-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5ca3d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca3d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ca3d-116">Remarks</span></span>

<span data-ttu-id="5ca3d-117">Se vários nomes de grupos de usuários estiverem no parâmetro *Usergroupnames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.</span><span class="sxs-lookup"><span data-stu-id="5ca3d-117">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="5ca3d-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="5ca3d-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5ca3d-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5ca3d-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5ca3d-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5ca3d-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5ca3d-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5ca3d-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5ca3d-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5ca3d-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca3d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ca3d-123">Requirements</span></span>



| <span data-ttu-id="5ca3d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ca3d-124">Requirement</span></span> | <span data-ttu-id="5ca3d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5ca3d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca3d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ca3d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca3d-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5ca3d-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5ca3d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ca3d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca3d-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ca3d-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5ca3d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ca3d-130">Namespace</span></span><br/>                | <span data-ttu-id="5ca3d-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5ca3d-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5ca3d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5ca3d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ca3d-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ca3d-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ca3d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5ca3d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca3d-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca3d-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5ca3d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ca3d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca3d-137">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="5ca3d-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

