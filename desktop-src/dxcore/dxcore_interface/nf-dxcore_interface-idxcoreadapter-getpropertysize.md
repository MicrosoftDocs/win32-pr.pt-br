---
title: IDXCoreAdapter::GetPropertySize
description: Para uma propriedade de adaptador especificada, recupera o tamanho do buffer, em bytes, que é necessário para uma chamada para [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105808382"
---
# <a name="idxcoreadaptergetpropertysize-method"></a><span data-ttu-id="50e2d-103">Método IDXCoreAdapter:: GetPropertySize</span><span class="sxs-lookup"><span data-stu-id="50e2d-103">IDXCoreAdapter::GetPropertySize method</span></span>

<span data-ttu-id="50e2d-104">Para uma propriedade de adaptador especificada, recupera o tamanho do buffer, em bytes, que é necessário para uma chamada para [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="50e2d-104">For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span> <span data-ttu-id="50e2d-105">Antes de chamar **GetPropertySize** para um tipo de propriedade, chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="50e2d-105">Before calling **GetPropertySize** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="50e2d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50e2d-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a><span data-ttu-id="50e2d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50e2d-107">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="50e2d-108">propriedade</span><span class="sxs-lookup"><span data-stu-id="50e2d-108">property</span></span>

<span data-ttu-id="50e2d-109">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="50e2d-109">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="50e2d-110">O tipo da propriedade cujo tamanho, em bytes, você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="50e2d-110">The type of the property whose size, in bytes, you wish to retrieve.</span></span>

### <a name="buffersize-out"></a><span data-ttu-id="50e2d-111">bufferSize [saída]</span><span class="sxs-lookup"><span data-stu-id="50e2d-111">bufferSize [out]</span></span>

<span data-ttu-id="50e2d-112">Tipo: **size_t \***</span><span class="sxs-lookup"><span data-stu-id="50e2d-112">Type: **size_t\***</span></span>

<span data-ttu-id="50e2d-113">Um ponteiro para um valor **size_t** .</span><span class="sxs-lookup"><span data-stu-id="50e2d-113">A pointer to a **size_t** value.</span></span> <span data-ttu-id="50e2d-114">A função desreferencia o ponteiro e define o valor para o tamanho, em bytes, do buffer de saída que você deve alocar e passar como o argumento *PropertyData* em sua chamada para [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="50e2d-114">The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

## <a name="returns"></a><span data-ttu-id="50e2d-115">Retornos</span><span class="sxs-lookup"><span data-stu-id="50e2d-115">Returns</span></span>

<span data-ttu-id="50e2d-116">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="50e2d-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="50e2d-117">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="50e2d-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="50e2d-118">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="50e2d-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="50e2d-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="50e2d-119">Return value</span></span>|<span data-ttu-id="50e2d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="50e2d-120">Description</span></span>|
|-|-|
|<span data-ttu-id="50e2d-121">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="50e2d-121">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="50e2d-122">O tipo de propriedade especificado na *Propriedade* não é reconhecido por este sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="50e2d-122">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="50e2d-123">Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="50e2d-123">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="50e2d-124">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="50e2d-124">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="50e2d-125">O adaptador não dá suporte ao tipo de propriedade especificado na *Propriedade* .</span><span class="sxs-lookup"><span data-stu-id="50e2d-125">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="50e2d-126">Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="50e2d-126">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="50e2d-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="50e2d-127">E_POINTER</span></span>|<span data-ttu-id="50e2d-128">`nullptr` foi fornecido para *BufferSize*.</span><span class="sxs-lookup"><span data-stu-id="50e2d-128">`nullptr` was provided for *bufferSize*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="50e2d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="50e2d-129">Remarks</span></span>

<span data-ttu-id="50e2d-130">Você pode chamar **GetPropertySize** em um adaptador que não é mais válido &mdash; . a função não falhará.</span><span class="sxs-lookup"><span data-stu-id="50e2d-130">You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.</span></span>

## <a name="see-also"></a><span data-ttu-id="50e2d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="50e2d-131">See also</span></span>

<span data-ttu-id="50e2d-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="50e2d-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>