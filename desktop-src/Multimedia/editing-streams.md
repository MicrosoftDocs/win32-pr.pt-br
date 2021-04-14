---
title: Edição de fluxos
description: Edição de fluxos
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- Função CreateEditableStream
- Função EditStreamCut
- Função EditStreamCopy
- Função EditStreamPaste
- Função EditStreamClone
- Função EditStreamSetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453651"
---
# <a name="editing-streams"></a><span data-ttu-id="f315e-109">Edição de fluxos</span><span class="sxs-lookup"><span data-stu-id="f315e-109">Editing Streams</span></span>

<span data-ttu-id="f315e-110">Você pode criar um fluxo que pode ser editado usando a função [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) .</span><span class="sxs-lookup"><span data-stu-id="f315e-110">You can create a stream that you can edit by using the [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) function.</span></span> <span data-ttu-id="f315e-111">Essa função inicializa o ambiente para editar um fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-111">This function initializes the environment for editing a stream.</span></span> <span data-ttu-id="f315e-112">Isso inclui a criação de uma interface para o novo fluxo e as tabelas de edição internas que controlam as alterações feitas no fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-112">This includes creating an interface to the new stream, and internal edit tables that track changes made to the stream.</span></span> <span data-ttu-id="f315e-113">**CreateEditableStream** retorna um ponteiro de fluxo para um fluxo editável que é exigido por outras funções de edição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-113">**CreateEditableStream** returns a stream pointer to an editable stream that is required by other stream-editing functions.</span></span> <span data-ttu-id="f315e-114">O ponteiro de fluxo editável também pode ser usado por outras funções AVIFile que aceitam ponteiros de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-114">The editable stream pointer can also be used by other AVIFile functions that accept stream pointers.</span></span>

<span data-ttu-id="f315e-115">Você pode recortar um ou mais exemplos de um fluxo editável usando a função [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) .</span><span class="sxs-lookup"><span data-stu-id="f315e-115">You can cut one or more samples from an editable stream by using the [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) function.</span></span> <span data-ttu-id="f315e-116">Para remover exemplos do fluxo editável, essa função adiciona uma entrada à tabela de edição.</span><span class="sxs-lookup"><span data-stu-id="f315e-116">To remove samples from the editable stream, this function adds an entry to the edit table.</span></span> <span data-ttu-id="f315e-117">Em seguida, a função coloca uma cópia dos exemplos recortados em um novo fluxo temporário cujo ponteiro de interface é retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="f315e-117">The function then places a copy of the cut samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="f315e-118">Você pode copiar um ou mais exemplos de um fluxo editável para um fluxo temporário usando a função [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) .</span><span class="sxs-lookup"><span data-stu-id="f315e-118">You can copy one or more samples from an editable stream into a temporary stream by using the [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) function.</span></span> <span data-ttu-id="f315e-119">**EditStreamCopy** coloca cópias dos exemplos em um novo fluxo temporário cujo ponteiro de interface é retornado em uma variável.</span><span class="sxs-lookup"><span data-stu-id="f315e-119">**EditStreamCopy** places copies of the samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="f315e-120">Você pode copiar um ou mais exemplos de um fluxo e colá-los em um fluxo editável usando a função [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) .</span><span class="sxs-lookup"><span data-stu-id="f315e-120">You can copy one or more samples from a stream and paste them into an editable stream by using the [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) function.</span></span> <span data-ttu-id="f315e-121">Para inserir os exemplos na posição especificada, essa função adiciona uma entrada na tabela de edição do fluxo editável de destino.</span><span class="sxs-lookup"><span data-stu-id="f315e-121">To insert the samples at the specified position, this function adds an entry in the edit table of the target editable stream.</span></span>

<span data-ttu-id="f315e-122">Você pode duplicar um fluxo editável usando a função [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) .</span><span class="sxs-lookup"><span data-stu-id="f315e-122">You can duplicate an editable stream by using the [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) function.</span></span> <span data-ttu-id="f315e-123">Essa função retorna um ponteiro para a interface de fluxo do novo fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-123">This function returns a pointer to the stream interface of the new stream.</span></span> <span data-ttu-id="f315e-124">Você pode copiar esses fluxos para a área de transferência ou usá-los para manter uma trilha de edições feitas em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-124">You can copy these streams to the clipboard or use them to maintain a trail of edits made to a stream.</span></span>

<span data-ttu-id="f315e-125">Você pode alterar várias das características de um fluxo editável usando a função [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f315e-125">You can change several of the characteristics of an editable stream by using the [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) function.</span></span> <span data-ttu-id="f315e-126">Essa função atualiza a configuração de prioridade, idioma, escala e taxa, hora de início, configuração de qualidade, dimensões e coordenadas de retângulo de destino e a descrição textual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-126">This function updates the priority setting, language, scale and rate, starting time, quality setting, destination rectangle dimensions and coordinates, and the textual description of the stream.</span></span> <span data-ttu-id="f315e-127">Esses itens são armazenados na estrutura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) associada ao fluxo editável.</span><span class="sxs-lookup"><span data-stu-id="f315e-127">These items are stored in the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure associated with the editable stream.</span></span>

<span data-ttu-id="f315e-128">Você também pode alterar a descrição textual de um fluxo editável usando a função [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) .</span><span class="sxs-lookup"><span data-stu-id="f315e-128">You can also change the textual description of an editable stream by using the [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) function.</span></span> <span data-ttu-id="f315e-129">Essa função atualiza o membro **szName** da estrutura **AVISTREAMINFO** associada ao fluxo editável.</span><span class="sxs-lookup"><span data-stu-id="f315e-129">This function updates the **szName** member of the **AVISTREAMINFO** structure associated with the editable stream.</span></span>

<span data-ttu-id="f315e-130">As funções de edição funcionam em fluxos.</span><span class="sxs-lookup"><span data-stu-id="f315e-130">The editing functions work on streams.</span></span> <span data-ttu-id="f315e-131">Você precisa recortar e colar cada fluxo individualmente e, em seguida, usar a função [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) para criar um novo ponteiro de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f315e-131">You need to cut and paste each stream individually, and then use the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function to create a new file pointer.</span></span>

> [!Note]  
> <span data-ttu-id="f315e-132">As tabelas de edição em um fluxo editável mantêm todas as alterações de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="f315e-132">The edit tables in an editable stream maintain all the changes for a stream.</span></span> <span data-ttu-id="f315e-133">O fluxo de origem nunca é alterado.</span><span class="sxs-lookup"><span data-stu-id="f315e-133">The source stream is never changed.</span></span>

 

 

 




