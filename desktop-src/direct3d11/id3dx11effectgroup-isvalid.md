---
title: Método IsValid ID3DX11EffectGroup (D3dx11effect. h)
description: Teste um efeito para ver se ele contém uma sintaxe válida. | Método IsValid ID3DX11EffectGroup (D3dx11effect. h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- Método IsValid Direct3D 11
- Método IsValid Direct3D 11, interface ID3DX11EffectGroup
- Interface ID3DX11EffectGroup Direct3D 11, método IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d1fd110a0f35f8a288517d72b69a6f5ad9f0ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968609"
---
# <a name="id3dx11effectgroupisvalid-method"></a><span data-ttu-id="12665-107">Método ID3DX11EffectGroup:: IsValid</span><span class="sxs-lookup"><span data-stu-id="12665-107">ID3DX11EffectGroup::IsValid method</span></span>

<span data-ttu-id="12665-108">Teste um efeito para ver se ele contém uma sintaxe válida.</span><span class="sxs-lookup"><span data-stu-id="12665-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="12665-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12665-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="12665-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12665-110">Parameters</span></span>

<span data-ttu-id="12665-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="12665-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12665-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12665-112">Return value</span></span>

<span data-ttu-id="12665-113">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12665-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="12665-114">**True** se a sintaxe do código for válida; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="12665-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="12665-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="12665-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="12665-116">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="12665-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="12665-117">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="12665-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="12665-118">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="12665-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12665-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12665-119">Requirements</span></span>



| <span data-ttu-id="12665-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12665-120">Requirement</span></span> | <span data-ttu-id="12665-121">Valor</span><span class="sxs-lookup"><span data-stu-id="12665-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12665-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12665-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12665-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="12665-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="12665-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12665-124">Library</span></span><br/> | <dl> <span data-ttu-id="12665-125"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="12665-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12665-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="12665-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12665-127">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="12665-127">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

