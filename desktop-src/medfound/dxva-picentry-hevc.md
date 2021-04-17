---
description: Especifica uma referência a uma superfície não compactada.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Estrutura de DXVA_PicEntry_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749517"
---
# <a name="dxva_picentry_hevc-structure"></a><span data-ttu-id="147f2-103">Estrutura de HEVC de DXVA \_ PicEntry \_</span><span class="sxs-lookup"><span data-stu-id="147f2-103">DXVA\_PicEntry\_HEVC structure</span></span>

<span data-ttu-id="147f2-104">Especifica uma referência a uma superfície não compactada.</span><span class="sxs-lookup"><span data-stu-id="147f2-104">Specifies a reference to an uncompressed surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="147f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="147f2-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a><span data-ttu-id="147f2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="147f2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="147f2-107">**Index7Bits**</span><span class="sxs-lookup"><span data-stu-id="147f2-107">**Index7Bits**</span></span>
</dt> <dd>

<span data-ttu-id="147f2-108">Um índice que identifica uma superfície não compactada.</span><span class="sxs-lookup"><span data-stu-id="147f2-108">An index that identifies an uncompressed surface .</span></span>

</dd> <dt>

<span data-ttu-id="147f2-109">**AssociatedFlag**</span><span class="sxs-lookup"><span data-stu-id="147f2-109">**AssociatedFlag**</span></span> 
</dt> <dd>

<span data-ttu-id="147f2-110">Sinalizador de 1 bit opcional associado à superfície.</span><span class="sxs-lookup"><span data-stu-id="147f2-110">Optional 1-bit flag associated with the surface.</span></span> <span data-ttu-id="147f2-111">O significado do sinalizador depende do contexto.</span><span class="sxs-lookup"><span data-stu-id="147f2-111">The meaning of the flag depends on the context.</span></span> <span data-ttu-id="147f2-112">Por exemplo, ele pode especificar se o quadro de referência é uma referência de longo prazo ou uma referência de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="147f2-112">For example, it can specify whether the reference frame is a long-term reference or a short-term reference.</span></span>

</dd> <dt>

<span data-ttu-id="147f2-113">**bPicEntry**</span><span class="sxs-lookup"><span data-stu-id="147f2-113">**bPicEntry**</span></span>
</dt> <dd>

<span data-ttu-id="147f2-114">Acessa todos os 8 bits da União.</span><span class="sxs-lookup"><span data-stu-id="147f2-114">Accesses the entire 8 bits of the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="147f2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="147f2-115">Requirements</span></span>



| <span data-ttu-id="147f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="147f2-116">Requirement</span></span> | <span data-ttu-id="147f2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="147f2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="147f2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="147f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="147f2-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="147f2-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="147f2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="147f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="147f2-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="147f2-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="147f2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="147f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="147f2-123"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="147f2-123"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="147f2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="147f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147f2-125">Estruturas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="147f2-125">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




