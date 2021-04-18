---
title: Método IsLoadBalancingServer da classe Win32_TSGatewayLoadBalancer
description: Determina se o servidor de gateway de área de trabalho de Área de Trabalho Remota (Gateway RD) pode executar o balanceamento de carga.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsLoadBalancingServer
- Método IsLoadBalancingServer Serviços de Área de Trabalho Remota, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Serviços de Área de Trabalho Remota, método IsLoadBalancingServer
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105799998"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="011cf-106">Método IsLoadBalancingServer da classe Win32 \_ TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="011cf-106">IsLoadBalancingServer method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="011cf-107">Determina se o servidor de gateway de área de trabalho de Área de Trabalho Remota (Gateway RD) pode executar o balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="011cf-107">Determines whether the Remote Desktop Gateway (RD Gateway) server can perform load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="011cf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="011cf-108">Syntax</span></span>


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a><span data-ttu-id="011cf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="011cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="011cf-110">*Balanceamento de carga* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="011cf-110">*LoadBalancing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="011cf-111">**True** se o servidor puder executar o balanceamento de carga e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="011cf-111">**TRUE** if the server can perform load balancing, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="011cf-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="011cf-112">Return value</span></span>

<span data-ttu-id="011cf-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="011cf-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="011cf-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="011cf-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="011cf-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="011cf-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="011cf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="011cf-116">Remarks</span></span>

<span data-ttu-id="011cf-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="011cf-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="011cf-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="011cf-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="011cf-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="011cf-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="011cf-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="011cf-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="011cf-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="011cf-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="011cf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="011cf-122">Requirements</span></span>



| <span data-ttu-id="011cf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="011cf-123">Requirement</span></span> | <span data-ttu-id="011cf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="011cf-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="011cf-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="011cf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="011cf-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="011cf-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="011cf-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="011cf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="011cf-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="011cf-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="011cf-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="011cf-129">Namespace</span></span><br/>                | <span data-ttu-id="011cf-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="011cf-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="011cf-131">MOF</span><span class="sxs-lookup"><span data-stu-id="011cf-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="011cf-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="011cf-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="011cf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="011cf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="011cf-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="011cf-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="011cf-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="011cf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011cf-136">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="011cf-136">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

