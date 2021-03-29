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
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968547"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="51670-104">Estrutura XMUINT4</span><span class="sxs-lookup"><span data-stu-id="51670-104">XMUINT4 structure</span></span>

<span data-ttu-id="51670-105">Descreve um vetor inteiro não assinado 4D.</span><span class="sxs-lookup"><span data-stu-id="51670-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="51670-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51670-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="51670-107">Membros</span><span class="sxs-lookup"><span data-stu-id="51670-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="51670-108">**x**</span><span class="sxs-lookup"><span data-stu-id="51670-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="51670-109">componente x do vetor.</span><span class="sxs-lookup"><span data-stu-id="51670-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="51670-110">**y**</span><span class="sxs-lookup"><span data-stu-id="51670-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="51670-111">componente y do vetor.</span><span class="sxs-lookup"><span data-stu-id="51670-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="51670-112">**z**</span><span class="sxs-lookup"><span data-stu-id="51670-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="51670-113">componente z do vetor.</span><span class="sxs-lookup"><span data-stu-id="51670-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="51670-114">**w**</span><span class="sxs-lookup"><span data-stu-id="51670-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="51670-115">componente w do vetor.</span><span class="sxs-lookup"><span data-stu-id="51670-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51670-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51670-116">Requirements</span></span>



| <span data-ttu-id="51670-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="51670-117">Requirement</span></span> | <span data-ttu-id="51670-118">Valor</span><span class="sxs-lookup"><span data-stu-id="51670-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51670-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51670-119">Header</span></span><br/> | <dl> <span data-ttu-id="51670-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="51670-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51670-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="51670-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51670-122">Estruturas</span><span class="sxs-lookup"><span data-stu-id="51670-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="51670-123">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="51670-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





