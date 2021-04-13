---
description: A TAPI atribui identificadores de sessão que são exclusivos para cada sessão e aplicativo.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificador de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370792"
---
# <a name="session-identifier"></a><span data-ttu-id="e0f02-103">Identificador de sessão</span><span class="sxs-lookup"><span data-stu-id="e0f02-103">Session Identifier</span></span>

<span data-ttu-id="e0f02-104">A TAPI atribui identificadores de sessão que são exclusivos para cada sessão e aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0f02-104">TAPI assigns session identifiers that are unique for each session and application.</span></span> <span data-ttu-id="e0f02-105">Um aplicativo usa um identificador de sessão para se comunicar com a TAPI em relação a uma sessão específica.</span><span class="sxs-lookup"><span data-stu-id="e0f02-105">An application uses a session identifier to communicate with TAPI concerning a specific session.</span></span> <span data-ttu-id="e0f02-106">Um aplicativo normalmente Obtém um identificador criando uma nova sessão de comunicações ou quando a TAPI oferece uma sessão.</span><span class="sxs-lookup"><span data-stu-id="e0f02-106">An application typically obtains an identifier either by creating a new communications session or when TAPI offers a session.</span></span>

<span data-ttu-id="e0f02-107">Um identificador de sessão não pode ser usado para passar informações para outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e0f02-107">A session identifier cannot be used to pass information to another application.</span></span> <span data-ttu-id="e0f02-108">Para essa finalidade, use a [ID de chamada](call-id-ovr.md), que pode ser atribuída por um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e0f02-108">For this purpose, use the [Call ID](call-id-ovr.md), which may be assigned by a service provider.</span></span>

<span data-ttu-id="e0f02-109">Consulte [iniciar uma sessão](initiate-a-session-ovr.md) para obter informações sobre operações que criam sessões e retornam um identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="e0f02-109">See [Initiate a session](initiate-a-session-ovr.md) for information on operations that create sessions and return a session identifier.</span></span> <span data-ttu-id="e0f02-110">Consulte [responder à sessão iniciada em outro lugar](respond-to-session-initiated-elsewhere-ovr.md) para operações que adquirem identificadores de sessão da TAPI.</span><span class="sxs-lookup"><span data-stu-id="e0f02-110">See [Respond to session initiated elsewhere](respond-to-session-initiated-elsewhere-ovr.md) for operations that acquire session identifiers from TAPI.</span></span> <span data-ttu-id="e0f02-111">Consulte [encerrar uma sessão](terminate-a-session-ovr.md) para obter informações sobre como liberar recursos de sessão.</span><span class="sxs-lookup"><span data-stu-id="e0f02-111">See [Terminate a Session](terminate-a-session-ovr.md) for information on releasing session resources.</span></span>

<span data-ttu-id="e0f02-112">Todos os provedores de serviço devem oferecer suporte a alguma forma de identificação de sessão.</span><span class="sxs-lookup"><span data-stu-id="e0f02-112">All service providers must support some form of session identification.</span></span>

<span data-ttu-id="e0f02-113">**TAPI 2. x:** O identificador principal de uma sessão de comunicações é o identificador de chamada.</span><span class="sxs-lookup"><span data-stu-id="e0f02-113">**TAPI 2.x:** The primary identifier of a communications session is the call handle.</span></span>

<span data-ttu-id="e0f02-114">**TAPI 3. x:** Uma sessão é representada por um [objeto de chamada](call-object.md) e o identificador primário é um ponteiro para a interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="e0f02-114">**TAPI 3.x:** A session is represented by a [Call Object](call-object.md) and the primary identifier is a pointer to the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span>

 

 



