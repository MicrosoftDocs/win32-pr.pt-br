---
description: Implementado pelo navegador. Expõe métodos que gerenciam qual monitor contém a barra de tarefas do Windows em um sistema de vários monitores.
title: Interface IMultiMonitorDockingSite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989112"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="18969-104">Interface IMultiMonitorDockingSite</span><span class="sxs-lookup"><span data-stu-id="18969-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="18969-105">Implementado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="18969-105">Implemented by the browser.</span></span> <span data-ttu-id="18969-106">Expõe métodos que gerenciam qual monitor contém a barra de tarefas do Windows em um sistema de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="18969-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="18969-107">Membros</span><span class="sxs-lookup"><span data-stu-id="18969-107">Members</span></span>

<span data-ttu-id="18969-108">A interface **IMultiMonitorDockingSite** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="18969-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="18969-109">**IMultiMonitorDockingSite** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="18969-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="18969-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="18969-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="18969-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="18969-111">Methods</span></span>

<span data-ttu-id="18969-112">A interface **IMultiMonitorDockingSite** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="18969-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="18969-113">Método</span><span class="sxs-lookup"><span data-stu-id="18969-113">Method</span></span>                                                            | <span data-ttu-id="18969-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="18969-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18969-115">**Getmonitor**</span><span class="sxs-lookup"><span data-stu-id="18969-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="18969-116">Obtém o monitor padrão atual.</span><span class="sxs-lookup"><span data-stu-id="18969-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="18969-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="18969-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="18969-118">Verifica se o monitor está ativo e disponível.</span><span class="sxs-lookup"><span data-stu-id="18969-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="18969-119">**Setmonitor**</span><span class="sxs-lookup"><span data-stu-id="18969-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="18969-120">Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="18969-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18969-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="18969-121">Remarks</span></span>

<span data-ttu-id="18969-122">Normalmente, você não implementa a interface **IMultiMonitorDockingSite** .</span><span class="sxs-lookup"><span data-stu-id="18969-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="18969-123">O navegador de shell implementa essa interface para dar suporte a vários monitores.</span><span class="sxs-lookup"><span data-stu-id="18969-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="18969-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18969-124">Requirements</span></span>



| <span data-ttu-id="18969-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="18969-125">Requirement</span></span> | <span data-ttu-id="18969-126">Valor</span><span class="sxs-lookup"><span data-stu-id="18969-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="18969-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18969-127">Minimum supported client</span></span><br/> | <span data-ttu-id="18969-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="18969-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="18969-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18969-129">Minimum supported server</span></span><br/> | <span data-ttu-id="18969-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18969-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
