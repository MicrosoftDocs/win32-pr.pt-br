---
title: Método DisableSerialPorts da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade SerialPortsDisabled.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisableSerialPorts
- Método DisableSerialPorts Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método DisableSerialPorts
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644378"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="fd9e8-106">Método DisableSerialPorts da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="fd9e8-106">DisableSerialPorts method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="fd9e8-107">Define a propriedade **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="fd9e8-107">Sets the **SerialPortsDisabled** property.</span></span> <span data-ttu-id="fd9e8-108">Se a propriedade **DeviceRedirectionType** tiver um valor de "2", a propriedade **SerialPortsDisabled** controlará o redirecionamento das portas seriais para sessões que são estabelecidas por meio do servidor gateway de área de trabalho remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="fd9e8-108">If the **DeviceRedirectionType** property has a value of "2", the **SerialPortsDisabled** property controls redirection of the serial ports for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9e8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd9e8-109">Syntax</span></span>


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="fd9e8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd9e8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd9e8-111">*Desabilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd9e8-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9e8-112">Novo valor para a propriedade **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="fd9e8-112">New value for the **SerialPortsDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd9e8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd9e8-113">Return value</span></span>

<span data-ttu-id="fd9e8-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fd9e8-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fd9e8-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fd9e8-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd9e8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd9e8-117">Remarks</span></span>

<span data-ttu-id="fd9e8-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fd9e8-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fd9e8-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fd9e8-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fd9e8-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fd9e8-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fd9e8-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd9e8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd9e8-123">Requirements</span></span>



| <span data-ttu-id="fd9e8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd9e8-124">Requirement</span></span> | <span data-ttu-id="fd9e8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fd9e8-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9e8-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd9e8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9e8-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fd9e8-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fd9e8-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd9e8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9e8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd9e8-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fd9e8-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd9e8-130">Namespace</span></span><br/>                | <span data-ttu-id="fd9e8-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="fd9e8-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fd9e8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fd9e8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd9e8-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd9e8-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd9e8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fd9e8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd9e8-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd9e8-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fd9e8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd9e8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9e8-137">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="fd9e8-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

