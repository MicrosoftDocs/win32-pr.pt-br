---
title: Método SetUserGroupNames da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade usergroupnames para esta Área de Trabalho Remota política de autorização de conexão (RD \ 160; CAP).
ms.assetid: 03c9b2c5-8769-46f2-941f-302d798dd3a1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetUserGroupNames
- Método SetUserGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ca948b63cd106e7284b00c2c5f9e54c6dfa86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768542"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="11c49-106">Método SetUserGroupNames da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="11c49-106">SetUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="11c49-107">Define a propriedade **Usergroupnames** para esta área de trabalho remota política de autorização de conexão (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="11c49-107">Sets the **UserGroupNames** property for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="11c49-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11c49-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="11c49-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11c49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c49-110">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11c49-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c49-111">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="11c49-111">List of semicolon-separated user group names.</span></span> <span data-ttu-id="11c49-112">Os nomes são do formato *domínio \\ userGroupName*.</span><span class="sxs-lookup"><span data-stu-id="11c49-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="11c49-113">Se o usuário pertencer a qualquer um desses grupos de usuários, o usuário terá permissão para acessar o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="11c49-113">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c49-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11c49-114">Return value</span></span>

<span data-ttu-id="11c49-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="11c49-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="11c49-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="11c49-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="11c49-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="11c49-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11c49-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="11c49-118">Remarks</span></span>

<span data-ttu-id="11c49-119">Se vários nomes de grupos de usuários estiverem no parâmetro *Usergroupnames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.</span><span class="sxs-lookup"><span data-stu-id="11c49-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="11c49-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="11c49-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="11c49-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="11c49-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="11c49-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="11c49-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="11c49-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="11c49-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="11c49-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="11c49-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="11c49-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c49-125">Requirements</span></span>



| <span data-ttu-id="11c49-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c49-126">Requirement</span></span> | <span data-ttu-id="11c49-127">Valor</span><span class="sxs-lookup"><span data-stu-id="11c49-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c49-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11c49-128">Minimum supported client</span></span><br/> | <span data-ttu-id="11c49-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="11c49-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="11c49-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11c49-130">Minimum supported server</span></span><br/> | <span data-ttu-id="11c49-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11c49-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="11c49-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="11c49-132">Namespace</span></span><br/>                | <span data-ttu-id="11c49-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="11c49-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="11c49-134">MOF</span><span class="sxs-lookup"><span data-stu-id="11c49-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11c49-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11c49-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="11c49-136">DLL</span><span class="sxs-lookup"><span data-stu-id="11c49-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c49-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c49-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="11c49-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="11c49-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c49-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="11c49-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

