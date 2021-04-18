---
title: IDXCoreAdapter::QueryState
description: Recupera o estado atual do item especificado no adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105795484"
---
# <a name="idxcoreadapterquerystate-method"></a><span data-ttu-id="a0be9-103">Método IDXCoreAdapter:: QueryState</span><span class="sxs-lookup"><span data-stu-id="a0be9-103">IDXCoreAdapter::QueryState method</span></span>

<span data-ttu-id="a0be9-104">Recupera o estado atual do item especificado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="a0be9-104">Retrieves the current state of the specified item on the adapter.</span></span> <span data-ttu-id="a0be9-105">Antes de chamar **QueryState** para um tipo de propriedade, chame [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e so (sistema operacional).</span><span class="sxs-lookup"><span data-stu-id="a0be9-105">Before calling **QueryState** for a property type, call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0be9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0be9-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a><span data-ttu-id="a0be9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0be9-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="a0be9-108">state</span><span class="sxs-lookup"><span data-stu-id="a0be9-108">state</span></span>

<span data-ttu-id="a0be9-109">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="a0be9-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="a0be9-110">O tipo de item de estado no adaptador cujo estado você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="a0be9-110">The kind of state item on the adapter whose state you wish to retrieve.</span></span> <span data-ttu-id="a0be9-111">Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador.</span><span class="sxs-lookup"><span data-stu-id="a0be9-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="a0be9-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="a0be9-112">inputStateDetailsSize</span></span>

<span data-ttu-id="a0be9-113">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="a0be9-113">Type: **size_t**</span></span>

<span data-ttu-id="a0be9-114">O tamanho, em bytes, do buffer de detalhes de estado de entrada que você (opcionalmente) aloca e fornece em *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="a0be9-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="a0be9-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="a0be9-115">inputStateDetails [in]</span></span>

<span data-ttu-id="a0be9-116">Tipo: **void const \***</span><span class="sxs-lookup"><span data-stu-id="a0be9-116">Type: **void const\***</span></span>

<span data-ttu-id="a0be9-117">Um ponteiro opcional para um buffer de detalhes de estado de entrada constante que você aloca em seu aplicativo, contendo qualquer informação sobre a solicitação necessária para o tipo de estado que você especificar no *estado*.</span><span class="sxs-lookup"><span data-stu-id="a0be9-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="a0be9-118">Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre qualquer requisito de buffer de entrada para um determinado tipo de estado.</span><span class="sxs-lookup"><span data-stu-id="a0be9-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="outputbuffersize"></a><span data-ttu-id="a0be9-119">outputBufferSize</span><span class="sxs-lookup"><span data-stu-id="a0be9-119">outputBufferSize</span></span>

<span data-ttu-id="a0be9-120">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="a0be9-120">Type: **size_t**</span></span>

<span data-ttu-id="a0be9-121">O tamanho, em bytes, do buffer de saída que você aloca e fornece em *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="a0be9-121">The size, in bytes, of the output buffer that you allocate and provide in *outputBuffer*.</span></span>

### <a name="outputbuffer-out"></a><span data-ttu-id="a0be9-122">outputBuffer [saída]</span><span class="sxs-lookup"><span data-stu-id="a0be9-122">outputBuffer [out]</span></span>

<span data-ttu-id="a0be9-123">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="a0be9-123">Type: **void\***</span></span>

<span data-ttu-id="a0be9-124">Um ponteiro para um buffer de saída que você aloca em seu aplicativo e que a função preenche.</span><span class="sxs-lookup"><span data-stu-id="a0be9-124">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="a0be9-125">Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre o requisito de buffer de saída para um determinado tipo de estado.</span><span class="sxs-lookup"><span data-stu-id="a0be9-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the output buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="a0be9-126">Retornos</span><span class="sxs-lookup"><span data-stu-id="a0be9-126">Returns</span></span>

<span data-ttu-id="a0be9-127">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="a0be9-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="a0be9-128">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a0be9-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a0be9-129">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a0be9-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="a0be9-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a0be9-130">Return value</span></span>|<span data-ttu-id="a0be9-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0be9-131">Description</span></span>|
|-|-|
|<span data-ttu-id="a0be9-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="a0be9-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="a0be9-133">O adaptador não está mais em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="a0be9-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="a0be9-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="a0be9-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="a0be9-135">O tipo de estado especificado no *estado* não é reconhecido por este sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="a0be9-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="a0be9-136">Chame [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="a0be9-136">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="a0be9-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a0be9-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="a0be9-138">O adaptador não dá suporte ao tipo de estado especificado no *estado* .</span><span class="sxs-lookup"><span data-stu-id="a0be9-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="a0be9-139">Chame [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="a0be9-139">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="a0be9-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a0be9-140">E_INVALIDARG</span></span>|<span data-ttu-id="a0be9-141">Um tamanho de buffer insuficiente é fornecido para *OUTPUTBUFFER* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).</span><span class="sxs-lookup"><span data-stu-id="a0be9-141">An insufficient buffer size is provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="a0be9-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="a0be9-142">E_POINTER</span></span>|<span data-ttu-id="a0be9-143">`nullptr` foi fornecido para *OUTPUTBUFFER* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).</span><span class="sxs-lookup"><span data-stu-id="a0be9-143">`nullptr` was provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="remarks"></a><span data-ttu-id="a0be9-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0be9-144">Remarks</span></span>

<span data-ttu-id="a0be9-145">Consulte [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador e quais entradas e saídas são usadas.</span><span class="sxs-lookup"><span data-stu-id="a0be9-145">See [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind, and what inputs and outputs are used.</span></span> <span data-ttu-id="a0be9-146">Essa função zera o buffer *OUTPUTBUFFER* antes de preenchê-lo.</span><span class="sxs-lookup"><span data-stu-id="a0be9-146">This function zeros out the *outputBuffer* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0be9-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0be9-147">See also</span></span>

<span data-ttu-id="a0be9-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a0be9-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>