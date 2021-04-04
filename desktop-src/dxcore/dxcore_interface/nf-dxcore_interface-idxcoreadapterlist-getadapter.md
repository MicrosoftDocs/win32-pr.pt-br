---
title: IDXCoreAdapterList::GetAdapter
description: Recupera um adaptador específico por índice de um objeto de lista do adaptador DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007975"
---
# <a name="idxcoreadapterlistgetadapter-method"></a><span data-ttu-id="9bc46-103">Método IDXCoreAdapterList:: getadapter</span><span class="sxs-lookup"><span data-stu-id="9bc46-103">IDXCoreAdapterList::GetAdapter method</span></span>

<span data-ttu-id="9bc46-104">Recupera um adaptador específico por índice de um objeto de lista do adaptador DXCore.</span><span class="sxs-lookup"><span data-stu-id="9bc46-104">Retrieves a specific adapter by index from a DXCore adapter list object.</span></span> <span data-ttu-id="9bc46-105">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="9bc46-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc46-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bc46-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="9bc46-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bc46-107">Parameters</span></span>

### <a name="index"></a><span data-ttu-id="9bc46-108">índice</span><span class="sxs-lookup"><span data-stu-id="9bc46-108">index</span></span>

<span data-ttu-id="9bc46-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="9bc46-109">Type: **uint32_t**</span></span>

<span data-ttu-id="9bc46-110">Um índice de base zero, identificando uma instância de adaptador dentro da lista de adaptadores DXCore.</span><span class="sxs-lookup"><span data-stu-id="9bc46-110">A zero-based index, identifying an adapter instance within the DXCore adapter list.</span></span>

### <a name="riid"></a><span data-ttu-id="9bc46-111">riid</span><span class="sxs-lookup"><span data-stu-id="9bc46-111">riid</span></span>

<span data-ttu-id="9bc46-112">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="9bc46-112">Type: **REFIID**</span></span>

<span data-ttu-id="9bc46-113">Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="9bc46-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="9bc46-114">Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="9bc46-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="9bc46-115">ppvAdapter [saída]</span><span class="sxs-lookup"><span data-stu-id="9bc46-115">ppvAdapter [out]</span></span>

<span data-ttu-id="9bc46-116">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="9bc46-116">Type: **void\*\***</span></span>

<span data-ttu-id="9bc46-117">O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="9bc46-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="9bc46-118">Após o retorno bem-sucedido, *\* ppvAdapter* (o endereço desreferenciado) contém um ponteiro para o adaptador DXCore criado.</span><span class="sxs-lookup"><span data-stu-id="9bc46-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="9bc46-119">Retornos</span><span class="sxs-lookup"><span data-stu-id="9bc46-119">Returns</span></span>

<span data-ttu-id="9bc46-120">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="9bc46-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="9bc46-121">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="9bc46-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="9bc46-122">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc46-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="9bc46-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9bc46-123">Return value</span></span>|<span data-ttu-id="9bc46-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bc46-124">Description</span></span>|
|-|-|
|<span data-ttu-id="9bc46-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="9bc46-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="9bc46-126">O *índice* é válido, mas o adaptador não está mais em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="9bc46-126">The *index* is valid, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="9bc46-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9bc46-127">E_INVALIDARG</span></span>|<span data-ttu-id="9bc46-128">O *índice* fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="9bc46-128">The provided *index* is not valid.</span></span>|
|<span data-ttu-id="9bc46-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="9bc46-129">E_NOINTERFACE</span></span>|<span data-ttu-id="9bc46-130">Um valor inválido foi fornecido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="9bc46-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="9bc46-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="9bc46-131">E_POINTER</span></span>|<span data-ttu-id="9bc46-132">`nullptr` foi fornecido para *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="9bc46-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9bc46-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bc46-133">Remarks</span></span>

<span data-ttu-id="9bc46-134">Várias chamadas passando um índice que representa o mesmo adaptador retornam ponteiros de interface idênticos, mesmo entre diferentes listas de adaptadores.</span><span class="sxs-lookup"><span data-stu-id="9bc46-134">Multiple calls passing an index that represents the same adapter return identical interface pointers, even across different adapter lists.</span></span> <span data-ttu-id="9bc46-135">Como resultado, é seguro comparar os ponteiros de interface para determinar se vários ponteiros se referem ao mesmo objeto de adaptador.</span><span class="sxs-lookup"><span data-stu-id="9bc46-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bc46-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bc46-136">See also</span></span>

<span data-ttu-id="9bc46-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="9bc46-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>