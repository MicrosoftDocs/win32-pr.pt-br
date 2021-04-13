---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Recupera o objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para um LUID especificado, se disponível.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366439"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a><span data-ttu-id="2bf1d-103">Método IDXCoreAdapterFactory:: GetAdapterByLuid</span><span class="sxs-lookup"><span data-stu-id="2bf1d-103">IDXCoreAdapterFactory::GetAdapterByLuid method</span></span>

<span data-ttu-id="2bf1d-104">Recupera o objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para um LUID especificado, se disponível.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-104">Retrieves the DXCore adapter object ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) for a specified LUID, if available.</span></span> <span data-ttu-id="2bf1d-105">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="2bf1d-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf1d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bf1d-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="2bf1d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bf1d-107">Parameters</span></span>

### <a name="adapterluid"></a><span data-ttu-id="2bf1d-108">adapterLUID</span><span class="sxs-lookup"><span data-stu-id="2bf1d-108">adapterLUID</span></span>

<span data-ttu-id="2bf1d-109">Tipo: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span><span class="sxs-lookup"><span data-stu-id="2bf1d-109">Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span></span>

<span data-ttu-id="2bf1d-110">O valor local exclusivo que identifica a instância do adaptador.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-110">The locally unique value that identifies the adapter instance.</span></span>

### <a name="riid-in"></a><span data-ttu-id="2bf1d-111">riid [in]</span><span class="sxs-lookup"><span data-stu-id="2bf1d-111">riid [in]</span></span>

<span data-ttu-id="2bf1d-112">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="2bf1d-112">Type: **REFIID**</span></span>

<span data-ttu-id="2bf1d-113">Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="2bf1d-114">Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="2bf1d-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="2bf1d-115">ppvAdapter [saída]</span><span class="sxs-lookup"><span data-stu-id="2bf1d-115">ppvAdapter [out]</span></span>

<span data-ttu-id="2bf1d-116">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="2bf1d-116">Type: **void\*\***</span></span>

<span data-ttu-id="2bf1d-117">O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="2bf1d-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="2bf1d-118">Após o retorno bem-sucedido, *\* ppvAdapter* (o endereço desreferenciado) contém um ponteiro para o adaptador DXCore criado.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="2bf1d-119">Retornos</span><span class="sxs-lookup"><span data-stu-id="2bf1d-119">Returns</span></span>

<span data-ttu-id="2bf1d-120">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="2bf1d-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="2bf1d-121">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2bf1d-122">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf1d-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="2bf1d-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2bf1d-123">Return value</span></span>|<span data-ttu-id="2bf1d-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="2bf1d-124">Description</span></span>|
|-|-|
|<span data-ttu-id="2bf1d-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="2bf1d-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="2bf1d-126">O LUID de adaptador passado em *adapterLUID* é reconhecido, mas o adaptador não está mais em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-126">The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="2bf1d-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2bf1d-127">E_INVALIDARG</span></span>|<span data-ttu-id="2bf1d-128">Não há tal LUID de adaptador, pois o valor passado em *adapterLUID* está disponível por meio de DXCore.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-128">No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.</span></span>|
|<span data-ttu-id="2bf1d-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="2bf1d-129">E_NOINTERFACE</span></span>|<span data-ttu-id="2bf1d-130">Um valor inválido foi fornecido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="2bf1d-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="2bf1d-131">E_POINTER</span></span>|<span data-ttu-id="2bf1d-132">`nullptr` foi fornecido para *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2bf1d-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bf1d-133">Remarks</span></span>

<span data-ttu-id="2bf1d-134">Várias chamadas passando o mesmo [LUID](/windows/win32/api/winnt/ns-winnt-luid) retornam ponteiros de interface idênticos.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-134">Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-luid) return identical interface pointers.</span></span> <span data-ttu-id="2bf1d-135">Como resultado, é seguro comparar os ponteiros de interface para determinar se vários ponteiros se referem ao mesmo objeto de adaptador.</span><span class="sxs-lookup"><span data-stu-id="2bf1d-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bf1d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bf1d-136">See also</span></span>

<span data-ttu-id="2bf1d-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2bf1d-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>