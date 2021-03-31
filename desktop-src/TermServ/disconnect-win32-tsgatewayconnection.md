---
title: Método Disconnect da classe Win32_TSGatewayConnection
description: Desconecta a conexão do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 8c424e58-aa89-4ec6-acea-5b571d3f4c21
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de desconexão
- Método Disconnect Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnection
- Serviços de Área de Trabalho Remota de classe de Win32_TSGatewayConnection, método de desconexão
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.Disconnect
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53101e5ca3529c5033adc918f1f9ad11a3b45f7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644282"
---
# <a name="disconnect-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="71824-106">Método Disconnect da classe Win32 \_ TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="71824-106">Disconnect method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="71824-107">Desconecta a conexão do servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="71824-107">Disconnects the connection from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="71824-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71824-108">Syntax</span></span>


```mof
uint32 Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="71824-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71824-109">Parameters</span></span>

<span data-ttu-id="71824-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="71824-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71824-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71824-111">Return value</span></span>

<span data-ttu-id="71824-112">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="71824-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="71824-113">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="71824-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="71824-114">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="71824-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71824-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="71824-115">Remarks</span></span>

<span data-ttu-id="71824-116">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="71824-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="71824-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="71824-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="71824-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="71824-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="71824-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="71824-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="71824-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="71824-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="71824-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71824-121">Requirements</span></span>



| <span data-ttu-id="71824-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71824-122">Requirement</span></span> | <span data-ttu-id="71824-123">Valor</span><span class="sxs-lookup"><span data-stu-id="71824-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71824-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71824-124">Minimum supported client</span></span><br/> | <span data-ttu-id="71824-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="71824-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="71824-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71824-126">Minimum supported server</span></span><br/> | <span data-ttu-id="71824-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71824-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="71824-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="71824-128">Namespace</span></span><br/>                | <span data-ttu-id="71824-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="71824-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="71824-130">MOF</span><span class="sxs-lookup"><span data-stu-id="71824-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71824-131"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71824-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="71824-132">DLL</span><span class="sxs-lookup"><span data-stu-id="71824-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71824-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71824-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="71824-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="71824-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71824-135">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="71824-135">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

