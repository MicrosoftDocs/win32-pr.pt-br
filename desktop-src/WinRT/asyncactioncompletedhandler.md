---
description: Representa o método que é chamado quando uma ação assíncrona é concluída.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interface AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798276"
---
# <a name="asyncactioncompletedhandler-interface"></a><span data-ttu-id="21b7d-103">Interface AsyncActionCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="21b7d-103">AsyncActionCompletedHandler interface</span></span>

<span data-ttu-id="21b7d-104">Representa o método que é chamado quando uma ação assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="21b7d-104">Represents the method that is called when an asynchronous action completes.</span></span>

## <a name="members"></a><span data-ttu-id="21b7d-105">Membros</span><span class="sxs-lookup"><span data-stu-id="21b7d-105">Members</span></span>

<span data-ttu-id="21b7d-106">A interface **AsyncActionCompletedHandler** herda de [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span><span class="sxs-lookup"><span data-stu-id="21b7d-106">The **AsyncActionCompletedHandler** interface inherits from [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span></span> <span data-ttu-id="21b7d-107">**AsyncActionCompletedHandler** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="21b7d-107">**AsyncActionCompletedHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="21b7d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="21b7d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21b7d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="21b7d-109">Methods</span></span>

<span data-ttu-id="21b7d-110">A interface **AsyncActionCompletedHandler** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="21b7d-110">The **AsyncActionCompletedHandler** interface has these methods.</span></span>



| <span data-ttu-id="21b7d-111">Método</span><span class="sxs-lookup"><span data-stu-id="21b7d-111">Method</span></span>                                               | <span data-ttu-id="21b7d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="21b7d-112">Description</span></span>                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21b7d-113">**Chame**</span><span class="sxs-lookup"><span data-stu-id="21b7d-113">**Invoke**</span></span>](asyncactioncompletedhandler-invoke.md) | <span data-ttu-id="21b7d-114">Invoca o método que é chamado quando a ação assíncrona especificada é concluída.</span><span class="sxs-lookup"><span data-stu-id="21b7d-114">Invokes the method that is called when the specified asynchronous action completes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="21b7d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="21b7d-115">Remarks</span></span>

<span data-ttu-id="21b7d-116">Atribua um **AsyncActionCompletedHandler** a um [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) para receber uma notificação quando a ação assíncrona for concluída.</span><span class="sxs-lookup"><span data-stu-id="21b7d-116">Assign an **AsyncActionCompletedHandler** to an [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) to receive a notification when the asynchronous action completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b7d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21b7d-117">Requirements</span></span>



| <span data-ttu-id="21b7d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="21b7d-118">Requirement</span></span> | <span data-ttu-id="21b7d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="21b7d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b7d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21b7d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="21b7d-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="21b7d-121">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="21b7d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21b7d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="21b7d-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21b7d-123">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="21b7d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21b7d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="21b7d-125"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21b7d-125"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b7d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="21b7d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b7d-127">**IAsyncInfo**</span><span class="sxs-lookup"><span data-stu-id="21b7d-127">**IAsyncInfo**</span></span>](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

