---
description: Esta seção examina uma parte de um aplicativo de exemplo que opera na rede muito devagar. Ao longo desta seção, são feitas modificações no código inicial para melhorar seu desempenho.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Melhorando um aplicativo lento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782614"
---
# <a name="improving-a-slow-application"></a><span data-ttu-id="853e8-104">Melhorando um aplicativo lento</span><span class="sxs-lookup"><span data-stu-id="853e8-104">Improving a Slow Application</span></span>

<span data-ttu-id="853e8-105">Esta seção examina uma parte de um aplicativo de exemplo que opera na rede muito devagar.</span><span class="sxs-lookup"><span data-stu-id="853e8-105">This section examines a portion of a sample application that operates over the network very slowly.</span></span> <span data-ttu-id="853e8-106">Ao longo desta seção, são feitas modificações no código inicial para melhorar seu desempenho.</span><span class="sxs-lookup"><span data-stu-id="853e8-106">Throughout this section, modifications are made to the initial code to improve its performance.</span></span>

<span data-ttu-id="853e8-107">O exemplo fictício é a parte atualizada de um jogo chamado Life.</span><span class="sxs-lookup"><span data-stu-id="853e8-107">The mock sample is the updated portion for a game called Life.</span></span> <span data-ttu-id="853e8-108">O aplicativo é escrito de modo que o cliente executa os cálculos para as atualizações e as envia para o servidor.</span><span class="sxs-lookup"><span data-stu-id="853e8-108">The application is written such that the client performs the calculations for the updates and sends them to the server.</span></span> <span data-ttu-id="853e8-109">Em seguida, o servidor exibe o campo de vida resultante.</span><span class="sxs-lookup"><span data-stu-id="853e8-109">The server then displays the resulting Life field.</span></span> <span data-ttu-id="853e8-110">A saída do cliente é um fluxo de bytes, agrupados em três (tercetos), cada terceto representando uma atualização de célula.</span><span class="sxs-lookup"><span data-stu-id="853e8-110">The output from the client is a stream of bytes, grouped in threes (triplets), each triplet representing one cell update.</span></span> <span data-ttu-id="853e8-111">Os bytes no terceto representam a linha, a coluna e o valor, respectivamente, para a célula.</span><span class="sxs-lookup"><span data-stu-id="853e8-111">The bytes in the triplet represent the row, column, and value, respectively, for the cell.</span></span>

<span data-ttu-id="853e8-112">Este exemplo começa como um aplicativo de desempenho intencionalmente insatisfatório, que fornece a linha de base da qual as melhorias de desempenho podem ser ilustradas.</span><span class="sxs-lookup"><span data-stu-id="853e8-112">This sample begins as an intentionally poor performing application, which provides the baseline from which performance improvements can be illustrated.</span></span> <span data-ttu-id="853e8-113">A partir daí, o código é melhorado três vezes para resolver vários problemas que afetam o desempenho.</span><span class="sxs-lookup"><span data-stu-id="853e8-113">From there, the code is improved three times to address various issues that affect performance.</span></span> <span data-ttu-id="853e8-114">Esses exemplos devem ser lidos em ordem, uma vez que cada iteração melhora na versão anterior.</span><span class="sxs-lookup"><span data-stu-id="853e8-114">These samples should be read in order, as each iteration improves on the previous version.</span></span>

<span data-ttu-id="853e8-115">O código de linha de base e as revisões que melhoram esse código são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="853e8-115">The baseline code, and the revisions that improve that code, are the following:</span></span>

-   [<span data-ttu-id="853e8-116">A versão de linha de base: um aplicativo com muito mau desempenho</span><span class="sxs-lookup"><span data-stu-id="853e8-116">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
-   [<span data-ttu-id="853e8-117">Revisão 1: limpando o óbvio</span><span class="sxs-lookup"><span data-stu-id="853e8-117">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
-   [<span data-ttu-id="853e8-118">Revisão 2: redesignação para menos conexões</span><span class="sxs-lookup"><span data-stu-id="853e8-118">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
-   [<span data-ttu-id="853e8-119">Revisão 3: envio de bloco compactado</span><span class="sxs-lookup"><span data-stu-id="853e8-119">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
-   [<span data-ttu-id="853e8-120">Aprimoramentos futuros</span><span class="sxs-lookup"><span data-stu-id="853e8-120">Future Improvements</span></span>](future-improvements-2.md)

> [!WARNING]
> <span data-ttu-id="853e8-121">Os primeiros exemplos do aplicativo fornecem um desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código.</span><span class="sxs-lookup"><span data-stu-id="853e8-121">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="853e8-122">Não use esses exemplos de código em seu aplicativo; Eles são apenas para fins ilustrativos.</span><span class="sxs-lookup"><span data-stu-id="853e8-122">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="853e8-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="853e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="853e8-124">Aplicativos de alto desempenho do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="853e8-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



