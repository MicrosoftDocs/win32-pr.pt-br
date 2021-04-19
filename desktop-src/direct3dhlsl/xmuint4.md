---
title: Estrutura XMUINT4
description: Descreve um vetor inteiro não assinado 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- XMUINT4 estrutura HLSL
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
ms.openlocfilehash: 7e461d5b10f01f61de3fcfd721c4a6b1350c7d68
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222844"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="d2d0e-104">Estrutura XMUINT4</span><span class="sxs-lookup"><span data-stu-id="d2d0e-104">XMUINT4 structure</span></span>

<span data-ttu-id="d2d0e-105">Descreve um vetor inteiro não assinado 4D.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d0e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2d0e-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="d2d0e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d2d0e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d2d0e-108">**x**</span><span class="sxs-lookup"><span data-stu-id="d2d0e-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="d2d0e-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="d2d0e-110">**y**</span><span class="sxs-lookup"><span data-stu-id="d2d0e-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="d2d0e-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="d2d0e-112">**z**</span><span class="sxs-lookup"><span data-stu-id="d2d0e-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="d2d0e-113">componente z do vetor.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="d2d0e-114">**w**</span><span class="sxs-lookup"><span data-stu-id="d2d0e-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="d2d0e-115">componente w do vetor.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>




## <a name="remarks"></a><span data-ttu-id="d2d0e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2d0e-116">Remarks</span></span>

<span data-ttu-id="d2d0e-117">Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` cabeçalho no SDK do DirectX (junho de 2010) para uso do C++.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-117">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="d2d0e-118">A versão mais recente desse cabeçalho no pacote NuGet [Microsoft. DXSDK. D3DX não o](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) define, e se baseia em [DirectX:: XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) em DirectXMath em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-118">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMUINT4](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmuint4) in DirectXMath instead.</span></span>




## <a name="requirements"></a><span data-ttu-id="d2d0e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2d0e-119">Requirements</span></span>



| <span data-ttu-id="d2d0e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d0e-120">Requirement</span></span> | <span data-ttu-id="d2d0e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d2d0e-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d0e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2d0e-122">Header</span></span><br/> | <dl> <span data-ttu-id="d2d0e-123"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="d2d0e-123"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d0e-124">Veja também</span><span class="sxs-lookup"><span data-stu-id="d2d0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d0e-125">Estruturas</span><span class="sxs-lookup"><span data-stu-id="d2d0e-125">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="d2d0e-126">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="d2d0e-126">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
