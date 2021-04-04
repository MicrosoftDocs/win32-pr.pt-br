---
title: Método SetCookieAuthenticationAllowed da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade CookieAuthenticationAllowed.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetCookieAuthenticationAllowed
- Método SetCookieAuthenticationAllowed Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetCookieAuthenticationAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085300"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e7bf6-106">Método SetCookieAuthenticationAllowed da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="e7bf6-106">SetCookieAuthenticationAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e7bf6-107">Define a propriedade **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="e7bf6-107">Sets the **CookieAuthenticationAllowed** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bf6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7bf6-108">Syntax</span></span>


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="e7bf6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7bf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bf6-110">*Permitido* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7bf6-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bf6-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e7bf6-111">Type: **boolean**</span></span>

<span data-ttu-id="e7bf6-112">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e7bf6-112">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bf6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7bf6-113">Return value</span></span>

<span data-ttu-id="e7bf6-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7bf6-114">Type: **uint32**</span></span>

<span data-ttu-id="e7bf6-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e7bf6-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e7bf6-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e7bf6-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e7bf6-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e7bf6-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7bf6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7bf6-118">Remarks</span></span>

<span data-ttu-id="e7bf6-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e7bf6-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e7bf6-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e7bf6-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e7bf6-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e7bf6-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e7bf6-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e7bf6-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e7bf6-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e7bf6-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bf6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7bf6-124">Requirements</span></span>



| <span data-ttu-id="e7bf6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7bf6-125">Requirement</span></span> | <span data-ttu-id="e7bf6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e7bf6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bf6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bf6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bf6-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e7bf6-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e7bf6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7bf6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bf6-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7bf6-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="e7bf6-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7bf6-131">Namespace</span></span><br/>                | <span data-ttu-id="e7bf6-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e7bf6-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e7bf6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="e7bf6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7bf6-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf6-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7bf6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e7bf6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7bf6-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7bf6-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e7bf6-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7bf6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bf6-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="e7bf6-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

