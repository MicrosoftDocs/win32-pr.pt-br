---
title: Método SetPasswordAllowed da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade PasswordAllowed, que habilita ou desabilita o suporte para usar uma senha para se conectar ao servidor de gateway de área de trabalho de Área de Trabalho Remota (Gateway RD).
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetPasswordAllowed
- Método SetPasswordAllowed Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetPasswordAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetPasswordAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8bda5fde2fd79cc02697fd270fc307ef5f410f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369870"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6606c-106">Método SetPasswordAllowed da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="6606c-106">SetPasswordAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6606c-107">Define a propriedade **PasswordAllowed** , que habilita ou desabilita o suporte para usar uma senha para se conectar ao servidor de gateway de área de trabalho de área de trabalho remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="6606c-107">Sets the **PasswordAllowed** property, which enables or disables support for using a password to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6606c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6606c-108">Syntax</span></span>


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="6606c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6606c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6606c-110">*Permitido* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6606c-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6606c-111">Novo valor de **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="6606c-111">New **PasswordAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6606c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6606c-112">Return value</span></span>

<span data-ttu-id="6606c-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="6606c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6606c-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6606c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6606c-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6606c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6606c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6606c-116">Remarks</span></span>

<span data-ttu-id="6606c-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="6606c-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6606c-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6606c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6606c-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6606c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6606c-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6606c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6606c-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6606c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6606c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6606c-122">Requirements</span></span>



| <span data-ttu-id="6606c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6606c-123">Requirement</span></span> | <span data-ttu-id="6606c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6606c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6606c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6606c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6606c-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6606c-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6606c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6606c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6606c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6606c-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6606c-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6606c-129">Namespace</span></span><br/>                | <span data-ttu-id="6606c-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6606c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6606c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6606c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6606c-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6606c-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6606c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6606c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6606c-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6606c-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6606c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6606c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6606c-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="6606c-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

