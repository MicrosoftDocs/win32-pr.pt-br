---
description: Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave armazenado em um formato de dados compactado.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interface ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105756795"
---
# <a name="id3dxcompressedanimationset-interface"></a><span data-ttu-id="5c185-103">Interface ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5c185-103">ID3DXCompressedAnimationSet interface</span></span>

<span data-ttu-id="5c185-104">Um aplicativo usa os métodos dessa interface para implementar um conjunto de animações de quadro chave armazenado em um formato de dados compactado.</span><span class="sxs-lookup"><span data-stu-id="5c185-104">An application uses the methods of this interface to implement a key frame animation set stored in a compressed data format.</span></span>

## <a name="members"></a><span data-ttu-id="5c185-105">Membros</span><span class="sxs-lookup"><span data-stu-id="5c185-105">Members</span></span>

<span data-ttu-id="5c185-106">A interface **ID3DXCompressedAnimationSet** herda de [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="5c185-106">The **ID3DXCompressedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="5c185-107">**ID3DXCompressedAnimationSet** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5c185-107">**ID3DXCompressedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="5c185-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c185-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5c185-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c185-109">Methods</span></span>

<span data-ttu-id="5c185-110">A interface **ID3DXCompressedAnimationSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5c185-110">The **ID3DXCompressedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="5c185-111">Método</span><span class="sxs-lookup"><span data-stu-id="5c185-111">Method</span></span>                                                                                  | <span data-ttu-id="5c185-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c185-112">Description</span></span>                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="5c185-113">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="5c185-113">**GetCallbackKeys**</span></span>](id3dxcompressedanimationset--getcallbackkeys.md)                 | <span data-ttu-id="5c185-114">Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="5c185-114">Fills an array with callback key data used for key frame animation.</span></span><br/>   |
| [<span data-ttu-id="5c185-115">**GetCompressedData**</span><span class="sxs-lookup"><span data-stu-id="5c185-115">**GetCompressedData**</span></span>](id3dxcompressedanimationset--getcompresseddata.md)             | <span data-ttu-id="5c185-116">Obtém o buffer de dados que armazena dados de animação de quadro chave compactados.</span><span class="sxs-lookup"><span data-stu-id="5c185-116">Gets the data buffer that stores compressed key frame animation data.</span></span><br/> |
| [<span data-ttu-id="5c185-117">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="5c185-117">**GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)           | <span data-ttu-id="5c185-118">Obtém o número de chaves de retorno de chamada no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="5c185-118">Gets the number of callback keys in the animation set.</span></span><br/>                |
| [<span data-ttu-id="5c185-119">**Getreproduzirtype**</span><span class="sxs-lookup"><span data-stu-id="5c185-119">**GetPlaybackType**</span></span>](id3dxcompressedanimationset--getplaybacktype.md)                 | <span data-ttu-id="5c185-120">Obtém o tipo do loop de reprodução do conjunto de animação.</span><span class="sxs-lookup"><span data-stu-id="5c185-120">Gets the type of the animation set playback loop.</span></span><br/>                     |
| [<span data-ttu-id="5c185-121">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="5c185-121">**GetSourceTicksPerSecond**</span></span>](id3dxcompressedanimationset--getsourcetickspersecond.md) | <span data-ttu-id="5c185-122">Obtém o número de tiques de quadros-chave de animação que ocorrem por segundo.</span><span class="sxs-lookup"><span data-stu-id="5c185-122">Gets the number of animation key frame ticks that occur per second.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="5c185-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c185-123">Remarks</span></span>

<span data-ttu-id="5c185-124">Crie uma animação de quadro chave de formato compactado definida com [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="5c185-124">Create a compressed-format key frame animation set with [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span></span>

<span data-ttu-id="5c185-125">O tipo LPD3DXCOMPRESSEDANIMATIONSET é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="5c185-125">The LPD3DXCOMPRESSEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="5c185-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c185-126">Requirements</span></span>



| <span data-ttu-id="5c185-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c185-127">Requirement</span></span> | <span data-ttu-id="5c185-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5c185-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c185-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c185-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5c185-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c185-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5c185-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c185-131">Library</span></span><br/> | <dl> <span data-ttu-id="5c185-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c185-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c185-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c185-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c185-134">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="5c185-134">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="5c185-135">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5c185-135">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




