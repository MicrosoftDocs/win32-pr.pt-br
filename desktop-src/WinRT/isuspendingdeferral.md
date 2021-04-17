---
description: Gerencia uma operação de suspensão de aplicativo atrasada.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interface ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749524"
---
# <a name="isuspendingdeferral-interface"></a><span data-ttu-id="d57e5-103">Interface ISuspendingDeferral</span><span class="sxs-lookup"><span data-stu-id="d57e5-103">ISuspendingDeferral interface</span></span>

<span data-ttu-id="d57e5-104">Gerencia uma operação de suspensão de aplicativo atrasada.</span><span class="sxs-lookup"><span data-stu-id="d57e5-104">Manages a delayed app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="d57e5-105">Membros</span><span class="sxs-lookup"><span data-stu-id="d57e5-105">Members</span></span>

<span data-ttu-id="d57e5-106">A interface **ISuspendingDeferral** herda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="d57e5-106">The **ISuspendingDeferral** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="d57e5-107">**ISuspendingDeferral** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d57e5-107">**ISuspendingDeferral** also has these types of members:</span></span>

-   [<span data-ttu-id="d57e5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="d57e5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d57e5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d57e5-109">Methods</span></span>

<span data-ttu-id="d57e5-110">A interface **ISuspendingDeferral** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d57e5-110">The **ISuspendingDeferral** interface has these methods.</span></span>



| <span data-ttu-id="d57e5-111">Método</span><span class="sxs-lookup"><span data-stu-id="d57e5-111">Method</span></span>                                           | <span data-ttu-id="d57e5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d57e5-112">Description</span></span>                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d57e5-113">**Concluir**</span><span class="sxs-lookup"><span data-stu-id="d57e5-113">**Complete**</span></span>](isuspendingdeferral-complete.md) | <span data-ttu-id="d57e5-114">Notifica o sistema que o aplicativo salvou seus dados e está pronto para ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="d57e5-114">Notifies the system that the app has saved its data and is ready to be suspended.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d57e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d57e5-115">Requirements</span></span>



| <span data-ttu-id="d57e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d57e5-116">Requirement</span></span> | <span data-ttu-id="d57e5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d57e5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d57e5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d57e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d57e5-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d57e5-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d57e5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d57e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d57e5-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d57e5-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d57e5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d57e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d57e5-123"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57e5-123"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="d57e5-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="d57e5-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d57e5-125"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d57e5-125"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57e5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d57e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57e5-127">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="d57e5-127">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="d57e5-128">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="d57e5-128">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> <dt>

[<span data-ttu-id="d57e5-129">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="d57e5-129">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 
