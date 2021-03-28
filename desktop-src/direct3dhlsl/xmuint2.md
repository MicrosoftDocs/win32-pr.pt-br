---
title: Estrutura XMUINT2
description: Descreve um vetor inteiro sem sinal 2D.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- XMUINT2 estrutura HLSL
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
ms.openlocfilehash: 73d14bd43ec3b75a2bf503b7d742b6c69881475b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968546"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="c9cf1-104">Estrutura XMUINT2</span><span class="sxs-lookup"><span data-stu-id="c9cf1-104">XMUINT2 structure</span></span>

<span data-ttu-id="c9cf1-105">Descreve um vetor inteiro sem sinal 2D.</span><span class="sxs-lookup"><span data-stu-id="c9cf1-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cf1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9cf1-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="c9cf1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c9cf1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9cf1-108">**x**</span><span class="sxs-lookup"><span data-stu-id="c9cf1-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="c9cf1-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="c9cf1-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="c9cf1-110">**y**</span><span class="sxs-lookup"><span data-stu-id="c9cf1-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="c9cf1-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="c9cf1-111">y-component of the vector.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9cf1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9cf1-112">Requirements</span></span>



| <span data-ttu-id="c9cf1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9cf1-113">Requirement</span></span> | <span data-ttu-id="c9cf1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c9cf1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cf1-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9cf1-115">Header</span></span><br/> | <dl> <span data-ttu-id="c9cf1-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9cf1-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9cf1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cf1-118">Estruturas</span><span class="sxs-lookup"><span data-stu-id="c9cf1-118">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="c9cf1-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="c9cf1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





