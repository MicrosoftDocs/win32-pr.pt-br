---
title: Método SetAuthenticationPluginAndRecycleRpcApplicationPools da classe Win32_TSGatewayServerSettings
description: Define o plug-in de autenticação atual para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) e recicla os pools de aplicativos RPC no IIS.
ms.assetid: cdceaf50-3d0a-4af0-9ad5-fb43760fcf7b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetAuthenticationPluginAndRecycleRpcApplicationPools
- Método SetAuthenticationPluginAndRecycleRpcApplicationPools Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetAuthenticationPluginAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPluginAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b234e04c349d20ea178de12f050190b30193d444
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644454"
---
# <a name="setauthenticationpluginandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="2a69f-106">Método SetAuthenticationPluginAndRecycleRpcApplicationPools da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="2a69f-106">SetAuthenticationPluginAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="2a69f-107">Define o plug-in de autenticação atual para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) e recicla os pools de aplicativos RPC no IIS.</span><span class="sxs-lookup"><span data-stu-id="2a69f-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

<span data-ttu-id="2a69f-108">Esse método é equivalente a chamar os métodos [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) e [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) em sequência.</span><span class="sxs-lookup"><span data-stu-id="2a69f-108">This method is equivalent to calling the [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) and [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) methods in sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a69f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a69f-109">Syntax</span></span>


```mof
uint32 SetAuthenticationPluginAndRecycleRpcApplicationPools(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="2a69f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a69f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a69f-111">*Pluginname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a69f-111">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a69f-112">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2a69f-112">Type: **string**</span></span>

<span data-ttu-id="2a69f-113">Nome do plug-in de autenticação</span><span class="sxs-lookup"><span data-stu-id="2a69f-113">Name of the authentication plug-in</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a69f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a69f-114">Return value</span></span>

<span data-ttu-id="2a69f-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a69f-115">Type: **uint32**</span></span>

<span data-ttu-id="2a69f-116">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="2a69f-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2a69f-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="2a69f-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2a69f-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2a69f-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a69f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a69f-119">Remarks</span></span>

<span data-ttu-id="2a69f-120">Chamar esse método resulta na desconexão de todas as conexões existentes.</span><span class="sxs-lookup"><span data-stu-id="2a69f-120">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="2a69f-121">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="2a69f-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2a69f-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2a69f-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2a69f-123">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2a69f-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2a69f-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="2a69f-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2a69f-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2a69f-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a69f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a69f-126">Requirements</span></span>



| <span data-ttu-id="2a69f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a69f-127">Requirement</span></span> | <span data-ttu-id="2a69f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2a69f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a69f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a69f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2a69f-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2a69f-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2a69f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a69f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2a69f-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2a69f-132">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="2a69f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a69f-133">Namespace</span></span><br/>                | <span data-ttu-id="2a69f-134">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2a69f-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2a69f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2a69f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a69f-136"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a69f-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a69f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2a69f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a69f-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a69f-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2a69f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a69f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a69f-140">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="2a69f-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="2a69f-141">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="2a69f-141">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="2a69f-142">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="2a69f-142">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

