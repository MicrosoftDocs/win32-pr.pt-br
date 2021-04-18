---
description: A estrutura CAPTUREFILTER contém dados de filtro de captura.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Estrutura CAPTUREFILTER (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758297"
---
# <a name="capturefilter-structure"></a><span data-ttu-id="d15b3-103">Estrutura CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="d15b3-103">CAPTUREFILTER structure</span></span>

<span data-ttu-id="d15b3-104">A estrutura **CAPTUREFILTER** contém dados de filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="d15b3-104">The **CAPTUREFILTER** structure contains capture filter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d15b3-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a><span data-ttu-id="d15b3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d15b3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d15b3-107">**FilterFlags**</span><span class="sxs-lookup"><span data-stu-id="d15b3-107">**FilterFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-108">Sinalizadores que descrevem o conteúdo do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="d15b3-108">Flags that describe the contents of the capture filter.</span></span>



| <span data-ttu-id="d15b3-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d15b3-109">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="d15b3-110">Significado</span><span class="sxs-lookup"><span data-stu-id="d15b3-110">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <span data-ttu-id="d15b3-111"><dt>**CAPTUREFILTER \_ \_Os sinalizadores incluem \_ todos os \_ SAPs**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d15b3-111"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS**</dt> <dt>0x0001</dt></span></span> </dl>       | <span data-ttu-id="d15b3-112">Inclui todos os SAPs como quadros aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="d15b3-112">Includes all SAPs as acceptable frames.</span></span><br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <span data-ttu-id="d15b3-113"><dt>**CAPTUREFILTER \_ \_Os sinalizadores incluem \_ todos os \_ ETYPES**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="d15b3-113"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="d15b3-114">Incluir todos os ETYPEs como quadros aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="d15b3-114">Include all Etypes as acceptable frames.</span></span><br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <span data-ttu-id="d15b3-115"><dt>**CAPTUREFILTER \_ 0x0008 \_ \_ somente locais de sinalizadores**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d15b3-115"><dt>**CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY**</dt> <dt>0x0008</dt></span></span> </dl>                          | <span data-ttu-id="d15b3-116">Sem modo P</span><span class="sxs-lookup"><span data-stu-id="d15b3-116">No P-mode</span></span><br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <span data-ttu-id="d15b3-117"><dt>**CAPTUREFILTER \_ Os \_ sinalizadores \_ mantêm**</dt> o <dt>0x0020</dt> bruto</span><span class="sxs-lookup"><span data-stu-id="d15b3-117"><dt>**CAPTUREFILTER\_FLAGS\_KEEP\_RAW**</dt> <dt>0x0020</dt></span></span> </dl>                                | <span data-ttu-id="d15b3-118">Mantenha os quadros MAC SMT e token ring.</span><span class="sxs-lookup"><span data-stu-id="d15b3-118">Keep SMT and token ring MAC frames.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="d15b3-119">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="d15b3-119">**lpSapTable**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-120">Ponteiro para uma matriz de valores SAP.</span><span class="sxs-lookup"><span data-stu-id="d15b3-120">Pointer to an array of SAP values.</span></span> <span data-ttu-id="d15b3-121">Esse membro indica os valores SAP que são válidos para passar para o driver.</span><span class="sxs-lookup"><span data-stu-id="d15b3-121">This member indicates the SAP values that are valid to pass to the driver.</span></span> <span data-ttu-id="d15b3-122">Se CAPTUREFILTER \_ flags \_ incluir \_ todos os \_ SAPs for definido, isso se tornará uma lista de exceção (inclua todos os SAPs, exceto esses).</span><span class="sxs-lookup"><span data-stu-id="d15b3-122">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (include all SAPS except these).</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-123">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="d15b3-123">**lpEtypeTable**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-124">Ponteiro para uma matriz de valores de ETYPE.</span><span class="sxs-lookup"><span data-stu-id="d15b3-124">Pointer to an array of Etype values.</span></span> <span data-ttu-id="d15b3-125">Isso indica os valores de ETYPE que são válidos para passar para o driver.</span><span class="sxs-lookup"><span data-stu-id="d15b3-125">This indicates those Etype values that are valid to pass to the driver.</span></span> <span data-ttu-id="d15b3-126">Se \_ os sinalizadores CAPTUREFILTERs \_ incluírem \_ todos os \_ ETYPEs forem definidos, isso se tornará uma lista de exceção (inclua todos os ETYPEs, exceto estes).</span><span class="sxs-lookup"><span data-stu-id="d15b3-126">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (include all Etypes except these).</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-127">**nSaps**</span><span class="sxs-lookup"><span data-stu-id="d15b3-127">**nSaps**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-128">Número de SAPs na tabela SAP.</span><span class="sxs-lookup"><span data-stu-id="d15b3-128">Number of SAPs in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-129">**nEtypes**</span><span class="sxs-lookup"><span data-stu-id="d15b3-129">**nEtypes**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-130">Número de ETYPEs na tabela ETYPE.</span><span class="sxs-lookup"><span data-stu-id="d15b3-130">Number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-131">**Endereço de endereçamento**</span><span class="sxs-lookup"><span data-stu-id="d15b3-131">**AddressTable**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-132">Nome da tabela de endereços.</span><span class="sxs-lookup"><span data-stu-id="d15b3-132">Name of the address table.</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-133">**FilterExpression**</span><span class="sxs-lookup"><span data-stu-id="d15b3-133">**FilterExpression**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-134">Uma estrutura de expressão.</span><span class="sxs-lookup"><span data-stu-id="d15b3-134">An EXPRESSION structure.</span></span> <span data-ttu-id="d15b3-135">Contém a parte de correspondência de padrões do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="d15b3-135">This contains the pattern match portion of the capture filter.</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-136">**Gatilho**</span><span class="sxs-lookup"><span data-stu-id="d15b3-136">**Trigger**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-137">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d15b3-137">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-138">**nFrameBytesToCopy**</span><span class="sxs-lookup"><span data-stu-id="d15b3-138">**nFrameBytesToCopy**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-139">Se esse membro não for 0, ele especificará quantos bytes serão mantidos de cada quadro recebido.</span><span class="sxs-lookup"><span data-stu-id="d15b3-139">If this member is not 0, then it specifies how many bytes to keep of each frame received.</span></span> <span data-ttu-id="d15b3-140">Se for 0, mantenha todo o quadro.</span><span class="sxs-lookup"><span data-stu-id="d15b3-140">If it is 0, then keep the whole frame.</span></span>

</dd> <dt>

<span data-ttu-id="d15b3-141">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="d15b3-141">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d15b3-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d15b3-142">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d15b3-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="d15b3-143">Remarks</span></span>

<span data-ttu-id="d15b3-144">A combinação de sinalizadores, valores e expressões determina quais quadros serão passados pelo driver que usa esses dados de estrutura.</span><span class="sxs-lookup"><span data-stu-id="d15b3-144">The combination of flags, values, and expressions determine which frames will be passed by the driver that uses this structure data.</span></span> <span data-ttu-id="d15b3-145">Para obter mais informações sobre como implementar uma estrutura **CAPTUREFILTER** , consulte [filtros de captura](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d15b3-145">For more information about implementing a **CAPTUREFILTER** structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d15b3-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d15b3-146">Requirements</span></span>



| <span data-ttu-id="d15b3-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="d15b3-147">Requirement</span></span> | <span data-ttu-id="d15b3-148">Valor</span><span class="sxs-lookup"><span data-stu-id="d15b3-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d15b3-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d15b3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d15b3-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d15b3-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d15b3-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d15b3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d15b3-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d15b3-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d15b3-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d15b3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="d15b3-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d15b3-154"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d15b3-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="d15b3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15b3-156">Endereço de endereçamento</span><span class="sxs-lookup"><span data-stu-id="d15b3-156">ADDRESSTABLE</span></span>](addresstable.md)
</dt> <dt>

[<span data-ttu-id="d15b3-157">ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="d15b3-157">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="d15b3-158">EXPRESSÃO</span><span class="sxs-lookup"><span data-stu-id="d15b3-158">EXPRESSION</span></span>](expression.md)
</dt> <dt>

[<span data-ttu-id="d15b3-159">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="d15b3-159">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="d15b3-160">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="d15b3-160">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




