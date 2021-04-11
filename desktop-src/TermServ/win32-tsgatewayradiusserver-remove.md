---
title: Método Remove da classe Win32_TSGatewayRADIUSServer
description: Remove o servidor atual de serviço RADIUS (RADIUS).
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Remover o método Serviços de Área de Trabalho Remota
- Método Remove Serviços de Área de Trabalho Remota, interface Win32_TSGatewayRADIUSServer
- Serviços de Área de Trabalho Remota de interface Win32_TSGatewayRADIUSServer, remover método
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a91fc4a3ba8bf638dcffd76e3bf3517795674fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295869"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="ee24a-106">Método Remove da classe Win32 \_ TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="ee24a-106">Remove method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="ee24a-107">Remove o servidor atual de serviço RADIUS (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="ee24a-107">Removes the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee24a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee24a-108">Syntax</span></span>


```mof
uint32 Remove();
```



## <a name="parameters"></a><span data-ttu-id="ee24a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee24a-109">Parameters</span></span>

<span data-ttu-id="ee24a-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ee24a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ee24a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee24a-111">Return value</span></span>

<span data-ttu-id="ee24a-112">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ee24a-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ee24a-113">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ee24a-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ee24a-114">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ee24a-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee24a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee24a-115">Remarks</span></span>

<span data-ttu-id="ee24a-116">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="ee24a-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ee24a-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ee24a-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ee24a-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ee24a-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ee24a-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="ee24a-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ee24a-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ee24a-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee24a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee24a-121">Requirements</span></span>



| <span data-ttu-id="ee24a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee24a-122">Requirement</span></span> | <span data-ttu-id="ee24a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ee24a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee24a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee24a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ee24a-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ee24a-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ee24a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee24a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ee24a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee24a-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ee24a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee24a-128">Namespace</span></span><br/>                | <span data-ttu-id="ee24a-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ee24a-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ee24a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ee24a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee24a-131"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee24a-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee24a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ee24a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee24a-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee24a-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ee24a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee24a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee24a-135">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="ee24a-135">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

