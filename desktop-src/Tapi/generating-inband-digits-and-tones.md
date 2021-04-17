---
description: Depois que uma chamada está no estado conectado, as informações podem ser transmitidas sobre ela.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Gerando dígitos de banda e tons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766231"
---
# <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="542c1-103">Gerando dígitos de banda e tons</span><span class="sxs-lookup"><span data-stu-id="542c1-103">Generating Inband Digits and Tones</span></span>

<span data-ttu-id="542c1-104">Depois que uma chamada está no estado *conectado* , as informações podem ser transmitidas sobre ela.</span><span class="sxs-lookup"><span data-stu-id="542c1-104">After a call is in the *connected* state, information can be transmitted over it.</span></span> <span data-ttu-id="542c1-105">São fornecidas duas funções que permitem a sinalização de faixa de ponta a ponta entre o aplicativo e equipamentos de estação remota, como uma secretária eletrônica.</span><span class="sxs-lookup"><span data-stu-id="542c1-105">Two functions are provided that allow end-to-end inband signaling between the application and remote station equipment such as an answering machine.</span></span> <span data-ttu-id="542c1-106">Uma função é [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), que gera dígitos de inband em uma chamada, sinalizando-os pelo canal de voz.</span><span class="sxs-lookup"><span data-stu-id="542c1-106">One function is [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), which generates inband digits on a call, signaling them over the voice channel.</span></span> <span data-ttu-id="542c1-107">Os dígitos podem ser sinalizados como sequências rotativa/pulso ou como tons DTMF.</span><span class="sxs-lookup"><span data-stu-id="542c1-107">Digits can be signaled as either rotary/pulse sequences or as DTMF tones.</span></span> <span data-ttu-id="542c1-108">A outra função é [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), que permite que o aplicativo gere um de vários tons de várias frequências (sobre o fluxo de mídia).</span><span class="sxs-lookup"><span data-stu-id="542c1-108">The other function is [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), which enables the application to generate one of a variety of multifrequency tones inband (over the media stream).</span></span> <span data-ttu-id="542c1-109">Isso gera tons de telefonia, como, por exemplo, toque, alarme sonoro e ocupado, bem como tons arbitrários de multifrequências e multicadências.</span><span class="sxs-lookup"><span data-stu-id="542c1-109">This generates telephony tones, such as ringback, beep, and busy, as well as arbitrary multifrequency, multicadenced tones.</span></span>

<span data-ttu-id="542c1-110">Somente uma geração de dígito ou Tom pode estar em andamento em uma chamada a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="542c1-110">Only one digit or tone generation can be in progress on a call at any one time.</span></span> <span data-ttu-id="542c1-111">Quando a geração de dígitos ou tons é concluída, uma mensagem de [**\_ geração de linha**](line-generate.md) é enviada para o aplicativo que solicitou a geração.</span><span class="sxs-lookup"><span data-stu-id="542c1-111">When digit or tone generation completes, a [**LINE\_GENERATE**](line-generate.md) message is sent to the application that requested the generation.</span></span> <span data-ttu-id="542c1-112">No caso em que vários dígitos são gerados, apenas uma única mensagem é enviada de volta após a geração de todos os dígitos.</span><span class="sxs-lookup"><span data-stu-id="542c1-112">In the case where multiple digits are generated, only a single message is sent back after all digits have been generated.</span></span> <span data-ttu-id="542c1-113">Chamar [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ou [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) enquanto a geração de dígito ou Tom está em andamento anulará a geração atualmente em andamento e enviará a mensagem de geração de linha \_ para o aplicativo cuja geração foi anulada com uma indicação de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="542c1-113">Calling [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) or [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) while digit or tone generation is in progress will abort the generation currently in progress and send the LINE\_GENERATE message to the application whose generation was aborted with a cancel indication.</span></span>

 

 



