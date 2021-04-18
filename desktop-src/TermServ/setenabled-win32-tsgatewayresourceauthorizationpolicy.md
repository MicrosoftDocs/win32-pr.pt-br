---
title: Método sethabilitado da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Habilita ou desabilita a política de autorização de recursos de Área de Trabalho Remota (RD \ 160; RAP) definindo a propriedade Enabled.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método sethabilitado
- Método sethabilitado Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método sethabilitado
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455861"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="adc38-106">Método sethabilitado da \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="adc38-106">SetEnabled method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="adc38-107">Habilita ou desabilita a RD RAP (política de autorização de recursos) de Área de Trabalho Remota definindo a propriedade **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="adc38-107">Enables or disables the Remote Desktop resource authorization policy (RD RAP) by setting the **Enabled** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc38-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adc38-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="adc38-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adc38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc38-110">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adc38-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adc38-111">Se **for true**, a RD RAP será habilitada.</span><span class="sxs-lookup"><span data-stu-id="adc38-111">If **True**, the RD RAP will be enabled.</span></span> <span data-ttu-id="adc38-112">Se **for false**, a RD RAP será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="adc38-112">If **False**, the RD RAP will be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc38-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="adc38-113">Return value</span></span>

<span data-ttu-id="adc38-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="adc38-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="adc38-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="adc38-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="adc38-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="adc38-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="adc38-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="adc38-117">Remarks</span></span>

<span data-ttu-id="adc38-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="adc38-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="adc38-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="adc38-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="adc38-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="adc38-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="adc38-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="adc38-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="adc38-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="adc38-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="adc38-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adc38-123">Requirements</span></span>



| <span data-ttu-id="adc38-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="adc38-124">Requirement</span></span> | <span data-ttu-id="adc38-125">Valor</span><span class="sxs-lookup"><span data-stu-id="adc38-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="adc38-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adc38-126">Minimum supported client</span></span><br/> | <span data-ttu-id="adc38-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="adc38-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="adc38-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adc38-128">Minimum supported server</span></span><br/> | <span data-ttu-id="adc38-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adc38-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="adc38-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="adc38-130">Namespace</span></span><br/>                | <span data-ttu-id="adc38-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="adc38-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="adc38-132">MOF</span><span class="sxs-lookup"><span data-stu-id="adc38-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adc38-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="adc38-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="adc38-134">DLL</span><span class="sxs-lookup"><span data-stu-id="adc38-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adc38-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adc38-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="adc38-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="adc38-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc38-137">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="adc38-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

