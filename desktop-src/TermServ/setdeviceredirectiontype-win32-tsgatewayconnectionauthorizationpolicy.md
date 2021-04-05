---
title: Método SetDeviceRedirectionType da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade DeviceRedirectionType, que controla quais dispositivos serão redirecionados.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetDeviceRedirectionType
- Método SetDeviceRedirectionType Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetDeviceRedirectionType
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918366"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="894ed-106">Método SetDeviceRedirectionType da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="894ed-106">SetDeviceRedirectionType method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="894ed-107">Define a propriedade **DeviceRedirectionType** , que controla quais dispositivos serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="894ed-107">Sets the **DeviceRedirectionType** property, which controls which devices will be redirected.</span></span>

## <a name="syntax"></a><span data-ttu-id="894ed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="894ed-108">Syntax</span></span>


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a><span data-ttu-id="894ed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="894ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="894ed-110">*DeviceRedirectionType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="894ed-110">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="894ed-111">O tipo de redirecionamento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="894ed-111">The device redirection type.</span></span>

<dt>

<span data-ttu-id="894ed-112">0</span><span class="sxs-lookup"><span data-stu-id="894ed-112">0</span></span>
</dt> <dd>

<span data-ttu-id="894ed-113">Todos os dispositivos serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="894ed-113">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="894ed-114">1</span><span class="sxs-lookup"><span data-stu-id="894ed-114">1</span></span>
</dt> <dd>

<span data-ttu-id="894ed-115">Nenhum dispositivo será redirecionado.</span><span class="sxs-lookup"><span data-stu-id="894ed-115">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="894ed-116">2</span><span class="sxs-lookup"><span data-stu-id="894ed-116">2</span></span>
</dt> <dd>

<span data-ttu-id="894ed-117">Os dispositivos especificados não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="894ed-117">Specified devices will not be redirected.</span></span> <span data-ttu-id="894ed-118">As propriedades **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controlam quais dispositivos não serão redirecionados.</span><span class="sxs-lookup"><span data-stu-id="894ed-118">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="894ed-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="894ed-119">Return value</span></span>

<span data-ttu-id="894ed-120">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="894ed-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="894ed-121">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="894ed-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="894ed-122">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="894ed-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="894ed-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="894ed-123">Remarks</span></span>

<span data-ttu-id="894ed-124">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="894ed-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="894ed-125">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="894ed-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="894ed-126">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="894ed-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="894ed-127">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="894ed-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="894ed-128">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="894ed-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="894ed-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="894ed-129">Requirements</span></span>



| <span data-ttu-id="894ed-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="894ed-130">Requirement</span></span> | <span data-ttu-id="894ed-131">Valor</span><span class="sxs-lookup"><span data-stu-id="894ed-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="894ed-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="894ed-132">Minimum supported client</span></span><br/> | <span data-ttu-id="894ed-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="894ed-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="894ed-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="894ed-134">Minimum supported server</span></span><br/> | <span data-ttu-id="894ed-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="894ed-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="894ed-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="894ed-136">Namespace</span></span><br/>                | <span data-ttu-id="894ed-137">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="894ed-137">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="894ed-138">MOF</span><span class="sxs-lookup"><span data-stu-id="894ed-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="894ed-139"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="894ed-139"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="894ed-140">DLL</span><span class="sxs-lookup"><span data-stu-id="894ed-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="894ed-141"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="894ed-141"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="894ed-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="894ed-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894ed-143">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="894ed-143">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

