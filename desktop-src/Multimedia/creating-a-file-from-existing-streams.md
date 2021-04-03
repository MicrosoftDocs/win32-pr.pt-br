---
title: Criando um arquivo de fluxos existentes
description: Criando um arquivo de fluxos existentes
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- Função AVISave
- Função AVISaveV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc422d2170ccd49b8a9746666db7ebbcd7dff14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916193"
---
# <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="7dfda-105">Criando um arquivo de fluxos existentes</span><span class="sxs-lookup"><span data-stu-id="7dfda-105">Creating a File from Existing Streams</span></span>

<span data-ttu-id="7dfda-106">Uma maneira de criar um arquivo que contém fluxos de dados é combinar fluxos existentes em um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="7dfda-106">One way to create a file that contains data streams is to combine existing streams into a new file.</span></span> <span data-ttu-id="7dfda-107">Os fluxos que fornecem dados para o novo arquivo podem residir na memória ou em um ou mais arquivos.</span><span class="sxs-lookup"><span data-stu-id="7dfda-107">The streams that provide data for the new file can reside in memory or in one or more files.</span></span>

<span data-ttu-id="7dfda-108">Você pode criar um arquivo de vários fluxos usando a função [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) .</span><span class="sxs-lookup"><span data-stu-id="7dfda-108">You can build a file from several streams by using the [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) function.</span></span> <span data-ttu-id="7dfda-109">Essa função cria um arquivo e grava os fluxos de dados especificados em sua sequência de chamada para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7dfda-109">This function creates a file and writes the data streams specified in its calling sequence to the file.</span></span> <span data-ttu-id="7dfda-110">A sequência de chamada para **AVISave** usa um número variável de argumentos que incluem interfaces para os fluxos combinados no novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="7dfda-110">The calling sequence for **AVISave** uses a variable number of arguments that include interfaces for the streams combined in the new file.</span></span>

<span data-ttu-id="7dfda-111">Você também pode combinar fluxos de dados em um novo arquivo usando a função [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) .</span><span class="sxs-lookup"><span data-stu-id="7dfda-111">You can also combine data streams in a new file by using the [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) function.</span></span> <span data-ttu-id="7dfda-112">Essa função fornece a mesma funcionalidade que **AVISave**, mas quando você usa **AVISaveV**, seu aplicativo especifica os fluxos de dados como uma matriz, não como um número variável de argumentos.</span><span class="sxs-lookup"><span data-stu-id="7dfda-112">This function provides the same functionality as **AVISave**, but when you use **AVISaveV**, your application specifies the data streams as an array, not as a variable number of arguments.</span></span>

<span data-ttu-id="7dfda-113">Você pode criar uma caixa de diálogo na qual o usuário pode selecionar configurações de compactação para o novo arquivo usando a função [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) .</span><span class="sxs-lookup"><span data-stu-id="7dfda-113">You can create a dialog box in which the user can select compression settings for the new file by using the [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) function.</span></span> <span data-ttu-id="7dfda-114">A caixa de diálogo exibe as configurações de compactação atuais e permite que o usuário as edite.</span><span class="sxs-lookup"><span data-stu-id="7dfda-114">The dialog box displays the current compression settings and lets the user edit them.</span></span> <span data-ttu-id="7dfda-115">As alterações de configuração de compactação são armazenadas em uma estrutura [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) .</span><span class="sxs-lookup"><span data-stu-id="7dfda-115">Compression setting changes are stored in an [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) structure.</span></span>

<span data-ttu-id="7dfda-116">Você também pode incluir uma função de retorno de chamada com [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) e [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) que seu aplicativo pode usar para exibir o progresso da gravação do arquivo e, se necessário, permitir que o usuário cancele a operação de salvamento.</span><span class="sxs-lookup"><span data-stu-id="7dfda-116">You can also include a callback function with [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) and [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) that your application can use to display the progress of writing the file and, if needed, let the user cancel the save operation.</span></span> <span data-ttu-id="7dfda-117">Você pode incluir o endereço da função de chamada de retorno na sequência de chamada de **AVISave** ou **AVISaveV**.</span><span class="sxs-lookup"><span data-stu-id="7dfda-117">You can include the address of the callback function in the calling sequence of **AVISave** or **AVISaveV**.</span></span>

<span data-ttu-id="7dfda-118">Você pode permitir que o usuário selecione um nome de arquivo para o novo arquivos usando a função [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="7dfda-118">You can let the user select a filename for the new file by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function.</span></span> <span data-ttu-id="7dfda-119">Essa função exibe a caixa de diálogo Salvar como na qual o usuário pode visualizar o primeiro fluxo (normalmente o fluxo de vídeo) de um arquivo AVI.</span><span class="sxs-lookup"><span data-stu-id="7dfda-119">This function displays the Save As dialog box in which the user can preview the first stream (normally the video stream) of an AVI file.</span></span>

<span data-ttu-id="7dfda-120">Você pode criar um ponteiro de interface de arquivo (e um arquivo virtual) para um grupo de fluxos usando a função [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="7dfda-120">You can create a file interface pointer (and a virtual file) for a group of streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="7dfda-121">Outras funções AVIFile podem usar o ponteiro de interface de arquivo retornado por essa função para acessar os fluxos no arquivo virtual.</span><span class="sxs-lookup"><span data-stu-id="7dfda-121">Other AVIFile functions can use the file interface pointer returned by this function to access the streams in the virtual file.</span></span> <span data-ttu-id="7dfda-122">Depois de terminar de usar o arquivo virtual, exclua o ponteiro de interface de arquivo usando a função [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="7dfda-122">After you finish using the virtual file, delete the file interface pointer by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span>

> [!Note]  
> <span data-ttu-id="7dfda-123">Para minimizar a degradação da imagem e do áudio, evite compactar um arquivo AVI mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="7dfda-123">To minimize image and audio degradation, avoid compressing an AVI file more than once.</span></span> <span data-ttu-id="7dfda-124">Combine pedaços de vídeo não compactados em seu sistema de edição e, em seguida, compacte o produto final.</span><span class="sxs-lookup"><span data-stu-id="7dfda-124">Combine uncompressed pieces of video in your editing system and then compress the final product.</span></span> <span data-ttu-id="7dfda-125">Para obter informações sobre opções de compactação, consulte [Gerenciador de compactação de vídeo](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="7dfda-125">For information about compression options, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 

 




