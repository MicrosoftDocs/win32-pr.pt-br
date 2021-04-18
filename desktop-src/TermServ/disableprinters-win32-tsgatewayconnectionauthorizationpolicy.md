---
title: Método DisablePrinters da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade PrintersDisabled. Se a propriedade DeviceRedirectionType tiver um valor de \ 0034; 2 \ 0034;, a propriedade PrintersDisabled controlará o redirecionamento das impressoras para sessões estabelecidas por meio do servidor gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisablePrinters
- Método DisablePrinters Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método DisablePrinters
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625425170bd5e29b953db8299048261e9351bff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764748"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="fe45d-107">Método DisablePrinters da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="fe45d-107">DisablePrinters method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="fe45d-108">Define a propriedade **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="fe45d-108">Sets the **PrintersDisabled** property.</span></span> <span data-ttu-id="fe45d-109">Se a propriedade **DeviceRedirectionType** tiver um valor de "2", a propriedade **PrintersDisabled** controlará o redirecionamento das impressoras que são estabelecidas por meio do servidor de gateway de área de trabalho remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="fe45d-109">If the **DeviceRedirectionType** property has a value of "2", the **PrintersDisabled** property controls redirection of the printers for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe45d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe45d-110">Syntax</span></span>


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="fe45d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe45d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe45d-112">*Desabilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe45d-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe45d-113">Novo valor para a propriedade **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="fe45d-113">New value for the **PrintersDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe45d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe45d-114">Return value</span></span>

<span data-ttu-id="fe45d-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="fe45d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fe45d-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fe45d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fe45d-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fe45d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe45d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe45d-118">Remarks</span></span>

<span data-ttu-id="fe45d-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="fe45d-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fe45d-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fe45d-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fe45d-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fe45d-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fe45d-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fe45d-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fe45d-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fe45d-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe45d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe45d-124">Requirements</span></span>



| <span data-ttu-id="fe45d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe45d-125">Requirement</span></span> | <span data-ttu-id="fe45d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fe45d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe45d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe45d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fe45d-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fe45d-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fe45d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe45d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fe45d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe45d-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fe45d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="fe45d-131">Namespace</span></span><br/>                | <span data-ttu-id="fe45d-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="fe45d-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fe45d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fe45d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe45d-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe45d-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe45d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fe45d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe45d-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe45d-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fe45d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe45d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe45d-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="fe45d-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

