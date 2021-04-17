---
description: A estrutura de entrega do PF \_ define os protocolos que são entregues ao analisador ou os protocolos que o analisador transfere para o.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Estrutura de PF_HANDOFFSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749237"
---
# <a name="pf_handoffset-structure"></a><span data-ttu-id="f7643-103">Estrutura de entrega do PF \_</span><span class="sxs-lookup"><span data-stu-id="f7643-103">PF\_HANDOFFSET structure</span></span>

<span data-ttu-id="f7643-104">A estrutura de **\_ entrega do PF** define os protocolos que são entregues ao analisador ou os protocolos que o analisador transfere para o.</span><span class="sxs-lookup"><span data-stu-id="f7643-104">The **PF\_HANDOFFSET** structure defines the protocols that hand off to the parser, or the protocols that the parser hands off to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7643-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7643-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a><span data-ttu-id="f7643-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f7643-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f7643-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="f7643-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="f7643-108">Número de protocolos.</span><span class="sxs-lookup"><span data-stu-id="f7643-108">Number of protocols.</span></span>

</dd> <dt>

<span data-ttu-id="f7643-109">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="f7643-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="f7643-110">Uma matriz de [estruturas \_ HANDOFFENTRY de PF](pf-handoffentry.md) que definem cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="f7643-110">An array of [PF\_HANDOFFENTRY](pf-handoffentry.md) structures that define each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7643-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7643-111">Remarks</span></span>

<span data-ttu-id="f7643-112">A estrutura de [ \_ PARSERINFO de PF](pf-parserinfo.md) usa a estrutura de **\_ entrega do PF** para listar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7643-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_HANDOFFSET** structure to list the following:</span></span>

-   <span data-ttu-id="f7643-113">Quais protocolos estão disponíveis para o analisador.</span><span class="sxs-lookup"><span data-stu-id="f7643-113">Which protocols hand off to the parser.</span></span>
-   <span data-ttu-id="f7643-114">Para quais protocolos o analisador passa.</span><span class="sxs-lookup"><span data-stu-id="f7643-114">Which protocols the parser hands off to.</span></span>

<span data-ttu-id="f7643-115">A estrutura de **\_ entrega do PF** deve ser alocada usando **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="f7643-115">The **PF\_HANDOFFSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7643-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7643-116">Requirements</span></span>



| <span data-ttu-id="f7643-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7643-117">Requirement</span></span> | <span data-ttu-id="f7643-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f7643-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f7643-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7643-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f7643-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7643-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f7643-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7643-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f7643-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7643-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f7643-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f7643-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7643-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7643-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7643-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7643-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7643-126">PARSERINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="f7643-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="f7643-127">HANDOFFENTRY de PF \_</span><span class="sxs-lookup"><span data-stu-id="f7643-127">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)
</dt> </dl>

 

 




