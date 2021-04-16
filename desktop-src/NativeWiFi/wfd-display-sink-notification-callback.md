---
description: Define a função de retorno de chamada&\# 8212; que você implementa em seu aplicativo&\# 8212; que foi especificado para a função WFDStartDisplaySink.
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK função de retorno de chamada (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751097"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a><span data-ttu-id="430d5-103">Função de retorno de chamada de notificação do coletor de \_ vídeo WFD \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="430d5-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK callback function</span></span>

<span data-ttu-id="430d5-104">A função de **retorno de chamada de \_ notificação do coletor de vídeo \_ \_ \_ WFD** define a função de retorno de chamada, que você implementa em seu aplicativo — que foi especificada para a função [**WFDStartDisplaySink**](wfdstartdisplaysink.md) .</span><span class="sxs-lookup"><span data-stu-id="430d5-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK** function defines the callback function—which you implement in your app—that was specified to the [**WFDStartDisplaySink**](wfdstartdisplaysink.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="430d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="430d5-105">Syntax</span></span>


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a><span data-ttu-id="430d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="430d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="430d5-107">*pvContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="430d5-107">*pvContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="430d5-108">Um ponteiro de contexto opcional passado para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="430d5-108">An optional context pointer passed to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="430d5-109">*pNotification* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="430d5-109">*pNotification* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="430d5-110">Um ponteiro para uma struct que contém dados sobre a notificação do coletor de exibição.</span><span class="sxs-lookup"><span data-stu-id="430d5-110">A pointer to a struct containing data about the display sink notification.</span></span>

</dd> <dt>

<span data-ttu-id="430d5-111">*pNotificationResult* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="430d5-111">*pNotificationResult* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="430d5-112">Um ponteiro para uma struct que contém dados que seu aplicativo pode definir opcionalmente para indicar o resultado do processamento da notificação do coletor de exibição.</span><span class="sxs-lookup"><span data-stu-id="430d5-112">A pointer to a struct containing data that your app can optionally set to indicate the result of processing the display sink notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="430d5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="430d5-113">Requirements</span></span>



| <span data-ttu-id="430d5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="430d5-114">Requirement</span></span> | <span data-ttu-id="430d5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="430d5-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="430d5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="430d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="430d5-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="430d5-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="430d5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="430d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="430d5-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="430d5-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="430d5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="430d5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="430d5-121"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="430d5-121"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




