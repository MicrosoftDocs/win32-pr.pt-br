---
title: Tipos de dados da API do servidor HTTP versão 2,0
description: Tipos de dados da API do servidor HTTP versão 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105787530"
---
# <a name="http-server-api-version-20-data-types"></a><span data-ttu-id="46e52-103">Tipos de dados da API do servidor HTTP versão 2,0</span><span class="sxs-lookup"><span data-stu-id="46e52-103">HTTP Server API Version 2.0 Data Types</span></span>

<span data-ttu-id="46e52-104">A API do servidor HTTP usa vários tipos de identificador de finalidade especial declarados no cabeçalho http. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="46e52-104">The HTTP Server API uses various special purpose identifier types declared in the Http.h header as follows:</span></span>

-   <span data-ttu-id="46e52-105">**UShort** parâmetro \_ \_ \_ de tempo limite de configuração do serviço http \_ , \* \_ parâmetro de \_ \_ tempo limite da configuração do serviço PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="46e52-105">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>
-   <span data-ttu-id="46e52-106">**ULONGLONG** ID opaca HTTP \_ \_ , \* \_ ID opaca \_ PHTTP</span><span class="sxs-lookup"><span data-stu-id="46e52-106">**ULONGLONG** HTTP\_OPAQUE\_ID, \*PHTTP\_OPAQUE\_ID</span></span>
-   <span data-ttu-id="46e52-107">**Http \_ ID \_** \_ de solicitação HTTP \_ de ID opaca, \* \_ ID de solicitação PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="46e52-107">**HTTP\_OPAQUE\_ID** HTTP\_REQUEST\_ID, \*PHTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="46e52-108">**Http \_ ID \_** \_ de conexão http \_ de ID opaca, \* \_ ID de conexão PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="46e52-108">**HTTP\_OPAQUE\_ID** HTTP\_CONNECTION\_ID, \*PHTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="46e52-109">**Http \_ ID \_** \_ de conexão bruta http de ID opaca \_ \_ , \* ID de \_ conexão bruta PHTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="46e52-109">**HTTP\_OPAQUE\_ID** HTTP\_RAW\_CONNECTION\_ID, \*PHTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="46e52-110">**UShort** parâmetro \_ \_ \_ de tempo limite de configuração do serviço http \_ , \* \_ parâmetro de \_ \_ tempo limite da configuração do serviço PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="46e52-110">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>

<span data-ttu-id="46e52-111">Um aplicativo não deve tentar gerar ou modificar nenhum identificador que pertença a um desses tipos.</span><span class="sxs-lookup"><span data-stu-id="46e52-111">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




