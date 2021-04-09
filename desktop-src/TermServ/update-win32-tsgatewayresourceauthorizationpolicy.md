---
title: Método Update da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Atualiza a política de autorização de recursos do Área de Trabalho Remota atual (RD \ 160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de atualização
- Método Update Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Serviços de Área de Trabalho Remota de classe Win32_TSGatewayResourceAuthorizationPolicy, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085756"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="c95cf-106">Método Update da classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="c95cf-106">Update method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="c95cf-107">Atualiza a RD RAP (política de autorização de recursos) do Área de Trabalho Remota atual.</span><span class="sxs-lookup"><span data-stu-id="c95cf-107">Updates the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="c95cf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c95cf-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="c95cf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c95cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c95cf-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-111">Nome da RD RAP.</span><span class="sxs-lookup"><span data-stu-id="c95cf-111">Name of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-112">*Descrição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-113">Descrição da RD RAP.</span><span class="sxs-lookup"><span data-stu-id="c95cf-113">Description of the RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-114">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-114">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-115">Indica se a RD RAP deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="c95cf-115">Indicates whether the RD RAP should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-116">*ResourceGroupName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-116">*ResourceGroupName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-117">Nome do grupo de recursos associado a esta RD RAP.</span><span class="sxs-lookup"><span data-stu-id="c95cf-117">Resource group name associated with this RD RAP.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-118">*ResourceGroupType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-118">*ResourceGroupType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-119">Tipo de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c95cf-119">Resource group type.</span></span>

<dt>

<span data-ttu-id="c95cf-120">RT</span><span class="sxs-lookup"><span data-stu-id="c95cf-120">"RG"</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-121">Grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c95cf-121">Resource group.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-122">CG</span><span class="sxs-lookup"><span data-stu-id="c95cf-122">"CG"</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-123">Grupo de computadores, conforme armazenado em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c95cf-123">Computer group, as stored in Active Directory Domain Services.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-124">OS</span><span class="sxs-lookup"><span data-stu-id="c95cf-124">"ALL"</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-125">Todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="c95cf-125">All resources.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c95cf-126">*Usergroupnames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-126">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-127">Lista de nomes de grupos de usuários separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="c95cf-127">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="c95cf-128">Os nomes são do formato *domínio \\ userGroupName*.</span><span class="sxs-lookup"><span data-stu-id="c95cf-128">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="c95cf-129">Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido.</span><span class="sxs-lookup"><span data-stu-id="c95cf-129">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-130">De *protocolo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-130">*ProtocolNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-131">Lista separada por ponto e vírgula de nomes de protocolo que estão habilitados para esta política.</span><span class="sxs-lookup"><span data-stu-id="c95cf-131">Semicolon-separated list of protocol names that are enabled for this policy.</span></span> <span data-ttu-id="c95cf-132">Os nomes devem corresponder ao retorno do método [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) da classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="c95cf-132">Names must match the return of the [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) method of the [**Win32\_TSGatewayServerSettings**](win32-tsgatewayserversettings.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="c95cf-133">*Portnumbers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c95cf-133">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c95cf-134">Lista separada por ponto e vírgula de números de porta que estão habilitados para esta política.</span><span class="sxs-lookup"><span data-stu-id="c95cf-134">Semicolon-separated list of port numbers that are enabled for this policy.</span></span> <span data-ttu-id="c95cf-135">Para permitir qualquer número de porta, defina " \* ".</span><span class="sxs-lookup"><span data-stu-id="c95cf-135">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c95cf-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c95cf-136">Return value</span></span>

<span data-ttu-id="c95cf-137">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="c95cf-137">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c95cf-138">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c95cf-138">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c95cf-139">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c95cf-139">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c95cf-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="c95cf-140">Remarks</span></span>

<span data-ttu-id="c95cf-141">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="c95cf-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c95cf-142">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c95cf-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c95cf-143">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c95cf-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c95cf-144">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c95cf-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c95cf-145">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c95cf-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c95cf-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c95cf-146">Requirements</span></span>



| <span data-ttu-id="c95cf-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c95cf-147">Requirement</span></span> | <span data-ttu-id="c95cf-148">Valor</span><span class="sxs-lookup"><span data-stu-id="c95cf-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c95cf-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c95cf-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c95cf-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c95cf-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c95cf-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c95cf-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c95cf-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c95cf-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c95cf-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="c95cf-153">Namespace</span></span><br/>                | <span data-ttu-id="c95cf-154">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c95cf-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c95cf-155">MOF</span><span class="sxs-lookup"><span data-stu-id="c95cf-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c95cf-156"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c95cf-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c95cf-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c95cf-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c95cf-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c95cf-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c95cf-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="c95cf-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c95cf-160">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c95cf-160">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

