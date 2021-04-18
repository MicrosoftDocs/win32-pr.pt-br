---
description: Descreve uma tabela de quantificação JPEG.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: Estrutura de DXGI_JPEG_QUANTIZATION_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751772"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a><span data-ttu-id="dcddd-103">\_Estrutura de \_ tabela de quantificação JPEG dxgi \_</span><span class="sxs-lookup"><span data-stu-id="dcddd-103">DXGI\_JPEG\_QUANTIZATION\_TABLE structure</span></span>

<span data-ttu-id="dcddd-104">Descreve uma tabela de quantificação JPEG.</span><span class="sxs-lookup"><span data-stu-id="dcddd-104">Describes a JPEG quantization table.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcddd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcddd-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a><span data-ttu-id="dcddd-106">Membros</span><span class="sxs-lookup"><span data-stu-id="dcddd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dcddd-107">**Elementos**</span><span class="sxs-lookup"><span data-stu-id="dcddd-107">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="dcddd-108">Uma matriz de bytes que contém os elementos da tabela quantização.</span><span class="sxs-lookup"><span data-stu-id="dcddd-108">An array of bytes containing the elements of the quantization table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dcddd-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcddd-109">Requirements</span></span>



| <span data-ttu-id="dcddd-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcddd-110">Requirement</span></span> | <span data-ttu-id="dcddd-111">Valor</span><span class="sxs-lookup"><span data-stu-id="dcddd-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcddd-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dcddd-112">Header</span></span><br/> | <dl> <span data-ttu-id="dcddd-113"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcddd-113"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcddd-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcddd-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcddd-115">Estruturas DXGI</span><span class="sxs-lookup"><span data-stu-id="dcddd-115">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




