---
description: A estrutura ADDRESSPAIR constrói um filtro de captura.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Estrutura ADDRESSPAIR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787486"
---
# <a name="addresspair-structure"></a><span data-ttu-id="88617-103">Estrutura ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="88617-103">ADDRESSPAIR structure</span></span>

<span data-ttu-id="88617-104">A estrutura **ADDRESSPAIR** constrói um filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="88617-104">The **ADDRESSPAIR** structure constructs a capture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="88617-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88617-105">Syntax</span></span>


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a><span data-ttu-id="88617-106">Membros</span><span class="sxs-lookup"><span data-stu-id="88617-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88617-107">**AddressFlags**</span><span class="sxs-lookup"><span data-stu-id="88617-107">**AddressFlags**</span></span>
</dt> <dd>

<span data-ttu-id="88617-108">Sinalizadores que descrevem os endereços usados por um filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="88617-108">Flags that describe the addresses used by a capture filter.</span></span> <span data-ttu-id="88617-109">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="88617-109">See Remarks for more information.</span></span>



| <span data-ttu-id="88617-110">Valor</span><span class="sxs-lookup"><span data-stu-id="88617-110">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="88617-111">Significado</span><span class="sxs-lookup"><span data-stu-id="88617-111">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <span data-ttu-id="88617-112"><dt>**sinalizadores de endereço \_ \_ correspondem ao \_ DST**</dt></span><span class="sxs-lookup"><span data-stu-id="88617-112"><dt>**ADDRESS\_FLAGS\_MATCH\_DST**</dt></span></span> </dl>                 | <span data-ttu-id="88617-113">Corresponde ao endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="88617-113">Matches the destination address.</span></span><br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <span data-ttu-id="88617-114"><dt>**os \_ sinalizadores de endereço \_ correspondem \_ src**</dt></span><span class="sxs-lookup"><span data-stu-id="88617-114"><dt>**ADDRESS\_FLAGS\_MATCH\_SRC**</dt></span></span> </dl>                 | <span data-ttu-id="88617-115">Corresponde ao endereço de origem.</span><span class="sxs-lookup"><span data-stu-id="88617-115">Matches the source address.</span></span><br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <span data-ttu-id="88617-116"><dt>**sinalizadores de endereço \_ \_ excluídos**</dt></span><span class="sxs-lookup"><span data-stu-id="88617-116"><dt>**ADDRESS\_FLAGS\_EXCLUDED**</dt></span></span> </dl>                     | <span data-ttu-id="88617-117">Exclui o quadro se esse endereço for encontrado.</span><span class="sxs-lookup"><span data-stu-id="88617-117">Excludes the frame if this address is found.</span></span><br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <span data-ttu-id="88617-118"><dt>**Endereço do \_ grupo de horário de Verão dos sinalizadores de endereços \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="88617-118"><dt>**ADDRESS\_FLAGS\_DST\_GROUP\_ADDR**</dt></span></span> </dl> | <span data-ttu-id="88617-119">Corresponde somente ao grupo de bits.</span><span class="sxs-lookup"><span data-stu-id="88617-119">Matches group bit only.</span></span> <span data-ttu-id="88617-120">Use isso para mensagens de tipo de difusão.</span><span class="sxs-lookup"><span data-stu-id="88617-120">Use this for broadcast-type messages.</span></span><br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <span data-ttu-id="88617-121"><dt>**sinalizadores de endereço \_ \_ correspondem a \_ ambos**</dt></span><span class="sxs-lookup"><span data-stu-id="88617-121"><dt>**ADDRESS\_FLAGS\_MATCH\_BOTH**</dt></span></span> </dl>              | <span data-ttu-id="88617-122">Corresponde aos endereços de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="88617-122">Matches destination and source addresses.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="88617-123">**NalReserved**</span><span class="sxs-lookup"><span data-stu-id="88617-123">**NalReserved**</span></span>
</dt> <dd>

<span data-ttu-id="88617-124">Isso é reservado.</span><span class="sxs-lookup"><span data-stu-id="88617-124">This is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="88617-125">**DstAddress**</span><span class="sxs-lookup"><span data-stu-id="88617-125">**DstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88617-126">Endereço de destino do elemento de par de endereços.</span><span class="sxs-lookup"><span data-stu-id="88617-126">Destination address of the address pair element.</span></span>

</dd> <dt>

<span data-ttu-id="88617-127">**SrcAddress**</span><span class="sxs-lookup"><span data-stu-id="88617-127">**SrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="88617-128">Endereço de origem do elemento de par de endereços.</span><span class="sxs-lookup"><span data-stu-id="88617-128">Source address of the address pair element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88617-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="88617-129">Remarks</span></span>

<span data-ttu-id="88617-130">Os sinalizadores do membro **AddressFlags** podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="88617-130">The flags of the **AddressFlags** member can be combined.</span></span> <span data-ttu-id="88617-131">Por exemplo, a configuração a seguir excluirá o quadro se o endereço de origem especificado for detectado.</span><span class="sxs-lookup"><span data-stu-id="88617-131">For example the following setting excludes the frame if the specified source address is detected.</span></span>

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

<span data-ttu-id="88617-132">Para obter mais informações sobre como implementar essa estrutura, consulte [filtros de captura](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="88617-132">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88617-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88617-133">Requirements</span></span>



| <span data-ttu-id="88617-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="88617-134">Requirement</span></span> | <span data-ttu-id="88617-135">Valor</span><span class="sxs-lookup"><span data-stu-id="88617-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88617-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88617-136">Minimum supported client</span></span><br/> | <span data-ttu-id="88617-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88617-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="88617-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88617-138">Minimum supported server</span></span><br/> | <span data-ttu-id="88617-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88617-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88617-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="88617-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="88617-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="88617-141"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88617-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="88617-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88617-143">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="88617-143">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




