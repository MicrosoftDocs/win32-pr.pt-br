---
title: Método MoveUp da classe Win32_TSGatewayRADIUSServer
description: Move esse servidor de serviço RADIUS (RADIUS) uma posição para cima na ordem de prioridade.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método MoveUp
- Método MoveUp Serviços de Área de Trabalho Remota, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Serviços de Área de Trabalho Remota, método MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499758"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="c5e21-106">Método MoveUp da classe Win32 \_ TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="c5e21-106">MoveUp method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="c5e21-107">Move esse servidor de serviço RADIUS (RADIUS) uma posição para cima na ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="c5e21-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position up in the priority order.</span></span> <span data-ttu-id="c5e21-108">Esse método diminui a propriedade **Priority** do servidor RADIUS atual e incrementa a propriedade **Priority** do servidor RADIUS que precede o servidor RADIUS atual.</span><span class="sxs-lookup"><span data-stu-id="c5e21-108">This method decrements the **Priority** property of the current RADIUS server and increments the **Priority** property of the RADIUS server that precedes the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e21-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5e21-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="c5e21-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5e21-110">Parameters</span></span>

<span data-ttu-id="c5e21-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c5e21-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5e21-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5e21-112">Return value</span></span>

<span data-ttu-id="c5e21-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="c5e21-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c5e21-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c5e21-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c5e21-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c5e21-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5e21-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5e21-116">Remarks</span></span>

<span data-ttu-id="c5e21-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="c5e21-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c5e21-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c5e21-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c5e21-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c5e21-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c5e21-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c5e21-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c5e21-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c5e21-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e21-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e21-122">Requirements</span></span>



| <span data-ttu-id="c5e21-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e21-123">Requirement</span></span> | <span data-ttu-id="c5e21-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c5e21-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e21-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5e21-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e21-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c5e21-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c5e21-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5e21-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e21-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5e21-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c5e21-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5e21-129">Namespace</span></span><br/>                | <span data-ttu-id="c5e21-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c5e21-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c5e21-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c5e21-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5e21-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5e21-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5e21-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c5e21-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5e21-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5e21-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c5e21-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5e21-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e21-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c5e21-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

