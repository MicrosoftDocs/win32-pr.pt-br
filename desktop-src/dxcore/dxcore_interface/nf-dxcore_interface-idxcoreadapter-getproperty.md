---
title: IDXCoreAdapter::GetProperty
description: Recupera o valor da propriedade de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294435"
---
# <a name="idxcoreadaptergetproperty-method"></a><span data-ttu-id="a2654-103">Método IDXCoreAdapter:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="a2654-103">IDXCoreAdapter::GetProperty method</span></span>

<span data-ttu-id="a2654-104">Recupera o valor da propriedade de adaptador especificada.</span><span class="sxs-lookup"><span data-stu-id="a2654-104">Retrieves the value of the specified adapter property.</span></span> <span data-ttu-id="a2654-105">Antes de chamar **GetProperty** para um tipo de propriedade, chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="a2654-105">Before calling **GetProperty** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span> <span data-ttu-id="a2654-106">Além disso, antes de chamar **GetProperty**, chame [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar o tamanho necessário do buffer no qual receber o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a2654-106">Also before calling **GetProperty**, call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the necessary size of the buffer in which to receive the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2654-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2654-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a><span data-ttu-id="a2654-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2654-108">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="a2654-109">propriedade</span><span class="sxs-lookup"><span data-stu-id="a2654-109">property</span></span>

<span data-ttu-id="a2654-110">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="a2654-110">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="a2654-111">O tipo da propriedade cujo valor você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="a2654-111">The type of the property whose value you wish to retrieve.</span></span> <span data-ttu-id="a2654-112">Consulte a tabela em [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obter mais informações sobre cada propriedade de adaptador.</span><span class="sxs-lookup"><span data-stu-id="a2654-112">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

### <a name="buffersize"></a><span data-ttu-id="a2654-113">bufferSize</span><span class="sxs-lookup"><span data-stu-id="a2654-113">bufferSize</span></span>

<span data-ttu-id="a2654-114">Tipo: **size_t**</span><span class="sxs-lookup"><span data-stu-id="a2654-114">Type: **size_t**</span></span>

<span data-ttu-id="a2654-115">O tamanho, em bytes, do buffer de saída que você aloca e fornece em *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="a2654-115">The size, in bytes, of the output buffer that you allocate and provide in *propertyData*.</span></span>

### <a name="propertydata-out"></a><span data-ttu-id="a2654-116">propertyData [saída]</span><span class="sxs-lookup"><span data-stu-id="a2654-116">propertyData [out]</span></span>

<span data-ttu-id="a2654-117">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="a2654-117">Type: **void\***</span></span>

<span data-ttu-id="a2654-118">Um ponteiro para um buffer de saída que você aloca em seu aplicativo e que a função preenche.</span><span class="sxs-lookup"><span data-stu-id="a2654-118">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="a2654-119">Chame [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar o tamanho que o buffer *PropertyData* deve ter para uma determinada propriedade de adaptador.</span><span class="sxs-lookup"><span data-stu-id="a2654-119">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="a2654-120">Retornos</span><span class="sxs-lookup"><span data-stu-id="a2654-120">Returns</span></span>

<span data-ttu-id="a2654-121">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="a2654-121">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="a2654-122">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a2654-122">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a2654-123">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a2654-123">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="a2654-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a2654-124">Return value</span></span>|<span data-ttu-id="a2654-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2654-125">Description</span></span>|
|-|-|
|<span data-ttu-id="a2654-126">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="a2654-126">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="a2654-127">O tipo de propriedade especificado na *Propriedade* não é reconhecido por este sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="a2654-127">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="a2654-128">Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="a2654-128">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="a2654-129">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a2654-129">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="a2654-130">O adaptador não dá suporte ao tipo de propriedade especificado na *Propriedade* .</span><span class="sxs-lookup"><span data-stu-id="a2654-130">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="a2654-131">Chame [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) para confirmar que o tipo de propriedade está disponível para este adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="a2654-131">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="a2654-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a2654-132">E_INVALIDARG</span></span>|<span data-ttu-id="a2654-133">Um tamanho de buffer insuficiente é fornecido em *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="a2654-133">An insufficient buffer size is provided in *propertyData*.</span></span> <span data-ttu-id="a2654-134">Chame [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para determinar o tamanho que o buffer *PropertyData* deve ter para uma determinada propriedade de adaptador.</span><span class="sxs-lookup"><span data-stu-id="a2654-134">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>|
|<span data-ttu-id="a2654-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="a2654-135">E_POINTER</span></span>|<span data-ttu-id="a2654-136">`nullptr` foi fornecido para *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="a2654-136">`nullptr` was provided for *propertyData*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a2654-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2654-137">Remarks</span></span>

<span data-ttu-id="a2654-138">Você pode chamar **GetProperty** em um adaptador que não é mais válido &mdash; . a função não falhará como resultado disso.</span><span class="sxs-lookup"><span data-stu-id="a2654-138">You can call **GetProperty** on an adapter that's no longer valid&mdash;the function won't fail as a result of that.</span></span> <span data-ttu-id="a2654-139">Essa função zera o buffer *PropertyData* antes de preenchê-lo.</span><span class="sxs-lookup"><span data-stu-id="a2654-139">This function zeros out the *propertyData* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2654-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2654-140">See also</span></span>

<span data-ttu-id="a2654-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a2654-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>