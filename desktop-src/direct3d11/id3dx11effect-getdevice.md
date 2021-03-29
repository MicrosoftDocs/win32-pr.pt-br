---
title: Método GetDevice ID3DX11Effect (D3dx11effect. h)
description: Obtenha o dispositivo que criou o efeito.
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- Método GetDevice Direct3D 11
- Método GetDevice Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, método GetDevice
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173134"
---
# <a name="id3dx11effectgetdevice-method"></a><span data-ttu-id="d659d-106">Método ID3DX11Effect:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="d659d-106">ID3DX11Effect::GetDevice method</span></span>

<span data-ttu-id="d659d-107">Obtenha o dispositivo que criou o efeito.</span><span class="sxs-lookup"><span data-stu-id="d659d-107">Get the device that created the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="d659d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d659d-108">Syntax</span></span>


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="d659d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d659d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d659d-110">*ppDevice*</span><span class="sxs-lookup"><span data-stu-id="d659d-110">*ppDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d659d-111">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span><span class="sxs-lookup"><span data-stu-id="d659d-111">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span></span>

<span data-ttu-id="d659d-112">Um ponteiro para um [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span><span class="sxs-lookup"><span data-stu-id="d659d-112">A pointer to an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d659d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d659d-113">Return value</span></span>

<span data-ttu-id="d659d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d659d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d659d-115">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d659d-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d659d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d659d-116">Remarks</span></span>

<span data-ttu-id="d659d-117">Um efeito é criado para um dispositivo específico, chamando uma função como [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="d659d-117">An effect is created for a specific device, by calling a function such as [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

> [!Note]  
> <span data-ttu-id="d659d-118">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="d659d-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d659d-119">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="d659d-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d659d-120">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d659d-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d659d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d659d-121">Requirements</span></span>



| <span data-ttu-id="d659d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d659d-122">Requirement</span></span> | <span data-ttu-id="d659d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d659d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d659d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d659d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d659d-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d659d-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d659d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d659d-126">Library</span></span><br/> | <dl> <span data-ttu-id="d659d-127"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="d659d-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d659d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d659d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d659d-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="d659d-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





