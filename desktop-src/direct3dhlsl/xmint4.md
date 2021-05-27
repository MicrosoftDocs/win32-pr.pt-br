---
title: Estrutura XMINT4
description: Descreve um vetor inteiro 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- HLSL da estrutura XMINT4
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead9e7da8d48025c456ae6e57b0ffe64cdb00f46
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549951"
---
# <a name="xmint4-structure"></a><span data-ttu-id="6e6d0-104">Estrutura XMINT4</span><span class="sxs-lookup"><span data-stu-id="6e6d0-104">XMINT4 structure</span></span>

<span data-ttu-id="6e6d0-105">Descreve um vetor inteiro 4D.</span><span class="sxs-lookup"><span data-stu-id="6e6d0-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e6d0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e6d0-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="6e6d0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="6e6d0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e6d0-108">**x**</span><span class="sxs-lookup"><span data-stu-id="6e6d0-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="6e6d0-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="6e6d0-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="6e6d0-110">**y**</span><span class="sxs-lookup"><span data-stu-id="6e6d0-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="6e6d0-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="6e6d0-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="6e6d0-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="6e6d0-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="6e6d0-113">z-component do vetor.</span><span class="sxs-lookup"><span data-stu-id="6e6d0-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="6e6d0-114">**w**</span><span class="sxs-lookup"><span data-stu-id="6e6d0-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="6e6d0-115">w-component do vetor.</span><span class="sxs-lookup"><span data-stu-id="6e6d0-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e6d0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e6d0-116">Requirements</span></span>



| <span data-ttu-id="6e6d0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e6d0-117">Requirement</span></span> | <span data-ttu-id="6e6d0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6e6d0-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6d0-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e6d0-119">Header</span></span><br/> | <dl> <span data-ttu-id="6e6d0-120"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="6e6d0-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="6e6d0-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e6d0-121">Remarks</span></span>

<span data-ttu-id="6e6d0-122">Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` header no SDK do DirectX (junho de 2010) para uso do C++.</span><span class="sxs-lookup"><span data-stu-id="6e6d0-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="6e6d0-123">A versão mais recente desse header no Pacote NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) não o define mais e depende de [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) no DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="6e6d0-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="6e6d0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e6d0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e6d0-125">Estruturas</span><span class="sxs-lookup"><span data-stu-id="6e6d0-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="6e6d0-126">Desempacotar e empacotar formato DXGI \_ para In-Place edição de imagem</span><span class="sxs-lookup"><span data-stu-id="6e6d0-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>