---
description: 'Chame isso após ID3DX10Sprite:: flush. Se \_ o estado de salvamento de Sprite do D3DX10 \_ \_ tiver sido especificado quando ID3DX10Sprite:: BEGIN for chamado, essa API restaurará o estado do dispositivo para como ele estava antes de ID3DX10Sprite:: Begin ser chamado.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'Método ID3DX10Sprite:: End (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762164"
---
# <a name="id3dx10spriteend-method"></a><span data-ttu-id="860b9-104">Método ID3DX10Sprite:: End</span><span class="sxs-lookup"><span data-stu-id="860b9-104">ID3DX10Sprite::End method</span></span>

<span data-ttu-id="860b9-105">Chame isso após ID3DX10Sprite:: flush.</span><span class="sxs-lookup"><span data-stu-id="860b9-105">Call this after ID3DX10Sprite::Flush.</span></span> <span data-ttu-id="860b9-106">Se \_ o estado de salvamento de Sprite do D3DX10 \_ \_ tiver sido especificado quando ID3DX10Sprite:: BEGIN for chamado, essa API restaurará o estado do dispositivo para como ele estava antes de ID3DX10Sprite:: Begin ser chamado.</span><span class="sxs-lookup"><span data-stu-id="860b9-106">If D3DX10\_SPRITE\_SAVE\_STATE was specified when ID3DX10Sprite::Begin was called, this API will restore the device state to how it was before ID3DX10Sprite::Begin was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="860b9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="860b9-107">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="860b9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="860b9-108">Parameters</span></span>

<span data-ttu-id="860b9-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="860b9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="860b9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="860b9-110">Return value</span></span>

<span data-ttu-id="860b9-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="860b9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="860b9-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="860b9-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="860b9-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="860b9-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="860b9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="860b9-114">Requirements</span></span>



| <span data-ttu-id="860b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="860b9-115">Requirement</span></span> | <span data-ttu-id="860b9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="860b9-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="860b9-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="860b9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="860b9-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="860b9-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="860b9-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="860b9-119">Library</span></span><br/> | <dl> <span data-ttu-id="860b9-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="860b9-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="860b9-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="860b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="860b9-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="860b9-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="860b9-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="860b9-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




