---
description: Grava um evento completo em uma sessão.
title: EtwEventWriteFull
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 5ea3de0dba842544b0ffacc785fb138bdda571a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920472"
---
# <a name="etweventwritefull-function"></a><span data-ttu-id="501d8-103">Função EtwEventWriteFull</span><span class="sxs-lookup"><span data-stu-id="501d8-103">EtwEventWriteFull function</span></span>

<span data-ttu-id="501d8-104">[A função EtwEventWriteFull e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra.]</span><span class="sxs-lookup"><span data-stu-id="501d8-104">[The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="501d8-105">Grava um evento completo em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="501d8-105">Writes a full event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="501d8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="501d8-106">Syntax</span></span>

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="501d8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="501d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="501d8-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="501d8-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="501d8-109">RegHandle para o provedor.</span><span class="sxs-lookup"><span data-stu-id="501d8-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="501d8-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="501d8-110">*EventDescriptor*</span></span> 
</dt> <dd>

<span data-ttu-id="501d8-111">Descritor de evento do evento a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="501d8-111">Event Descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="501d8-112">*EventProperty*</span><span class="sxs-lookup"><span data-stu-id="501d8-112">*EventProperty*</span></span>
</dt> <dd>

<span data-ttu-id="501d8-113">Sinalizador fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="501d8-113">Flag given by the user.</span></span>

</dd> <dt>

<span data-ttu-id="501d8-114">*ActivityId*</span><span class="sxs-lookup"><span data-stu-id="501d8-114">*ActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="501d8-115">ID da atividade.</span><span class="sxs-lookup"><span data-stu-id="501d8-115">Activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="501d8-116">*RelatedActivityId*</span><span class="sxs-lookup"><span data-stu-id="501d8-116">*RelatedActivityId*</span></span>
</dt> <dd>

<span data-ttu-id="501d8-117">ID da atividade relacionada.</span><span class="sxs-lookup"><span data-stu-id="501d8-117">Related activity Id.</span></span>

</dd> <dt>

<span data-ttu-id="501d8-118">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="501d8-118">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="501d8-119">O número de itens de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="501d8-119">The number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="501d8-120">*UserData*</span><span class="sxs-lookup"><span data-stu-id="501d8-120">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="501d8-121">Ponteiro para uma matriz de itens de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="501d8-121">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="501d8-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="501d8-122">Return value</span></span>

<span data-ttu-id="501d8-123">Um código de erro Win32.</span><span class="sxs-lookup"><span data-stu-id="501d8-123">A Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="501d8-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="501d8-124">Remarks</span></span>

<span data-ttu-id="501d8-125">A função EtwEventWriteFull e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra.</span><span class="sxs-lookup"><span data-stu-id="501d8-125">The EtwEventWriteFull function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="501d8-126">Para manter a compatibilidade do seu aplicativo, é melhor usar funções públicas em vez disso.</span><span class="sxs-lookup"><span data-stu-id="501d8-126">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>


## <a name="requirements"></a><span data-ttu-id="501d8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="501d8-127">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="501d8-128">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="501d8-128">**Target Platform**</span></span> | <span data-ttu-id="501d8-129">Windows</span><span class="sxs-lookup"><span data-stu-id="501d8-129">Windows</span></span> |
| <span data-ttu-id="501d8-130">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="501d8-130">**Header**</span></span> | <span data-ttu-id="501d8-131">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="501d8-131">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="501d8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="501d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501d8-133">EventWrite</span><span class="sxs-lookup"><span data-stu-id="501d8-133">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="501d8-134">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="501d8-134">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
