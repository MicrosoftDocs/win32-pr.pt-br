---
title: Método MoveDown da classe Win32_TSGatewayRADIUSServer
description: Move esse servidor de serviço RADIUS (RADIUS) uma posição para baixo na ordem de prioridade.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método MoveDown
- Método MoveDown Serviços de Área de Trabalho Remota, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Serviços de Área de Trabalho Remota, método MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b652eb5e9cfc36f0d41e14d9953b295d35e660be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499348"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="9954d-106">Método MoveDown da classe Win32 \_ TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="9954d-106">MoveDown method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="9954d-107">Move esse servidor de serviço RADIUS (RADIUS) uma posição para baixo na ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="9954d-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position down in the priority order.</span></span> <span data-ttu-id="9954d-108">Esse método incrementa a propriedade **Priority** do servidor RADIUS atual e decrementa a propriedade **Priority** do servidor RADIUS que segue o servidor RADIUS atual.</span><span class="sxs-lookup"><span data-stu-id="9954d-108">This method increments the **Priority** property of the current RADIUS server and decrements the **Priority** property of the RADIUS server that follows the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9954d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9954d-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="9954d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9954d-110">Parameters</span></span>

<span data-ttu-id="9954d-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9954d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9954d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9954d-112">Return value</span></span>

<span data-ttu-id="9954d-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="9954d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9954d-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9954d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9954d-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9954d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9954d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9954d-116">Remarks</span></span>

<span data-ttu-id="9954d-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="9954d-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9954d-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9954d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9954d-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9954d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9954d-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9954d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9954d-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9954d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9954d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9954d-122">Requirements</span></span>



| <span data-ttu-id="9954d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9954d-123">Requirement</span></span> | <span data-ttu-id="9954d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9954d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9954d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9954d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9954d-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9954d-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9954d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9954d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9954d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9954d-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9954d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9954d-129">Namespace</span></span><br/>                | <span data-ttu-id="9954d-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9954d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9954d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9954d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9954d-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9954d-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9954d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9954d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9954d-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9954d-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9954d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9954d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9954d-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="9954d-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

