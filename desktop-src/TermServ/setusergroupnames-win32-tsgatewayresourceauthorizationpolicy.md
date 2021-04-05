---
title: Método SetUserGroupNames da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Define a propriedade usergroupnames para a política de autorização de recursos de Área de Trabalho Remota (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetUserGroupNames
- Método SetUserGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085759"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="7e485-106">Método SetUserGroupNames da classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="7e485-106">SetUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="7e485-107">Define a propriedade **Usergroupnames** para o área de trabalho remota RD RAP (política de autorização de recursos).</span><span class="sxs-lookup"><span data-stu-id="7e485-107">Sets the **UserGroupNames** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e485-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e485-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="7e485-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e485-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e485-110">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e485-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e485-111">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="7e485-111">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="7e485-112">Os nomes são do formato *domínio \\ userGroupName*.</span><span class="sxs-lookup"><span data-stu-id="7e485-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="7e485-113">Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido.</span><span class="sxs-lookup"><span data-stu-id="7e485-113">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e485-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e485-114">Return value</span></span>

<span data-ttu-id="7e485-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7e485-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7e485-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7e485-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7e485-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7e485-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e485-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e485-118">Remarks</span></span>

<span data-ttu-id="7e485-119">Se vários nomes de grupos de usuários estiverem no parâmetro *Usergroupnames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.</span><span class="sxs-lookup"><span data-stu-id="7e485-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="7e485-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7e485-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7e485-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7e485-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7e485-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7e485-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7e485-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7e485-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7e485-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7e485-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e485-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e485-125">Requirements</span></span>



| <span data-ttu-id="7e485-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e485-126">Requirement</span></span> | <span data-ttu-id="7e485-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7e485-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e485-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e485-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7e485-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7e485-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7e485-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e485-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7e485-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e485-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7e485-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e485-132">Namespace</span></span><br/>                | <span data-ttu-id="7e485-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="7e485-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7e485-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7e485-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e485-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e485-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e485-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7e485-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e485-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e485-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7e485-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e485-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e485-139">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="7e485-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

