---
title: Método AddUserGroupNames da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Adiciona a lista de nomes de grupos de usuários existentes separados por ponto e vírgula aos grupos de usuários existente na propriedade usergroupnames.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddUserGroupNames
- Método AddUserGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c5c3fcb57c60ff2ca4c14d2e42ff0acdc84f0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918140"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="fbda0-106">Método AddUserGroupNames da classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="fbda0-106">AddUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="fbda0-107">Adiciona a lista de nomes de grupos de usuários existentes separados por ponto e vírgula aos grupos de usuários existente na propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="fbda0-107">Adds the specified semicolon-separated list of user group names to the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbda0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbda0-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="fbda0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbda0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbda0-110">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbda0-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbda0-111">Lista separada por ponto-e-vírgula de nomes de grupos de usuários a serem adicionados à propriedade **Usergroupnames** .</span><span class="sxs-lookup"><span data-stu-id="fbda0-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="fbda0-112">Os nomes de grupos de usuários devem ter o formato *domínio \\ userGroupName*.</span><span class="sxs-lookup"><span data-stu-id="fbda0-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbda0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbda0-113">Return value</span></span>

<span data-ttu-id="fbda0-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="fbda0-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fbda0-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fbda0-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fbda0-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fbda0-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fbda0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbda0-117">Remarks</span></span>

<span data-ttu-id="fbda0-118">Se vários nomes de grupos de usuários estiverem no parâmetro *Usergroupnames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.</span><span class="sxs-lookup"><span data-stu-id="fbda0-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="fbda0-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="fbda0-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fbda0-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fbda0-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fbda0-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fbda0-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fbda0-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fbda0-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fbda0-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fbda0-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbda0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbda0-124">Requirements</span></span>



| <span data-ttu-id="fbda0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbda0-125">Requirement</span></span> | <span data-ttu-id="fbda0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fbda0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbda0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbda0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fbda0-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fbda0-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fbda0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbda0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fbda0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbda0-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fbda0-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbda0-131">Namespace</span></span><br/>                | <span data-ttu-id="fbda0-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="fbda0-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fbda0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fbda0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbda0-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbda0-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbda0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fbda0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbda0-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbda0-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fbda0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbda0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbda0-138">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="fbda0-138">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

