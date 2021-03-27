---
title: Método Destroy ID3DX11DataProcessor (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Destrói o processador após a conclusão de um item de trabalho.
ms.assetid: 759641c0-ef86-42ee-88b9-3fcb7a171d86
keywords:
- Método Destroy Direct3D 11
- Método Destroy Direct3D 11, interface ID3DX11DataProcessor
- Interface ID3DX11DataProcessor Direct3D 11, método Destroy
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af92f8b3a22ba9a62258e8b24589a662eda22592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837978"
---
# <a name="id3dx11dataprocessordestroy-method"></a><span data-ttu-id="615f7-107">ID3DX11DataProcessor: método estroy de:D</span><span class="sxs-lookup"><span data-stu-id="615f7-107">ID3DX11DataProcessor::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="615f7-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="615f7-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="615f7-109">Destrói o processador após a conclusão de um item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="615f7-109">Destroys the processor after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="615f7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="615f7-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="615f7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="615f7-111">Parameters</span></span>

<span data-ttu-id="615f7-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="615f7-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="615f7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="615f7-113">Return value</span></span>

<span data-ttu-id="615f7-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="615f7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="615f7-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="615f7-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="615f7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="615f7-116">Remarks</span></span>

<span data-ttu-id="615f7-117">Esse método é usado por uma [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="615f7-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="615f7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="615f7-118">Requirements</span></span>



| <span data-ttu-id="615f7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="615f7-119">Requirement</span></span> | <span data-ttu-id="615f7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="615f7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="615f7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="615f7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="615f7-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="615f7-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="615f7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="615f7-123">Library</span></span><br/> | <dl> <span data-ttu-id="615f7-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="615f7-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="615f7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="615f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615f7-126">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="615f7-126">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="615f7-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="615f7-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





