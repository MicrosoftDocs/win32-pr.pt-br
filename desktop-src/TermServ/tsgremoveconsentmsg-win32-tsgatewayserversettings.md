---
title: Método TSGRemoveConsentMsg da classe Win32_TSGatewayServerSettings
description: Remove a mensagem administrativa para o servidor de gateway. | Método TSGRemoveConsentMsg da classe Win32_TSGatewayServerSettings
ms.assetid: 626dc9ca-d6a1-48ab-84ec-cfccb8e720c2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método TSGRemoveConsentMsg
- Método TSGRemoveConsentMsg Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método TSGRemoveConsentMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24cd002ebb1a953d25cf129b4e5f3b4174842199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837856"
---
# <a name="tsgremoveconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="a4bda-107">Método TSGRemoveConsentMsg da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="a4bda-107">TSGRemoveConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="a4bda-108">Remove a mensagem administrativa para o servidor de gateway.</span><span class="sxs-lookup"><span data-stu-id="a4bda-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bda-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4bda-109">Syntax</span></span>


```mof
uint32 TSGRemoveConsentMsg();
```



## <a name="parameters"></a><span data-ttu-id="a4bda-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4bda-110">Parameters</span></span>

<span data-ttu-id="a4bda-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a4bda-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4bda-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4bda-112">Return value</span></span>

<span data-ttu-id="a4bda-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a4bda-113">Type: **uint32**</span></span>

<span data-ttu-id="a4bda-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a4bda-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a4bda-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a4bda-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a4bda-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a4bda-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4bda-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4bda-117">Remarks</span></span>

<span data-ttu-id="a4bda-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="a4bda-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a4bda-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a4bda-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4bda-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a4bda-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a4bda-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a4bda-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4bda-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a4bda-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bda-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4bda-123">Requirements</span></span>



| <span data-ttu-id="a4bda-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4bda-124">Requirement</span></span> | <span data-ttu-id="a4bda-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a4bda-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4bda-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4bda-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a4bda-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a4bda-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a4bda-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4bda-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a4bda-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4bda-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="a4bda-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4bda-130">Namespace</span></span><br/>                | <span data-ttu-id="a4bda-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a4bda-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a4bda-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a4bda-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4bda-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4bda-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4bda-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a4bda-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4bda-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4bda-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a4bda-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4bda-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4bda-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="a4bda-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

