---
description: A interface IMonitor fornece métodos que controlam a operação do monitor. Esses métodos são chamados pelo serviço de controle de monitor (MCSVC).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interface IMonitor (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827465"
---
# <a name="imonitor-interface"></a><span data-ttu-id="5c6ad-104">Interface IMonitor</span><span class="sxs-lookup"><span data-stu-id="5c6ad-104">IMonitor interface</span></span>

<span data-ttu-id="5c6ad-105">A interface **iMonitor** fornece métodos que controlam a operação do monitor.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-105">The **IMonitor** interface provides methods that control monitor operation.</span></span> <span data-ttu-id="5c6ad-106">Esses métodos são chamados pelo [*serviço de controle de monitor*](m.md) (MCSVC).</span><span class="sxs-lookup"><span data-stu-id="5c6ad-106">These methods are called by the [*Monitor Control Service*](m.md) (MCSVC).</span></span>

## <a name="members"></a><span data-ttu-id="5c6ad-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5c6ad-107">Members</span></span>

<span data-ttu-id="5c6ad-108">A interface **iMonitor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5c6ad-108">The **IMonitor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5c6ad-109">**IMonitor** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5c6ad-109">**IMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="5c6ad-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c6ad-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5c6ad-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c6ad-111">Methods</span></span>

<span data-ttu-id="5c6ad-112">A interface **iMonitor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-112">The **IMonitor** interface has these methods.</span></span>



| <span data-ttu-id="5c6ad-113">Método</span><span class="sxs-lookup"><span data-stu-id="5c6ad-113">Method</span></span>                                        | <span data-ttu-id="5c6ad-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c6ad-114">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c6ad-115">**Configurar doconfigure**</span><span class="sxs-lookup"><span data-stu-id="5c6ad-115">**DoConfigure**</span></span>](imonitor-doconfigure.md)   | <span data-ttu-id="5c6ad-116">Atualiza a configuração do monitor.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-116">Updates monitor configuration.</span></span><br/>                                                                           |
| [<span data-ttu-id="5c6ad-117">**Doinitialize**</span><span class="sxs-lookup"><span data-stu-id="5c6ad-117">**DoInitialize**</span></span>](imonitor-doinitialize.md) | <span data-ttu-id="5c6ad-118">Inicializa um monitor.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-118">Initializes a monitor.</span></span><br/>                                                                                   |
| [<span data-ttu-id="5c6ad-119">**Nos quadros**</span><span class="sxs-lookup"><span data-stu-id="5c6ad-119">**OnFrames**</span></span>](imonitor-onframes.md)         | <span data-ttu-id="5c6ad-120">Indica o status de um evento de quadro.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-120">Indicates the status of a frame event.</span></span><br/>                                                                   |
| [<span data-ttu-id="5c6ad-121">**Star**</span><span class="sxs-lookup"><span data-stu-id="5c6ad-121">**OnStart**</span></span>](imonitor-onstart.md)           | <span data-ttu-id="5c6ad-122">Indica que o monitor foi configurado com êxito e que a captura de dados está prestes a começar.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-122">Indicates that the monitor has been configured successfully and that the data capture is about to begin.</span></span><br/> |
| [<span data-ttu-id="5c6ad-123">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="5c6ad-123">**OnStatus**</span></span>](imonitor-onstatus.md)         | <span data-ttu-id="5c6ad-124">Indica um evento de status NPP.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-124">Indicates an NPP status event.</span></span><br/>                                                                           |
| [<span data-ttu-id="5c6ad-125">**OnStop**</span><span class="sxs-lookup"><span data-stu-id="5c6ad-125">**OnStop**</span></span>](imonitor-onstop.md)             | <span data-ttu-id="5c6ad-126">Indica a conclusão da captura de dados.</span><span class="sxs-lookup"><span data-stu-id="5c6ad-126">Indicates data capture completion.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="5c6ad-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c6ad-127">Requirements</span></span>



| <span data-ttu-id="5c6ad-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c6ad-128">Requirement</span></span> | <span data-ttu-id="5c6ad-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5c6ad-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6ad-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c6ad-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5c6ad-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c6ad-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5c6ad-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c6ad-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5c6ad-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c6ad-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c6ad-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c6ad-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c6ad-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c6ad-135"><dt>Netmon.h</dt></span></span> </dl> |



 

