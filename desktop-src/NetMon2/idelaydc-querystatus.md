---
description: 'Método IDelaydC:: QueryStatus – o método QueryStatus recupera o status do NPP.'
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'Método IDelaydC:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 13d1e34b57302d263b81ed64df0b136dc01177b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118454"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="6effa-103">Método IDelaydC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="6effa-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="6effa-104">O método **QueryStatus** recupera o status do NPP.</span><span class="sxs-lookup"><span data-stu-id="6effa-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="6effa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6effa-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="6effa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6effa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6effa-107">*pNetworkStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6effa-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6effa-108">Ponteiro para uma estrutura [NETWORKSTATUS](networkstatus.md) retornada que indica o estado atual (captura, pausa, parada e assim por diante) do NPP.</span><span class="sxs-lookup"><span data-stu-id="6effa-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="6effa-109">É sua responsabilidade alocar e liberar a memória associada à estrutura **NETWORKSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="6effa-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6effa-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6effa-110">Return value</span></span>

<span data-ttu-id="6effa-111">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="6effa-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6effa-112">Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:</span><span class="sxs-lookup"><span data-stu-id="6effa-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="6effa-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6effa-113">Return code</span></span>                                                                                              | <span data-ttu-id="6effa-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6effa-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6effa-115"><dt>**NMERR \_ \_ parâmetro inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="6effa-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="6effa-116">O parâmetro *pNetworkStatus* não está apontando para uma estrutura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="6effa-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="6effa-117">Aloque memória para essa estrutura e chame o método **IDelaydC:: QueryStatus** novamente.</span><span class="sxs-lookup"><span data-stu-id="6effa-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6effa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6effa-118">Remarks</span></span>

<span data-ttu-id="6effa-119">Esse método pode ser chamado a qualquer momento depois que [CreateNPPInterface](createnppinterface.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="6effa-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="6effa-120">Ele pode ser chamado para ver se o NPP está conectado à rede, para descobrir o status da captura atual e para ver se há gatilhos pendentes.</span><span class="sxs-lookup"><span data-stu-id="6effa-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="6effa-121">Antes de chamar esse método, você deve alocar a memória necessária para a estrutura [NETWORKSTATUS](networkstatus.md) e liberar essa memória quando a estrutura não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="6effa-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6effa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6effa-122">Requirements</span></span>



| <span data-ttu-id="6effa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6effa-123">Requirement</span></span> | <span data-ttu-id="6effa-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6effa-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6effa-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6effa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6effa-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6effa-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6effa-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6effa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6effa-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6effa-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6effa-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6effa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6effa-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6effa-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6effa-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6effa-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6effa-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6effa-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6effa-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6effa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6effa-134">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="6effa-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="6effa-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="6effa-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="6effa-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="6effa-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




