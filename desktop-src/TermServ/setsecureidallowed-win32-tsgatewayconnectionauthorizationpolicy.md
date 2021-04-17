---
title: Método SetSecureIdAllowed da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Este método está reservado para uso futuro.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSecureIdAllowed
- Método SetSecureIdAllowed Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetSecureIdAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e61c158a7dfcafb6d1d5ac66833e42284b818d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813025"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="47cb0-106">Método SetSecureIdAllowed da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="47cb0-106">SetSecureIdAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="47cb0-107">Este método está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="47cb0-107">This method is reserved for future use.</span></span>

<span data-ttu-id="47cb0-108">Define a propriedade **SecureIdAllowed** , que é reservada para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="47cb0-108">Sets the **SecureIdAllowed** property, which is reserved for future use.</span></span>

## <a name="syntax"></a><span data-ttu-id="47cb0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47cb0-109">Syntax</span></span>


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="47cb0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47cb0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47cb0-111">*Permitido* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47cb0-111">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47cb0-112">Novo valor de **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="47cb0-112">New **SecureIdAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47cb0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47cb0-113">Return value</span></span>

<span data-ttu-id="47cb0-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="47cb0-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="47cb0-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="47cb0-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="47cb0-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="47cb0-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="47cb0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="47cb0-117">Remarks</span></span>

<span data-ttu-id="47cb0-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="47cb0-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="47cb0-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="47cb0-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="47cb0-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="47cb0-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="47cb0-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="47cb0-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="47cb0-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="47cb0-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="47cb0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47cb0-123">Requirements</span></span>



| <span data-ttu-id="47cb0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="47cb0-124">Requirement</span></span> | <span data-ttu-id="47cb0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="47cb0-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47cb0-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47cb0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="47cb0-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="47cb0-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="47cb0-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47cb0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="47cb0-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47cb0-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="47cb0-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="47cb0-130">Namespace</span></span><br/>                | <span data-ttu-id="47cb0-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="47cb0-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="47cb0-132">MOF</span><span class="sxs-lookup"><span data-stu-id="47cb0-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47cb0-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47cb0-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="47cb0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="47cb0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47cb0-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47cb0-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="47cb0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="47cb0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47cb0-137">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="47cb0-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

