---
title: Funções de retorno de chamada de aplicativo cliente
description: Dois tipos de assinaturas de retorno de chamada.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364301"
---
# <a name="client-application-callback-functions"></a><span data-ttu-id="9d10d-103">Funções de retorno de chamada de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="9d10d-103">Client Application Callback Functions</span></span>

<span data-ttu-id="9d10d-104">O Windows Biometric Framework dá suporte a dois tipos de assinaturas de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9d10d-104">The Windows Biometric Framework supports two types of callback signatures.</span></span> <span data-ttu-id="9d10d-105">A partir do Windows 8, há suporte para o retorno de chamada a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d10d-105">Beginning with Windows 8, the following callback is supported.</span></span> <span data-ttu-id="9d10d-106">Recomendamos que você implemente esse retorno de chamada para todos os novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9d10d-106">We recommend that you implement this callback for all new applications.</span></span> <span data-ttu-id="9d10d-107">No entanto, esse retorno de chamada não pode ser usado no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d10d-107">This callback cannot, however, be used in Windows 7.</span></span>



| <span data-ttu-id="9d10d-108">Callback</span><span class="sxs-lookup"><span data-stu-id="9d10d-108">Callback</span></span>                                                                                     | <span data-ttu-id="9d10d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d10d-109">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d10d-110">**\_retorno de \_ chamada de conclusão ASsíncrona PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="9d10d-110">**PWINBIO\_ASYNC\_COMPLETION\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | <span data-ttu-id="9d10d-111">Notifica o aplicativo cliente de que uma operação assíncrona iniciou usando [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) ou [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) foi concluída.</span><span class="sxs-lookup"><span data-stu-id="9d10d-111">Notifies the client application that an asynchronous operation started by using [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) or [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) has completed.</span></span><br/> |



 

<span data-ttu-id="9d10d-112">As seguintes funções de retorno de chamada foram introduzidas no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d10d-112">The following callback functions were introduced in Windows 7.</span></span> <span data-ttu-id="9d10d-113">Recomendamos que você não os implemente para novos aplicativos direcionados para o Windows 8 e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="9d10d-113">We recommend that you do not implement them for new applications that target Windows 8 and later operating systems.</span></span>



| <span data-ttu-id="9d10d-114">Callback</span><span class="sxs-lookup"><span data-stu-id="9d10d-114">Callback</span></span>                                                                                 | <span data-ttu-id="9d10d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d10d-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d10d-116">**retorno de chamada de \_ captura PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="9d10d-116">**PWINBIO\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | <span data-ttu-id="9d10d-117">Retorna os resultados da função assíncrona [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="9d10d-117">Returns results from the asynchronous [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="9d10d-118">**\_retorno de \_ chamada de captura de registro do PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="9d10d-118">**PWINBIO\_ENROLL\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | <span data-ttu-id="9d10d-119">Retorna os resultados da função assíncrona [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="9d10d-119">Returns results from the asynchronous [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="9d10d-120">**retorno de chamada de \_ evento PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="9d10d-120">**PWINBIO\_EVENT\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | <span data-ttu-id="9d10d-121">Retorna os resultados da função assíncrona [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .</span><span class="sxs-lookup"><span data-stu-id="9d10d-121">Returns results from the asynchronous [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function.</span></span><br/>           |
| [<span data-ttu-id="9d10d-122">**PWINBIO \_ identificar \_ retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="9d10d-122">**PWINBIO\_IDENTIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | <span data-ttu-id="9d10d-123">Retorna os resultados da função assíncrona [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="9d10d-123">Returns results from the asynchronous [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) function.</span></span><br/>           |
| [<span data-ttu-id="9d10d-124">**PWINBIO \_ localizar \_ retorno de chamada do sensor \_**</span><span class="sxs-lookup"><span data-stu-id="9d10d-124">**PWINBIO\_LOCATE\_SENSOR\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | <span data-ttu-id="9d10d-125">Retorna os resultados da função assíncrona [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .</span><span class="sxs-lookup"><span data-stu-id="9d10d-125">Returns results from the asynchronous [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) function.</span></span><br/>   |
| [<span data-ttu-id="9d10d-126">**PWINBIO \_ verificar \_ retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="9d10d-126">**PWINBIO\_VERIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | <span data-ttu-id="9d10d-127">Retorna os resultados da função assíncrona [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="9d10d-127">Returns results from the asynchronous [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) function.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="9d10d-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d10d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d10d-129">Referência de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="9d10d-129">Client Application Reference</span></span>](client-application-reference.md)
</dt> </dl>

 

 





