---
title: Estrutura XMINT4
description: Descreve um vetor de inteiro 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- XMINT4 estrutura HLSL
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
ms.openlocfilehash: d532f3a2a2332874f7b7c22f17992c22984e3f86
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222834"
---
# <a name="xmint4-structure"></a><span data-ttu-id="5db81-104">Estrutura XMINT4</span><span class="sxs-lookup"><span data-stu-id="5db81-104">XMINT4 structure</span></span>

<span data-ttu-id="5db81-105">Descreve um vetor de inteiro 4D.</span><span class="sxs-lookup"><span data-stu-id="5db81-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db81-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5db81-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="5db81-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5db81-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5db81-108">**x**</span><span class="sxs-lookup"><span data-stu-id="5db81-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="5db81-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="5db81-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="5db81-110">**y**</span><span class="sxs-lookup"><span data-stu-id="5db81-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="5db81-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="5db81-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="5db81-112">**z**</span><span class="sxs-lookup"><span data-stu-id="5db81-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="5db81-113">componente z do vetor.</span><span class="sxs-lookup"><span data-stu-id="5db81-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="5db81-114">**w**</span><span class="sxs-lookup"><span data-stu-id="5db81-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="5db81-115">componente w do vetor.</span><span class="sxs-lookup"><span data-stu-id="5db81-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5db81-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5db81-116">Requirements</span></span>



| <span data-ttu-id="5db81-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5db81-117">Requirement</span></span> | <span data-ttu-id="5db81-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5db81-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db81-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5db81-119">Header</span></span><br/> | <dl> <span data-ttu-id="5db81-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="5db81-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="remarks"></a><span data-ttu-id="5db81-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5db81-121">Remarks</span></span>

<span data-ttu-id="5db81-122">Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` cabeçalho no SDK do DirectX (junho de 2010) para uso do C++.</span><span class="sxs-lookup"><span data-stu-id="5db81-122">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="5db81-123">A versão mais recente desse cabeçalho no pacote NuGet [Microsoft. DXSDK. D3DX não o](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) define, e se baseia em [DirectX:: XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) em DirectXMath em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5db81-123">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint4) in DirectXMath instead.</span></span>



## <a name="see-also"></a><span data-ttu-id="5db81-124">Veja também</span><span class="sxs-lookup"><span data-stu-id="5db81-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db81-125">Estruturas</span><span class="sxs-lookup"><span data-stu-id="5db81-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="5db81-126">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="5db81-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
