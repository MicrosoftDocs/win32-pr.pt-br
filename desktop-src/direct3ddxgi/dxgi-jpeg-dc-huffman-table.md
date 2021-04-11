---
description: Descreve uma tabela de Huffman de DC JPEG.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: Estrutura de DXGI_JPEG_DC_HUFFMAN_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172975"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a><span data-ttu-id="1205a-103">\_Estrutura de \_ tabela de HUFFMAN de CD \_ \_ de dxgi JPEG2000</span><span class="sxs-lookup"><span data-stu-id="1205a-103">DXGI\_JPEG\_DC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="1205a-104">Descreve uma tabela de Huffman de DC JPEG.</span><span class="sxs-lookup"><span data-stu-id="1205a-104">Describes a JPEG DC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1205a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1205a-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="1205a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1205a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1205a-107">**CodeCounts**</span><span class="sxs-lookup"><span data-stu-id="1205a-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="1205a-108">O número de códigos para cada comprimento de código.</span><span class="sxs-lookup"><span data-stu-id="1205a-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="1205a-109">**CodeValues**</span><span class="sxs-lookup"><span data-stu-id="1205a-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="1205a-110">Os valores do código Huffman, em ordem de aumento do tamanho do código.</span><span class="sxs-lookup"><span data-stu-id="1205a-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1205a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1205a-111">Requirements</span></span>



| <span data-ttu-id="1205a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1205a-112">Requirement</span></span> | <span data-ttu-id="1205a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1205a-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1205a-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1205a-114">Header</span></span><br/> | <dl> <span data-ttu-id="1205a-115"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="1205a-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1205a-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="1205a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1205a-117">Estruturas DXGI</span><span class="sxs-lookup"><span data-stu-id="1205a-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




