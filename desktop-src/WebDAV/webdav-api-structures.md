---
title: Estruturas da API do WebDAV
description: As estruturas a seguir são usadas na API do WebDAV.
ms.assetid: 1fa7b740-ac93-4756-ac9f-6a8cb4ea8bc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe54d58ef03bc8057336cb0e4bbbe3e833fb59c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294280"
---
# <a name="webdav-api-structures"></a><span data-ttu-id="70498-103">Estruturas da API do WebDAV</span><span class="sxs-lookup"><span data-stu-id="70498-103">WebDAV API Structures</span></span>

<span data-ttu-id="70498-104">As estruturas a seguir são usadas na API do WebDAV.</span><span class="sxs-lookup"><span data-stu-id="70498-104">The following structures are used in the WebDAV API.</span></span>



| <span data-ttu-id="70498-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="70498-105">Structure</span></span>                                                   | <span data-ttu-id="70498-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="70498-106">Description</span></span>                                                                                                                                                                                         |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70498-107">**BLOB de autenticação de retorno de \_ chamada DAV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70498-107">**DAV\_CALLBACK\_AUTH\_BLOB**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_auth_blob) | <span data-ttu-id="70498-108">Essa estrutura é usada para armazenar um [*blob*](/windows/desktop/SecGloss/b-gly) de autenticação que foi recuperado pela função de retorno de chamada [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) .</span><span class="sxs-lookup"><span data-stu-id="70498-108">This structure is used to store an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) that was retrieved by the [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function.</span></span> |
| [<span data-ttu-id="70498-109">**UNP de autenticação de retorno de \_ chamada DAV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70498-109">**DAV\_CALLBACK\_AUTH\_UNP**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_auth_unp)   | <span data-ttu-id="70498-110">Essa estrutura é usada para armazenar informações de nome de usuário e senha que foram recuperadas pela função de retorno de chamada [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) .</span><span class="sxs-lookup"><span data-stu-id="70498-110">This structure is used to store user name and password information that was retrieved by the [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function.</span></span>                                               |
| [<span data-ttu-id="70498-111">**\_credenciais de retorno de chamada DAV \_**</span><span class="sxs-lookup"><span data-stu-id="70498-111">**DAV\_CALLBACK\_CRED**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_cred)            | <span data-ttu-id="70498-112">A função de retorno de chamada [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) usa essa estrutura para armazenar informações de credenciais de usuário.</span><span class="sxs-lookup"><span data-stu-id="70498-112">The [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function uses this structure to store user credential information.</span></span>                                                                               |



 

 

 