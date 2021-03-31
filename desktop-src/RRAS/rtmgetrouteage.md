---
title: Função RtmGetRouteAge (RTM. h)
description: A função RtmGetRouteAge retorna a idade de uma rota. A idade é o tempo, em segundos, desde que foi criada ou atualizada pela última vez.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- Função RtmGetRouteAge RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644820"
---
# <a name="rtmgetrouteage-function"></a><span data-ttu-id="beb4d-105">Função RtmGetRouteAge</span><span class="sxs-lookup"><span data-stu-id="beb4d-105">RtmGetRouteAge function</span></span>

<span data-ttu-id="beb4d-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="beb4d-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="beb4d-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="beb4d-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="beb4d-108">A função **RtmGetRouteAge** retorna a idade de uma rota.</span><span class="sxs-lookup"><span data-stu-id="beb4d-108">The **RtmGetRouteAge** function returns the age of a route.</span></span> <span data-ttu-id="beb4d-109">A idade é o tempo, em segundos, desde que foi criada ou atualizada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="beb4d-109">The age is the time, in seconds, since it was created or last updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb4d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="beb4d-110">Syntax</span></span>


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="beb4d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="beb4d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb4d-112">*Rota* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="beb4d-112">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb4d-113">Ponteiro para uma estrutura específica de família de protocolos que especifica os dados de rota obtidos recentemente do Gerenciador de tabelas de roteamento.</span><span class="sxs-lookup"><span data-stu-id="beb4d-113">Pointer to a protocol-family-specific structure that specifies route data recently obtained from the routing table manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb4d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="beb4d-114">Return value</span></span>

<span data-ttu-id="beb4d-115">O valor de retorno é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="beb4d-115">The return value is one of the following values.</span></span>



| <span data-ttu-id="beb4d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="beb4d-116">Value</span></span>                                                                                   | <span data-ttu-id="beb4d-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb4d-117">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="beb4d-118"><dt>**Rota**</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-118"><dt>**RouteAge**</dt></span></span> </dl> | <span data-ttu-id="beb4d-119">O tempo em segundos desde que uma rota foi criada ou atualizada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="beb4d-119">The time in seconds since a route was created or last updated.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="beb4d-120"><dt>**INFINITE**</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-120"><dt>**INFINITE**</dt></span></span> </dl> | <span data-ttu-id="beb4d-121">O conteúdo da estrutura de rota é inválido.</span><span class="sxs-lookup"><span data-stu-id="beb4d-121">The content of the route structure is invalid.</span></span> <span data-ttu-id="beb4d-122">Nesse caso, uma chamada para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna um \_ parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="beb4d-122">In this case, a call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_PARAMETER.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="beb4d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="beb4d-123">Remarks</span></span>

<span data-ttu-id="beb4d-124">A idade da rota é computada do \_ membro de carimbo de data/hora RR da estrutura que é apontada pelo parâmetro *Route* .</span><span class="sxs-lookup"><span data-stu-id="beb4d-124">The route age is computed from the RR\_TimeStamp member of the structure that is pointed to by the *Route* parameter.</span></span> <span data-ttu-id="beb4d-125">O Gerenciador de tabela de roteamento define o valor desse membro quando uma rota é adicionada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="beb4d-125">The routing table manager sets the value of this member when a route is added or updated.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb4d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb4d-126">Requirements</span></span>



| <span data-ttu-id="beb4d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb4d-127">Requirement</span></span> | <span data-ttu-id="beb4d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="beb4d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="beb4d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beb4d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="beb4d-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="beb4d-130">None supported</span></span><br/>                                                          |
| <span data-ttu-id="beb4d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beb4d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="beb4d-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="beb4d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="beb4d-133">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="beb4d-133">End of server support</span></span><br/>    | <span data-ttu-id="beb4d-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="beb4d-134">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="beb4d-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="beb4d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="beb4d-136"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-136"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="beb4d-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="beb4d-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="beb4d-138"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-138"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="beb4d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="beb4d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beb4d-140"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-140"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb4d-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="beb4d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb4d-142">Referência da versão 1 do Gerenciador de tabela de roteamento \_</span><span class="sxs-lookup"><span data-stu-id="beb4d-142">Routing Table Manager Version\_1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="beb4d-143">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="beb4d-143">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="beb4d-144">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="beb4d-144">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="beb4d-145">**\_rota de IP RTM \_**</span><span class="sxs-lookup"><span data-stu-id="beb4d-145">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="beb4d-146">**\_rota IPX do RTM \_**</span><span class="sxs-lookup"><span data-stu-id="beb4d-146">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

