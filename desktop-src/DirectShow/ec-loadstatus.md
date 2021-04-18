---
description: Notifica o aplicativo sobre o progresso ao abrir um arquivo de rede.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780634"
---
# <a name="ec_loadstatus"></a><span data-ttu-id="04e31-103">loadstatus do EC \_</span><span class="sxs-lookup"><span data-stu-id="04e31-103">EC\_LOADSTATUS</span></span>

<span data-ttu-id="04e31-104">Notifica o aplicativo sobre o progresso ao abrir um arquivo de rede.</span><span class="sxs-lookup"><span data-stu-id="04e31-104">Notifies the application of progress when opening a network file.</span></span>

## <a name="parameters"></a><span data-ttu-id="04e31-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04e31-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e31-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="04e31-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="04e31-107">Código de status.</span><span class="sxs-lookup"><span data-stu-id="04e31-107">Status code.</span></span> <span data-ttu-id="04e31-108">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="04e31-108">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="04e31-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="04e31-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="04e31-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="04e31-110">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="04e31-111">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="04e31-111">Default Action</span></span>

<span data-ttu-id="04e31-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="04e31-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e31-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="04e31-113">Remarks</span></span>

<span data-ttu-id="04e31-114">O filtro de [leitor ASF do WM](wm-asf-reader-filter.md) e o filtro de [origem do Windows Media](windows-media-source-filter.md) herdado enviam esse evento.</span><span class="sxs-lookup"><span data-stu-id="04e31-114">The [WM ASF Reader](wm-asf-reader-filter.md) filter and the legacy [Windows Media Source](windows-media-source-filter.md) filter send this event.</span></span> <span data-ttu-id="04e31-115">O primeiro parâmetro de evento tem um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="04e31-115">The first event parameter has one of the following values.</span></span>



| <span data-ttu-id="04e31-116">Valor</span><span class="sxs-lookup"><span data-stu-id="04e31-116">Value</span></span>                        | <span data-ttu-id="04e31-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="04e31-117">Description</span></span>                                    |
|------------------------------|------------------------------------------------|
| <span data-ttu-id="04e31-118">\_loadstatus \_ encerrado</span><span class="sxs-lookup"><span data-stu-id="04e31-118">AM\_LOADSTATUS\_CLOSED</span></span>       | <span data-ttu-id="04e31-119">O filtro de origem fechou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="04e31-119">The source filter has closed the file.</span></span>         |
| <span data-ttu-id="04e31-120">\_conexão do LOADstatus \_</span><span class="sxs-lookup"><span data-stu-id="04e31-120">AM\_LOADSTATUS\_CONNECTING</span></span>   | <span data-ttu-id="04e31-121">O filtro de origem está se conectando ao servidor.</span><span class="sxs-lookup"><span data-stu-id="04e31-121">The source filter is connecting to the server.</span></span> |
| <span data-ttu-id="04e31-122">\_LOADINGDESCR LOADstatus \_</span><span class="sxs-lookup"><span data-stu-id="04e31-122">AM\_LOADSTATUS\_LOADINGDESCR</span></span> | <span data-ttu-id="04e31-123">Não usado.</span><span class="sxs-lookup"><span data-stu-id="04e31-123">Not used.</span></span>                                      |
| <span data-ttu-id="04e31-124">\_LOADINGMCAST LOADstatus \_</span><span class="sxs-lookup"><span data-stu-id="04e31-124">AM\_LOADSTATUS\_LOADINGMCAST</span></span> | <span data-ttu-id="04e31-125">Não usado</span><span class="sxs-lookup"><span data-stu-id="04e31-125">Not used</span></span>                                       |
| <span data-ttu-id="04e31-126">\_loadstatus \_ localizando</span><span class="sxs-lookup"><span data-stu-id="04e31-126">AM\_LOADSTATUS\_LOCATING</span></span>     | <span data-ttu-id="04e31-127">O filtro de origem está localizando os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="04e31-127">The source filter is locating requested data.</span></span>  |
| <span data-ttu-id="04e31-128">\_loadstatus \_ aberto</span><span class="sxs-lookup"><span data-stu-id="04e31-128">AM\_LOADSTATUS\_OPEN</span></span>         | <span data-ttu-id="04e31-129">O filtro de origem abriu o arquivo.</span><span class="sxs-lookup"><span data-stu-id="04e31-129">The source filter has opened the file.</span></span>         |
| <span data-ttu-id="04e31-130">\_abertura de LOADSTATUS am \_</span><span class="sxs-lookup"><span data-stu-id="04e31-130">AM\_LOADSTATUS\_OPENING</span></span>      | <span data-ttu-id="04e31-131">O filtro de origem está abrindo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="04e31-131">The source filter is opening the file.</span></span>         |



 

## <a name="requirements"></a><span data-ttu-id="04e31-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04e31-132">Requirements</span></span>



| <span data-ttu-id="04e31-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e31-133">Requirement</span></span> | <span data-ttu-id="04e31-134">Valor</span><span class="sxs-lookup"><span data-stu-id="04e31-134">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04e31-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04e31-135">Header</span></span><br/> | <dl> <span data-ttu-id="04e31-136"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="04e31-136"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04e31-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="04e31-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e31-138">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="04e31-138">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="04e31-139">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="04e31-139">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




