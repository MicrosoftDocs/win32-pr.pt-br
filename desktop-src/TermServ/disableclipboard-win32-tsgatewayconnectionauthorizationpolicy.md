---
title: Método DisableClipboard da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade ClipboardDisabled. Se a propriedade DeviceRedirectionType tiver um valor de \ 0034; 2 \ 0034;, a propriedade ClipboardDisabled controlará o redirecionamento da área de transferência para sessões que são estabelecidas por meio do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisableClipboard
- Método DisableClipboard Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método DisableClipboard
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779280"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="ac2eb-107">Método DisableClipboard da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="ac2eb-107">DisableClipboard method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="ac2eb-108">Define a propriedade **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="ac2eb-108">Sets the **ClipboardDisabled** property.</span></span> <span data-ttu-id="ac2eb-109">Se a propriedade **DeviceRedirectionType** tiver um valor de "2", a propriedade **ClipboardDisabled** controlará o redirecionamento da área de transferência para sessões que são estabelecidas por meio do servidor gateway de área de trabalho remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="ac2eb-109">If the **DeviceRedirectionType** property has a value of "2", the **ClipboardDisabled** property controls redirection of the clipboard for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2eb-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac2eb-110">Syntax</span></span>


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="ac2eb-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac2eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac2eb-112">*Desabilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac2eb-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac2eb-113">Novo valor para a propriedade **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="ac2eb-113">New value for the **ClipboardDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac2eb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac2eb-114">Return value</span></span>

<span data-ttu-id="ac2eb-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ac2eb-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ac2eb-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ac2eb-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ac2eb-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ac2eb-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ac2eb-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac2eb-118">Remarks</span></span>

<span data-ttu-id="ac2eb-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="ac2eb-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ac2eb-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ac2eb-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ac2eb-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ac2eb-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ac2eb-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ac2eb-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ac2eb-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ac2eb-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac2eb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac2eb-124">Requirements</span></span>



| <span data-ttu-id="ac2eb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac2eb-125">Requirement</span></span> | <span data-ttu-id="ac2eb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ac2eb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac2eb-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac2eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac2eb-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ac2eb-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ac2eb-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac2eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac2eb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac2eb-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ac2eb-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac2eb-131">Namespace</span></span><br/>                | <span data-ttu-id="ac2eb-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ac2eb-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ac2eb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="ac2eb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac2eb-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac2eb-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac2eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ac2eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac2eb-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac2eb-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ac2eb-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac2eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac2eb-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="ac2eb-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

