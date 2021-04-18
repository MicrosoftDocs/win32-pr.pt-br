---
description: A estrutura de acompanhamento de PF \_ define os protocolos que podem preceder ou seguir um protocolo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Estrutura de PF_FOLLOWSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757235"
---
# <a name="pf_followset-structure"></a><span data-ttu-id="ee4f0-103">Estrutura de acompanhamento de PF \_</span><span class="sxs-lookup"><span data-stu-id="ee4f0-103">PF\_FOLLOWSET structure</span></span>

<span data-ttu-id="ee4f0-104">A estrutura de **\_ acompanhamento de PF** define os protocolos que podem preceder ou seguir um protocolo.</span><span class="sxs-lookup"><span data-stu-id="ee4f0-104">The **PF\_FOLLOWSET** structure defines the protocols that may precede or follow a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee4f0-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a><span data-ttu-id="ee4f0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ee4f0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee4f0-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="ee4f0-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="ee4f0-108">Número de protocolos na lista.</span><span class="sxs-lookup"><span data-stu-id="ee4f0-108">Number of protocols in the list.</span></span>

</dd> <dt>

<span data-ttu-id="ee4f0-109">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="ee4f0-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="ee4f0-110">Matriz de [estruturas \_ FOLLOWENTRY de PF](pf-followentry.md) que descrevem cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="ee4f0-110">Array of [PF\_FOLLOWENTRY](pf-followentry.md) structures that describe each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee4f0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee4f0-111">Remarks</span></span>

<span data-ttu-id="ee4f0-112">A estrutura de [ \_ PARSERINFO de PF](pf-parserinfo.md) usa a estrutura de **\_ acompanhamento de PF** para listar os protocolos que podem preceder ou seguir o protocolo que o analisador detecta.</span><span class="sxs-lookup"><span data-stu-id="ee4f0-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_FOLLOWSET** structure to list the protocols that may precede or follow the protocol that the parser detects.</span></span>

<span data-ttu-id="ee4f0-113">Monitor de Rede usa as informações na estrutura do conjunto de **PP-PF \_** para atualizar os seguintes conjuntos de analisadores específicos.</span><span class="sxs-lookup"><span data-stu-id="ee4f0-113">Network Monitor uses the information in the **PF\_FOLLOWSET** structure to update the follow sets of specific parsers.</span></span> <span data-ttu-id="ee4f0-114">A estrutura de **\_ acompanhamento de PF** deve ser alocada usando **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="ee4f0-114">The **PF\_FOLLOWSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee4f0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4f0-115">Requirements</span></span>



| <span data-ttu-id="ee4f0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4f0-116">Requirement</span></span> | <span data-ttu-id="ee4f0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ee4f0-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4f0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee4f0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4f0-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee4f0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ee4f0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee4f0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4f0-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee4f0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ee4f0-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee4f0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4f0-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4f0-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee4f0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee4f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4f0-125">FOLLOWENTRY de PF \_</span><span class="sxs-lookup"><span data-stu-id="ee4f0-125">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)
</dt> <dt>

[<span data-ttu-id="ee4f0-126">PARSERINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="ee4f0-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> </dl>

 

 




