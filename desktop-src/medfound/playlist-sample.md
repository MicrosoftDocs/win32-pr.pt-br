---
description: Exemplo de playlist
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Exemplo de playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761626"
---
# <a name="playlist-sample"></a><span data-ttu-id="fce2b-103">Exemplo de playlist</span><span class="sxs-lookup"><span data-stu-id="fce2b-103">Playlist Sample</span></span>

<span data-ttu-id="fce2b-104">Mostra como usar Microsoft Media Foundation para reproduzir uma sequência de arquivos de áudio em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="fce2b-104">Shows how to use Microsoft Media Foundation to play a sequence of audio files in a playlist.</span></span> <span data-ttu-id="fce2b-105">O exemplo usa a [origem do sequenciador](sequencer-source.md) para criar e gerenciar a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="fce2b-105">The sample uses the [Sequencer Source](sequencer-source.md) to create and manage the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="fce2b-106">Este exemplo não está mais incluído no SDK.</span><span class="sxs-lookup"><span data-stu-id="fce2b-106">This sample is no longer included in the SDK.</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="fce2b-107">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="fce2b-107">APIs Demonstrated</span></span>

<span data-ttu-id="fce2b-108">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="fce2b-108">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="fce2b-109">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="fce2b-109">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [<span data-ttu-id="fce2b-110">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="fce2b-110">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [<span data-ttu-id="fce2b-111">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="fce2b-111">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a><span data-ttu-id="fce2b-112">Uso</span><span class="sxs-lookup"><span data-stu-id="fce2b-112">Usage</span></span>

<span data-ttu-id="fce2b-113">O exemplo de playlist cria um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="fce2b-113">The Playlist sample builds a Windows application.</span></span>

-   <span data-ttu-id="fce2b-114">Para criar uma nova lista de reprodução, selecione **Adicionar à lista de reprodução** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="fce2b-114">To create a new playlist, select **Add to Playlist** from the **File** menu.</span></span> <span data-ttu-id="fce2b-115">Na caixa de diálogo **Abrir arquivo** , selecione um ou mais arquivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="fce2b-115">In the **Open File** dialog, select one or more audio files.</span></span> <span data-ttu-id="fce2b-116">Os arquivos são adicionados à playlist.</span><span class="sxs-lookup"><span data-stu-id="fce2b-116">The files are added to the playlist.</span></span>
-   <span data-ttu-id="fce2b-117">Para reproduzir a sequência, clique em **reproduzir**.</span><span class="sxs-lookup"><span data-stu-id="fce2b-117">To play the sequence, click **Play**.</span></span>
-   <span data-ttu-id="fce2b-118">Para pausar o segmento atual, clique em **Pausar**.</span><span class="sxs-lookup"><span data-stu-id="fce2b-118">To pause the current segment, click **Pause**.</span></span>
-   <span data-ttu-id="fce2b-119">Para parar o segmento atual, clique em **parar**.</span><span class="sxs-lookup"><span data-stu-id="fce2b-119">To stop the current segment, click **Stop**.</span></span>
-   <span data-ttu-id="fce2b-120">Para ignorar um arquivo, clique duas vezes no item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="fce2b-120">To skip to a file, double-click the item in the playlist.</span></span>
-   <span data-ttu-id="fce2b-121">Para excluir um arquivo da lista de reprodução, selecione o item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="fce2b-121">To delete a file from the playlist, select the item in the playlist.</span></span> <span data-ttu-id="fce2b-122">Em seguida, selecione **remover da lista de reprodução** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="fce2b-122">Then select **Remove from Playlist** from the **File** menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce2b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce2b-123">Requirements</span></span>



| <span data-ttu-id="fce2b-124">Produto</span><span class="sxs-lookup"><span data-stu-id="fce2b-124">Product</span></span>                                                        | <span data-ttu-id="fce2b-125">Versão</span><span class="sxs-lookup"><span data-stu-id="fce2b-125">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="fce2b-126">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="fce2b-126">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="fce2b-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fce2b-127">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="fce2b-128">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="fce2b-128">Downloading the Sample</span></span>

<span data-ttu-id="fce2b-129">Este exemplo está disponível nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="fce2b-129">This sample is available in the following locations.</span></span>



| <span data-ttu-id="fce2b-130">Local</span><span class="sxs-lookup"><span data-stu-id="fce2b-130">Location</span></span>                                                     | <span data-ttu-id="fce2b-131">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="fce2b-131">Path/URL</span></span>                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="fce2b-132">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="fce2b-132">Windows SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=8279) | <span data-ttu-id="fce2b-133">*Raiz* \\ do SDK Exemplos de \\ playlist de multimídia \\ mediafoundation \\</span><span class="sxs-lookup"><span data-stu-id="fce2b-133">*SDK Root*\\Samples\\multimedia\\mediafoundation\\Playlist</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fce2b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fce2b-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fce2b-135">[Exemplo de BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fce2b-135">[BasicPlayback Sample](/previous-versions//bb970475(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fce2b-136">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fce2b-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="fce2b-137">Origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="fce2b-137">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 
