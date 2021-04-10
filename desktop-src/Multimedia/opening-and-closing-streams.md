---
title: Abrindo e fechando fluxos
description: Abrindo e fechando fluxos
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- Função AVIFileGetStream
- Função AVIStreamRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005234"
---
# <a name="opening-and-closing-streams"></a><span data-ttu-id="27af9-105">Abrindo e fechando fluxos</span><span class="sxs-lookup"><span data-stu-id="27af9-105">Opening and Closing Streams</span></span>

<span data-ttu-id="27af9-106">A abertura de fluxos de dados é semelhante à abertura de arquivos.</span><span class="sxs-lookup"><span data-stu-id="27af9-106">Opening data streams is similar to opening files.</span></span> <span data-ttu-id="27af9-107">Você pode abrir um fluxo usando a função [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) .</span><span class="sxs-lookup"><span data-stu-id="27af9-107">You can open a stream by using the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) function.</span></span> <span data-ttu-id="27af9-108">Essa função cria uma interface de fluxo, coloca um identificador do fluxo na interface e retorna um ponteiro para a interface.</span><span class="sxs-lookup"><span data-stu-id="27af9-108">This function creates a stream interface, places a handle of the stream in the interface, and returns a pointer to the interface.</span></span> <span data-ttu-id="27af9-109">O **AVIFileGetStream** também mantém uma contagem de referência dos aplicativos que abriram um fluxo, mas não aqueles que o fecharam.</span><span class="sxs-lookup"><span data-stu-id="27af9-109">**AVIFileGetStream** also maintains a reference count of the applications that have opened a stream, but not of those that have closed it.</span></span>

<span data-ttu-id="27af9-110">Se você quiser acessar um único fluxo em um arquivo, poderá abrir o arquivo e o fluxo usando a função [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) .</span><span class="sxs-lookup"><span data-stu-id="27af9-110">If you want to access a single stream in a file, you can open the file and the stream by using the [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) function.</span></span> <span data-ttu-id="27af9-111">Essa função combina as operações e os argumentos de função das funções [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileGetStream** .</span><span class="sxs-lookup"><span data-stu-id="27af9-111">This function combines the operations and function arguments of the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileGetStream** functions.</span></span>

<span data-ttu-id="27af9-112">Para acessar mais de um fluxo em um arquivo, use **AVIFileOpen** uma vez seguido por várias chamadas para **AVIFileGetStream**.</span><span class="sxs-lookup"><span data-stu-id="27af9-112">To access more than one stream in a file, use **AVIFileOpen** once followed by multiple calls to **AVIFileGetStream**.</span></span>

<span data-ttu-id="27af9-113">Você pode incrementar a contagem de referência de um fluxo usando a função [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) para manter um fluxo aberto ao usar uma função que normalmente fecharia o fluxo.</span><span class="sxs-lookup"><span data-stu-id="27af9-113">You can increment the reference count of a stream by using the [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) function to keep a stream open when using a function that would normally close the stream.</span></span>

<span data-ttu-id="27af9-114">Você pode fechar um fluxo usando a função [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="27af9-114">You can close a stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="27af9-115">Essa função decrementa a contagem de referência do fluxo e o fecha quando a contagem de referência chega a zero.</span><span class="sxs-lookup"><span data-stu-id="27af9-115">This function decrements the reference count of the stream and closes it when the reference count reaches zero.</span></span> <span data-ttu-id="27af9-116">Seus aplicativos devem balancear a contagem de referência incluindo uma chamada para **AVIStreamRelease** para cada uso da função [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** ou **AVIStreamOpenFromFile** .</span><span class="sxs-lookup"><span data-stu-id="27af9-116">Your applications should balance the reference count by including a call to **AVIStreamRelease** for each use of the [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef**, or **AVIStreamOpenFromFile** function.</span></span> <span data-ttu-id="27af9-117">Quando você libera um fluxo que foi aberto usando **AVIStreamOpenFromFile**, o avifile fecha o arquivo que contém o fluxo.</span><span class="sxs-lookup"><span data-stu-id="27af9-117">When you release a stream that has been opened by using **AVIStreamOpenFromFile**, AVIFile closes the file containing the stream.</span></span> <span data-ttu-id="27af9-118">Se o seu aplicativo liberar um arquivo que tem fluxos de dados abertos, o AVIFile não fechará os fluxos até que todos os fluxos sejam liberados.</span><span class="sxs-lookup"><span data-stu-id="27af9-118">If your application releases a file that has open data streams, AVIFile will not close the streams until all of the streams are released.</span></span>

 

 




