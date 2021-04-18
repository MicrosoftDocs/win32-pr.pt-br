---
title: IDXCoreAdapterList::GetFactory
description: 'Recupera um ponteiro de interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) para o objeto de fábrica do adaptador DXCore. | IDXCoreAdapterList:: GetFactory'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105802156"
---
# <a name="idxcoreadapterlistgetfactory-method"></a><span data-ttu-id="f66ab-104">Método IDXCoreAdapterList:: GetFactory</span><span class="sxs-lookup"><span data-stu-id="f66ab-104">IDXCoreAdapterList::GetFactory method</span></span>

<span data-ttu-id="f66ab-105">Recupera um ponteiro de interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) para o objeto de fábrica do adaptador DXCore.</span><span class="sxs-lookup"><span data-stu-id="f66ab-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="f66ab-106">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="f66ab-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f66ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f66ab-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="f66ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f66ab-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="f66ab-109">riid</span><span class="sxs-lookup"><span data-stu-id="f66ab-109">riid</span></span>

<span data-ttu-id="f66ab-110">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="f66ab-110">Type: **REFIID**</span></span>

<span data-ttu-id="f66ab-111">Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="f66ab-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="f66ab-112">Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="f66ab-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="f66ab-113">ppvFactory [saída]</span><span class="sxs-lookup"><span data-stu-id="f66ab-113">ppvFactory [out]</span></span>

<span data-ttu-id="f66ab-114">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="f66ab-114">Type: **void\*\***</span></span>

<span data-ttu-id="f66ab-115">O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="f66ab-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="f66ab-116">Após o retorno bem-sucedido, *\* ppvFactory* (o endereço desreferenciado) contém um ponteiro para o objeto de fábrica do adaptador DXCore existente.</span><span class="sxs-lookup"><span data-stu-id="f66ab-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="f66ab-117">Antes de retornar, a função incrementa a contagem de referência na interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) do objeto de fábrica.</span><span class="sxs-lookup"><span data-stu-id="f66ab-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="f66ab-118">Retornos</span><span class="sxs-lookup"><span data-stu-id="f66ab-118">Returns</span></span>

<span data-ttu-id="f66ab-119">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f66ab-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f66ab-120">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f66ab-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f66ab-121">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f66ab-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="f66ab-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f66ab-122">Return value</span></span>|<span data-ttu-id="f66ab-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f66ab-123">Description</span></span>|
|-|-|
|<span data-ttu-id="f66ab-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="f66ab-124">E_NOINTERFACE</span></span>|<span data-ttu-id="f66ab-125">Um valor inválido foi fornecido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="f66ab-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="f66ab-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="f66ab-126">E_POINTER</span></span>|<span data-ttu-id="f66ab-127">`nullptr` foi fornecido para *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="f66ab-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f66ab-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f66ab-128">Remarks</span></span>

<span data-ttu-id="f66ab-129">Durante o tempo em que uma referência existe em uma interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , uma interface [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) ou uma interface [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , chamadas adicionais para [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList:: GetFactory]()ou [IDXCoreAdapter:: GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) retornarão ponteiros para o mesmo objeto, aumentando a contagem de referência da interface **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="f66ab-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](), or [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="f66ab-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f66ab-130">See also</span></span>

<span data-ttu-id="f66ab-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f66ab-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
