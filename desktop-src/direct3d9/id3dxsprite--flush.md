---
description: 'Força a envio de todos os sprites em lotes para o dispositivo. Os Estados do dispositivo permanecem como estavam após a última chamada para ID3DXSprite:: Begin. A lista de sprites em lote é desmarcada.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'Método ID3DXSprite:: flush (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105766417"
---
# <a name="id3dxspriteflush-method"></a><span data-ttu-id="4814a-105">Método ID3DXSprite:: flush</span><span class="sxs-lookup"><span data-stu-id="4814a-105">ID3DXSprite::Flush method</span></span>

<span data-ttu-id="4814a-106">Força a envio de todos os sprites em lotes para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4814a-106">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="4814a-107">Os Estados do dispositivo permanecem como estavam após a última chamada para [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="4814a-107">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="4814a-108">A lista de sprites em lote é desmarcada.</span><span class="sxs-lookup"><span data-stu-id="4814a-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="4814a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4814a-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="4814a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4814a-110">Parameters</span></span>

<span data-ttu-id="4814a-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4814a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4814a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4814a-112">Return value</span></span>

<span data-ttu-id="4814a-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4814a-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4814a-114">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4814a-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4814a-115">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="4814a-115">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="4814a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4814a-116">Requirements</span></span>



| <span data-ttu-id="4814a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4814a-117">Requirement</span></span> | <span data-ttu-id="4814a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4814a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4814a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4814a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4814a-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4814a-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4814a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4814a-121">Library</span></span><br/> | <dl> <span data-ttu-id="4814a-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4814a-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4814a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4814a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4814a-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="4814a-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="4814a-125">**ID3DXSprite:: End**</span><span class="sxs-lookup"><span data-stu-id="4814a-125">**ID3DXSprite::End**</span></span>](id3dxsprite--end.md)
</dt> </dl>

 

 




