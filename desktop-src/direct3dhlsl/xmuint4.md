---
title: Estrutura XMUINT4
description: Descreve um vetor inteiro sem sinal 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- Estrutura XMUINT4 HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e424b4e5fd1c97f5aec01571d887b54dbb143b7
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549891"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="87244-104">Estrutura XMUINT4</span><span class="sxs-lookup"><span data-stu-id="87244-104">XMUINT4 structure</span></span>

<span data-ttu-id="87244-105">Descreve um vetor inteiro sem sinal 4D.</span><span class="sxs-lookup"><span data-stu-id="87244-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="87244-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87244-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="87244-107">Membros</span><span class="sxs-lookup"><span data-stu-id="87244-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="87244-108">**x**</span><span class="sxs-lookup"><span data-stu-id="87244-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="87244-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="87244-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="87244-110">**y**</span><span class="sxs-lookup"><span data-stu-id="87244-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="87244-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="87244-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="87244-112">**Z**</span><span class="sxs-lookup"><span data-stu-id="87244-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="87244-113">z-component do vetor.</span><span class="sxs-lookup"><span data-stu-id="87244-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="87244-114">**w**</span><span class="sxs-lookup"><span data-stu-id="87244-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="87244-115">w-component do vetor.</span><span class="sxs-lookup"><span data-stu-id="87244-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="87244-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="87244-116">Remarks</span></span>

<span data-ttu-id="87244-117">Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` header no SDK do DirectX (junho de 2010) para uso do C++.</span><span class="sxs-lookup"><span data-stu-id="87244-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="87244-118">A versão mais recente desse header no Pacote NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) não o define mais e depende de [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) no DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="87244-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="87244-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87244-119">Requirements</span></span>



| <span data-ttu-id="87244-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="87244-120">Requirement</span></span> | <span data-ttu-id="87244-121">Valor</span><span class="sxs-lookup"><span data-stu-id="87244-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87244-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87244-122">Header</span></span><br/> | <dl> <span data-ttu-id="87244-123"><dt>D3DX \_ DXGIFormatConvert.inl</dt></span><span class="sxs-lookup"><span data-stu-id="87244-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87244-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="87244-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87244-125">Estruturas</span><span class="sxs-lookup"><span data-stu-id="87244-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="87244-126">Desempacotar e empacotar formato DXGI \_ para In-Place edição de imagem</span><span class="sxs-lookup"><span data-stu-id="87244-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>