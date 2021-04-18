---
description: Você pode extrair arquivos de um gabinete de duas maneiras. A primeira e mais simples é aproveitar o processamento automático de gabinetes incorporados às funções de instalação.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extraindo arquivos de gabinetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750426"
---
# <a name="extracting-files-from-cabinets"></a><span data-ttu-id="2dc13-104">Extraindo arquivos de gabinetes</span><span class="sxs-lookup"><span data-stu-id="2dc13-104">Extracting Files from Cabinets</span></span>

<span data-ttu-id="2dc13-105">Você pode extrair arquivos de um gabinete de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="2dc13-105">You can extract files from a cabinet in two ways.</span></span> <span data-ttu-id="2dc13-106">A primeira e mais simples é aproveitar o processamento automático de gabinetes incorporados às funções de instalação.</span><span class="sxs-lookup"><span data-stu-id="2dc13-106">The first and simplest way is to take advantage of the automatic cabinet processing built into the setup functions.</span></span>

<span data-ttu-id="2dc13-107">As funções de instalação, como [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)e [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), verificam a compactação em cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="2dc13-107">The installation functions, such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), check the compression on each file.</span></span> <span data-ttu-id="2dc13-108">Se o arquivo estiver em um gabinete, as funções primeiro pesquisarão um arquivo com esse nome fora do gabinete.</span><span class="sxs-lookup"><span data-stu-id="2dc13-108">If the file is in a cabinet, the functions first search for a file of that name outside the cabinet.</span></span> <span data-ttu-id="2dc13-109">Se for encontrado, as funções instalarão o arquivo externo, ignorando o arquivo dentro do gabinete.</span><span class="sxs-lookup"><span data-stu-id="2dc13-109">If found, the functions install the external file, ignoring the file inside the cabinet.</span></span> <span data-ttu-id="2dc13-110">Isso permite que você atualize um único arquivo dentro do gabinete sem recriar o gabinete.</span><span class="sxs-lookup"><span data-stu-id="2dc13-110">This enables you to update a single file inside the cabinet without rebuilding the cabinet.</span></span>

<span data-ttu-id="2dc13-111">As funções de instalação também controlam quais arquivos em um gabinete foram recuperados, para que um arquivo seja extraído apenas uma vez, mesmo que ele seja instalado várias vezes.</span><span class="sxs-lookup"><span data-stu-id="2dc13-111">The setup functions also track which files in a cabinet have been retrieved, so that a file is extracted only once, even if it is installed several times.</span></span>

<span data-ttu-id="2dc13-112">A segunda maneira de extrair arquivos de um gabinete é usando [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="2dc13-112">The second way to extract files from a cabinet is by using [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="2dc13-113">Essa função itera em cada arquivo em um gabinete, enviando uma notificação para uma rotina de retorno de chamada para cada arquivo encontrado.</span><span class="sxs-lookup"><span data-stu-id="2dc13-113">This function iterates through each file in a cabinet, sending a notification to a callback routine for each file found.</span></span> <span data-ttu-id="2dc13-114">A rotina de retorno de chamada retorna um valor que indica se o arquivo deve ser extraído ou ignorado.</span><span class="sxs-lookup"><span data-stu-id="2dc13-114">The callback routine then returns a value that indicates whether the file should be extracted or skipped.</span></span>

> [!Note]  
> <span data-ttu-id="2dc13-115">A API de instalação não fornece uma rotina de retorno de chamada padrão para manipular notificações de gabinete.</span><span class="sxs-lookup"><span data-stu-id="2dc13-115">The Setup API does not supply a default callback routine to handle cabinet notifications.</span></span> <span data-ttu-id="2dc13-116">Se você chamar [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitamente, deverá fornecer uma rotina de retorno de chamada para processar as notificações de gabinete que a função retorna.</span><span class="sxs-lookup"><span data-stu-id="2dc13-116">If you call [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitly, you must supply a callback routine to process the cabinet notifications that the function returns.</span></span>

 

 

 



