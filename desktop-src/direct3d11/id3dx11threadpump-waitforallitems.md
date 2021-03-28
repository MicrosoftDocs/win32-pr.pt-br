---
title: Método ID3DX11ThreadPump WaitForAllItems (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Aguarda a conclusão de todos os itens de trabalho na bomba do thread.
ms.assetid: 6dfdaee8-e563-4c37-a2c1-4b115e29c434
keywords:
- Método WaitForAllItems Direct3D 11
- Método WaitForAllItems Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, método WaitForAllItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.WaitForAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40abbab67d6743be2190d5e81c733f63b52b32f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989316"
---
# <a name="id3dx11threadpumpwaitforallitems-method"></a><span data-ttu-id="87cf9-107">Método ID3DX11ThreadPump:: WaitForAllItems</span><span class="sxs-lookup"><span data-stu-id="87cf9-107">ID3DX11ThreadPump::WaitForAllItems method</span></span>

> [!Note]  
> <span data-ttu-id="87cf9-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="87cf9-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="87cf9-109">Aguarda a conclusão de todos os itens de trabalho na bomba do thread.</span><span class="sxs-lookup"><span data-stu-id="87cf9-109">Waits for all work items in the thread pump to finish.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cf9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87cf9-110">Syntax</span></span>


```C++
HRESULT WaitForAllItems();
```



## <a name="parameters"></a><span data-ttu-id="87cf9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87cf9-111">Parameters</span></span>

<span data-ttu-id="87cf9-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="87cf9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87cf9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87cf9-113">Return value</span></span>

<span data-ttu-id="87cf9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="87cf9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="87cf9-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="87cf9-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87cf9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87cf9-116">Requirements</span></span>



| <span data-ttu-id="87cf9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="87cf9-117">Requirement</span></span> | <span data-ttu-id="87cf9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="87cf9-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87cf9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87cf9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="87cf9-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="87cf9-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="87cf9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87cf9-121">Library</span></span><br/> | <dl> <span data-ttu-id="87cf9-122"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87cf9-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87cf9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="87cf9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cf9-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="87cf9-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="87cf9-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="87cf9-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





