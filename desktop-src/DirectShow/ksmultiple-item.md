---
description: A \_ estrutura do item KSMULTIPLE descreve o tamanho e a contagem de propriedades de comprimento variável em Pins do modo kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: Estrutura de KSMULTIPLE_ITEM (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759495"
---
# <a name="ksmultiple_item-structure"></a><span data-ttu-id="1d4de-103">\_Estrutura de item KSMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="1d4de-103">KSMULTIPLE\_ITEM structure</span></span>

<span data-ttu-id="1d4de-104">A `KSMULTIPLE_ITEM` estrutura descreve o tamanho e a contagem de propriedades de comprimento variável em Pins do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="1d4de-104">The `KSMULTIPLE_ITEM` structure describes the size and count of variable-length properties on kernel-mode pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d4de-105">Syntax</span></span>


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a><span data-ttu-id="1d4de-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1d4de-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d4de-107">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="1d4de-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="1d4de-108">Tamanho do bloco de memória retornado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="1d4de-108">Size of the returned memory block, in bytes.</span></span> <span data-ttu-id="1d4de-109">O tamanho inclui a estrutura do **\_ Item KSMULTIPLE** e os itens que o seguem.</span><span class="sxs-lookup"><span data-stu-id="1d4de-109">The size includes the **KSMULTIPLE\_ITEM** structure and the items that follow it.</span></span>

</dd> <dt>

<span data-ttu-id="1d4de-110">**Count**</span><span class="sxs-lookup"><span data-stu-id="1d4de-110">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="1d4de-111">Especifica o número total de itens que seguem essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="1d4de-111">Specifies the total number of items that follow this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d4de-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d4de-112">Requirements</span></span>



| <span data-ttu-id="1d4de-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4de-113">Requirement</span></span> | <span data-ttu-id="1d4de-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1d4de-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="1d4de-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d4de-115">Header</span></span><br/> | <dl> <span data-ttu-id="1d4de-116"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4de-116"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4de-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d4de-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4de-118">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="1d4de-118">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="1d4de-119">**IKsPin::KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="1d4de-119">**IKsPin::KsQueryMediums**</span></span>](ikspin-ksquerymediums.md)
</dt> <dt>

[<span data-ttu-id="1d4de-120">**REGPINMEDIUM**</span><span class="sxs-lookup"><span data-stu-id="1d4de-120">**REGPINMEDIUM**</span></span>](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




