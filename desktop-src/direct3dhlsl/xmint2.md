---
title: Estrutura XMINT2
description: Descreve um vetor de inteiro 2D.
ms.assetid: 651f62f8-577d-4356-9bbc-0d4a9ca8fb01
keywords:
- XMINT2 estrutura HLSL
topic_type:
- apiref
api_name:
- XMINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e93e26933ad6b3829848e7e826d8d9685e9f141
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222854"
---
# <a name="xmint2-structure"></a><span data-ttu-id="abcec-104">Estrutura XMINT2</span><span class="sxs-lookup"><span data-stu-id="abcec-104">XMINT2 structure</span></span>

<span data-ttu-id="abcec-105">Descreve um vetor de inteiro 2D.</span><span class="sxs-lookup"><span data-stu-id="abcec-105">Describes an 2D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="abcec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abcec-106">Syntax</span></span>


``` syntax
typedef struct _XMINT2 {
  INT x;
  INT y;
} XMINT2;
```



## <a name="members"></a><span data-ttu-id="abcec-107">Membros</span><span class="sxs-lookup"><span data-stu-id="abcec-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="abcec-108">**x**</span><span class="sxs-lookup"><span data-stu-id="abcec-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="abcec-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="abcec-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="abcec-110">**y**</span><span class="sxs-lookup"><span data-stu-id="abcec-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="abcec-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="abcec-111">y-component of the vector.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="abcec-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="abcec-112">Remarks</span></span>

<span data-ttu-id="abcec-113">Essa estrutura é definida no ``D3DX\_DXGIFormatConvert.inl`` cabeçalho no SDK do DirectX (junho de 2010) para uso do C++.</span><span class="sxs-lookup"><span data-stu-id="abcec-113">This structure is defined in the ``D3DX\_DXGIFormatConvert.inl`` header in the DirectX SDK (June 2010) for use from C++.</span></span> <span data-ttu-id="abcec-114">A versão mais recente desse cabeçalho no pacote NuGet [Microsoft. DXSDK. D3DX não o](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) define, e se baseia em [DirectX:: XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) em DirectXMath em vez disso.</span><span class="sxs-lookup"><span data-stu-id="abcec-114">The latest version of this header in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet Package no longer defines it, and relies on [DirectX::XMINT2](https://docs.microsoft.com/en-us/windows/win32/api/directxmath/ns-directxmath-xmint2) in DirectXMath instead.</span></span>



## <a name="requirements"></a><span data-ttu-id="abcec-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abcec-115">Requirements</span></span>



| <span data-ttu-id="abcec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="abcec-116">Requirement</span></span> | <span data-ttu-id="abcec-117">Valor</span><span class="sxs-lookup"><span data-stu-id="abcec-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abcec-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abcec-118">Header</span></span><br/> | <dl> <span data-ttu-id="abcec-119"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="abcec-119"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abcec-120">Veja também</span><span class="sxs-lookup"><span data-stu-id="abcec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abcec-121">Estruturas</span><span class="sxs-lookup"><span data-stu-id="abcec-121">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="abcec-122">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="abcec-122">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>
