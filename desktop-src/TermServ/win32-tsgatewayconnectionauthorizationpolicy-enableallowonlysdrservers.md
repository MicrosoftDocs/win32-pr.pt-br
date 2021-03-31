---
title: Método EnableAllowOnlySDRServers da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Usado para alternar a propriedade AllowOnlySDRServers.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableAllowOnlySDRServers
- Método EnableAllowOnlySDRServers Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método EnableAllowOnlySDRServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644588"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="3ed30-106">Método EnableAllowOnlySDRServers da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="3ed30-106">EnableAllowOnlySDRServers method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="3ed30-107">Usado para alternar a propriedade **AllowOnlySDRServers** .</span><span class="sxs-lookup"><span data-stu-id="3ed30-107">Used to toggle the **AllowOnlySDRServers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed30-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ed30-108">Syntax</span></span>


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a><span data-ttu-id="3ed30-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ed30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed30-110">*AllowOnlySDRServers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ed30-110">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed30-111">Se definido como **true**, as conexões serão permitidas somente para proteger os servidores RDS do redirecionamento de dispositivo (SDR).</span><span class="sxs-lookup"><span data-stu-id="3ed30-111">If set to **True**, connections will be allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="3ed30-112">Se definido como **false**, as conexões serão permitidas a servidores RDS mais antigos também</span><span class="sxs-lookup"><span data-stu-id="3ed30-112">If set to **False**, connections will be allowed to older RDS servers also</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed30-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ed30-113">Return value</span></span>

<span data-ttu-id="3ed30-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="3ed30-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3ed30-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3ed30-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3ed30-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3ed30-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed30-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ed30-117">Requirements</span></span>



| <span data-ttu-id="3ed30-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed30-118">Requirement</span></span> | <span data-ttu-id="3ed30-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed30-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed30-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed30-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3ed30-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3ed30-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed30-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3ed30-123">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="3ed30-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ed30-124">Namespace</span></span><br/>                | <span data-ttu-id="3ed30-125">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="3ed30-125">ROOT\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3ed30-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3ed30-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ed30-127"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ed30-127"><dt>TsGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ed30-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3ed30-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed30-129"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ed30-129"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3ed30-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3ed30-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed30-131">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="3ed30-131">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





