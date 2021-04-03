---
title: Função RtmGetNetworkCount (RTM. h)
description: A função RtmGetNetworkCount recupera o número de redes para as quais o Gerenciador de tabela de roteamento tem rotas.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- Função RtmGetNetworkCount RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644627"
---
# <a name="rtmgetnetworkcount-function"></a><span data-ttu-id="220c9-104">Função RtmGetNetworkCount</span><span class="sxs-lookup"><span data-stu-id="220c9-104">RtmGetNetworkCount function</span></span>

<span data-ttu-id="220c9-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="220c9-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="220c9-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="220c9-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="220c9-107">A função **RtmGetNetworkCount** recupera o número de redes para as quais o Gerenciador de tabela de roteamento tem rotas.</span><span class="sxs-lookup"><span data-stu-id="220c9-107">The **RtmGetNetworkCount** function retrieves the number of networks to which the routing table manager has routes.</span></span>

## <a name="syntax"></a><span data-ttu-id="220c9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="220c9-108">Syntax</span></span>


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a><span data-ttu-id="220c9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="220c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="220c9-110">*ProtocolFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="220c9-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="220c9-111">Especifica para qual tipo de rede obter informações de rota, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="220c9-111">Specifies for which type of network to obtain route information, for example, IP or IPX.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="220c9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="220c9-112">Return value</span></span>

<span data-ttu-id="220c9-113">Se a função for realizada com sucesso, o valor de retorno será a contagem de rede, o número de redes conhecidas para os protocolos de roteamento da família de protocolos especificada.</span><span class="sxs-lookup"><span data-stu-id="220c9-113">If the function succeeds, the return value is the network count, the number of networks known to the routing protocols of the specified protocol family.</span></span>

<span data-ttu-id="220c9-114">Se o valor de retorno for zero, nenhuma rota estará disponível ou a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="220c9-114">If the return value is zero, either no routes are available, or the operation failed.</span></span> <span data-ttu-id="220c9-115">Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="220c9-115">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="220c9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="220c9-116">Value</span></span>                                                                                                    | <span data-ttu-id="220c9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="220c9-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="220c9-118"><dt>**SEM \_ erros**</dt></span><span class="sxs-lookup"><span data-stu-id="220c9-118"><dt>**NO\_ERROR**</dt></span></span> </dl>                 | <span data-ttu-id="220c9-119">A operação foi bem-sucedida, mas não há rotas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="220c9-119">The operation succeeded, but no routes are available.</span></span><br/>                                             |
| <dl> <span data-ttu-id="220c9-120"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="220c9-120"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="220c9-121">O valor do parâmetro *ProtocolFamily* não corresponde a nenhuma família de protocolos instalada.</span><span class="sxs-lookup"><span data-stu-id="220c9-121">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="220c9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="220c9-122">Requirements</span></span>



| <span data-ttu-id="220c9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="220c9-123">Requirement</span></span> | <span data-ttu-id="220c9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="220c9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="220c9-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="220c9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="220c9-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="220c9-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="220c9-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="220c9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="220c9-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="220c9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="220c9-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="220c9-129">End of server support</span></span><br/>    | <span data-ttu-id="220c9-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="220c9-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="220c9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="220c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="220c9-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="220c9-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="220c9-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="220c9-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="220c9-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="220c9-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="220c9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="220c9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="220c9-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="220c9-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="220c9-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="220c9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="220c9-138">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="220c9-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="220c9-139">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="220c9-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="220c9-140">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="220c9-140">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="220c9-141">Identificadores da família de protocolos RTMv1</span><span class="sxs-lookup"><span data-stu-id="220c9-141">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

