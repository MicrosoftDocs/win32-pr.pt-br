---
description: A interface IMonitorEventer fornece métodos para enviar eventos e alocar e liberar recursos de monitor.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interface IMonitorEventer (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827035"
---
# <a name="imonitoreventer-interface"></a><span data-ttu-id="41cc3-103">Interface IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="41cc3-103">IMonitorEventer interface</span></span>

<span data-ttu-id="41cc3-104">A interface **IMonitorEventer** fornece métodos para enviar eventos e alocar e liberar recursos de monitor.</span><span class="sxs-lookup"><span data-stu-id="41cc3-104">The **IMonitorEventer** interface provides methods for submitting events and allocating and freeing monitor resources.</span></span>

## <a name="members"></a><span data-ttu-id="41cc3-105">Membros</span><span class="sxs-lookup"><span data-stu-id="41cc3-105">Members</span></span>

<span data-ttu-id="41cc3-106">A interface **IMonitorEventer** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="41cc3-106">The **IMonitorEventer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="41cc3-107">**IMonitorEventer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="41cc3-107">**IMonitorEventer** also has these types of members:</span></span>

-   [<span data-ttu-id="41cc3-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="41cc3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="41cc3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="41cc3-109">Methods</span></span>

<span data-ttu-id="41cc3-110">A interface **IMonitorEventer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="41cc3-110">The **IMonitorEventer** interface has these methods.</span></span>



| <span data-ttu-id="41cc3-111">Método</span><span class="sxs-lookup"><span data-stu-id="41cc3-111">Method</span></span>                                                 | <span data-ttu-id="41cc3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="41cc3-112">Description</span></span>                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="41cc3-113">**FreeEventData**</span><span class="sxs-lookup"><span data-stu-id="41cc3-113">**FreeEventData**</span></span>](imonitoreventer-freeeventdata.md) | <span data-ttu-id="41cc3-114">Libera espaço alocado para monitorar dados.</span><span class="sxs-lookup"><span data-stu-id="41cc3-114">Frees space allocated for monitor data.</span></span><br/> |
| [<span data-ttu-id="41cc3-115">**GetEventData**</span><span class="sxs-lookup"><span data-stu-id="41cc3-115">**GetEventData**</span></span>](imonitoreventer-geteventdata.md)   | <span data-ttu-id="41cc3-116">Aloca espaço para monitorar dados.</span><span class="sxs-lookup"><span data-stu-id="41cc3-116">Allocates space for monitor data.</span></span><br/>       |
| [<span data-ttu-id="41cc3-117">**SendNMEvent**</span><span class="sxs-lookup"><span data-stu-id="41cc3-117">**SendNMEvent**</span></span>](imonitoreventer-sendnmevent.md)     | <span data-ttu-id="41cc3-118">Envia eventos para o WMI.</span><span class="sxs-lookup"><span data-stu-id="41cc3-118">Submits events to WMI.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="41cc3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41cc3-119">Requirements</span></span>



| <span data-ttu-id="41cc3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="41cc3-120">Requirement</span></span> | <span data-ttu-id="41cc3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="41cc3-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41cc3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41cc3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41cc3-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41cc3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41cc3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41cc3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41cc3-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41cc3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41cc3-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="41cc3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="41cc3-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41cc3-127"><dt>Netmon.h</dt></span></span> </dl> |



 

