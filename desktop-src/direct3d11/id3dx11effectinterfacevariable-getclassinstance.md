---
title: Método ID3DX11EffectInterfaceVariable GetClassInstance (D3dx11effect. h)
description: Obter uma instância de classe.
ms.assetid: a965f4e7-1761-45f1-a72e-7ad0ed1ad671
keywords:
- Método GetClassInstance Direct3D 11
- Método GetClassInstance Direct3D 11, interface ID3DX11EffectInterfaceVariable
- Interface ID3DX11EffectInterfaceVariable Direct3D 11, método GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f729da6ee84d76dd37a40a7946438e367c1a4cbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930659"
---
# <a name="id3dx11effectinterfacevariablegetclassinstance-method"></a><span data-ttu-id="e681b-106">Método ID3DX11EffectInterfaceVariable:: GetClassInstance</span><span class="sxs-lookup"><span data-stu-id="e681b-106">ID3DX11EffectInterfaceVariable::GetClassInstance method</span></span>

<span data-ttu-id="e681b-107">Obter uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="e681b-107">Get a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="e681b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e681b-108">Syntax</span></span>


```C++
HRESULT GetClassInstance(
   ID3DX11EffectClassInstanceVariable **ppEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="e681b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e681b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e681b-110">*ppEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="e681b-110">*ppEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e681b-111">Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e681b-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\*\***</span></span>

<span data-ttu-id="e681b-112">Ponteiro para um ponteiro [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) que será definido para a instância de classe.</span><span class="sxs-lookup"><span data-stu-id="e681b-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) pointer that will be set to the class instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e681b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e681b-113">Return value</span></span>

<span data-ttu-id="e681b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e681b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e681b-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e681b-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e681b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e681b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e681b-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="e681b-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e681b-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e681b-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e681b-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e681b-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e681b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e681b-120">Requirements</span></span>



| <span data-ttu-id="e681b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e681b-121">Requirement</span></span> | <span data-ttu-id="e681b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e681b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e681b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e681b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e681b-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e681b-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e681b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e681b-125">Library</span></span><br/> | <dl> <span data-ttu-id="e681b-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="e681b-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e681b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e681b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e681b-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="e681b-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





