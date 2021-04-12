---
title: Método DeleteAllServers da classe Win32_TSGatewayLoadBalancer
description: Exclui todos os servidores de balanceamento de carga de Área de Trabalho Remota gateway (gateway de área de trabalho remota) que participam do farm de balanceamento de carga.
ms.assetid: 091ed866-8f2b-47b8-990b-e9a6d7e1194c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteAllServers
- Método DeleteAllServers Serviços de Área de Trabalho Remota, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Serviços de Área de Trabalho Remota, método DeleteAllServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteAllServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8004b4cfe811394acb328938775fcc9947bbbd19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499266"
---
# <a name="deleteallservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="baa82-106">Método DeleteAllServers da classe Win32 \_ TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="baa82-106">DeleteAllServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="baa82-107">Exclui todos os servidores de balanceamento de carga de Área de Trabalho Remota gateway (gateway de área de trabalho remota) que participam do farm de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="baa82-107">Deletes all Remote Desktop Gateway (RD Gateway) load-balancing servers that are participating in the load-balancing farm.</span></span>

## <a name="syntax"></a><span data-ttu-id="baa82-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="baa82-108">Syntax</span></span>


```mof
uint32 DeleteAllServers();
```



## <a name="parameters"></a><span data-ttu-id="baa82-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baa82-109">Parameters</span></span>

<span data-ttu-id="baa82-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="baa82-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="baa82-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="baa82-111">Return value</span></span>

<span data-ttu-id="baa82-112">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="baa82-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="baa82-113">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="baa82-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="baa82-114">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="baa82-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="baa82-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="baa82-115">Remarks</span></span>

<span data-ttu-id="baa82-116">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="baa82-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="baa82-117">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="baa82-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="baa82-118">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="baa82-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="baa82-119">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="baa82-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="baa82-120">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="baa82-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="baa82-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baa82-121">Requirements</span></span>



| <span data-ttu-id="baa82-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="baa82-122">Requirement</span></span> | <span data-ttu-id="baa82-123">Valor</span><span class="sxs-lookup"><span data-stu-id="baa82-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="baa82-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baa82-124">Minimum supported client</span></span><br/> | <span data-ttu-id="baa82-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="baa82-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="baa82-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baa82-126">Minimum supported server</span></span><br/> | <span data-ttu-id="baa82-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baa82-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="baa82-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="baa82-128">Namespace</span></span><br/>                | <span data-ttu-id="baa82-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="baa82-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="baa82-130">MOF</span><span class="sxs-lookup"><span data-stu-id="baa82-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="baa82-131"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="baa82-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="baa82-132">DLL</span><span class="sxs-lookup"><span data-stu-id="baa82-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baa82-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baa82-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="baa82-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="baa82-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa82-135">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="baa82-135">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

