---
title: Método SetDefaultPluginsAndRecycleRpcApplicationPools da classe Win32_TSGatewayServerSettings
description: Define os plug-ins de autenticação e autorização atuais para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) e recicla os pools de aplicativos RPC no IIS.
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetDefaultPluginsAndRecycleRpcApplicationPools
- Método SetDefaultPluginsAndRecycleRpcApplicationPools Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetDefaultPluginsAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919038"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="1c434-106">Método SetDefaultPluginsAndRecycleRpcApplicationPools da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="1c434-106">SetDefaultPluginsAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="1c434-107">Define os plug-ins de autenticação e autorização atuais para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) e recicla os pools de aplicativos RPC no IIS.</span><span class="sxs-lookup"><span data-stu-id="1c434-107">Sets the current authentication and authorization plug-ins for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c434-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c434-108">Syntax</span></span>


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="1c434-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c434-109">Parameters</span></span>

<span data-ttu-id="1c434-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1c434-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c434-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c434-111">Return value</span></span>

<span data-ttu-id="1c434-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c434-112">Type: **uint32**</span></span>

<span data-ttu-id="1c434-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="1c434-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1c434-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="1c434-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1c434-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1c434-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c434-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c434-116">Remarks</span></span>

<span data-ttu-id="1c434-117">Chamar esse método resulta na desconexão de todas as conexões existentes.</span><span class="sxs-lookup"><span data-stu-id="1c434-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="1c434-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="1c434-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1c434-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1c434-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c434-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1c434-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1c434-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="1c434-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c434-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1c434-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c434-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c434-123">Requirements</span></span>



| <span data-ttu-id="1c434-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c434-124">Requirement</span></span> | <span data-ttu-id="1c434-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1c434-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c434-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c434-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c434-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1c434-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1c434-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c434-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c434-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1c434-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="1c434-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c434-130">Namespace</span></span><br/>                | <span data-ttu-id="1c434-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="1c434-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1c434-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1c434-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c434-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c434-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c434-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1c434-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c434-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c434-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1c434-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c434-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c434-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="1c434-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

