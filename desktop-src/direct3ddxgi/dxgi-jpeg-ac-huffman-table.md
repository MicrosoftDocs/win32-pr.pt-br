---
description: Descreve uma tabela de Huffman de AC JPEG.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: Estrutura de DXGI_JPEG_AC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764198"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a><span data-ttu-id="75d65-103">Estrutura de tabela do DXGI \_ JPEG \_ AC- \_ HUFFMAN \_</span><span class="sxs-lookup"><span data-stu-id="75d65-103">DXGI\_JPEG\_AC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="75d65-104">Descreve uma tabela de Huffman de AC JPEG.</span><span class="sxs-lookup"><span data-stu-id="75d65-104">Describes a JPEG AC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d65-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75d65-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="75d65-106">Membros</span><span class="sxs-lookup"><span data-stu-id="75d65-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="75d65-107">**CodeCounts**</span><span class="sxs-lookup"><span data-stu-id="75d65-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="75d65-108">O número de códigos para cada comprimento de código.</span><span class="sxs-lookup"><span data-stu-id="75d65-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="75d65-109">**CodeValues**</span><span class="sxs-lookup"><span data-stu-id="75d65-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="75d65-110">Os valores do código Huffman, em ordem de aumento do tamanho do código.</span><span class="sxs-lookup"><span data-stu-id="75d65-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75d65-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75d65-111">Requirements</span></span>



| <span data-ttu-id="75d65-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="75d65-112">Requirement</span></span> | <span data-ttu-id="75d65-113">Valor</span><span class="sxs-lookup"><span data-stu-id="75d65-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75d65-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75d65-114">Header</span></span><br/> | <dl> <span data-ttu-id="75d65-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="75d65-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d65-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="75d65-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d65-117">Estruturas DXGI</span><span class="sxs-lookup"><span data-stu-id="75d65-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




