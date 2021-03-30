---
title: Manipulando erros de aplicativo do servidor
description: Se o aplicativo de servidor processar com êxito o arquivo carregado, o aplicativo deverá retornar 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635020"
---
# <a name="handling-server-application-errors"></a><span data-ttu-id="9afaa-103">Manipulando erros de aplicativo do servidor</span><span class="sxs-lookup"><span data-stu-id="9afaa-103">Handling Server Application Errors</span></span>

<span data-ttu-id="9afaa-104">Se o aplicativo de servidor processar com êxito o arquivo carregado, o aplicativo deverá retornar 200.</span><span class="sxs-lookup"><span data-stu-id="9afaa-104">If the server application successfully processes the uploaded file, the application should return 200.</span></span> <span data-ttu-id="9afaa-105">Se o aplicativo não retornar 200, o cliente BITS usará o código de erro para determinar se o erro é um erro transitório ou erro fatal.</span><span class="sxs-lookup"><span data-stu-id="9afaa-105">If the application does not return 200, the BITS client uses the error code to determine if the error is a transient error or fatal error.</span></span>

<span data-ttu-id="9afaa-106">Todos os códigos de erro 3xx são erros transitórios, exceto 300-305 e 307, que são erros fatais.</span><span class="sxs-lookup"><span data-stu-id="9afaa-106">All 3xx error codes are transient errors except 300 - 305 and 307, which are fatal errors.</span></span> <span data-ttu-id="9afaa-107">Todos os códigos de erro 4xx são erros fatais, exceto 408 e 409, que são erros transitórios.</span><span class="sxs-lookup"><span data-stu-id="9afaa-107">All 4xx error codes are fatal errors except for 408 and 409, which are transient errors.</span></span> <span data-ttu-id="9afaa-108">Todos os códigos de erro 5xx são erros transitórios, exceto 501 e 505, que são erros fatais.</span><span class="sxs-lookup"><span data-stu-id="9afaa-108">All 5xx error codes are transient errors except 501 and 505, which are fatal errors.</span></span> <span data-ttu-id="9afaa-109">Todos os outros códigos HTTP são considerados erros transitórios.</span><span class="sxs-lookup"><span data-stu-id="9afaa-109">All other HTTP codes are considered transient errors.</span></span> <span data-ttu-id="9afaa-110">Observe que um código de erro 403 é o único código de erro que impede que o BITS envie o arquivo de upload para o aplicativo de servidor novamente.</span><span class="sxs-lookup"><span data-stu-id="9afaa-110">Note that a 403 error code is the only error code that prevents BITS from posting the upload file to the server application again.</span></span>

<span data-ttu-id="9afaa-111">Para recuperar o erro, chame o método [**IBackgroundCopyError:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) .</span><span class="sxs-lookup"><span data-stu-id="9afaa-111">To retrieve the error, call the [**IBackgroundCopyError::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) method.</span></span> <span data-ttu-id="9afaa-112">O contexto de erro será um \_ aplicativo remoto de contexto de erro BG \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9afaa-112">The error context will be BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION.</span></span>

 

 




