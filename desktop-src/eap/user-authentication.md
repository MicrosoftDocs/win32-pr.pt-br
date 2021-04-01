---
title: Autenticação de Usuário
description: O próprio protocolo de autenticação pode autenticar o usuário por meio de EAP protegido (PEAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103638925"
---
# <a name="user-authentication"></a><span data-ttu-id="97118-103">Autenticação de Usuário</span><span class="sxs-lookup"><span data-stu-id="97118-103">User Authentication</span></span>

<span data-ttu-id="97118-104">O próprio protocolo de autenticação pode autenticar o usuário por meio de EAP protegido (PEAP).</span><span class="sxs-lookup"><span data-stu-id="97118-104">The authentication protocol itself can authenticate the user via Protected EAP (PEAP).</span></span> <span data-ttu-id="97118-105">Também há dois provedores de autenticação internos no sistema operacional: autenticação de domínio do Windows (acessada por meio de serviços de diretório) e RADIUS (Remote Access dial-in User Service).</span><span class="sxs-lookup"><span data-stu-id="97118-105">There are also two authentication providers built into the operating system: Windows domain authentication (accessed via Directory Services) and Remote Access Dial-In User Service (RADIUS).</span></span>

<span data-ttu-id="97118-106">No caso em que o RADIUS é o provedor de autenticação, o plug-in EAP é instalado no servidor RADIUS, e não no servidor AP (ponto de acesso sem fio), como um servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="97118-106">In the case where RADIUS is the authentication provider, the EAP Plug-in is installed on the RADIUS server rather than on the wireless Access Point (AP) server, such as a RAS server.</span></span> <span data-ttu-id="97118-107">O servidor AP passa pacotes EAP diretamente do cliente para o serviço de autenticação no servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="97118-107">The AP server passes EAP packets directly from the client to the authentication service on the RADIUS server.</span></span> <span data-ttu-id="97118-108">O servidor AP não processa nenhuma das informações nos pacotes EAP, mas deve aceitar as chaves de criptografia geradas pelo PEAP do lado do servidor (256 bits) para criar a conexão segura.</span><span class="sxs-lookup"><span data-stu-id="97118-108">The AP server does not process any of the information in the EAP packets, but it must accept the server-side, full strength (256 bit) PEAP generated encryption keys in order to create the secure connection.</span></span>

 

 




