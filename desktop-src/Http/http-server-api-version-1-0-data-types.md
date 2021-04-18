---
title: Tipos de dados da API do servidor HTTP versão 1,0
description: A API do servidor HTTP usa vários tipos de identificador de finalidade especial declarados no arquivo de cabeçalho http. h como inteiros de 64 bits sem sinal.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- Tipo de HTTP_CONNECTION_ID HTTP
- Tipo de HTTP_RAW_CONNECTION_ID HTTP
- Tipo de HTTP_REQUEST_ID HTTP
- Tipo de HTTP_URL_CONTEXT HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810368"
---
# <a name="http-server-api-version-10-data-types"></a><span data-ttu-id="84dfa-107">Tipos de dados da API do servidor HTTP versão 1,0</span><span class="sxs-lookup"><span data-stu-id="84dfa-107">HTTP Server API Version 1.0 Data Types</span></span>

<span data-ttu-id="84dfa-108">A API do servidor HTTP usa vários tipos de identificador de finalidade especial declarados no arquivo de cabeçalho http. h como inteiros de 64 bits sem sinal (**ULONGLONGs**):</span><span class="sxs-lookup"><span data-stu-id="84dfa-108">The HTTP Server API uses various special purpose identifier types declared in the Http.h header file as 64-bit unsigned integers (**ULONGLONGs**):</span></span>

-   <span data-ttu-id="84dfa-109">\_ID da conexão http \_</span><span class="sxs-lookup"><span data-stu-id="84dfa-109">HTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="84dfa-110">\_ID de \_ conexão \_ bruta http</span><span class="sxs-lookup"><span data-stu-id="84dfa-110">HTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="84dfa-111">\_ID da solicitação HTTP \_</span><span class="sxs-lookup"><span data-stu-id="84dfa-111">HTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="84dfa-112">\_contexto de URL http \_</span><span class="sxs-lookup"><span data-stu-id="84dfa-112">HTTP\_URL\_CONTEXT</span></span>

<span data-ttu-id="84dfa-113">Um aplicativo não deve tentar gerar ou modificar nenhum identificador que pertença a um desses tipos.</span><span class="sxs-lookup"><span data-stu-id="84dfa-113">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




