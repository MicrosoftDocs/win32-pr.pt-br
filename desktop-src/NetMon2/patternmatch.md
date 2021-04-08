---
description: A estrutura PATTERNMATCH define os elementos de padrão usados para avaliar um quadro.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Estrutura PATTERNMATCH (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922003"
---
# <a name="patternmatch-structure"></a><span data-ttu-id="9bd7b-103">Estrutura PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="9bd7b-103">PATTERNMATCH structure</span></span>

<span data-ttu-id="9bd7b-104">A estrutura **PATTERNMATCH** define os elementos de padrão usados para avaliar um quadro.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-104">The **PATTERNMATCH** structure defines pattern elements used to evaluate a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bd7b-105">Syntax</span></span>


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a><span data-ttu-id="9bd7b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9bd7b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9bd7b-107">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="9bd7b-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9bd7b-108">Sinalizadores de correspondência de padrões:</span><span class="sxs-lookup"><span data-stu-id="9bd7b-108">Pattern match flags:</span></span>



| <span data-ttu-id="9bd7b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="9bd7b-109">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="9bd7b-110">Significado</span><span class="sxs-lookup"><span data-stu-id="9bd7b-110">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <span data-ttu-id="9bd7b-111"><dt>**Padrão \_ Sinalizadores de correspondência \_ \_ não**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7b-111"><dt>**PATTERN\_MATCH\_FLAGS\_NOT**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="9bd7b-112">Quando definido, esse sinalizador retém os quadros que não têm o padrão especificado no ponto adequado.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-112">When set, this flag retains frames that lack the specified pattern in the proper spot.</span></span><br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <span data-ttu-id="9bd7b-113"><dt>**Padrão \_ Porta de sinalizadores de correspondência \_ \_ \_ especificada**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7b-113"><dt>**PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="9bd7b-114">Busca um valor de número de porta.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-114">Seeks a port number value.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="9bd7b-115">**OffsetBasis**</span><span class="sxs-lookup"><span data-stu-id="9bd7b-115">**OffsetBasis**</span></span>
</dt> <dd>

<span data-ttu-id="9bd7b-116">Tipos de deslocamento, que podem ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="9bd7b-116">Types of offset, which can be one of the following:</span></span>



| <span data-ttu-id="9bd7b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9bd7b-117">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="9bd7b-118">Significado</span><span class="sxs-lookup"><span data-stu-id="9bd7b-118">Meaning</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <span data-ttu-id="9bd7b-119"><dt>**DESLOCAMENTO \_ \_ de base relativo \_ ao \_ quadro**</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7b-119"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_FRAME**</dt></span></span> </dl>                                         | <span data-ttu-id="9bd7b-120">Define um deslocamento, em bytes, em relação ao início do quadro.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-120">Sets an offset, in bytes, relative to start of the frame.</span></span><br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <span data-ttu-id="9bd7b-121"><dt>**DESLOCAMENTO \_ \_ de base \_ relativo \_ ao \_ protocolo efetivo**</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7b-121"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="9bd7b-122">Define um deslocamento, em bytes, em relação ao início do protocolo referenciado.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-122">Sets an offset, in bytes, relative to the start of the referenced protocol.</span></span><br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <span data-ttu-id="9bd7b-123"><dt>**DESLOCAMENTO \_ \_ de base relativo \_ ao \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7b-123"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IPX**</dt></span></span> </dl>                                               | <span data-ttu-id="9bd7b-124">Define um deslocamento, em bytes, somente relativo ao IPX.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-124">Sets an offset, in bytes, only relative to IPX.</span></span><br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <span data-ttu-id="9bd7b-125"><dt>**DESLOCAMENTO \_ \_ de base relativo \_ ao \_ IP**</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7b-125"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IP**</dt></span></span> </dl>                                                  | <span data-ttu-id="9bd7b-126">Define um deslocamento, em bytes, somente relativo ao IP.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-126">Sets an offset, in bytes, only relative to IP.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="9bd7b-127">**Porta**</span><span class="sxs-lookup"><span data-stu-id="9bd7b-127">**Port**</span></span>
</dt> <dd>

<span data-ttu-id="9bd7b-128">Valor da porta, se especificado.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-128">Port value, if specified.</span></span>

</dd> <dt>

<span data-ttu-id="9bd7b-129">**Deslocamento**</span><span class="sxs-lookup"><span data-stu-id="9bd7b-129">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="9bd7b-130">O deslocamento, em bytes, relativo ao **OffsetBasis**.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-130">The offset, in bytes, relative to the **OffsetBasis**.</span></span>

</dd> <dt>

<span data-ttu-id="9bd7b-131">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="9bd7b-131">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="9bd7b-132">Comprimento do padrão correspondente.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-132">Length of the matched pattern.</span></span>

</dd> <dt>

<span data-ttu-id="9bd7b-133">**PatternToMatch**</span><span class="sxs-lookup"><span data-stu-id="9bd7b-133">**PatternToMatch**</span></span>
</dt> <dd>

<span data-ttu-id="9bd7b-134">Padrão a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-134">Pattern to match.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bd7b-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bd7b-135">Remarks</span></span>

<span data-ttu-id="9bd7b-136">Essa estrutura é usada para construir um filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="9bd7b-136">This structure is used to construct a capture filter.</span></span> <span data-ttu-id="9bd7b-137">Para obter mais informações sobre como implementar essa estrutura, consulte [filtros de captura](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="9bd7b-137">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

<span data-ttu-id="9bd7b-138">Um filtro de captura pode conter até quatro estruturas **PATTERNMATCH** .</span><span class="sxs-lookup"><span data-stu-id="9bd7b-138">A capture filter can contain up to four **PATTERNMATCH** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd7b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bd7b-139">Requirements</span></span>



| <span data-ttu-id="9bd7b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd7b-140">Requirement</span></span> | <span data-ttu-id="9bd7b-141">Valor</span><span class="sxs-lookup"><span data-stu-id="9bd7b-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd7b-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bd7b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9bd7b-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9bd7b-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9bd7b-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bd7b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9bd7b-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9bd7b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9bd7b-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9bd7b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bd7b-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bd7b-147"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bd7b-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bd7b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd7b-149">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="9bd7b-149">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




