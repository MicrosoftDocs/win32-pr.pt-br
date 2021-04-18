---
title: Constantes de tempo limite de associação (rpcdce. h)
description: A Biblioteca RPC usa as constantes de tempo limite de associação para especificar a quantidade de tempo relativa que deve ser gasta para estabelecer uma associação ao servidor antes de desistir.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105785392"
---
# <a name="binding-time-out-constants"></a><span data-ttu-id="a1ec3-103">Constantes de tempo limite de associação</span><span class="sxs-lookup"><span data-stu-id="a1ec3-103">Binding Time-out Constants</span></span>

<span data-ttu-id="a1ec3-104">A Biblioteca RPC usa as constantes de tempo limite de associação para especificar a quantidade de tempo relativa que deve ser gasta para estabelecer uma associação ao servidor antes de desistir.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-104">The RPC library uses the binding time-out constants to specify the relative amount of time that should be spent to establish a binding to the server before giving up.</span></span> <span data-ttu-id="a1ec3-105">O tempo limite pode ser habilitado com uma chamada para a função [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) .</span><span class="sxs-lookup"><span data-stu-id="a1ec3-105">The timeout can be enabled with a call to the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function.</span></span> <span data-ttu-id="a1ec3-106">A lista a seguir contém os valores de tempo limite válidos.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-106">The following list contains the valid time-out values.</span></span>



| <span data-ttu-id="a1ec3-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="a1ec3-107">Constant/value</span></span>                                                                                                                                                                                                                                                                | <span data-ttu-id="a1ec3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1ec3-108">Description</span></span>                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <span data-ttu-id="a1ec3-109"><dt>**RPC \_ \_ \_ \_ Tempo limite infinito de associação C**</dt> <dt> 10</dt></span><span class="sxs-lookup"><span data-stu-id="a1ec3-109"><dt>**RPC\_C\_BINDING\_INFINITE\_TIMEOUT**</dt> <dt> 10 </dt></span></span> </dl> | <span data-ttu-id="a1ec3-110">Continua tentando estabelecer comunicações para sempre.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-110">Keeps trying to establish communications forever.</span></span><br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <span data-ttu-id="a1ec3-111"><dt>**RPC \_ \_ \_ \_ Tempo limite mínimo de associação de C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a1ec3-111"><dt>**RPC\_C\_BINDING\_MIN\_TIMEOUT**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="a1ec3-112">Tenta a quantidade mínima de tempo para o protocolo de rede que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-112">Tries the minimum amount of time for the network protocol being used.</span></span> <span data-ttu-id="a1ec3-113">Esse valor favorece o tempo de resposta em relação à exatidão para determinar se o servidor está em execução.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-113">This value favors response time over correctness in determining whether the server is running.</span></span><br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <span data-ttu-id="a1ec3-114"><dt>**RPC \_ \_ \_ \_ Tempo limite padrão de associação C**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a1ec3-114"><dt>**RPC\_C\_BINDING\_DEFAULT\_TIMEOUT**</dt> <dt>5</dt></span></span> </dl>       | <span data-ttu-id="a1ec3-115">Tenta uma quantidade média de tempo para o protocolo de rede ser usado.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-115">Tries an average amount of time for the network protocol being used.</span></span> <span data-ttu-id="a1ec3-116">Esse valor fornece a exatidão para determinar se um servidor está em execução e dá um tempo de resposta igual a peso.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-116">This value gives correctness in determining whether a server is running and gives response time equal weight.</span></span> <span data-ttu-id="a1ec3-117">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-117">This is the default value.</span></span><br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <span data-ttu-id="a1ec3-118"><dt>**RPC \_ \_ \_ \_ Tempo limite máximo de associação de C**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a1ec3-118"><dt>**RPC\_C\_BINDING\_MAX\_TIMEOUT**</dt> <dt>9</dt></span></span> </dl>                   | <span data-ttu-id="a1ec3-119">Tenta a quantidade mais longa de tempo para o protocolo de rede que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-119">Tries the longest amount of time for the network protocol being used.</span></span> <span data-ttu-id="a1ec3-120">Esse valor favorece a exatidão para determinar se um servidor está sendo executado no tempo de resposta.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-120">This value favors correctness in determining whether a server is running over response time.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="a1ec3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1ec3-121">Remarks</span></span>

<span data-ttu-id="a1ec3-122">Os valores na tabela anterior não estão em segundos.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-122">The values in the preceding table are not in seconds.</span></span> <span data-ttu-id="a1ec3-123">Esses valores representam uma quantidade relativa de tempo em uma escala de zero a 10.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-123">These values represent a relative amount of time on a scale of zero to 10.</span></span> <span data-ttu-id="a1ec3-124">Para obter mais informações sobre como evitar atrasos de comunicação, consulte impedindo os bloqueios do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="a1ec3-124">For more information on avoiding communication delays, refer to Preventing Client-side Hangs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1ec3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1ec3-125">Requirements</span></span>



| <span data-ttu-id="a1ec3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1ec3-126">Requirement</span></span> | <span data-ttu-id="a1ec3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a1ec3-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ec3-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1ec3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a1ec3-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1ec3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a1ec3-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1ec3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a1ec3-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1ec3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a1ec3-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a1ec3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1ec3-133"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1ec3-133"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





