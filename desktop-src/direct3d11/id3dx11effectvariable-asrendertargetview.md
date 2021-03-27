---
title: Método ID3DX11EffectVariable AsRenderTargetView (D3dx11effect. h)
description: Obter uma variável render-Target-View.
ms.assetid: 1eec342e-267a-4eab-886a-a309758065c7
keywords:
- Método AsRenderTargetView Direct3D 11
- Método AsRenderTargetView Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, método AsRenderTargetView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRenderTargetView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca6270503ff786b3f4a319e3f068ba76acada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989426"
---
# <a name="id3dx11effectvariableasrendertargetview-method"></a><span data-ttu-id="2d8fb-106">Método ID3DX11EffectVariable:: AsRenderTargetView</span><span class="sxs-lookup"><span data-stu-id="2d8fb-106">ID3DX11EffectVariable::AsRenderTargetView method</span></span>

<span data-ttu-id="2d8fb-107">Obter uma variável render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-107">Get a render-target-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8fb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d8fb-108">Syntax</span></span>


```C++
ID3DX11EffectRenderTargetViewVariable* AsRenderTargetView();
```



## <a name="parameters"></a><span data-ttu-id="2d8fb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d8fb-109">Parameters</span></span>

<span data-ttu-id="2d8fb-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d8fb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d8fb-111">Return value</span></span>

<span data-ttu-id="2d8fb-112">Tipo: **[ **ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d8fb-112">Type: **[**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md)\***</span></span>

<span data-ttu-id="2d8fb-113">Um ponteiro para uma variável render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-113">A pointer to a render-target-view variable.</span></span> <span data-ttu-id="2d8fb-114">Consulte [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="2d8fb-114">See [**ID3DX11EffectRenderTargetViewVariable**](id3dx11effectrendertargetviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8fb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d8fb-115">Remarks</span></span>

<span data-ttu-id="2d8fb-116">Esse método retorna uma versão da variável de efeito que foi especializada para uma variável render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-116">This method returns a version of the effect variable that has been specialized to a render-target-view variable.</span></span> <span data-ttu-id="2d8fb-117">De forma semelhante a uma conversão, essa especialização retornará um objeto inválido se a variável de efeito não contiver dados de exibição de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain render-target-view data.</span></span>

<span data-ttu-id="2d8fb-118">Os aplicativos podem testar a validade do objeto retornado chamando [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="2d8fb-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="2d8fb-119">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2d8fb-120">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="2d8fb-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2d8fb-121">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2d8fb-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d8fb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d8fb-122">Requirements</span></span>



| <span data-ttu-id="2d8fb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d8fb-123">Requirement</span></span> | <span data-ttu-id="2d8fb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2d8fb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8fb-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d8fb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2d8fb-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d8fb-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2d8fb-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d8fb-127">Library</span></span><br/> | <dl> <span data-ttu-id="2d8fb-128"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="2d8fb-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d8fb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d8fb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d8fb-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="2d8fb-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





