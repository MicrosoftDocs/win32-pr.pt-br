---
description: A estrutura ADDRESStable contém uma tabela de pares de endereços.
ms.assetid: 84577b6c-9d43-4e53-9f8d-33685329b11d
title: Estrutura de ADDRESStable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 41acab19f83fdcc88a384c0407b666a7f641a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461230"
---
# <a name="addresstable-structure"></a><span data-ttu-id="e165e-103">Estrutura de endereço de endereçamento</span><span class="sxs-lookup"><span data-stu-id="e165e-103">ADDRESSTABLE structure</span></span>

<span data-ttu-id="e165e-104">A estrutura **AddressTable** contém uma tabela de pares de endereços.</span><span class="sxs-lookup"><span data-stu-id="e165e-104">The **ADDRESSTABLE** structure contains a table of address pairs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e165e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e165e-105">Syntax</span></span>


```C++
typedef struct _ADDRESSTABLE {
  DWORD       nAddressPairs;
  DWORD       nNonMacAddressPairs;
  ADDRESSPAIR AddressPair[MAX_ADDRESS_PAIRS];
} ADDRESSTABLE, *LPADDRESSTABLE;
```



## <a name="members"></a><span data-ttu-id="e165e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e165e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e165e-107">**nAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="e165e-107">**nAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="e165e-108">Número de pares de endereços na matriz **AddressPair** .</span><span class="sxs-lookup"><span data-stu-id="e165e-108">Number of address pairs in the **AddressPair** array.</span></span>

</dd> <dt>

<span data-ttu-id="e165e-109">**nNonMacAddressPairs**</span><span class="sxs-lookup"><span data-stu-id="e165e-109">**nNonMacAddressPairs**</span></span>
</dt> <dd>

<span data-ttu-id="e165e-110">Número de pares de endereços não MAC.</span><span class="sxs-lookup"><span data-stu-id="e165e-110">Number of non-MAC address pairs.</span></span>

</dd> <dt>

<span data-ttu-id="e165e-111">**AddressPair**</span><span class="sxs-lookup"><span data-stu-id="e165e-111">**AddressPair**</span></span>
</dt> <dd>

<span data-ttu-id="e165e-112">Matriz de pares de endereços.</span><span class="sxs-lookup"><span data-stu-id="e165e-112">Array of address pairs.</span></span> <span data-ttu-id="e165e-113">Observe que você só pode armazenar até oito pares de endereços por estrutura de endereço.</span><span class="sxs-lookup"><span data-stu-id="e165e-113">Note that you may only store up to eight address pairs per ADDRESSTABLE structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e165e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e165e-114">Remarks</span></span>

<span data-ttu-id="e165e-115">Use essa estrutura como parte do processo de construção do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="e165e-115">Use this structure as part of the capture filter construction process.</span></span> <span data-ttu-id="e165e-116">Para obter mais informações sobre como implementar essa estrutura, consulte [filtros de captura](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e165e-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e165e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e165e-117">Requirements</span></span>



| <span data-ttu-id="e165e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e165e-118">Requirement</span></span> | <span data-ttu-id="e165e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e165e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e165e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e165e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e165e-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e165e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e165e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e165e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e165e-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e165e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e165e-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e165e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e165e-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e165e-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e165e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e165e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e165e-127">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="e165e-127">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="e165e-128">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="e165e-128">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




