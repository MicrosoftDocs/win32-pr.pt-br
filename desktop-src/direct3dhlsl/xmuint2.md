---
title: Estrutura XMUINT2
description: Descreve um vetor inteiro sem sinal 2D.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- Estrutura XMUINT2 HLSL
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71168d08b8a91e09429a6f4e004c48c699635414
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549561"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="e7daa-104">Estrutura XMUINT2</span><span class="sxs-lookup"><span data-stu-id="e7daa-104">XMUINT2 structure</span></span>

<span data-ttu-id="e7daa-105">Descreve um vetor inteiro sem sinal 2D.</span><span class="sxs-lookup"><span data-stu-id="e7daa-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7daa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7daa-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="e7daa-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e7daa-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7daa-108">**x**</span><span class="sxs-lookup"><span data-stu-id="e7daa-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="e7daa-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="e7daa-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="e7daa-110">**y**</span><span class="sxs-lookup"><span data-stu-id="e7daa-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="e7daa-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="e7daa-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="e7daa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7daa-112">Remarks</span></span>

<span data-ttu-id="e7daa-113">Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` header no SDK do DirectX (junho de 2010) para uso do C++.</span><span class="sxs-lookup"><span data-stu-id="e7daa-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="e7daa-114">A versão mais recente desse header no Pacote NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) não o define mais e depende de [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) no DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="e7daa-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT2](/windows/win32/api/directxmath/ns-directxmath-xmuint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="e7daa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7daa-115">Requirements</span></span>



| <span data-ttu-id="e7daa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7daa-116">Requirement</span></span> | <span data-ttu-id="e7daa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e7daa-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7daa-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7daa-118">Header</span></span><br/> | <dl> <span data-ttu-id="e7daa-119"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="e7daa-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7daa-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7daa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7daa-121">Estruturas</span><span class="sxs-lookup"><span data-stu-id="e7daa-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="e7daa-122">Desempacotar e empacotar formato DXGI \_ para In-Place edição de imagem</span><span class="sxs-lookup"><span data-stu-id="e7daa-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>