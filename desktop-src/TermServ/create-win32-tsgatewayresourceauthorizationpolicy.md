---
title: Método Create da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Cria uma política de autorização de recursos de Área de Trabalho Remota (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369326"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="e574b-106">Método Create da classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="e574b-106">Create method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="e574b-107">Cria uma RD RAP (política de autorização de recursos) Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="e574b-107">Creates a Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="e574b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e574b-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="e574b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e574b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e574b-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-111">Nome da RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e574b-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-112">*Descrição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-113">Descrição da RD RAP.</span><span class="sxs-lookup"><span data-stu-id="e574b-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-114">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-115">Indica se a RD RAP deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="e574b-115">Indicates whether the RD RAP is to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-116">*ResourceGroupType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-116">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-117">Tipo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e574b-117">Resource group type.</span></span>

<dt>

<span data-ttu-id="e574b-118">RT</span><span class="sxs-lookup"><span data-stu-id="e574b-118">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="e574b-119">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e574b-119">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-120">CG</span><span class="sxs-lookup"><span data-stu-id="e574b-120">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="e574b-121">Grupo de computadores, conforme armazenado em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="e574b-121">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-122">OS</span><span class="sxs-lookup"><span data-stu-id="e574b-122">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="e574b-123">Todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="e574b-123">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e574b-124">*ResourceGroupName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-124">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e574b-125">Resource group name.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-126">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-127">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="e574b-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="e574b-128">Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido.</span><span class="sxs-lookup"><span data-stu-id="e574b-128">If the user belongs to any of these user groups, access will be permitted.</span></span> <span data-ttu-id="e574b-129">Os nomes de grupos de usuários devem ter o formato *domínio \\ userGroupName*.</span><span class="sxs-lookup"><span data-stu-id="e574b-129">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-130">De *protocolo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-131">Lista separada por ponto e vírgula de nomes de protocolo que estão habilitados para esta política.</span><span class="sxs-lookup"><span data-stu-id="e574b-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="e574b-132">Os nomes devem corresponder ao retorno do método [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) da classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="e574b-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e574b-133">*Portnumbers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e574b-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e574b-134">Lista separada por ponto e vírgula de números de porta que estão habilitados para esta política.</span><span class="sxs-lookup"><span data-stu-id="e574b-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="e574b-135">Para permitir qualquer número de porta, defina " \* ".</span><span class="sxs-lookup"><span data-stu-id="e574b-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e574b-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e574b-136">Return value</span></span>

<span data-ttu-id="e574b-137">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e574b-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e574b-138">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e574b-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e574b-139">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e574b-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e574b-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="e574b-140">Remarks</span></span>

<span data-ttu-id="e574b-141">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e574b-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e574b-142">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e574b-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e574b-143">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e574b-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e574b-144">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e574b-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e574b-145">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e574b-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e574b-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e574b-146">Requirements</span></span>



| <span data-ttu-id="e574b-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e574b-147">Requirement</span></span> | <span data-ttu-id="e574b-148">Valor</span><span class="sxs-lookup"><span data-stu-id="e574b-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e574b-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e574b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e574b-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e574b-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e574b-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e574b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e574b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e574b-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e574b-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="e574b-153">Namespace</span></span><br/>                | <span data-ttu-id="e574b-154">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e574b-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e574b-155">MOF</span><span class="sxs-lookup"><span data-stu-id="e574b-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e574b-156"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e574b-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e574b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e574b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e574b-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e574b-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e574b-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="e574b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e574b-160">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="e574b-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

