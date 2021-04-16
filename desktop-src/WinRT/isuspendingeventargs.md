---
description: Fornece dados para um evento de suspensão de aplicativo.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interface ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751572"
---
# <a name="isuspendingeventargs-interface"></a><span data-ttu-id="c31ac-103">Interface ISuspendingEventArgs</span><span class="sxs-lookup"><span data-stu-id="c31ac-103">ISuspendingEventArgs interface</span></span>

<span data-ttu-id="c31ac-104">Fornece dados para um evento de suspensão de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c31ac-104">Provides data for an app suspending event.</span></span>

## <a name="members"></a><span data-ttu-id="c31ac-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c31ac-105">Members</span></span>

<span data-ttu-id="c31ac-106">A interface **ISuspendingEventArgs** herda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="c31ac-106">The **ISuspendingEventArgs** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="c31ac-107">**ISuspendingEventArgs** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c31ac-107">**ISuspendingEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="c31ac-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c31ac-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c31ac-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c31ac-109">Properties</span></span>

<span data-ttu-id="c31ac-110">A interface **ISuspendingEventArgs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c31ac-110">The **ISuspendingEventArgs** interface has these properties.</span></span>



| <span data-ttu-id="c31ac-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c31ac-111">Property</span></span>                                                                           | <span data-ttu-id="c31ac-112">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c31ac-112">Access type</span></span>           | <span data-ttu-id="c31ac-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c31ac-113">Description</span></span>                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="c31ac-114">**SuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="c31ac-114">**SuspendingOperation**</span></span>](isuspendingeventargs-suspendingoperation.md)<br/> | <span data-ttu-id="c31ac-115">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c31ac-115">Read/write</span></span><br/> | <span data-ttu-id="c31ac-116">Obtém a operação de suspensão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c31ac-116">Gets the app suspending operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c31ac-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c31ac-117">Remarks</span></span>

<span data-ttu-id="c31ac-118">Esse objeto é acessado quando você implementa manipuladores de eventos como [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)e [**adiciona \_ suspensão**](/previous-versions//hh438376(v=vs.85)) para responder a eventos de suspensão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c31ac-118">This object is accessed when you implement event handlers like [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), and [**add\_Suspending**](/previous-versions//hh438376(v=vs.85)) to respond to app suspending events.</span></span>

## <a name="requirements"></a><span data-ttu-id="c31ac-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c31ac-119">Requirements</span></span>



| <span data-ttu-id="c31ac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c31ac-120">Requirement</span></span> | <span data-ttu-id="c31ac-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c31ac-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c31ac-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c31ac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c31ac-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c31ac-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c31ac-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c31ac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c31ac-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c31ac-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c31ac-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c31ac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c31ac-127"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="c31ac-127"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="c31ac-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="c31ac-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c31ac-129"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c31ac-129"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c31ac-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c31ac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31ac-131">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="c31ac-131">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="c31ac-132">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="c31ac-132">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> <dt>

[<span data-ttu-id="c31ac-133">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="c31ac-133">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 
