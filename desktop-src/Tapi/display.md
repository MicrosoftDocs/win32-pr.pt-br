---
description: A TAPI fornece acesso a uma exibição de telefones.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090450"
---
# <a name="display"></a><span data-ttu-id="fac0d-103">Monitor</span><span class="sxs-lookup"><span data-stu-id="fac0d-103">Display</span></span>

<span data-ttu-id="fac0d-104">A TAPI fornece acesso à exibição de um telefone.</span><span class="sxs-lookup"><span data-stu-id="fac0d-104">TAPI provides access to a phone's display.</span></span> <span data-ttu-id="fac0d-105">A exibição é modelada como uma área alfanumérica com linhas e colunas.</span><span class="sxs-lookup"><span data-stu-id="fac0d-105">The display is modeled as an alphanumeric area with rows and columns.</span></span> <span data-ttu-id="fac0d-106">Os recursos de dispositivo de um telefone indicam o tamanho da exibição de um telefone como o número de linhas e o número de colunas.</span><span class="sxs-lookup"><span data-stu-id="fac0d-106">A phone's device capabilities indicate the size of a phone's display as the number of rows and the number of columns.</span></span> <span data-ttu-id="fac0d-107">Ambos os números serão zero se o dispositivo de telefone não tiver uma exibição.</span><span class="sxs-lookup"><span data-stu-id="fac0d-107">Both these numbers are zero if the phone device does not have a display.</span></span> <span data-ttu-id="fac0d-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) para gravar informações na exibição de um dispositivo de telefone aberto e [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) para recuperar o conteúdo atual da exibição de um telefone.</span><span class="sxs-lookup"><span data-stu-id="fac0d-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) to write information to the display of an open phone device, and [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) to retrieve the current contents of a phone's display.</span></span>

<span data-ttu-id="fac0d-109">Quando a exibição de um dispositivo de telefone é alterada, uma mensagem de [**\_ estado de telefone**](phone-state.md) é enviada para a função de aplicativo para notificar o aplicativo sobre a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="fac0d-109">When the display of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="fac0d-110">Os parâmetros dessa mensagem fornecem uma indicação da alteração.</span><span class="sxs-lookup"><span data-stu-id="fac0d-110">Parameters to this message provide an indication of the change.</span></span>

 

 



