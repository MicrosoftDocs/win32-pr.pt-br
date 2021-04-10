---
description: Define métodos que manipulam os eventos da interface ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Interface ITabletEventSink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171855"
---
# <a name="itableteventsink-interface"></a><span data-ttu-id="dbb6b-103">Interface ITabletEventSink</span><span class="sxs-lookup"><span data-stu-id="dbb6b-103">ITabletEventSink interface</span></span>

<span data-ttu-id="dbb6b-104">Define métodos que manipulam os eventos da [**interface ITablet**](itablet.md) .</span><span class="sxs-lookup"><span data-stu-id="dbb6b-104">Defines methods that handle the [**ITablet Interface**](itablet.md) events.</span></span>

## <a name="members"></a><span data-ttu-id="dbb6b-105">Membros</span><span class="sxs-lookup"><span data-stu-id="dbb6b-105">Members</span></span>

<span data-ttu-id="dbb6b-106">A interface **ITabletEventSink** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dbb6b-106">The **ITabletEventSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dbb6b-107">**ITabletEventSink** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dbb6b-107">**ITabletEventSink** also has these types of members:</span></span>

-   [<span data-ttu-id="dbb6b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbb6b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dbb6b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbb6b-109">Methods</span></span>

<span data-ttu-id="dbb6b-110">A interface **ITabletEventSink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-110">The **ITabletEventSink** interface has these methods.</span></span>



| <span data-ttu-id="dbb6b-111">Método</span><span class="sxs-lookup"><span data-stu-id="dbb6b-111">Method</span></span>                                                        | <span data-ttu-id="dbb6b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbb6b-112">Description</span></span>                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbb6b-113">**ContextCreate**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-113">**ContextCreate**</span></span>](itableteventsink-contextcreate.md)       | <span data-ttu-id="dbb6b-114">Ocorre quando um novo contexto do Tablet é criado.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-114">Occurs when a new tablet context is created.</span></span><br/>                                          |
| [<span data-ttu-id="dbb6b-115">**ContextDestroy**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-115">**ContextDestroy**</span></span>](itableteventsink-contextdestroy.md)     | <span data-ttu-id="dbb6b-116">Ocorre quando um contexto do Tablet está sendo destruído.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-116">Occurs when a tablet context is being destroyed.</span></span><br/>                                      |
| [<span data-ttu-id="dbb6b-117">**CursorDown**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-117">**CursorDown**</span></span>](itableteventsink-cursordown.md)             | <span data-ttu-id="dbb6b-118">Ocorre quando a dica da caneta entra em contato com a superfície do Tablet de digitalização.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-118">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span><br/>                    |
| [<span data-ttu-id="dbb6b-119">**CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-119">**CursorInRange**</span></span>](itableteventsink-cursorinrange.md)       | <span data-ttu-id="dbb6b-120">Ocorre quando uma caneta entra dentro do intervalo de detecção do digitalizador.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-120">Occurs when a stylus comes within the digitizer's range of detection.</span></span><br/>                 |
| [<span data-ttu-id="dbb6b-121">**CursorMove**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-121">**CursorMove**</span></span>](itableteventsink-cursormove.md)             | <span data-ttu-id="dbb6b-122">Ocorre quando o cursor se move sobre o digitalizador digitalizador.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-122">Occurs when the cursor moves over the tablet digitizer.</span></span><br/>                               |
| [<span data-ttu-id="dbb6b-123">**CursorNew**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-123">**CursorNew**</span></span>](itableteventsink-cursornew.md)               | <span data-ttu-id="dbb6b-124">Ocorre quando uma nova caneta é adicionada ao sistema.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-124">Occurs when a new stylus is added to the system.</span></span><br/>                                      |
| [<span data-ttu-id="dbb6b-125">**CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-125">**CursorOutOfRange**</span></span>](itableteventsink-cursoroutofrange.md) | <span data-ttu-id="dbb6b-126">Ocorre quando a caneta deixa o intervalo de detecção física (proximidade) do Tablet.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-126">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span><br/> |
| [<span data-ttu-id="dbb6b-127">**CursorUp**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-127">**CursorUp**</span></span>](itableteventsink-cursorup.md)                 | <span data-ttu-id="dbb6b-128">Ocorre quando o usuário dispara a caneta da superfície digitalizadora do Tablet.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-128">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span><br/>         |
| [<span data-ttu-id="dbb6b-129">**Pacotes**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-129">**Packets**</span></span>](itableteventsink-packets.md)                   | <span data-ttu-id="dbb6b-130">Ocorre quando a caneta está sendo movida no digitalizador.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-130">Occurs when the stylus is moving on the digitizer.</span></span><br/>                                    |
| [<span data-ttu-id="dbb6b-131">**SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="dbb6b-131">**SystemEvent**</span></span>](itableteventsink-systemevent.md)           | <span data-ttu-id="dbb6b-132">Ocorre quando um evento do sistema está disponível.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-132">Occurs when a system event is available.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="dbb6b-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbb6b-133">Remarks</span></span>

<span data-ttu-id="dbb6b-134">Os desenvolvedores não devem usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-134">Developers should not use this interface.</span></span>

<span data-ttu-id="dbb6b-135">O código a seguir mostra como a interface **ITabletEventSink** é definida.</span><span class="sxs-lookup"><span data-stu-id="dbb6b-135">The following code shows how the **ITabletEventSink** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a><span data-ttu-id="dbb6b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbb6b-136">Requirements</span></span>



| <span data-ttu-id="dbb6b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb6b-137">Requirement</span></span> | <span data-ttu-id="dbb6b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb6b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb6b-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb6b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb6b-140">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dbb6b-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dbb6b-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb6b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb6b-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbb6b-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dbb6b-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbb6b-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="dbb6b-144"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbb6b-144"><dt>Wisptis.exe</dt></span></span> </dl> |



 

