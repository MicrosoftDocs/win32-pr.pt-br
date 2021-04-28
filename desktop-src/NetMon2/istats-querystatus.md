---
description: 'Método IStats:: QueryStatus – o método QueryStatus recupera o status do NPP.'
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: 'Método IStats:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7587c2fff56d305c0298948bdf8690fd801f3f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113474"
---
# <a name="istatsquerystatus-method"></a><span data-ttu-id="b0de2-103">Método IStats:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="b0de2-103">IStats::QueryStatus method</span></span>

<span data-ttu-id="b0de2-104">O método **QueryStatus** recupera o status do NPP.</span><span class="sxs-lookup"><span data-stu-id="b0de2-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0de2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0de2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="b0de2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0de2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0de2-107">*pNetworkStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0de2-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0de2-108">Ponteiro para uma estrutura [NETWORKSTATUS](networkstatus.md) retornada que indica o estado atual (captura, pausa, parada e assim por diante) do NPP.</span><span class="sxs-lookup"><span data-stu-id="b0de2-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="b0de2-109">É responsabilidade do aplicativo alocar e liberar a memória para a estrutura **NETWORKSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="b0de2-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0de2-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b0de2-110">Return value</span></span>

<span data-ttu-id="b0de2-111">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="b0de2-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b0de2-112">Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:</span><span class="sxs-lookup"><span data-stu-id="b0de2-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="b0de2-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b0de2-113">Return code</span></span>                                                                                              | <span data-ttu-id="b0de2-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0de2-114">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0de2-115"><dt>**NMERR \_ \_ parâmetro inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="b0de2-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="b0de2-116">O parâmetro *pNetworkStatus* não está apontando para uma estrutura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="b0de2-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="b0de2-117">Aloque memória para essa estrutura e chame o método **IStats:: QueryStatus** novamente.</span><span class="sxs-lookup"><span data-stu-id="b0de2-117">Allocate memory for this structure and call the **IStats::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0de2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0de2-118">Remarks</span></span>

<span data-ttu-id="b0de2-119">Esse método pode ser chamado a qualquer momento depois que o método [CreateNPPInterface](createnppinterface.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="b0de2-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="b0de2-120">Ele pode ser chamado para ver se o NPP está conectado à rede, para descobrir o status da captura atual e para ver se há gatilhos pendentes.</span><span class="sxs-lookup"><span data-stu-id="b0de2-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="b0de2-121">No entanto, antes de chamar esse método, você deve alocar a memória necessária para a estrutura [NETWORKSTATUS](networkstatus.md) e liberar essa memória quando a estrutura não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="b0de2-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0de2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0de2-122">Requirements</span></span>



| <span data-ttu-id="b0de2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0de2-123">Requirement</span></span> | <span data-ttu-id="b0de2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b0de2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0de2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0de2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b0de2-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0de2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b0de2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0de2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b0de2-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0de2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b0de2-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b0de2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0de2-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0de2-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b0de2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b0de2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0de2-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0de2-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0de2-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b0de2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0de2-134">IStats</span><span class="sxs-lookup"><span data-stu-id="b0de2-134">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="b0de2-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="b0de2-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="b0de2-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="b0de2-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




