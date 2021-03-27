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
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298725"
---
# <a name="xmint4-structure"></a><span data-ttu-id="e1ca2-104">Estrutura XMINT4</span><span class="sxs-lookup"><span data-stu-id="e1ca2-104">XMINT4 structure</span></span>

<span data-ttu-id="e1ca2-105">Descreve um vetor de inteiro 4D.</span><span class="sxs-lookup"><span data-stu-id="e1ca2-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ca2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1ca2-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="e1ca2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e1ca2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1ca2-108">**x**</span><span class="sxs-lookup"><span data-stu-id="e1ca2-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="e1ca2-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="e1ca2-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="e1ca2-110">**y**</span><span class="sxs-lookup"><span data-stu-id="e1ca2-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="e1ca2-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="e1ca2-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="e1ca2-112">**z**</span><span class="sxs-lookup"><span data-stu-id="e1ca2-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="e1ca2-113">componente z do vetor.</span><span class="sxs-lookup"><span data-stu-id="e1ca2-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="e1ca2-114">**w**</span><span class="sxs-lookup"><span data-stu-id="e1ca2-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="e1ca2-115">componente w do vetor.</span><span class="sxs-lookup"><span data-stu-id="e1ca2-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1ca2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1ca2-116">Requirements</span></span>



| <span data-ttu-id="e1ca2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1ca2-117">Requirement</span></span> | <span data-ttu-id="e1ca2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ca2-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ca2-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1ca2-119">Header</span></span><br/> | <dl> <span data-ttu-id="e1ca2-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e1ca2-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ca2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1ca2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ca2-122">Estruturas</span><span class="sxs-lookup"><span data-stu-id="e1ca2-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="e1ca2-123">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="e1ca2-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





