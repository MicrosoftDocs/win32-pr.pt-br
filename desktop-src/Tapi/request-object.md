---
description: O objeto de solicitação é criado usando COM CoCreateInstance e expõe uma interface, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objeto de solicitação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759042"
---
# <a name="request-object"></a><span data-ttu-id="d960d-103">Objeto de solicitação</span><span class="sxs-lookup"><span data-stu-id="d960d-103">Request Object</span></span>

<span data-ttu-id="d960d-104">O objeto de solicitação é criado usando COM **CoCreateInstance** e expõe uma interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span><span class="sxs-lookup"><span data-stu-id="d960d-104">The Request Object is created using COM **CoCreateInstance** and exposes one interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span></span> <span data-ttu-id="d960d-105">Essa interface expõe o método [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , que permite que um aplicativo TAPI 3 Use a telefonia assistida.</span><span class="sxs-lookup"><span data-stu-id="d960d-105">This interface exposes the [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) method, which allows a TAPI 3 application to use Assisted Telephony.</span></span> <span data-ttu-id="d960d-106">A telefonia assistida fornece aplicativos habilitados para telefonia com um mecanismo simples para fazer chamadas telefônicas sem exigir que o desenvolvedor se torne totalmente compensante em telefonia.</span><span class="sxs-lookup"><span data-stu-id="d960d-106">Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.</span></span>

<span data-ttu-id="d960d-107">Por exemplo, um aplicativo de planilha pode adicionar um botão "fazer chamada" usando a telefonia assistida sem implementar os controles mais elaborados disponíveis em um aplicativo TAPI completo.</span><span class="sxs-lookup"><span data-stu-id="d960d-107">For example, a spreadsheet application can add a "Make Call" button using Assisted Telephony without implementing the more elaborate controls available in a full TAPI application.</span></span>

<span data-ttu-id="d960d-108">Consulte a [visão geral de telefonia assistida](assisted-telephony-overview.md) para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="d960d-108">See the [Assisted Telephony Overview](assisted-telephony-overview.md) for additional information.</span></span>

 

 



