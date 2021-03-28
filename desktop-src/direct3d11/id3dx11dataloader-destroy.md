---
title: Método Destroy ID3DX11DataLoader (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Destrói o carregador após a conclusão de um item de trabalho.
ms.assetid: 5d86c4ad-3eb6-421f-bb77-c88e8f5b42bb
keywords:
- Método Destroy Direct3D 11
- Método Destroy Direct3D 11, interface ID3DX11DataLoader
- Interface ID3DX11DataLoader Direct3D 11, método Destroy
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Destroy
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c3a1c6511a00d66704c104b3b69150a8509e41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968706"
---
# <a name="id3dx11dataloaderdestroy-method"></a><span data-ttu-id="021e9-107">ID3DX11DataLoader: método estroy de:D</span><span class="sxs-lookup"><span data-stu-id="021e9-107">ID3DX11DataLoader::Destroy method</span></span>

> [!Note]  
> <span data-ttu-id="021e9-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="021e9-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="021e9-109">Destrói o carregador após a conclusão de um item de trabalho.</span><span class="sxs-lookup"><span data-stu-id="021e9-109">Destroys the loader after a work item completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="021e9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="021e9-110">Syntax</span></span>


```C++
HRESULT Destroy();
```



## <a name="parameters"></a><span data-ttu-id="021e9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="021e9-111">Parameters</span></span>

<span data-ttu-id="021e9-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="021e9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="021e9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="021e9-113">Return value</span></span>

<span data-ttu-id="021e9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="021e9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="021e9-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="021e9-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="021e9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="021e9-116">Remarks</span></span>

<span data-ttu-id="021e9-117">Esse método é usado por uma [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="021e9-117">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="021e9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="021e9-118">Requirements</span></span>



| <span data-ttu-id="021e9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="021e9-119">Requirement</span></span> | <span data-ttu-id="021e9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="021e9-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="021e9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="021e9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="021e9-122"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="021e9-122"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="021e9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="021e9-123">Library</span></span><br/> | <dl> <span data-ttu-id="021e9-124"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="021e9-124"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="021e9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="021e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021e9-126">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="021e9-126">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="021e9-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="021e9-127">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





