---
title: Aprimoramentos do analisador
description: Aprimoramentos do analisador
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- Aprimoramentos do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a22f4b4dced29e25662a6fc521057a055b56f70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364183"
---
# <a name="parser-enhancements"></a><span data-ttu-id="97be4-104">Aprimoramentos do analisador</span><span class="sxs-lookup"><span data-stu-id="97be4-104">Parser Enhancements</span></span>

<span data-ttu-id="97be4-105">No Windows Server 2003 com Service Pack 1 (SP1), a API do servidor HTTP permite as seguintes solicitações de clientes HTTP.</span><span class="sxs-lookup"><span data-stu-id="97be4-105">In Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API allows the following requests from HTTP clients.</span></span>

-   <span data-ttu-id="97be4-106">Solicitações que usam um single line feed (LF) como terminadores de linha.</span><span class="sxs-lookup"><span data-stu-id="97be4-106">Requests that use a single Line Feed (LF) as line terminators.</span></span>
-   <span data-ttu-id="97be4-107">Solicitações que contêm o LWS (espaço em branco linear) entre a linha de solicitação HTTP e o início dos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="97be4-107">Requests that contain linear white space (LWS) between the HTTP request line and start of headers.</span></span>

<span data-ttu-id="97be4-108">Esses comportamentos são habilitados por padrão e não são controlados pelas configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="97be4-108">These behaviors are enabled by default and are not controlled by registry settings.</span></span>

 

 




