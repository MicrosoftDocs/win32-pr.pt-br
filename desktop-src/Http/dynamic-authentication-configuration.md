---
title: Configuração de autenticação dinâmica
description: Os aplicativos podem alterar as configurações de autenticação em um grupo de URLs ou sessão de servidor a qualquer momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291913"
---
# <a name="dynamic-authentication-configuration"></a><span data-ttu-id="f80f8-103">Configuração de autenticação dinâmica</span><span class="sxs-lookup"><span data-stu-id="f80f8-103">Dynamic Authentication Configuration</span></span>

<span data-ttu-id="f80f8-104">Por padrão, a API do servidor HTTP não executa a autenticação, a menos que o aplicativo a habilite especificamente.</span><span class="sxs-lookup"><span data-stu-id="f80f8-104">By default, the HTTP Server API does not perform authentication unless the application specifically enables it.</span></span> <span data-ttu-id="f80f8-105">Os aplicativos podem alterar as configurações de autenticação em um grupo de URLs ou sessão de servidor a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="f80f8-105">Applications can change authentication configurations on a URL Group or server session at any time.</span></span> <span data-ttu-id="f80f8-106">As alterações na configuração de autenticação não afetam as solicitações que já foram autenticadas ou que estão sendo expedidas para o aplicativo</span><span class="sxs-lookup"><span data-stu-id="f80f8-106">Changes to the authentication configuration do not affect requests that are already authenticated or being dispatched to the application</span></span>

<span data-ttu-id="f80f8-107">Para esquemas de autenticação em que são necessários vários arredondamentos de handshake, a API do servidor HTTP descarta o handshake de autenticação se o esquema atual não tiver mais suporte devido a alterações de configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f80f8-107">For authentication schemes where multiple rounds of handshake are required, the HTTP Server API drops the authentication handshake if the current scheme is no longer supported due to configuration changes from the application.</span></span> <span data-ttu-id="f80f8-108">Por exemplo, se o aplicativo habilitar Negotiate e desabilitar o NTLM, e a API do servidor HTTP estiver no handshake de autenticação intermediária para NTLM, o handshake para NTLM será descartado e a solicitação será passada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f80f8-108">For example, if the application enables Negotiate and disables NTLM, and the HTTP Server API is in the intermediate authentication handshake for NTLM, the handshake for NTLM is discarded and the request is passed to the application.</span></span> <span data-ttu-id="f80f8-109">O aplicativo envia um desafio de autenticação 401 com os novos tipos de autenticação especificados no cabeçalho WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="f80f8-109">The application sends a 401 authentication challenge with the new authentication types specified in the WWW-Authenticate header.</span></span>

 

 




