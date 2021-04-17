---
description: Depois de criar um arquivo INF, você normalmente escreverá o código-fonte do seu aplicativo de instalação. Você chama as funções de instalação do seu aplicativo de instalação para executar muitas operações de instalação.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Criando aplicativos de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754493"
---
# <a name="creating-setup-applications"></a><span data-ttu-id="479bd-104">Criando aplicativos de instalação</span><span class="sxs-lookup"><span data-stu-id="479bd-104">Creating Setup Applications</span></span>

<span data-ttu-id="479bd-105">Depois de criar um arquivo INF, você normalmente escreverá o código-fonte do seu aplicativo de instalação.</span><span class="sxs-lookup"><span data-stu-id="479bd-105">After you create an INF file, you will typically write the source code for your setup application.</span></span> <span data-ttu-id="479bd-106">Você chama as funções de instalação do seu aplicativo de instalação para executar muitas operações de instalação.</span><span class="sxs-lookup"><span data-stu-id="479bd-106">You call the setup functions from your setup application to perform many installation operations.</span></span>

<span data-ttu-id="479bd-107">As etapas a seguir abrangem uma maneira de usar as funções de instalação para criar um aplicativo de instalação.</span><span class="sxs-lookup"><span data-stu-id="479bd-107">The following steps cover one way to use the setup functions to create a setup application.</span></span> <span data-ttu-id="479bd-108">Você pode usar este exemplo como um ponto de partida ou desenvolver seu próprio algoritmo de instalação.</span><span class="sxs-lookup"><span data-stu-id="479bd-108">You can use this example as a starting point, or develop your own installation algorithm.</span></span>

<span data-ttu-id="479bd-109">**Initialization**</span><span class="sxs-lookup"><span data-stu-id="479bd-109">**Initialization**</span></span>

-   [<span data-ttu-id="479bd-110">Abra o INF e, se apropriado, acrescente outros arquivos INF.</span><span class="sxs-lookup"><span data-stu-id="479bd-110">Open the INF and, if appropriate, append other INF files.</span></span>](opening-the-inf-file.md)
-   [<span data-ttu-id="479bd-111">Extraia informações de arquivo do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="479bd-111">Extract file information from the INF file.</span></span>](extracting-file-information-from-the-inf-file.md)
-   [<span data-ttu-id="479bd-112">Coletar informações de instalação do usuário.</span><span class="sxs-lookup"><span data-stu-id="479bd-112">Gather setup information from the user.</span></span>](gathering-setup-information-from-the-user.md)
-   [<span data-ttu-id="479bd-113">Crie uma fila.</span><span class="sxs-lookup"><span data-stu-id="479bd-113">Create a queue.</span></span>](creating-a-queue-and-queuing-file-operations.md)

<span data-ttu-id="479bd-114">**Arquivos de instalação**</span><span class="sxs-lookup"><span data-stu-id="479bd-114">**Install files**</span></span>

-   [<span data-ttu-id="479bd-115">Confirme a fila, especificando uma rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="479bd-115">Commit the queue, specifying a callback routine.</span></span>](committing-the-queue.md)
-   [<span data-ttu-id="479bd-116">Atualizar informações do registro.</span><span class="sxs-lookup"><span data-stu-id="479bd-116">Update registry information.</span></span>](updating-registry-information.md)

<span data-ttu-id="479bd-117">**Limpeza**</span><span class="sxs-lookup"><span data-stu-id="479bd-117">**Clean up**</span></span>

-   [<span data-ttu-id="479bd-118">Feche a fila de arquivos e o INF.</span><span class="sxs-lookup"><span data-stu-id="479bd-118">Close the file queue and INF.</span></span>](closing-the-file-queue-and-inf-file.md)
-   [<span data-ttu-id="479bd-119">Libere outros recursos do sistema e encerre o programa.</span><span class="sxs-lookup"><span data-stu-id="479bd-119">Release any other system resources and end the program.</span></span>](releasing-other-system-resources.md)

 

 



