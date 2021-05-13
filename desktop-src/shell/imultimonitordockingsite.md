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
ms.openlocfilehash: 5ea3461d00c16f7384d7396e2f03946d517c460f
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841887"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="6efdf-104">Interface IMultiMonitorDockingSite</span><span class="sxs-lookup"><span data-stu-id="6efdf-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="6efdf-105">Implementado pelo navegador.</span><span class="sxs-lookup"><span data-stu-id="6efdf-105">Implemented by the browser.</span></span> <span data-ttu-id="6efdf-106">Expõe métodos que gerenciam qual monitor contém a barra de tarefas do Windows em um sistema de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="6efdf-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="6efdf-107">Membros</span><span class="sxs-lookup"><span data-stu-id="6efdf-107">Members</span></span>

<span data-ttu-id="6efdf-108">A interface **IMultiMonitorDockingSite** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6efdf-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6efdf-109">**IMultiMonitorDockingSite** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6efdf-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="6efdf-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6efdf-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6efdf-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6efdf-111">Methods</span></span>

<span data-ttu-id="6efdf-112">A interface **IMultiMonitorDockingSite** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6efdf-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="6efdf-113">Método</span><span class="sxs-lookup"><span data-stu-id="6efdf-113">Method</span></span>                                                            | <span data-ttu-id="6efdf-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6efdf-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6efdf-115">**Getmonitor**</span><span class="sxs-lookup"><span data-stu-id="6efdf-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="6efdf-116">Obtém o monitor padrão atual.</span><span class="sxs-lookup"><span data-stu-id="6efdf-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="6efdf-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="6efdf-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="6efdf-118">Verifica se o monitor está ativo e disponível.</span><span class="sxs-lookup"><span data-stu-id="6efdf-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="6efdf-119">**Setmonitor**</span><span class="sxs-lookup"><span data-stu-id="6efdf-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="6efdf-120">Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.</span><span class="sxs-lookup"><span data-stu-id="6efdf-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6efdf-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6efdf-121">Remarks</span></span>

<span data-ttu-id="6efdf-122">Normalmente, você não implementa a interface **IMultiMonitorDockingSite** .</span><span class="sxs-lookup"><span data-stu-id="6efdf-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="6efdf-123">O navegador de shell implementa essa interface para dar suporte a vários monitores.</span><span class="sxs-lookup"><span data-stu-id="6efdf-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="6efdf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6efdf-124">Requirements</span></span>



| <span data-ttu-id="6efdf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6efdf-125">Requirement</span></span> | <span data-ttu-id="6efdf-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6efdf-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="6efdf-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6efdf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6efdf-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6efdf-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6efdf-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6efdf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6efdf-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6efdf-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
