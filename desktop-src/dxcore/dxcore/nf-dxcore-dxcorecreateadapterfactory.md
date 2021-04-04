---
title: DXCoreCreateAdapterFactory
description: Cria uma fábrica de adaptador DXCore, que pode ser usada para gerar outros objetos DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917557"
---
# <a name="dxcorecreateadapterfactory-function"></a><span data-ttu-id="1e3ab-103">Função DXCoreCreateAdapterFactory</span><span class="sxs-lookup"><span data-stu-id="1e3ab-103">DXCoreCreateAdapterFactory function</span></span>

## <a name="description"></a><span data-ttu-id="1e3ab-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e3ab-104">Description</span></span>

<span data-ttu-id="1e3ab-105">Cria uma fábrica de adaptador DXCore, que pode ser usada para gerar outros objetos DXCore.</span><span class="sxs-lookup"><span data-stu-id="1e3ab-105">Creates a DXCore adapter factory, which you can use to generate further DXCore objects.</span></span> <span data-ttu-id="1e3ab-106">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="1e3ab-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="1e3ab-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e3ab-107">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="1e3ab-108">riid</span><span class="sxs-lookup"><span data-stu-id="1e3ab-108">riid</span></span>

<span data-ttu-id="1e3ab-109">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="1e3ab-109">Type: **REFIID**</span></span>

<span data-ttu-id="1e3ab-110">Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="1e3ab-110">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="1e3ab-111">Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="1e3ab-111">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="1e3ab-112">ppvFactory [saída]</span><span class="sxs-lookup"><span data-stu-id="1e3ab-112">ppvFactory [out]</span></span>

<span data-ttu-id="1e3ab-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="1e3ab-113">Type: **void\*\***</span></span>

<span data-ttu-id="1e3ab-114">O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="1e3ab-114">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="1e3ab-115">Após o retorno bem-sucedido, *\* ppvFactory* (o endereço desreferenciado) contém um ponteiro para a fábrica DXCore criada.</span><span class="sxs-lookup"><span data-stu-id="1e3ab-115">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the DXCore factory created.</span></span>

## <a name="returns"></a><span data-ttu-id="1e3ab-116">Retornos</span><span class="sxs-lookup"><span data-stu-id="1e3ab-116">Returns</span></span>

<span data-ttu-id="1e3ab-117">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="1e3ab-117">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="1e3ab-118">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="1e3ab-118">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="1e3ab-119">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1e3ab-119">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="1e3ab-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1e3ab-120">Return value</span></span>|<span data-ttu-id="1e3ab-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e3ab-121">Description</span></span>|
|-|-|
|<span data-ttu-id="1e3ab-122">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="1e3ab-122">E_NOINTERFACE</span></span>|<span data-ttu-id="1e3ab-123">Um valor inválido foi fornecido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="1e3ab-123">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="1e3ab-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="1e3ab-124">E_POINTER</span></span>|<span data-ttu-id="1e3ab-125">`nullptr` foi fornecido para *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="1e3ab-125">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1e3ab-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e3ab-126">Remarks</span></span>

<span data-ttu-id="1e3ab-127">Durante o tempo em que uma referência existe em uma interface [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , uma interface [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) ou uma interface [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , chamadas adicionais para **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)ou [IDXCoreAdapter:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) retornarão ponteiros para o mesmo objeto, aumentando a contagem de referência da interface **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="1e3ab-127">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e3ab-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e3ab-128">See also</span></span>

<span data-ttu-id="1e3ab-129">[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="1e3ab-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>