---
description: Habilita a conclusão da tarefa.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interface TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171172"
---
# <a name="taskcompletionclient-interface"></a><span data-ttu-id="26cbf-103">Interface TaskCompletionClient</span><span class="sxs-lookup"><span data-stu-id="26cbf-103">TaskCompletionClient interface</span></span>

<span data-ttu-id="26cbf-104">Habilita a conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="26cbf-104">Enables task completion.</span></span>

## <a name="members"></a><span data-ttu-id="26cbf-105">Membros</span><span class="sxs-lookup"><span data-stu-id="26cbf-105">Members</span></span>

<span data-ttu-id="26cbf-106">A interface **TaskCompletionClient** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="26cbf-106">The **TaskCompletionClient** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="26cbf-107">**TaskCompletionClient** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="26cbf-107">**TaskCompletionClient** also has these types of members:</span></span>

-   [<span data-ttu-id="26cbf-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="26cbf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26cbf-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="26cbf-109">Methods</span></span>

<span data-ttu-id="26cbf-110">A interface **TaskCompletionClient** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="26cbf-110">The **TaskCompletionClient** interface has these methods.</span></span>



| <span data-ttu-id="26cbf-111">Método</span><span class="sxs-lookup"><span data-stu-id="26cbf-111">Method</span></span>                                                                    | <span data-ttu-id="26cbf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="26cbf-112">Description</span></span>                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [<span data-ttu-id="26cbf-113">**ApplyTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="26cbf-113">**ApplyTaskCompletion**</span></span>](taskcompletionclient-applytaskcompletion.md)   | <span data-ttu-id="26cbf-114">Inicia a conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="26cbf-114">Begins the task completion.</span></span><br/> |
| [<span data-ttu-id="26cbf-115">**RevokeTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="26cbf-115">**RevokeTaskCompletion**</span></span>](taskcompletionclient-revoketaskcompletion.md) | <span data-ttu-id="26cbf-116">Encerra a conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="26cbf-116">Ends the task completion.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="26cbf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="26cbf-117">Remarks</span></span>

<span data-ttu-id="26cbf-118">O GUID desta interface é "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span><span class="sxs-lookup"><span data-stu-id="26cbf-118">The GUID for this interface is "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span></span>

<span data-ttu-id="26cbf-119">Essa API foi preterida e pode não estar disponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="26cbf-119">This API is deprecated and may not be available in future versions of Windows.</span></span> <span data-ttu-id="26cbf-120">Os aplicativos devem usar as APIs no namespace [**Windows. ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="26cbf-120">Apps should use the APIs in the [**Windows.ApplicationModel.ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) namespace instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="26cbf-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26cbf-121">Requirements</span></span>



| <span data-ttu-id="26cbf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="26cbf-122">Requirement</span></span> | <span data-ttu-id="26cbf-123">Valor</span><span class="sxs-lookup"><span data-stu-id="26cbf-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26cbf-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26cbf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="26cbf-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="26cbf-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26cbf-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26cbf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="26cbf-127">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="26cbf-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="26cbf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="26cbf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26cbf-129"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26cbf-129"><dt>ExecModelClient.dll</dt></span></span> </dl> |



 

 
