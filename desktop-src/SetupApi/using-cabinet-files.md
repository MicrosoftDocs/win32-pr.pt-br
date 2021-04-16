---
description: As funções de instalação manipulam os gabinetes internamente. Para enumerar explicitamente e extrair arquivos de um gabinete, você pode chamar a função SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Usando arquivos de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754100"
---
# <a name="using-cabinet-files"></a><span data-ttu-id="21ab4-104">Usando arquivos de gabinete</span><span class="sxs-lookup"><span data-stu-id="21ab4-104">Using Cabinet Files</span></span>

<span data-ttu-id="21ab4-105">As funções de instalação manipulam os gabinetes internamente.</span><span class="sxs-lookup"><span data-stu-id="21ab4-105">The setup functions handle cabinets internally.</span></span> <span data-ttu-id="21ab4-106">Para enumerar explicitamente e extrair arquivos de um gabinete, você pode chamar a função [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="21ab4-106">To explicitly enumerate and extract files from a cabinet, you can call the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

<span data-ttu-id="21ab4-107">O tópico a seguir descreve o processamento de gabinete interno para as funções de instalação e como usar o [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="21ab4-107">The following topic describes the cabinet processing internal to the setup functions and how to use [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="21ab4-108">Também são discutidas as notificações enviadas pelo **SetupIterateCabinet** e o formato necessário de uma rotina de retorno de chamada de gabinete para processar essas notificações.</span><span class="sxs-lookup"><span data-stu-id="21ab4-108">Also discussed are the notifications sent by **SetupIterateCabinet** and the required format of a cabinet callback routine to process those notifications.</span></span>

-   [<span data-ttu-id="21ab4-109">Extraindo arquivos de gabinetes</span><span class="sxs-lookup"><span data-stu-id="21ab4-109">Extracting Files From Cabinets</span></span>](extracting-files-from-cabinets.md)
-   [<span data-ttu-id="21ab4-110">Criando uma rotina de retorno de chamada de gabinete</span><span class="sxs-lookup"><span data-stu-id="21ab4-110">Creating a Cabinet Callback Routine</span></span>](creating-a-cabinet-callback-routine.md)

 

 



