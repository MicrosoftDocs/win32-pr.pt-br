---
title: Estrutura de MPSTATUS_DATA (MpClient. h)
description: Contém dados sobre o status atual de um componente do produto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSTATUS_DATA
- Ponteiro de estrutura de PMPSTATUS_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644850"
---
# <a name="mpstatus_data-structure"></a><span data-ttu-id="82b5b-105">\_Estrutura de dados MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="82b5b-105">MPSTATUS\_DATA structure</span></span>

<span data-ttu-id="82b5b-106">Contém dados sobre o status atual de um componente do produto.</span><span class="sxs-lookup"><span data-stu-id="82b5b-106">Contains data about the current status of a component of the product.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b5b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82b5b-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a><span data-ttu-id="82b5b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="82b5b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="82b5b-109">**ComponentID**</span><span class="sxs-lookup"><span data-stu-id="82b5b-109">**ComponentID**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-110">Tipo: **[ **\_ ID de MPCOMPONENT**](mpcomponent-id.md)**</span><span class="sxs-lookup"><span data-stu-id="82b5b-110">Type: **[**MPCOMPONENT\_ID**](mpcomponent-id.md)**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-111">ID do componente específico para o qual o status é relatado.</span><span class="sxs-lookup"><span data-stu-id="82b5b-111">Specific component ID for which status is reported.</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-112">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="82b5b-112">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="82b5b-113">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-114">Status solicitado para o componente.</span><span class="sxs-lookup"><span data-stu-id="82b5b-114">Status requested for the component.</span></span> <span data-ttu-id="82b5b-115">**HRESULT** nos dados de retorno de chamada significa êxito ou falha para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="82b5b-115">**hResult** in the callback data signifies success or failure for the request.</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-116">**ComponentStatus**</span><span class="sxs-lookup"><span data-stu-id="82b5b-116">**ComponentStatus**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-117">Dados de status adicionais, dependendo do valor de **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-117">Extra status data depending on value of **ComponentID**.</span></span>

> [!Note]  
> <span data-ttu-id="82b5b-118">Atualmente resulta em um ponteiro para uma estrutura fictícia para todos os valores possíveis de **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-118">Currently results in a pointer to a dummy structure for all possible values of **ComponentID**.</span></span>

 

<dl> <dt>

<span data-ttu-id="82b5b-119">**P1**</span><span class="sxs-lookup"><span data-stu-id="82b5b-119">**p1**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-120">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-120">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-121">Quando **ComponentID**  ==  **MPCOMPONENT \_ como \_ assinatura**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-121">When **ComponentID** == **MPCOMPONENT\_AS\_SIGNATURE**.</span></span> <span data-ttu-id="82b5b-122">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-122">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-123">**P2**</span><span class="sxs-lookup"><span data-stu-id="82b5b-123">**p2**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-124">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-124">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-125">Quando **ComponentID**  ==  **MPCOMPONENT \_ a \_ assinatura do AV**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-125">When **ComponentID** == **MPCOMPONENT\_AV\_SIGNATURE**.</span></span> <span data-ttu-id="82b5b-126">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-126">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-127">**P3**</span><span class="sxs-lookup"><span data-stu-id="82b5b-127">**p3**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-128">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-128">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-129">Quando **ComponentID**  ==  **MPCOMPONENT \_ o \_ Monitor em tempo real**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-129">When **ComponentID** == **MPCOMPONENT\_REALTIME\_MONITOR**.</span></span> <span data-ttu-id="82b5b-130">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-130">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-131">**P4**</span><span class="sxs-lookup"><span data-stu-id="82b5b-131">**p4**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-132">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-132">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-133">Quando **ComponentID**  ==  **MPCOMPONENT a \_ \_ proteção do OnAccess**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-133">When **ComponentID** == **MPCOMPONENT\_ONACCESS\_PROTECTION**.</span></span> <span data-ttu-id="82b5b-134">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-134">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-135">**P5**</span><span class="sxs-lookup"><span data-stu-id="82b5b-135">**p5**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-136">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-136">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-137">Quando **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ Protection**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-137">When **ComponentID** == **MPCOMPONENT\_IOAV\_PROTECTION**.</span></span> <span data-ttu-id="82b5b-138">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-138">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-139">**P6**</span><span class="sxs-lookup"><span data-stu-id="82b5b-139">**p6**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-140">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-140">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-141">Quando **ComponentID**  ==  **MPCOMPONENT \_ comportamento \_ Monitor**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-141">When **ComponentID** == **MPCOMPONENT\_BEHAVIOR\_MONITOR**.</span></span> <span data-ttu-id="82b5b-142">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-142">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-143">**P7**</span><span class="sxs-lookup"><span data-stu-id="82b5b-143">**p7**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-144">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-144">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-145">Quando **ComponentID**  ==  **MPCOMPONENT \_ \_ verificação automática**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-145">When **ComponentID** == **MPCOMPONENT\_AUTO\_SCAN**.</span></span> <span data-ttu-id="82b5b-146">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-146">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-147">**P8**</span><span class="sxs-lookup"><span data-stu-id="82b5b-147">**p8**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-148">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-148">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-149">Quando **ComponentID**  ==  **MPCOMPONENT \_ \_ SIGUPDATE automático**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-149">When **ComponentID** == **MPCOMPONENT\_AUTO\_SIGUPDATE**.</span></span> <span data-ttu-id="82b5b-150">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-150">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-151">**P9**</span><span class="sxs-lookup"><span data-stu-id="82b5b-151">**p9**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-152">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-152">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-153">Quando **ComponentID**  ==  **MPCOMPONENT \_ IPC**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-153">When **ComponentID** == **MPCOMPONENT\_IPC**.</span></span> <span data-ttu-id="82b5b-154">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-154">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-155">**pa**</span><span class="sxs-lookup"><span data-stu-id="82b5b-155">**pa**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-156">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-156">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-157">Quando **ComponentID**  ==  **MPCOMPONENT \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-157">When **ComponentID** == **MPCOMPONENT\_NIS**.</span></span> <span data-ttu-id="82b5b-158">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-158">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b5b-159">**PB**</span><span class="sxs-lookup"><span data-stu-id="82b5b-159">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="82b5b-160">Tipo: **PMPSTATUS \_ DATAEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-160">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="82b5b-161">Quando **ComponentID**  ==  **MPCOMPONENT \_ Elam**.</span><span class="sxs-lookup"><span data-stu-id="82b5b-161">When **ComponentID** == **MPCOMPONENT\_ELAM**.</span></span> <span data-ttu-id="82b5b-162">Consulte [**MPSTATUS \_ DATAEX \_ não used**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="82b5b-162">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82b5b-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82b5b-163">Requirements</span></span>



| <span data-ttu-id="82b5b-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="82b5b-164">Requirement</span></span> | <span data-ttu-id="82b5b-165">Valor</span><span class="sxs-lookup"><span data-stu-id="82b5b-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82b5b-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82b5b-166">Minimum supported client</span></span><br/> | <span data-ttu-id="82b5b-167">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="82b5b-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="82b5b-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82b5b-168">Minimum supported server</span></span><br/> | <span data-ttu-id="82b5b-169">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="82b5b-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82b5b-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82b5b-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b5b-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="82b5b-171"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b5b-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="82b5b-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b5b-173">**ID do MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="82b5b-173">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="82b5b-174">**MPSTATUS \_ DATAEX \_ não usado**</span><span class="sxs-lookup"><span data-stu-id="82b5b-174">**MPSTATUS\_DATAEX\_UNUSED**</span></span>](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





