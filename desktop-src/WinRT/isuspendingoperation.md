---
description: Fornece informações sobre uma operação de suspensão de aplicativo.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interface ISuspendingOperation (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501712"
---
# <a name="isuspendingoperation-interface"></a><span data-ttu-id="4678d-103">Interface ISuspendingOperation</span><span class="sxs-lookup"><span data-stu-id="4678d-103">ISuspendingOperation interface</span></span>

<span data-ttu-id="4678d-104">Fornece informações sobre uma operação de suspensão de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4678d-104">Provides information about an app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="4678d-105">Membros</span><span class="sxs-lookup"><span data-stu-id="4678d-105">Members</span></span>

<span data-ttu-id="4678d-106">A interface **ISuspendingOperation** herda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="4678d-106">The **ISuspendingOperation** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="4678d-107">**ISuspendingOperation** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4678d-107">**ISuspendingOperation** also has these types of members:</span></span>

-   [<span data-ttu-id="4678d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="4678d-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="4678d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4678d-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4678d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4678d-110">Methods</span></span>

<span data-ttu-id="4678d-111">A interface **ISuspendingOperation** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4678d-111">The **ISuspendingOperation** interface has these methods.</span></span>



| <span data-ttu-id="4678d-112">Método</span><span class="sxs-lookup"><span data-stu-id="4678d-112">Method</span></span>                                                  | <span data-ttu-id="4678d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4678d-113">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="4678d-114">**Getadiamento**</span><span class="sxs-lookup"><span data-stu-id="4678d-114">**GetDeferral**</span></span>](isuspendingoperation-getdeferral.md) | <span data-ttu-id="4678d-115">Solicita que a operação de suspensão do aplicativo seja atrasada.</span><span class="sxs-lookup"><span data-stu-id="4678d-115">Requests that the app suspending operation be delayed.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4678d-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4678d-116">Properties</span></span>

<span data-ttu-id="4678d-117">A interface **ISuspendingOperation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4678d-117">The **ISuspendingOperation** interface has these properties.</span></span>



| <span data-ttu-id="4678d-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4678d-118">Property</span></span>                                                     | <span data-ttu-id="4678d-119">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4678d-119">Access type</span></span>           | <span data-ttu-id="4678d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="4678d-120">Description</span></span>                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4678d-121">**Prazo**</span><span class="sxs-lookup"><span data-stu-id="4678d-121">**Deadline**</span></span>](isuspendingoperation-deadline.md)<br/> | <span data-ttu-id="4678d-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4678d-122">Read/write</span></span><br/> | <span data-ttu-id="4678d-123">Obtém o tempo restante antes de uma operação de suspensão de aplicativo atrasado continuar.</span><span class="sxs-lookup"><span data-stu-id="4678d-123">Gets the time remaining before a delayed app suspending operation continues.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4678d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4678d-124">Requirements</span></span>



| <span data-ttu-id="4678d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4678d-125">Requirement</span></span> | <span data-ttu-id="4678d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4678d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4678d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4678d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4678d-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4678d-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4678d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4678d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4678d-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4678d-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4678d-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4678d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4678d-132"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="4678d-132"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="4678d-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="4678d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4678d-134"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4678d-134"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4678d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4678d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4678d-136">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="4678d-136">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="4678d-137">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="4678d-137">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> <dt>

[<span data-ttu-id="4678d-138">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="4678d-138">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 
