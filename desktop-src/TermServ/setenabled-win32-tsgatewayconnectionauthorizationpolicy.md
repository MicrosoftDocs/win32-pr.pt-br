---
title: Método sethabilitado da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade Enabled, que habilita ou desabilita a atual política de autorização de conexão de Serviços de Área de Trabalho Remota (RD \ 160; CAP).
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método sethabilitado
- Método sethabilitado Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método sethabilitado
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6584e8916db2f8070def3904d0ece6ec0ee5ae34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499345"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="a5c94-106">Método sethabilitado da \_ classe Win32 TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="a5c94-106">SetEnabled method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="a5c94-107">Define a propriedade **Enabled** , que habilita ou desabilita a política de autorização de conexão serviços de área de trabalho remota atual (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="a5c94-107">Sets the **Enabled** property, which enables or disables the current Remote Desktop Services connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c94-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5c94-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="a5c94-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5c94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c94-110">*Habilitado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5c94-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5c94-111">**True** se o RD CAP for habilitado, **False** se o RD CAP for desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a5c94-111">**True** if the RD CAP is to be enabled, **False** if the RD CAP is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c94-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5c94-112">Return value</span></span>

<span data-ttu-id="a5c94-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a5c94-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a5c94-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a5c94-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a5c94-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a5c94-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c94-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5c94-116">Remarks</span></span>

<span data-ttu-id="a5c94-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="a5c94-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a5c94-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5c94-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5c94-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a5c94-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a5c94-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a5c94-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5c94-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a5c94-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c94-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5c94-122">Requirements</span></span>



| <span data-ttu-id="a5c94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c94-123">Requirement</span></span> | <span data-ttu-id="a5c94-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a5c94-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c94-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5c94-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c94-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5c94-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a5c94-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5c94-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c94-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5c94-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a5c94-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5c94-129">Namespace</span></span><br/>                | <span data-ttu-id="a5c94-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a5c94-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a5c94-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a5c94-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5c94-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5c94-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5c94-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a5c94-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5c94-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5c94-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a5c94-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5c94-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c94-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="a5c94-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

