---
title: Método ID3DX11EffectInterfaceVariable SetClassInstance (D3dx11effect. h)
description: Define uma instância de classe.
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- Método SetClassInstance Direct3D 11
- Método SetClassInstance Direct3D 11, interface ID3DX11EffectInterfaceVariable
- Interface ID3DX11EffectInterfaceVariable Direct3D 11, método SetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968606"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a><span data-ttu-id="0de7e-106">Método ID3DX11EffectInterfaceVariable:: SetClassInstance</span><span class="sxs-lookup"><span data-stu-id="0de7e-106">ID3DX11EffectInterfaceVariable::SetClassInstance method</span></span>

<span data-ttu-id="0de7e-107">Define uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="0de7e-107">Sets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de7e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0de7e-108">Syntax</span></span>


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="0de7e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0de7e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de7e-110">*pEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="0de7e-110">*pEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="0de7e-111">Tipo: **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="0de7e-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="0de7e-112">Ponteiro para uma interface [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) .</span><span class="sxs-lookup"><span data-stu-id="0de7e-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de7e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0de7e-113">Return value</span></span>

<span data-ttu-id="0de7e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0de7e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0de7e-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0de7e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0de7e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0de7e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0de7e-117">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="0de7e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0de7e-118">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="0de7e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0de7e-119">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0de7e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0de7e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0de7e-120">Requirements</span></span>



| <span data-ttu-id="0de7e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0de7e-121">Requirement</span></span> | <span data-ttu-id="0de7e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0de7e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de7e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0de7e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0de7e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0de7e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0de7e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0de7e-125">Library</span></span><br/> | <dl> <span data-ttu-id="0de7e-126"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="0de7e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0de7e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0de7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de7e-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="0de7e-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





