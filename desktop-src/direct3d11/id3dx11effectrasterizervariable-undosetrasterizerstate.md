---
title: Método ID3DX11EffectRasterizerVariable UndoSetRasterizerState (D3dx11effect. h)
description: Reverte um estado de rasterizador definido anteriormente.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Método UndoSetRasterizerState Direct3D 11
- Método UndoSetRasterizerState Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, método UndoSetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173203"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a><span data-ttu-id="b5085-106">Método ID3DX11EffectRasterizerVariable:: UndoSetRasterizerState</span><span class="sxs-lookup"><span data-stu-id="b5085-106">ID3DX11EffectRasterizerVariable::UndoSetRasterizerState method</span></span>

<span data-ttu-id="b5085-107">Reverte um estado de rasterizador definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b5085-107">Reverts a previously set rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5085-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5085-108">Syntax</span></span>


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="b5085-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5085-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5085-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="b5085-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="b5085-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b5085-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b5085-112">Indexe em uma matriz de interfaces do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="b5085-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="b5085-113">Se houver apenas uma interface do rasterizador, use 0.</span><span class="sxs-lookup"><span data-stu-id="b5085-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5085-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5085-114">Return value</span></span>

<span data-ttu-id="b5085-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5085-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5085-116">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b5085-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5085-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5085-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5085-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="b5085-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b5085-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="b5085-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b5085-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b5085-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5085-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5085-121">Requirements</span></span>



| <span data-ttu-id="b5085-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5085-122">Requirement</span></span> | <span data-ttu-id="b5085-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b5085-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5085-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5085-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b5085-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5085-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b5085-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5085-126">Library</span></span><br/> | <dl> <span data-ttu-id="b5085-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="b5085-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5085-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5085-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5085-129">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="b5085-129">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

