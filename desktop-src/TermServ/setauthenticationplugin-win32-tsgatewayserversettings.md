---
title: Método SetAuthenticationPlugin da classe Win32_TSGatewayServerSettings
description: Define o plug-in de autenticação atual para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetAuthenticationPlugin
- Método SetAuthenticationPlugin Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetAuthenticationPlugin
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b5b332dd288a01f96b0eb0b3a99e7e45269cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645150"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="7b29d-106">Método SetAuthenticationPlugin da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="7b29d-106">SetAuthenticationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="7b29d-107">Define o plug-in de autenticação atual para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="7b29d-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b29d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b29d-108">Syntax</span></span>


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="7b29d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b29d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b29d-110">*Pluginname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7b29d-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b29d-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b29d-111">Type: **string**</span></span>

<span data-ttu-id="7b29d-112">O nome do novo plug-in de autenticação atual.</span><span class="sxs-lookup"><span data-stu-id="7b29d-112">The name of the new current authentication plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b29d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b29d-113">Return value</span></span>

<span data-ttu-id="7b29d-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b29d-114">Type: **uint32**</span></span>

<span data-ttu-id="7b29d-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7b29d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7b29d-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7b29d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7b29d-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7b29d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b29d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b29d-118">Remarks</span></span>

<span data-ttu-id="7b29d-119">Você deve chamar o método [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) para permitir que o plug-in de autenticação funcione.</span><span class="sxs-lookup"><span data-stu-id="7b29d-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authentication plug-in to work.</span></span>

<span data-ttu-id="7b29d-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7b29d-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7b29d-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7b29d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7b29d-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7b29d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7b29d-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7b29d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7b29d-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7b29d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b29d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b29d-125">Requirements</span></span>



| <span data-ttu-id="7b29d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b29d-126">Requirement</span></span> | <span data-ttu-id="7b29d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7b29d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b29d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b29d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7b29d-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7b29d-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7b29d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b29d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7b29d-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b29d-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="7b29d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b29d-132">Namespace</span></span><br/>                | <span data-ttu-id="7b29d-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="7b29d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7b29d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7b29d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b29d-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b29d-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b29d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7b29d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b29d-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b29d-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7b29d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b29d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b29d-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="7b29d-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="7b29d-140">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="7b29d-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

