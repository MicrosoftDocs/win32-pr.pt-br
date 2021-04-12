---
title: Funções de administração de usuário RAS
description: Usar as seguintes funções para gerenciar usuários de conexão discada
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454285"
---
# <a name="ras-user-administration-functions"></a><span data-ttu-id="30088-103">Funções de administração de usuário RAS</span><span class="sxs-lookup"><span data-stu-id="30088-103">RAS User Administration Functions</span></span>

<span data-ttu-id="30088-104">Use as seguintes funções para gerenciar usuários de conexão discada:</span><span class="sxs-lookup"><span data-stu-id="30088-104">Use the following functions to manage dial-up users:</span></span>

-   [<span data-ttu-id="30088-105">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="30088-105">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [<span data-ttu-id="30088-106">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="30088-106">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [<span data-ttu-id="30088-107">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="30088-107">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [<span data-ttu-id="30088-108">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="30088-108">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

<span data-ttu-id="30088-109">Para obter uma lista de usuários atuais em um domínio específico, use a função [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) .</span><span class="sxs-lookup"><span data-stu-id="30088-109">To obtain a list of current users on a particular domain, use the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function.</span></span> <span data-ttu-id="30088-110">O protótipo para essa função está no arquivo de cabeçalho lmaccess. h.</span><span class="sxs-lookup"><span data-stu-id="30088-110">The prototype for this function is in the lmaccess.h header file.</span></span>

 

 