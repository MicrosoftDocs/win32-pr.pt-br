---
title: Método MoveUp da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Move a política de autorização de conexão do Área de Trabalho Remota atual (RD \ 160; CAP) uma posição acima na ordem em que RD \ 160; As CAPs são avaliadas.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método MoveUp
- Método MoveUp Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81973261d156328aa1f306c26dd8bd9bdd20511f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455939"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="79e95-106">Método MoveUp da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="79e95-106">MoveUp method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="79e95-107">Move a Área de Trabalho Remota atual da política de autorização de conexão (RD CAP) para cima na ordem em que as RD CAPs são avaliadas.</span><span class="sxs-lookup"><span data-stu-id="79e95-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position up in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="79e95-108">Esse método decrementa a propriedade **Order** da RD CAP atual e incrementa a propriedade **Order** do RD CAP que precedeu a RD CAP atual.</span><span class="sxs-lookup"><span data-stu-id="79e95-108">This method decrements the **Order** property of the current RD CAP and increments the **Order** property of the RD CAP that preceded the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e95-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79e95-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="79e95-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79e95-110">Parameters</span></span>

<span data-ttu-id="79e95-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="79e95-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79e95-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79e95-112">Return value</span></span>

<span data-ttu-id="79e95-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="79e95-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="79e95-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="79e95-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="79e95-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="79e95-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79e95-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="79e95-116">Remarks</span></span>

<span data-ttu-id="79e95-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="79e95-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="79e95-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="79e95-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="79e95-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="79e95-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="79e95-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="79e95-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="79e95-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="79e95-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="79e95-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79e95-122">Requirements</span></span>



| <span data-ttu-id="79e95-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e95-123">Requirement</span></span> | <span data-ttu-id="79e95-124">Valor</span><span class="sxs-lookup"><span data-stu-id="79e95-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e95-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e95-125">Minimum supported client</span></span><br/> | <span data-ttu-id="79e95-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="79e95-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="79e95-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e95-127">Minimum supported server</span></span><br/> | <span data-ttu-id="79e95-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79e95-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="79e95-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="79e95-129">Namespace</span></span><br/>                | <span data-ttu-id="79e95-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="79e95-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="79e95-131">MOF</span><span class="sxs-lookup"><span data-stu-id="79e95-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79e95-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79e95-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="79e95-133">DLL</span><span class="sxs-lookup"><span data-stu-id="79e95-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e95-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e95-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="79e95-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="79e95-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e95-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="79e95-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="79e95-137">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="79e95-137">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

