---
description: Sinalizadores que restringem os dados a serem definidos ou retornados.
title: SRRF (shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011176"
---
# <a name="srrf"></a><span data-ttu-id="3ee65-103">SRRF</span><span class="sxs-lookup"><span data-stu-id="3ee65-103">SRRF</span></span>

<span data-ttu-id="3ee65-104">Sinalizadores que restringem os dados a serem definidos ou retornados.</span><span class="sxs-lookup"><span data-stu-id="3ee65-104">Flags that restrict the data to be set or returned.</span></span>



| <span data-ttu-id="3ee65-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="3ee65-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="3ee65-106">Description</span><span class="sxs-lookup"><span data-stu-id="3ee65-106">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <span data-ttu-id="3ee65-107"><dt>**SRRF \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-107"><dt>**SRRF\_RT\_REG\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="3ee65-108">Digite REG \_ None.</span><span class="sxs-lookup"><span data-stu-id="3ee65-108">Type REG\_NONE.</span></span><br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <span data-ttu-id="3ee65-109"><dt>**SRRF \_ RT \_ reg \_ sz**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-109"><dt>**SRRF\_RT\_REG\_SZ**</dt> <dt>0x00000002</dt></span></span> </dl>                       | <span data-ttu-id="3ee65-110">Digite REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="3ee65-110">Type REG\_SZ.</span></span> <span data-ttu-id="3ee65-111">\_Os tipos reg expande \_ sz são convertidos automaticamente em reg \_ sz, a menos que o \_ sinalizador NOEXPAND SRRF seja especificado.</span><span class="sxs-lookup"><span data-stu-id="3ee65-111">REG\_EXPAND\_SZ types are automatically converted to REG\_SZ unless the SRRF\_NOEXPAND flag is specified.</span></span><br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <span data-ttu-id="3ee65-112"><dt>**SRRF \_ \* \_ Reg \_ expandir \_ sz**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-112"><dt>**SRRF\_RT\_REG\_EXPAND\_SZ**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="3ee65-113">Digite REG \_ expande \_ sz.</span><span class="sxs-lookup"><span data-stu-id="3ee65-113">Type REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="3ee65-114">Se estiver recuperando um valor, você também deverá obter o \_ sinalizador NOEXPAND SRRF ou [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) falhará com um parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="3ee65-114">If retrieving a value, you must also get the SRRF\_NOEXPAND flag, or [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) fails with ERROR\_INVALID\_PARAMETER.</span></span><br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <span data-ttu-id="3ee65-115"><dt>**SRRF \_ 0x00000008 \_ de \_ binário do Reg de RT**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-115"><dt>**SRRF\_RT\_REG\_BINARY**</dt> <dt>0x00000008</dt></span></span> </dl>           | <span data-ttu-id="3ee65-116">Digite REG \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="3ee65-116">Type REG\_BINARY.</span></span><br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <span data-ttu-id="3ee65-117"><dt>**SRRF \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-117"><dt>**SRRF\_RT\_REG\_DWORD**</dt> <dt>0x00000010</dt></span></span> </dl>              | <span data-ttu-id="3ee65-118">Digite REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="3ee65-118">Type REG\_DWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <span data-ttu-id="3ee65-119"><dt>**SRRF \_ RT \_ reg \_ multi \_ sz**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-119"><dt>**SRRF\_RT\_REG\_MULTI\_SZ**</dt> <dt>0x00000020</dt></span></span> </dl>    | <span data-ttu-id="3ee65-120">Digite REG \_ multi \_ sz.</span><span class="sxs-lookup"><span data-stu-id="3ee65-120">Type REG\_MULTI\_SZ.</span></span><br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <span data-ttu-id="3ee65-121"><dt>**SRRF \_ RT \_ reg \_ QWORD**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-121"><dt>**SRRF\_RT\_REG\_QWORD**</dt> <dt>0x00000040</dt></span></span> </dl>              | <span data-ttu-id="3ee65-122">Digite REG \_ Qword.</span><span class="sxs-lookup"><span data-stu-id="3ee65-122">Type REG\_QWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <span data-ttu-id="3ee65-123"><dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-123"><dt>**SRRF\_RT\_DWORD**</dt> <dt>0x00000018</dt></span></span> </dl>                           | <span data-ttu-id="3ee65-124">\_Tipos binários reg DWORD e 32 bits \_ .</span><span class="sxs-lookup"><span data-stu-id="3ee65-124">REG\_DWORD and 32-bit REG\_BINARY types.</span></span> <span data-ttu-id="3ee65-125">Isso é equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="3ee65-125">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_DWORD.</span></span> <span data-ttu-id="3ee65-126">Se você recuperar um valor, se os dados binários do valor forem maiores que 32 bits, ele não será retornado.</span><span class="sxs-lookup"><span data-stu-id="3ee65-126">If retrieving a value, if the value's binary data is larger than 32 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <span data-ttu-id="3ee65-127"><dt>**SRRF \_ RT \_ QWORD**</dt> <dt>0x00000048</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-127"><dt>**SRRF\_RT\_QWORD**</dt> <dt>0x00000048</dt></span></span> </dl>                           | <span data-ttu-id="3ee65-128">\_Tipos binários reg QWORD e 64-bit \_ .</span><span class="sxs-lookup"><span data-stu-id="3ee65-128">REG\_QWORD and 64-bit REG\_BINARY types.</span></span> <span data-ttu-id="3ee65-129">Isso é equivalente a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ Qword.</span><span class="sxs-lookup"><span data-stu-id="3ee65-129">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_QWORD.</span></span> <span data-ttu-id="3ee65-130">Se você recuperar um valor, se os dados binários do valor forem maiores que 64 bits, ele não será retornado.</span><span class="sxs-lookup"><span data-stu-id="3ee65-130">If retrieving a value, if the value's binary data is larger than 64 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <span data-ttu-id="3ee65-131"><dt>**SRRF \_ RT \_ qualquer**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-131"><dt>**SRRF\_RT\_ANY**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                                 | <span data-ttu-id="3ee65-132">Todos os tipos.</span><span class="sxs-lookup"><span data-stu-id="3ee65-132">All types.</span></span> <span data-ttu-id="3ee65-133">Defina esse sinalizador se nenhum outro valor de RT de SRRF \_ for definido.</span><span class="sxs-lookup"><span data-stu-id="3ee65-133">Set this flag if no other SRRF\_RT value is set.</span></span><br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <span data-ttu-id="3ee65-134"><dt>**SRRF \_ RM \_ qualquer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-134"><dt>**SRRF\_RM\_ANY**</dt> <dt>0x00000000</dt></span></span> </dl>                                 | <span data-ttu-id="3ee65-135">Nenhuma restrição de modo.</span><span class="sxs-lookup"><span data-stu-id="3ee65-135">No mode restriction.</span></span> <span data-ttu-id="3ee65-136">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="3ee65-136">This is the default value.</span></span><br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <span data-ttu-id="3ee65-137"><dt>**SRRF \_ 0x00010000 \_ normal do RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-137"><dt>**SRRF\_RM\_NORMAL**</dt> <dt>0x00010000</dt></span></span> </dl>                        | <span data-ttu-id="3ee65-138">Restrinja o modo de inicialização do sistema para "inicialização normal".</span><span class="sxs-lookup"><span data-stu-id="3ee65-138">Restrict system startup mode to "normal boot".</span></span><br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <span data-ttu-id="3ee65-139"><dt>**SRRF \_ 0x00020000 \_ seguro do RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-139"><dt>**SRRF\_RM\_SAFE**</dt> <dt>0x00020000</dt></span></span> </dl>                              | <span data-ttu-id="3ee65-140">Restrinja o modo de inicialização do sistema para "modo de segurança".</span><span class="sxs-lookup"><span data-stu-id="3ee65-140">Restrict system startup mode to "safe mode".</span></span><br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <span data-ttu-id="3ee65-141"><dt>**SRRF \_ 0x00040000 RM \_ SAFENETWORK**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-141"><dt>**SRRF\_RM\_SAFENETWORK**</dt> <dt>0x00040000</dt></span></span> </dl>         | <span data-ttu-id="3ee65-142">Restrinja o modo de inicialização do sistema para "modo de segurança com rede".</span><span class="sxs-lookup"><span data-stu-id="3ee65-142">Restrict system startup mode to "safe mode with networking".</span></span><br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <span data-ttu-id="3ee65-143"><dt>**SRRF \_ 0x10000000 NOEXPAND**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-143"><dt>**SRRF\_NOEXPAND**</dt> <dt>0x10000000</dt></span></span> </dl>                            | <span data-ttu-id="3ee65-144">Não expanda automaticamente as \_ \_ cadeias de caracteres do ambiente reg Expand sz.</span><span class="sxs-lookup"><span data-stu-id="3ee65-144">Do not automatically expand REG\_EXPAND\_SZ environment strings.</span></span><br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <span data-ttu-id="3ee65-145"><dt>**SRRF \_ ZEROONFAILURE**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-145"><dt>**SRRF\_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="3ee65-146">Se for recuperar um valor, se *pvData* não for **nulo**, defina o conteúdo do buffer *pvData* como todos os zeros em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="3ee65-146">If retrieving a value, if *pvData* is not **NULL**, set the contents of the *pvData* buffer to all zeros on failure.</span></span><br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <span data-ttu-id="3ee65-147"><dt>**SRRF \_ NOVIRT**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-147"><dt>**SRRF\_NOVIRT**</dt> <dt>0x40000000</dt></span></span> </dl>                                  | <span data-ttu-id="3ee65-148">Ao recuperar um valor, se a chave solicitada for virtualizada, falha com o \_ arquivo de erro \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="3ee65-148">When retrieving a value, if the requested key is virtualized, fail with ERROR\_FILE\_NOT\_FOUND.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="3ee65-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ee65-149">Remarks</span></span>

<span data-ttu-id="3ee65-150">Esses valores são definidos em Shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="3ee65-150">These values are defined in Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ee65-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ee65-151">Requirements</span></span>



| <span data-ttu-id="3ee65-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ee65-152">Requirement</span></span> | <span data-ttu-id="3ee65-153">Valor</span><span class="sxs-lookup"><span data-stu-id="3ee65-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee65-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ee65-154">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee65-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ee65-155">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3ee65-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ee65-156">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee65-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ee65-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3ee65-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ee65-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ee65-159"><dt>Shlwapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ee65-159"><dt>Shlwapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ee65-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ee65-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee65-161">**SHRegSetValue**</span><span class="sxs-lookup"><span data-stu-id="3ee65-161">**SHRegSetValue**</span></span>](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[<span data-ttu-id="3ee65-162">**SHRegGetValue**</span><span class="sxs-lookup"><span data-stu-id="3ee65-162">**SHRegGetValue**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




