---
description: Uma janela de vídeo está sendo ativada ou desativada.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779543"
---
# <a name="ec_activate"></a><span data-ttu-id="743d9-103">ativação do EC \_</span><span class="sxs-lookup"><span data-stu-id="743d9-103">EC\_ACTIVATE</span></span>

<span data-ttu-id="743d9-104">Uma janela de vídeo está sendo ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="743d9-104">A video window is being activated or deactivated.</span></span>

## <a name="parameters"></a><span data-ttu-id="743d9-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="743d9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="743d9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="743d9-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="743d9-107">(**Bool**) **True** se a janela for ativada ou **false** se a janela for desativada.</span><span class="sxs-lookup"><span data-stu-id="743d9-107">(**BOOL**) **TRUE** if the window is activated, or **FALSE** if the window is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="743d9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="743d9-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="743d9-109">(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do processador.</span><span class="sxs-lookup"><span data-stu-id="743d9-109">(**IUnknown**\*) Pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="743d9-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="743d9-110">Default Action</span></span>

<span data-ttu-id="743d9-111">O Gerenciador de gráfico de filtro define o foco, por meio da interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="743d9-111">The filter graph manager sets the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="743d9-112">Ele não envia a notificação de eventos para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="743d9-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="743d9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="743d9-113">Remarks</span></span>

<span data-ttu-id="743d9-114">Um processador de vídeo envia esse evento sempre que sua janela é ativada ou desativada (ou seja, quando recebe uma mensagem do WM \_ ACTIVATEAPP).</span><span class="sxs-lookup"><span data-stu-id="743d9-114">A video renderer sends this event whenever its window is activated or deactivated (that is, when it receives a WM\_ACTIVATEAPP message).</span></span> <span data-ttu-id="743d9-115">A ativação ou desativação de janela pode ocorrer porque a janela obteve ou perdeu o foco, ou porque o renderizador mudou entre o modo de tela inteira e o modo em janela.</span><span class="sxs-lookup"><span data-stu-id="743d9-115">Window activation or deactivation can occur because the window has gained or lost focus, or because the renderer has switched between full-screen mode and windowed mode.</span></span>

<span data-ttu-id="743d9-116">Esse evento permite que o Gerenciador do grafo de filtro aloque recursos que dependem do foco da janela, como dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="743d9-116">This event enables the filter graph manager to allocate resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="743d9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="743d9-117">Requirements</span></span>



| <span data-ttu-id="743d9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="743d9-118">Requirement</span></span> | <span data-ttu-id="743d9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="743d9-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="743d9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="743d9-120">Header</span></span><br/> | <dl> <span data-ttu-id="743d9-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="743d9-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="743d9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="743d9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743d9-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="743d9-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="743d9-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="743d9-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




