---
title: WMT_STATUS notificação de eventos no DirectShow
description: '\_Notificação de eventos de status do WMT no DirectShow'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- SDK do Windows Media Format, WMT_STATUS notificações de eventos no DirectShow
- SDK do Windows Media Format, notificações de eventos
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), WMT_STATUS notificações de eventos no DirectShow
- ASF (formato de sistemas avançados), WMT_STATUS notificações de eventos no DirectShow
- ASF (Advanced Systems Format), notificações de eventos
- ASF (formato de sistemas avançados), notificações de eventos
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, notificações de eventos
- DirectShow, WMT_STATUS notificações de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12c953b2c9b1509ad1b3adc2831d2276fcd474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162324"
---
# <a name="wmt_status-event-notification-in-directshow"></a><span data-ttu-id="07f64-114">\_Notificação de eventos de status do WMT no DirectShow</span><span class="sxs-lookup"><span data-stu-id="07f64-114">WMT\_STATUS Event Notification in DirectShow</span></span>

<span data-ttu-id="07f64-115">O leitor de ASF e o gravador ASF encaminham eventos de [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="07f64-115">Both the ASF Reader and the ASF Writer forward [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) events to applications.</span></span> <span data-ttu-id="07f64-116">O gravador encaminha todos esses eventos, e o leitor encaminha apenas aqueles que pertencem à aquisição de licença do DRM.</span><span class="sxs-lookup"><span data-stu-id="07f64-116">The writer forwards all such events, and the reader forwards only those that pertain to DRM license acquisition.</span></span> <span data-ttu-id="07f64-117">Para receber essas notificações de eventos em seu aplicativo, adicione um caso para **o \_ \_ evento WMT do EC** em sua função de manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="07f64-117">To receive these event notifications in your application, add a case for the **EC\_WMT\_EVENT** in your event-handling function.</span></span> <span data-ttu-id="07f64-118">O parâmetro *lParam1* associado ao evento contém o código **de \_ status WMT** (que pode ser **WMT \_ erro**) e lParam2 contém os [**\_ dados de \_ evento \_ am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) que incluem o **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="07f64-118">The *lParam1* parameter associated with the event contains the **WMT\_STATUS** code (which can be **WMT\_ERROR**) and lParam2 contains an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) that includes the **HRESULT**.</span></span>

 

 