---
title: Serviços básicos
description: Serviços básicos
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- e/s de arquivo multimídia, serviços básicos
- e/s de arquivo, serviços básicos
- entrada e saída (e/s), serviços básicos
- E/s (entrada e saída), serviços básicos
- e/s básica
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365975"
---
# <a name="basic-services"></a><span data-ttu-id="b60bc-109">Serviços básicos</span><span class="sxs-lookup"><span data-stu-id="b60bc-109">Basic Services</span></span>

<span data-ttu-id="b60bc-110">O uso dos serviços de e/s básicos é semelhante ao uso dos serviços de e/s de arquivo de tempo de execução da biblioteca de tempo de execução do C.</span><span class="sxs-lookup"><span data-stu-id="b60bc-110">Using the basic I/O services is similar to using the run-time file I/O services of the C run-time library.</span></span> <span data-ttu-id="b60bc-111">Os arquivos devem ser abertos antes que possam ser lidos ou gravados.</span><span class="sxs-lookup"><span data-stu-id="b60bc-111">Files must be opened before they can be read or written.</span></span> <span data-ttu-id="b60bc-112">Após a leitura ou gravação, o arquivo deve ser fechado.</span><span class="sxs-lookup"><span data-stu-id="b60bc-112">After reading or writing, the file must be closed.</span></span> <span data-ttu-id="b60bc-113">Você também pode alterar o local de leitura ou gravação atual em um arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="b60bc-113">You can also change the current read or write location within an open file.</span></span>

<span data-ttu-id="b60bc-114">Antes de começar qualquer operação de e/s em um arquivo, você deve abrir o arquivo usando a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="b60bc-114">Before you begin any I/O operations to a file, you must open the file by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="b60bc-115">Essa função retorna um identificador de arquivo do tipo **HMMIO**.</span><span class="sxs-lookup"><span data-stu-id="b60bc-115">This function returns a file handle of type **HMMIO**.</span></span> <span data-ttu-id="b60bc-116">Você pode usar esse identificador de arquivo para identificar o arquivo aberto ao chamar outras funções de e/s de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b60bc-116">You can use this file handle to identify the open file when calling other file I/O functions.</span></span>

> [!Note]  
> <span data-ttu-id="b60bc-117">Um identificador de arquivo **HMMIO** não é um identificador de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="b60bc-117">An **HMMIO** file handle is not a standard file handle.</span></span> <span data-ttu-id="b60bc-118">Não use identificadores de arquivo **HMMIO** com funções de e/s de arquivo de tempo de execução do Win32 ou C.</span><span class="sxs-lookup"><span data-stu-id="b60bc-118">Do not use **HMMIO** file handles with Win32 or C run-time file I/O functions.</span></span>

 

<span data-ttu-id="b60bc-119">Ao usar o [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) para abrir um arquivo, você usa um sinalizador para especificar se você o está abrindo para leitura, gravação ou ambos.</span><span class="sxs-lookup"><span data-stu-id="b60bc-119">When you use [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) to open a file, you use a flag to specify whether you are opening it for reading, writing, or both.</span></span> <span data-ttu-id="b60bc-120">Você também pode especificar sinalizadores que permitem criar ou excluir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b60bc-120">You can also specify flags that enable you to create or delete a file.</span></span> <span data-ttu-id="b60bc-121">Use a função [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) para fechar um arquivo quando terminar de ler ou gravar nele.</span><span class="sxs-lookup"><span data-stu-id="b60bc-121">Use the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to close a file when you are finished reading or writing to it.</span></span>

<span data-ttu-id="b60bc-122">Você pode ler e gravar arquivos usando as funções [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) e [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b60bc-122">You can read and write files by using the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) and [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) functions respectively.</span></span> <span data-ttu-id="b60bc-123">A próxima operação de leitura ou gravação ocorre na posição atual do arquivo ou no ponteiro do arquivo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b60bc-123">The next read or write operation occurs at the current file position or file pointer in a file.</span></span> <span data-ttu-id="b60bc-124">A posição atual do arquivo é avançada cada vez que um arquivo é lido ou gravado.</span><span class="sxs-lookup"><span data-stu-id="b60bc-124">The current file position is advanced each time a file is read or written.</span></span>

<span data-ttu-id="b60bc-125">Você também pode alterar a posição atual do arquivo usando a função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="b60bc-125">You can also change the current file position by using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span> <span data-ttu-id="b60bc-126">Você deve garantir que especifique um local válido em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b60bc-126">You should ensure that you specify a valid location in a file.</span></span> <span data-ttu-id="b60bc-127">Se você especificar um local inválido, como após o final do arquivo, **mmioSeek** poderá não retornar um erro, mas as operações de e/s subsequentes poderão falhar.</span><span class="sxs-lookup"><span data-stu-id="b60bc-127">If you specify an invalid location, such as past the end of the file, **mmioSeek** may not return an error, but subsequent I/O operations could fail.</span></span>

<span data-ttu-id="b60bc-128">Há sinalizadores que você pode usar com a função **mmioOpen** para operações além da e/s de arquivo básico.</span><span class="sxs-lookup"><span data-stu-id="b60bc-128">There are flags you can use with the **mmioOpen** function for operations beyond basic file I/O.</span></span> <span data-ttu-id="b60bc-129">Ao especificar uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , por exemplo, você pode abrir arquivos de memória, especificar um procedimento de e/s personalizado ou fornecer um buffer para e/s armazenada em buffer.</span><span class="sxs-lookup"><span data-stu-id="b60bc-129">By specifying an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure, for example, you can open memory files, specify a custom I/O procedure, or supply a buffer for buffered I/O.</span></span>

 

 