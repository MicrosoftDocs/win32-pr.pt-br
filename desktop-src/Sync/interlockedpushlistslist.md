---
UID: ''
title: Função InterlockedPushListSList
description: Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: InterlockedPushListSListEx
ms.topic: reference
req.header:
- WinBase.h on Windows Vista, Windows 7, Windows Server 2008 and Windows Server 2008 R2
- InterlockedAPI.h on Windows 8 and Windows Server 2012
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-interlocked-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-interlocked-l1-1-0.dll
api_name:
- InterlockedPushListSList
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: ccecdae3af5119a86594c31856dac11ecb4507bc
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2020
ms.locfileid: "104365768"
---
# <a name="interlockedpushlistslist-function"></a><span data-ttu-id="9988a-103">Função InterlockedPushListSList</span><span class="sxs-lookup"><span data-stu-id="9988a-103">InterlockedPushListSList function</span></span>

## <a name="description"></a><span data-ttu-id="9988a-104">Description</span><span class="sxs-lookup"><span data-stu-id="9988a-104">Description</span></span>

<span data-ttu-id="9988a-105">Insere uma lista vinculada individualmente na frente de outra lista vinculada individualmente.</span><span class="sxs-lookup"><span data-stu-id="9988a-105">Inserts a singly-linked list at the front of another singly linked list.</span></span>
<span data-ttu-id="9988a-106">O acesso às listas é sincronizado em um sistema multiprocessador.</span><span class="sxs-lookup"><span data-stu-id="9988a-106">Access to the lists is synchronized on a multiprocessor system.</span></span>

```cpp
PSLIST_ENTRY  FASTCALL InterlockedPushListSList(
  _Inout_ PSLIST_HEADER ListHead,
  _Inout_ PSLIST_ENTRY  List,
  _Inout_ PSLIST_ENTRY  ListEnd,
  _In_    ULONG         Count
);
```

## <a name="parameters"></a><span data-ttu-id="9988a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9988a-107">Parameters</span></span>

### <a name="listhead-in-out"></a><span data-ttu-id="9988a-108">ListHead [in, out]</span><span class="sxs-lookup"><span data-stu-id="9988a-108">ListHead [in, out]</span></span>

<span data-ttu-id="9988a-109">Ponteiro para uma estrutura de **SLIST_HEADER** que representa o cabeçalho de uma lista vinculada individualmente.</span><span class="sxs-lookup"><span data-stu-id="9988a-109">Pointer to an **SLIST_HEADER** structure that represents the head of a singly linked list.</span></span>
<span data-ttu-id="9988a-110">A lista especificada pela *lista* e parâmetros *escutados* é inserida na frente desta lista.</span><span class="sxs-lookup"><span data-stu-id="9988a-110">The list specified by the *List* and *ListEnd* parameters is inserted at the front of this list.</span></span>

### <a name="list-in-out"></a><span data-ttu-id="9988a-111">Listar [entrada, saída]</span><span class="sxs-lookup"><span data-stu-id="9988a-111">List [in, out]</span></span>

<span data-ttu-id="9988a-112">Ponteiro para uma estrutura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa o primeiro item da lista a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="9988a-112">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the first item in the list to be inserted.</span></span>

### <a name="listend-in-out"></a><span data-ttu-id="9988a-113">Escutado [in, out]</span><span class="sxs-lookup"><span data-stu-id="9988a-113">ListEnd [in, out]</span></span>

<span data-ttu-id="9988a-114">Ponteiro para uma estrutura de [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) que representa o último item da lista a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="9988a-114">Pointer to an [SLIST_ENTRY](/windows/win32/api/winnt/ns-winnt-slist_entry) structure that represents the last item in the list to be inserted.</span></span>

### <a name="count-in"></a><span data-ttu-id="9988a-115">Contagem [em]</span><span class="sxs-lookup"><span data-stu-id="9988a-115">Count [in]</span></span>

<span data-ttu-id="9988a-116">O número de itens na lista a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="9988a-116">The number of items in the list to be inserted.</span></span>

## <a name="returns"></a><span data-ttu-id="9988a-117">Retornos</span><span class="sxs-lookup"><span data-stu-id="9988a-117">Returns</span></span>

<span data-ttu-id="9988a-118">O valor de retorno é o primeiro item anterior na lista especificada pelo parâmetro *ListHead* .</span><span class="sxs-lookup"><span data-stu-id="9988a-118">The return value is the previous first item in the list specified by the *ListHead* parameter.</span></span>
<span data-ttu-id="9988a-119">Se a lista estava vazia anteriormente, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9988a-119">If the list was previously empty, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9988a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9988a-120">Remarks</span></span>

<span data-ttu-id="9988a-121">Todos os itens de lista devem ser alinhados em um limite de **MEMORY_ALLOCATION_ALIGNMENT** ; caso contrário, essa função terá um comportamento não previsível.</span><span class="sxs-lookup"><span data-stu-id="9988a-121">All list items must be aligned on a **MEMORY_ALLOCATION_ALIGNMENT** boundary; otherwise, this function will behave unpredictably.</span></span>
<span data-ttu-id="9988a-122">Consulte **_aligned_malloc**.</span><span class="sxs-lookup"><span data-stu-id="9988a-122">See **_aligned_malloc**.</span></span>

<span data-ttu-id="9988a-123">**Windows 8 e Windows Server 2012:**  Essa função foi substituída por [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span><span class="sxs-lookup"><span data-stu-id="9988a-123">**Windows 8 and Windows Server 2012:**  This function has been superceded by [InterlockedPushListSListEx](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex).</span></span>
<span data-ttu-id="9988a-124">Ao compilar com **NTDDI_VERSION** definido como **NTDDI_WIN8** ou superior, chamadas para **InterlockedPushListSList** vão para **InterlockedPushListSListEx** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9988a-124">When compiling with **NTDDI_VERSION** set to **NTDDI_WIN8** or greater, calls to **InterlockedPushListSList** will go to **InterlockedPushListSListEx** instead.</span></span>

## <a name="see-also"></a><span data-ttu-id="9988a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9988a-125">See also</span></span>

[<span data-ttu-id="9988a-126">Listas vinculadas isoladamente interbloqueadas</span><span class="sxs-lookup"><span data-stu-id="9988a-126">Interlocked Singly Linked Lists</span></span>](/windows/desktop/Sync/interlocked-singly-linked-lists)

[<span data-ttu-id="9988a-127">InterlockedPopEntrySList</span><span class="sxs-lookup"><span data-stu-id="9988a-127">InterlockedPopEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)

[<span data-ttu-id="9988a-128">InterlockedPushEntrySList</span><span class="sxs-lookup"><span data-stu-id="9988a-128">InterlockedPushEntrySList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)

[<span data-ttu-id="9988a-129">InterlockedPushListSListEx</span><span class="sxs-lookup"><span data-stu-id="9988a-129">InterlockedPushListSListEx</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)

[<span data-ttu-id="9988a-130">InterlockedFlushSList</span><span class="sxs-lookup"><span data-stu-id="9988a-130">InterlockedFlushSList</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedflushslist)

[<span data-ttu-id="9988a-131">SLIST_ENTRY</span><span class="sxs-lookup"><span data-stu-id="9988a-131">SLIST_ENTRY</span></span>](/windows/win32/api/winnt/ns-winnt-slist_entry)

[<span data-ttu-id="9988a-132">Usando listas vinculadas individualmente</span><span class="sxs-lookup"><span data-stu-id="9988a-132">Using Singly Linked Lists</span></span>](/windows/desktop/Sync/using-singly-linked-lists)
