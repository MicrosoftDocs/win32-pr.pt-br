---
title: Método SetSessionTimeout da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define as propriedades SessionTimeout e SessionTimeoutAction.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSessionTimeout
- Método SetSessionTimeout Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetSessionTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499502"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="86e22-106">Método SetSessionTimeout da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="86e22-106">SetSessionTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="86e22-107">Define as propriedades **SessionTimeout** e **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="86e22-107">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e22-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86e22-108">Syntax</span></span>


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a><span data-ttu-id="86e22-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86e22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e22-110">*SessionTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86e22-110">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e22-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86e22-111">Type: **uint32**</span></span>

<span data-ttu-id="86e22-112">O novo valor de tempo limite, em minutos.</span><span class="sxs-lookup"><span data-stu-id="86e22-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="86e22-113">Um valor de 0 significa que não há nenhum tempo limite.</span><span class="sxs-lookup"><span data-stu-id="86e22-113">A value of 0 means there is no timeout.</span></span>

</dd> <dt>

<span data-ttu-id="86e22-114">*SessionTimeoutAction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86e22-114">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e22-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86e22-115">Type: **uint32**</span></span>

<span data-ttu-id="86e22-116">Especifica a ação a ser executada no caso de um tempo limite de sessão.</span><span class="sxs-lookup"><span data-stu-id="86e22-116">Specifies the action to be taken in case of a session timeout.</span></span> <span data-ttu-id="86e22-117">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="86e22-117">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="86e22-118">0</span><span class="sxs-lookup"><span data-stu-id="86e22-118">0</span></span>
</dt> <dd>

<span data-ttu-id="86e22-119">Desconecte a sessão.</span><span class="sxs-lookup"><span data-stu-id="86e22-119">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="86e22-120">1</span><span class="sxs-lookup"><span data-stu-id="86e22-120">1</span></span>
</dt> <dd>

<span data-ttu-id="86e22-121">Tentativa de autorizar a sessão novamente.</span><span class="sxs-lookup"><span data-stu-id="86e22-121">Attempt to re-authorize the session.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e22-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86e22-122">Return value</span></span>

<span data-ttu-id="86e22-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86e22-123">Type: **uint32**</span></span>

<span data-ttu-id="86e22-124">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="86e22-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="86e22-125">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="86e22-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="86e22-126">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="86e22-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="86e22-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="86e22-127">Remarks</span></span>

<span data-ttu-id="86e22-128">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="86e22-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="86e22-129">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="86e22-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86e22-130">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="86e22-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="86e22-131">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="86e22-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86e22-132">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="86e22-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="86e22-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86e22-133">Requirements</span></span>



| <span data-ttu-id="86e22-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="86e22-134">Requirement</span></span> | <span data-ttu-id="86e22-135">Valor</span><span class="sxs-lookup"><span data-stu-id="86e22-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86e22-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86e22-136">Minimum supported client</span></span><br/> | <span data-ttu-id="86e22-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="86e22-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="86e22-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86e22-138">Minimum supported server</span></span><br/> | <span data-ttu-id="86e22-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86e22-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="86e22-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="86e22-140">Namespace</span></span><br/>                | <span data-ttu-id="86e22-141">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="86e22-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="86e22-142">MOF</span><span class="sxs-lookup"><span data-stu-id="86e22-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86e22-143"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86e22-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="86e22-144">DLL</span><span class="sxs-lookup"><span data-stu-id="86e22-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e22-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e22-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="86e22-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="86e22-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e22-147">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="86e22-147">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

