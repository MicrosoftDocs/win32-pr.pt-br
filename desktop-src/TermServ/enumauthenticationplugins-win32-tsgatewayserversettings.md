---
title: Método EnumAuthenticationPlugins da classe Win32_TSGatewayServerSettings
description: Enumera todos os plug-ins de autenticação registrados.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnumAuthenticationPlugins
- Método EnumAuthenticationPlugins Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnumAuthenticationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0cd9d059a79749f657c6191e68e7bcd08555cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779431"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="6abd2-106">Método EnumAuthenticationPlugins da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="6abd2-106">EnumAuthenticationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="6abd2-107">Enumera todos os plug-ins de autenticação registrados.</span><span class="sxs-lookup"><span data-stu-id="6abd2-107">Enumerates all registered authentication plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abd2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6abd2-108">Syntax</span></span>


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="6abd2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6abd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6abd2-110">*Plug-ins* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6abd2-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6abd2-111">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6abd2-111">Type: **string\[\]**</span></span>

<span data-ttu-id="6abd2-112">Uma matriz de **cadeia de caracteres** que recebe os nomes dos plug-ins de autenticação registrados.</span><span class="sxs-lookup"><span data-stu-id="6abd2-112">A **string** array that receives the names of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="6abd2-113">*CLSIDs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6abd2-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6abd2-114">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6abd2-114">Type: **string\[\]**</span></span>

<span data-ttu-id="6abd2-115">Uma matriz de **cadeia de caracteres** que recebe os CLSIDs dos plug-ins de autenticação registrados.</span><span class="sxs-lookup"><span data-stu-id="6abd2-115">A **string** array that receives the CLSIDs of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="6abd2-116">*Descrições* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="6abd2-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6abd2-117">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6abd2-117">Type: **string\[\]**</span></span>

<span data-ttu-id="6abd2-118">Uma matriz de **cadeia de caracteres** que recebe as descrições dos plug-ins de autenticação registrados.</span><span class="sxs-lookup"><span data-stu-id="6abd2-118">A **string** array that receives the descriptions of the registered authentication plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6abd2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6abd2-119">Return value</span></span>

<span data-ttu-id="6abd2-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6abd2-120">Type: **uint32**</span></span>

<span data-ttu-id="6abd2-121">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="6abd2-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6abd2-122">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6abd2-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6abd2-123">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6abd2-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6abd2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6abd2-124">Remarks</span></span>

<span data-ttu-id="6abd2-125">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="6abd2-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6abd2-126">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6abd2-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6abd2-127">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6abd2-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6abd2-128">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6abd2-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6abd2-129">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6abd2-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6abd2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6abd2-130">Requirements</span></span>



| <span data-ttu-id="6abd2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6abd2-131">Requirement</span></span> | <span data-ttu-id="6abd2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="6abd2-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6abd2-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6abd2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6abd2-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6abd2-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6abd2-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6abd2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6abd2-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6abd2-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="6abd2-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="6abd2-137">Namespace</span></span><br/>                | <span data-ttu-id="6abd2-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6abd2-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6abd2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6abd2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6abd2-140"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6abd2-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6abd2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6abd2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6abd2-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6abd2-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6abd2-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="6abd2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abd2-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="6abd2-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

