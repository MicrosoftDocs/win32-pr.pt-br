---
description: 'Forçar a envio de todos os sprites em lotes para o dispositivo. Os Estados do dispositivo permanecem como estavam após a última chamada para ID3DX10Sprite:: Begin. A lista de sprites em lote é desmarcada.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'Método ID3DX10Sprite:: flush (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791628"
---
# <a name="id3dx10spriteflush-method"></a><span data-ttu-id="9515c-105">Método ID3DX10Sprite:: flush</span><span class="sxs-lookup"><span data-stu-id="9515c-105">ID3DX10Sprite::Flush method</span></span>

<span data-ttu-id="9515c-106">Forçar a envio de todos os sprites em lotes para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9515c-106">Force all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="9515c-107">Os Estados do dispositivo permanecem como estavam após a última chamada para ID3DX10Sprite:: Begin.</span><span class="sxs-lookup"><span data-stu-id="9515c-107">Device states remain as they were after the last call to ID3DX10Sprite::Begin.</span></span> <span data-ttu-id="9515c-108">A lista de sprites em lote é desmarcada.</span><span class="sxs-lookup"><span data-stu-id="9515c-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="9515c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9515c-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="9515c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9515c-110">Parameters</span></span>

<span data-ttu-id="9515c-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9515c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9515c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9515c-112">Return value</span></span>

<span data-ttu-id="9515c-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9515c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9515c-114">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9515c-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9515c-115">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9515c-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9515c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9515c-116">Requirements</span></span>



| <span data-ttu-id="9515c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9515c-117">Requirement</span></span> | <span data-ttu-id="9515c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9515c-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9515c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9515c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9515c-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9515c-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9515c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9515c-121">Library</span></span><br/> | <dl> <span data-ttu-id="9515c-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9515c-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9515c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9515c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9515c-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="9515c-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="9515c-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9515c-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




