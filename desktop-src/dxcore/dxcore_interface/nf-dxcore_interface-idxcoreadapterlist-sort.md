---
title: IDXCoreAdapterList::Sort
description: Classifica um objeto da lista de adaptadores DXCore com base em uma matriz de entrada fornecida de critérios de classificação.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084821"
---
# <a name="idxcoreadapterlistsort-method"></a><span data-ttu-id="77d51-103">Método IDXCoreAdapterList:: Sort</span><span class="sxs-lookup"><span data-stu-id="77d51-103">IDXCoreAdapterList::Sort method</span></span>

## <a name="description"></a><span data-ttu-id="77d51-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="77d51-104">Description</span></span>

<span data-ttu-id="77d51-105">Classifica um objeto da lista de adaptadores DXCore com base em uma matriz de entrada fornecida de critérios de classificação, em que os itens de matriz na matriz de critérios são fornecidos com um peso mais alto.</span><span class="sxs-lookup"><span data-stu-id="77d51-105">Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight.</span></span> <span data-ttu-id="77d51-106">A **classificação** ajuda a localizar mais facilmente o adaptador ideal em uma lista de adaptadores.</span><span class="sxs-lookup"><span data-stu-id="77d51-106">**Sort** helps you to more easily find your ideal adapter in an adapter list.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d51-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77d51-107">Syntax</span></span>

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a><span data-ttu-id="77d51-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77d51-108">Parameters</span></span>

### <a name="numpreferences"></a><span data-ttu-id="77d51-109">numPreferences</span><span class="sxs-lookup"><span data-stu-id="77d51-109">numPreferences</span></span>

<span data-ttu-id="77d51-110">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="77d51-110">Type: **uint32_t**</span></span>

<span data-ttu-id="77d51-111">O número de elementos que estão na matriz apontada pelo parâmetro de *preferências* .</span><span class="sxs-lookup"><span data-stu-id="77d51-111">The number of elements that are in the array pointed to by the *preferences* parameter.</span></span>

### <a name="preferences-in"></a><span data-ttu-id="77d51-112">Preferências [em]</span><span class="sxs-lookup"><span data-stu-id="77d51-112">preferences [in]</span></span>

<span data-ttu-id="77d51-113">Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***</span><span class="sxs-lookup"><span data-stu-id="77d51-113">Type: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)\***</span></span>

<span data-ttu-id="77d51-114">Um ponteiro para uma matriz constante de valores [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) , representando critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="77d51-114">A pointer to a constant array of [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) values, representing sort criteria.</span></span>

## <a name="returns"></a><span data-ttu-id="77d51-115">Retornos</span><span class="sxs-lookup"><span data-stu-id="77d51-115">Returns</span></span>

<span data-ttu-id="77d51-116">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="77d51-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="77d51-117">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="77d51-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="77d51-118">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="77d51-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="77d51-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="77d51-119">Return value</span></span>|<span data-ttu-id="77d51-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="77d51-120">Description</span></span>|
|-|-|
|<span data-ttu-id="77d51-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="77d51-121">E_INVALIDARG</span></span>|<span data-ttu-id="77d51-122">O argumento *numPreferences* é zero ou o argumento *Preferences* é `nullptr` .</span><span class="sxs-lookup"><span data-stu-id="77d51-122">The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.</span></span>|

## <a name="remarks"></a><span data-ttu-id="77d51-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="77d51-123">Remarks</span></span>

<span data-ttu-id="77d51-124">Nos casos em que um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) fornecido não é reconhecido pelo sistema operacional (SO), ele é ignorado e não fará com que a API falhe.</span><span class="sxs-lookup"><span data-stu-id="77d51-124">In cases where a provided [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail.</span></span> <span data-ttu-id="77d51-125">Os valores **DXCoreAdapterPreference** conhecidos ainda serão considerados nesse caso.</span><span class="sxs-lookup"><span data-stu-id="77d51-125">Known **DXCoreAdapterPreference** values will still be considered in this case.</span></span> <span data-ttu-id="77d51-126">Para determinar se um tipo de classificação é compreendido pela API, chame [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="77d51-126">To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

<span data-ttu-id="77d51-127">Os valores de **DXCoreAdapterPreference** que ocorrem anteriormente na matriz de *preferências* fornecida são tratados com prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="77d51-127">**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority.</span></span> 

<span data-ttu-id="77d51-128">Consulte a documentação de enumeração **DXCoreAdapterPreference** para obter detalhes sobre qual lógica é aplicada para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="77d51-128">Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type.</span></span> <span data-ttu-id="77d51-129">A lógica interna de um tipo pode ser desenvolvida conforme o sistema operacional é desenvolvido.</span><span class="sxs-lookup"><span data-stu-id="77d51-129">The internal logic for a type may develop as the OS develops.</span></span>

<span data-ttu-id="77d51-130">Quando a **classificação** retorna, os itens na lista de adaptadores DXCore terão sido classificados do mais preferível ao menos preferível.</span><span class="sxs-lookup"><span data-stu-id="77d51-130">When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable.</span></span> <span data-ttu-id="77d51-131">Portanto, chamar [IDXCoreAdapterList:: getadapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) com o índice 0 recupera o adaptador que melhor corresponde aos tipos de preferência de classificação solicitados; o índice 1 é a próxima melhor correspondência e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="77d51-131">So, calling [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.</span></span>

## <a name="see-also"></a><span data-ttu-id="77d51-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="77d51-132">See also</span></span>

<span data-ttu-id="77d51-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="77d51-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>