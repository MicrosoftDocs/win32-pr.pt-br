---
title: Método RecycleRpcApplicationPools da classe Win32_TSGatewayServerSettings
description: Recicla os pools de aplicativos RPC no IIS.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RecycleRpcApplicationPools
- Método RecycleRpcApplicationPools Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método RecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455049"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="22611-106">Método RecycleRpcApplicationPools da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="22611-106">RecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="22611-107">Recicla os pools de aplicativos RPC no IIS.</span><span class="sxs-lookup"><span data-stu-id="22611-107">Recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="22611-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22611-108">Syntax</span></span>


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="22611-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22611-109">Parameters</span></span>

<span data-ttu-id="22611-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="22611-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22611-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22611-111">Return value</span></span>

<span data-ttu-id="22611-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22611-112">Type: **uint32**</span></span>

<span data-ttu-id="22611-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="22611-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="22611-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="22611-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="22611-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="22611-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22611-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="22611-116">Remarks</span></span>

<span data-ttu-id="22611-117">Chamar esse método resulta na desconexão de todas as conexões existentes.</span><span class="sxs-lookup"><span data-stu-id="22611-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="22611-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="22611-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="22611-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="22611-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="22611-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="22611-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="22611-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="22611-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="22611-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="22611-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="22611-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22611-123">Requirements</span></span>



| <span data-ttu-id="22611-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="22611-124">Requirement</span></span> | <span data-ttu-id="22611-125">Valor</span><span class="sxs-lookup"><span data-stu-id="22611-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22611-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22611-126">Minimum supported client</span></span><br/> | <span data-ttu-id="22611-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="22611-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="22611-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22611-128">Minimum supported server</span></span><br/> | <span data-ttu-id="22611-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22611-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="22611-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="22611-130">Namespace</span></span><br/>                | <span data-ttu-id="22611-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="22611-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="22611-132">MOF</span><span class="sxs-lookup"><span data-stu-id="22611-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22611-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22611-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="22611-134">DLL</span><span class="sxs-lookup"><span data-stu-id="22611-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22611-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22611-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="22611-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="22611-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22611-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="22611-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="22611-138">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="22611-138">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

