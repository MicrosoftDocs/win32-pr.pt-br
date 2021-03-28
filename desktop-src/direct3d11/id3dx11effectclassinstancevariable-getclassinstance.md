---
title: Método ID3DX11EffectClassInstanceVariable GetClassInstance (D3dx11effect. h)
description: Obtém uma instância de classe.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Método GetClassInstance Direct3D 11
- Método GetClassInstance Direct3D 11, interface ID3DX11EffectClassInstanceVariable
- Interface ID3DX11EffectClassInstanceVariable Direct3D 11, método GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dae96d42a0088adc683ca93d7e3215c12912a87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298857"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a><span data-ttu-id="23aed-106">Método ID3DX11EffectClassInstanceVariable:: GetClassInstance</span><span class="sxs-lookup"><span data-stu-id="23aed-106">ID3DX11EffectClassInstanceVariable::GetClassInstance method</span></span>

<span data-ttu-id="23aed-107">Obtém uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="23aed-107">Gets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="23aed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23aed-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="23aed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23aed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23aed-110">*ppClassInstance*</span><span class="sxs-lookup"><span data-stu-id="23aed-110">*ppClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="23aed-111">Tipo: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span><span class="sxs-lookup"><span data-stu-id="23aed-111">Type: **[**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***</span></span>

<span data-ttu-id="23aed-112">Ponteiro para um ponteiro [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) que será definido como instância de classe.</span><span class="sxs-lookup"><span data-stu-id="23aed-112">Pointer to an [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointer that will be set to class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23aed-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23aed-113">Return value</span></span>

<span data-ttu-id="23aed-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23aed-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23aed-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="23aed-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23aed-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="23aed-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23aed-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="23aed-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23aed-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="23aed-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23aed-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="23aed-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23aed-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23aed-120">Requirements</span></span>



| <span data-ttu-id="23aed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23aed-121">Requirement</span></span> | <span data-ttu-id="23aed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="23aed-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23aed-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23aed-123">Header</span></span><br/>  | <dl> <span data-ttu-id="23aed-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="23aed-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23aed-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23aed-125">Library</span></span><br/> | <dl> <span data-ttu-id="23aed-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="23aed-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23aed-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="23aed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23aed-128">ID3DX11EffectClassInstanceVariable</span><span class="sxs-lookup"><span data-stu-id="23aed-128">ID3DX11EffectClassInstanceVariable</span></span>](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





