---
description: Recupera o status de NPP.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'Método IESP:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165350"
---
# <a name="iespquerystatus-method"></a><span data-ttu-id="99c4a-103">Método IESP:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="99c4a-103">IESP::QueryStatus method</span></span>

<span data-ttu-id="99c4a-104">O método **QueryStatus** recupera o status NPP.</span><span class="sxs-lookup"><span data-stu-id="99c4a-104">The **QueryStatus** method retrieves the NPP status.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99c4a-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="99c4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99c4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c4a-107">*pNetworkStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="99c4a-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99c4a-108">Um ponteiro para uma estrutura [NETWORKSTATUS](networkstatus.md) retornada que indica o estado atual (captura, pausa, parada e assim por diante) do NPP.</span><span class="sxs-lookup"><span data-stu-id="99c4a-108">A pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="99c4a-109">O usuário deve alocar e liberar a memória para a estrutura NETWORKSTATUS.</span><span class="sxs-lookup"><span data-stu-id="99c4a-109">The user must allocate and free the memory for the NETWORKSTATUS structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c4a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99c4a-110">Return value</span></span>

<span data-ttu-id="99c4a-111">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="99c4a-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="99c4a-112">Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:</span><span class="sxs-lookup"><span data-stu-id="99c4a-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="99c4a-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="99c4a-113">Return code</span></span>                                                                                              | <span data-ttu-id="99c4a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="99c4a-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99c4a-115"><dt>**NMERR \_ \_ parâmetro inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="99c4a-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="99c4a-116">O parâmetro *pNetworkStatus* não está apontando para uma estrutura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="99c4a-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="99c4a-117">Aloque memória para essa estrutura e chame **IESP:: QueryStatus** novamente.</span><span class="sxs-lookup"><span data-stu-id="99c4a-117">Allocate memory for this structure and call **IESP::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="99c4a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="99c4a-118">Remarks</span></span>

<span data-ttu-id="99c4a-119">Esse método pode ser chamado a qualquer momento após o [CreateNPPInterface](createnppinterface.md) ser chamado.</span><span class="sxs-lookup"><span data-stu-id="99c4a-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="99c4a-120">Você pode chamar esse método para ver se o NPP está conectado à rede, para descobrir o status da captura atual e para ver se há gatilhos pendentes.</span><span class="sxs-lookup"><span data-stu-id="99c4a-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="99c4a-121">Antes de chamar esse método, aloque a memória necessária para a estrutura [NETWORKSTATUS](networkstatus.md) e libere essa memória quando a estrutura não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="99c4a-121">Before calling this method, allocate the memory required for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer required.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c4a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99c4a-122">Requirements</span></span>



| <span data-ttu-id="99c4a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="99c4a-123">Requirement</span></span> | <span data-ttu-id="99c4a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="99c4a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c4a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99c4a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="99c4a-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99c4a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="99c4a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99c4a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="99c4a-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99c4a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="99c4a-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99c4a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="99c4a-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c4a-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="99c4a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="99c4a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99c4a-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c4a-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c4a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="99c4a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c4a-134">IESP</span><span class="sxs-lookup"><span data-stu-id="99c4a-134">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="99c4a-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="99c4a-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="99c4a-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="99c4a-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




