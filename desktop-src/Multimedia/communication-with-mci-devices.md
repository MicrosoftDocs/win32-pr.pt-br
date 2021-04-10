---
title: Comunicação com dispositivos MCI
description: Comunicação com dispositivos MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivos MCI, comunicando-se
- Macro MCIWndGetDeviceID
- função mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293918"
---
# <a name="communication-with-mci-devices"></a><span data-ttu-id="809a2-106">Comunicação com dispositivos MCI</span><span class="sxs-lookup"><span data-stu-id="809a2-106">Communication with MCI Devices</span></span>

<span data-ttu-id="809a2-107">É possível que cada dispositivo MCI use um ou mais dos seguintes como identificadores:</span><span class="sxs-lookup"><span data-stu-id="809a2-107">It is possible for each MCI device to use one or more of the following as identifiers:</span></span>

-   <span data-ttu-id="809a2-108">um identificador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="809a2-108">a device identifier</span></span>
-   <span data-ttu-id="809a2-109">um nome de dispositivo</span><span class="sxs-lookup"><span data-stu-id="809a2-109">a device name</span></span>
-   <span data-ttu-id="809a2-110">um alias</span><span class="sxs-lookup"><span data-stu-id="809a2-110">an alias</span></span>
-   <span data-ttu-id="809a2-111">o nome de arquivo do conteúdo carregado no momento.</span><span class="sxs-lookup"><span data-stu-id="809a2-111">the filename of the currently loaded content.</span></span>

<span data-ttu-id="809a2-112">O MCIWnd fornece macros que você pode usar para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="809a2-112">MCIWnd provides macros you can use to retrieve this information.</span></span> <span data-ttu-id="809a2-113">Você pode usar essas informações para se comunicar por meio do MCI diretamente com dispositivos MCI associados ao MCIWnd Windows.</span><span class="sxs-lookup"><span data-stu-id="809a2-113">You can then use this information to communicate through MCI directly with MCI devices associated with MCIWnd windows.</span></span>

<span data-ttu-id="809a2-114">Você pode recuperar o identificador do dispositivo MCI atual usando a macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="809a2-114">You can retrieve the identifier of the current MCI device by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span> <span data-ttu-id="809a2-115">O identificador do dispositivo MCI é um valor numérico que identifica a instância do dispositivo MCI que seu aplicativo está usando.</span><span class="sxs-lookup"><span data-stu-id="809a2-115">The MCI device identifier is a numerical value that identifies the instance of the MCI device your application is using.</span></span> <span data-ttu-id="809a2-116">Seu aplicativo pode usar esse identificador ao se comunicar com um dispositivo MCI usando a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="809a2-116">Your application can use this identifier when communicating with an MCI device by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="809a2-117">Para recuperar o nome do dispositivo MCI atual, use a macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="809a2-117">To retrieve the name of the current MCI device, use the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span> <span data-ttu-id="809a2-118">O nome do dispositivo MCI é uma cadeia de caracteres terminada em nulo que identifica o tipo de dispositivo associado a uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="809a2-118">The MCI device name is a null-terminated string that identifies the device type associated with an MCIWnd window.</span></span> <span data-ttu-id="809a2-119">Seu aplicativo pode usar esse nome ao se comunicar com um dispositivo MCI usando o **mciSendCommand**.</span><span class="sxs-lookup"><span data-stu-id="809a2-119">Your application can use this name when communicating with an MCI device by using **mciSendCommand**.</span></span>

<span data-ttu-id="809a2-120">Você pode recuperar o alias do dispositivo MCI atual usando a macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="809a2-120">You can retrieve the alias of the current MCI device by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span> <span data-ttu-id="809a2-121">Seu aplicativo pode usar esse alias ao se comunicar com um dispositivo MCI usando a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="809a2-121">Your application can use this alias when communicating with an MCI device by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>

<span data-ttu-id="809a2-122">Por fim, você pode recuperar o nome de arquivo usado por um dispositivo MCI usando a macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="809a2-122">Finally, you can retrieve the filename used by an MCI device by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span> <span data-ttu-id="809a2-123">O nome do arquivo identifica o conteúdo atualmente associado a uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="809a2-123">The filename identifies the content currently associated with an MCIWnd window.</span></span> <span data-ttu-id="809a2-124">Seu aplicativo pode usar esse nome de arquivo ao se comunicar com um dispositivo MCI usando **mciSendCommand** ou **mciSendString**.</span><span class="sxs-lookup"><span data-stu-id="809a2-124">Your application can use this filename when communicating with a MCI device by using **mciSendCommand** or **mciSendString**.</span></span>

 

 