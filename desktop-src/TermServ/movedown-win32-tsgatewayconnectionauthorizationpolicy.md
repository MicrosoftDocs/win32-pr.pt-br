---
title: Método MoveDown da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Move a política de autorização de conexão do Área de Trabalho Remota atual (RD \ 160; CAP) uma posição para baixo na ordem em que RD \ 160; As CAPs são avaliadas.
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método MoveDown
- Método MoveDown Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e5b2e2b56a60d78f827f8989c0317cb003e511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766945"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0a8f2-106">Método MoveDown da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="0a8f2-106">MoveDown method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0a8f2-107">Move a Área de Trabalho Remota atual da política de autorização de conexão (RD CAP) uma posição para baixo na ordem em que as RD CAPs são avaliadas.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position down in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="0a8f2-108">Esse método incrementa a propriedade **Order** da RD CAP atual e decrementa a propriedade **Order** do RD CAP que seguiu a RD CAP atual.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-108">This method increments the **Order** property of the current RD CAP and decrements the **Order** property of the RD CAP that followed the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a8f2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a8f2-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="0a8f2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a8f2-110">Parameters</span></span>

<span data-ttu-id="0a8f2-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a8f2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a8f2-112">Return value</span></span>

<span data-ttu-id="0a8f2-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0a8f2-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0a8f2-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0a8f2-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a8f2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a8f2-116">Remarks</span></span>

<span data-ttu-id="0a8f2-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0a8f2-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0a8f2-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0a8f2-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0a8f2-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0a8f2-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0a8f2-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0a8f2-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a8f2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a8f2-122">Requirements</span></span>



| <span data-ttu-id="0a8f2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a8f2-123">Requirement</span></span> | <span data-ttu-id="0a8f2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0a8f2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a8f2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a8f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0a8f2-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0a8f2-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0a8f2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a8f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0a8f2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a8f2-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0a8f2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a8f2-129">Namespace</span></span><br/>                | <span data-ttu-id="0a8f2-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="0a8f2-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0a8f2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0a8f2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a8f2-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a8f2-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a8f2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0a8f2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a8f2-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a8f2-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0a8f2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a8f2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a8f2-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="0a8f2-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="0a8f2-137">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="0a8f2-137">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

