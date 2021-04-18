---
description: Identifica dados de animação de quadro chave compactados.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Estrutura XFILECOMPRESSEDANIMATIONSET (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788012"
---
# <a name="xfilecompressedanimationset-structure"></a><span data-ttu-id="61e30-103">Estrutura XFILECOMPRESSEDANIMATIONSET</span><span class="sxs-lookup"><span data-stu-id="61e30-103">XFILECOMPRESSEDANIMATIONSET structure</span></span>

<span data-ttu-id="61e30-104">Identifica dados de animação de quadro chave compactados.</span><span class="sxs-lookup"><span data-stu-id="61e30-104">Identifies compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e30-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61e30-105">Syntax</span></span>


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a><span data-ttu-id="61e30-106">Membros</span><span class="sxs-lookup"><span data-stu-id="61e30-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="61e30-107">**CompressedBlockSize**</span><span class="sxs-lookup"><span data-stu-id="61e30-107">**CompressedBlockSize**</span></span>
</dt> <dd>

<span data-ttu-id="61e30-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61e30-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61e30-109">Tamanho total, em bytes, dos dados compactados no buffer de dados da animação do quadro chave compactado.</span><span class="sxs-lookup"><span data-stu-id="61e30-109">Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>

</dd> <dt>

<span data-ttu-id="61e30-110">**TicksPerSec**</span><span class="sxs-lookup"><span data-stu-id="61e30-110">**TicksPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="61e30-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61e30-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61e30-112">Número de tiques de quadros-chave de animação que ocorrem por segundo.</span><span class="sxs-lookup"><span data-stu-id="61e30-112">Number of animation key frame ticks that occur per second.</span></span>

</dd> <dt>

<span data-ttu-id="61e30-113">**Reproduztype**</span><span class="sxs-lookup"><span data-stu-id="61e30-113">**PlaybackType**</span></span>
</dt> <dd>

<span data-ttu-id="61e30-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61e30-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61e30-115">Tipo do loop de reprodução do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="61e30-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="61e30-116">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="61e30-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="61e30-117">**BufferLength**</span><span class="sxs-lookup"><span data-stu-id="61e30-117">**BufferLength**</span></span>
</dt> <dd>

<span data-ttu-id="61e30-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61e30-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="61e30-119">O tamanho mínimo do buffer, em bytes, necessário para manter os dados da animação do quadro chave compactado.</span><span class="sxs-lookup"><span data-stu-id="61e30-119">Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="61e30-120">Valor é igual a ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="61e30-120">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61e30-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61e30-121">Requirements</span></span>



| <span data-ttu-id="61e30-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="61e30-122">Requirement</span></span> | <span data-ttu-id="61e30-123">Valor</span><span class="sxs-lookup"><span data-stu-id="61e30-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61e30-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61e30-124">Header</span></span><br/> | <dl> <span data-ttu-id="61e30-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="61e30-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61e30-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="61e30-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e30-127">Estruturas de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="61e30-127">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="61e30-128">**ID3DXCompressedAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="61e30-128">**ID3DXCompressedAnimationSet**</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
