---
title: IDXCoreAdapter::SetState
description: Define o estado do item especificado no adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105790432"
---
# <a name="idxcoreadaptersetstate-method"></a><span data-ttu-id="35769-103">Método IDXCoreAdapter:: SetState</span><span class="sxs-lookup"><span data-stu-id="35769-103">IDXCoreAdapter::SetState method</span></span>

<span data-ttu-id="35769-104">Define o estado do item especificado no adaptador.</span><span class="sxs-lookup"><span data-stu-id="35769-104">Sets the state of the specified item on the adapter.</span></span> <span data-ttu-id="35769-105">Antes de chamar **SetState** para um tipo de propriedade, chame [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que a configuração do tipo de estado está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="35769-105">Before calling **SetState** for a property type, call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="35769-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35769-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a><span data-ttu-id="35769-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35769-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="35769-108">state</span><span class="sxs-lookup"><span data-stu-id="35769-108">state</span></span>

<span data-ttu-id="35769-109">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="35769-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="35769-110">O tipo de item de estado no adaptador cujo estado você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="35769-110">The kind of state item on the adapter whose state you wish to set.</span></span> <span data-ttu-id="35769-111">Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador.</span><span class="sxs-lookup"><span data-stu-id="35769-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="35769-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="35769-112">inputStateDetailsSize</span></span>

<span data-ttu-id="35769-113">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="35769-113">Type: **size_t**</span></span>

<span data-ttu-id="35769-114">O tamanho, em bytes, do buffer de detalhes de estado de entrada que você (opcionalmente) aloca e fornece em *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="35769-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="35769-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="35769-115">inputStateDetails [in]</span></span>

<span data-ttu-id="35769-116">Tipo: **void const \***</span><span class="sxs-lookup"><span data-stu-id="35769-116">Type: **void const\***</span></span>

<span data-ttu-id="35769-117">Um ponteiro opcional para um buffer de detalhes de estado de entrada constante que você aloca em seu aplicativo, contendo qualquer informação sobre a solicitação necessária para o tipo de estado que você especificar no *estado*.</span><span class="sxs-lookup"><span data-stu-id="35769-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="35769-118">Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre qualquer requisito de buffer de entrada para um determinado tipo de estado.</span><span class="sxs-lookup"><span data-stu-id="35769-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="inputdatasize"></a><span data-ttu-id="35769-119">inputDataSize</span><span class="sxs-lookup"><span data-stu-id="35769-119">inputDataSize</span></span>

<span data-ttu-id="35769-120">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="35769-120">Type: **size_t**</span></span>

<span data-ttu-id="35769-121">O tamanho, em bytes, do buffer de entrada que você aloca e fornece em *inputData*.</span><span class="sxs-lookup"><span data-stu-id="35769-121">The size, in bytes, of the input buffer that you allocate and provide in *inputData*.</span></span>

### <a name="inputdata-in"></a><span data-ttu-id="35769-122">inputData [in]</span><span class="sxs-lookup"><span data-stu-id="35769-122">inputData [in]</span></span>

<span data-ttu-id="35769-123">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="35769-123">Type: **void\***</span></span>

<span data-ttu-id="35769-124">Um ponteiro para um buffer de entrada que você aloca em seu aplicativo, contendo as informações de estado a serem definidas para o item de Estado cujo tipo você especificar no *estado*.</span><span class="sxs-lookup"><span data-stu-id="35769-124">A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*.</span></span> <span data-ttu-id="35769-125">Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre o requisito de buffer de entrada para um determinado tipo de estado.</span><span class="sxs-lookup"><span data-stu-id="35769-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the input buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="35769-126">Retornos</span><span class="sxs-lookup"><span data-stu-id="35769-126">Returns</span></span>

<span data-ttu-id="35769-127">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="35769-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="35769-128">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="35769-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="35769-129">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="35769-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="35769-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="35769-130">Return value</span></span>|<span data-ttu-id="35769-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="35769-131">Description</span></span>|
|-|-|
|<span data-ttu-id="35769-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="35769-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="35769-133">O adaptador não está mais em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="35769-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="35769-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="35769-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="35769-135">O tipo de estado especificado no *estado* não é reconhecido por este sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="35769-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="35769-136">Chame [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que a configuração do tipo de estado está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="35769-136">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="35769-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="35769-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="35769-138">O adaptador não dá suporte ao tipo de estado especificado no *estado* .</span><span class="sxs-lookup"><span data-stu-id="35769-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="35769-139">Chame [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) para confirmar que a configuração do tipo de estado está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="35769-139">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="35769-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="35769-140">E_INVALIDARG</span></span>|<span data-ttu-id="35769-141">Um tamanho de buffer insuficiente é fornecido para *inputData* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).</span><span class="sxs-lookup"><span data-stu-id="35769-141">An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="35769-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="35769-142">E_POINTER</span></span>|<span data-ttu-id="35769-143">`nullptr` foi fornecido para *inputData* (ou para *inputStateDetails* onde um buffer de detalhes de estado de entrada é necessário).</span><span class="sxs-lookup"><span data-stu-id="35769-143">`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="see-also"></a><span data-ttu-id="35769-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="35769-144">See also</span></span>

<span data-ttu-id="35769-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="35769-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>