---
title: Personalizando o projeto de exemplo
description: Personalizando o projeto de exemplo
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Lojas online do Windows Media Player, personalizando projetos de exemplo
- lojas online, personalizando projetos de exemplo
- Digite 2 lojas online, personalizando projetos de exemplo
- Lojas online do Windows Media Player, projetos de exemplo
- lojas online, projetos de exemplo
- Digite 2 lojas online, projetos de exemplo
- Personalizando projetos de exemplo
- exemplos, tipo 2 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916559"
---
# <a name="customizing-the-sample-project"></a><span data-ttu-id="42157-111">Personalizando o projeto de exemplo</span><span class="sxs-lookup"><span data-stu-id="42157-111">Customizing the Sample Project</span></span>

<span data-ttu-id="42157-112">Ao criar sua própria loja online, você desejará alterar as implementações dos seguintes métodos no arquivo chamado seuprojeto. cpp:</span><span class="sxs-lookup"><span data-stu-id="42157-112">When creating your own online store, you will want to change the implementations of the following methods in the file named YourProject.cpp:</span></span>

-   <span data-ttu-id="42157-113">**CYourProject:: allowPlay**.</span><span class="sxs-lookup"><span data-stu-id="42157-113">**CYourProject::allowPlay**.</span></span> <span data-ttu-id="42157-114">Use essa função para aplicar suas regras de negócio para permitir a reprodução de conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="42157-114">Use this function to apply your business rules for permitting playback of protected content.</span></span>
-   <span data-ttu-id="42157-115">**CYourProject:: permitir cdburn**.</span><span class="sxs-lookup"><span data-stu-id="42157-115">**CYourProject::allow CDBurn**.</span></span> <span data-ttu-id="42157-116">Use essa função para aplicar suas regras de negócio para permitir que os usuários copiem conteúdo protegido em um CD.</span><span class="sxs-lookup"><span data-stu-id="42157-116">Use this function to apply your business rules for allowing users to copy protected content to a CD.</span></span>
-   <span data-ttu-id="42157-117">**CYourProject:: allowPDATransfer**.</span><span class="sxs-lookup"><span data-stu-id="42157-117">**CYourProject::allowPDATransfer**.</span></span> <span data-ttu-id="42157-118">Use essa função para aplicar suas regras de negócio para permitir que os usuários transfiram conteúdo protegido em um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="42157-118">Use this function to apply your business rules for allowing users to transfer protected content to a portable device.</span></span>
-   <span data-ttu-id="42157-119">**CYourProject:: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="42157-119">**CYourProject::startBackgroundProcessing**.</span></span> <span data-ttu-id="42157-120">Use essa função para iniciar as tarefas de processamento em segundo plano que você precisa.</span><span class="sxs-lookup"><span data-stu-id="42157-120">Use this function to initiate any background processing tasks you require.</span></span> <span data-ttu-id="42157-121">Por exemplo, você pode usar isso como uma oportunidade de verificar se há licenças expiradas.</span><span class="sxs-lookup"><span data-stu-id="42157-121">For example, you might use this as an opportunity to check for expired licenses.</span></span>
-   <span data-ttu-id="42157-122">**CYourProject::D eviceavailable**.</span><span class="sxs-lookup"><span data-stu-id="42157-122">**CYourProject::deviceAvailable**.</span></span> <span data-ttu-id="42157-123">Use essa função para iniciar qualquer tarefa relacionada a um dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="42157-123">Use this function to initiate any tasks related to a connected device.</span></span>
-   <span data-ttu-id="42157-124">**CYourProject::P repareforsync**.</span><span class="sxs-lookup"><span data-stu-id="42157-124">**CYourProject::prepareForSync**.</span></span> <span data-ttu-id="42157-125">Use essa função para executar as tarefas necessárias antes de sincronizar mídia digital para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42157-125">Use this function to perform necessary tasks just before synchronizing digital media to the device.</span></span>
-   <span data-ttu-id="42157-126">**CYourProject:: CreateEvent**.</span><span class="sxs-lookup"><span data-stu-id="42157-126">**CYourProject::serviceEvent**.</span></span> <span data-ttu-id="42157-127">Use essa função para iniciar e encerrar tarefas que você deseja executar quando sua loja online for a ativa.</span><span class="sxs-lookup"><span data-stu-id="42157-127">Use this function to begin and end tasks that you want to run when your online store is the active one.</span></span>
-   <span data-ttu-id="42157-128">**CYourProject:: stopBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="42157-128">**CYourProject::stopBackgroundProcessing**.</span></span> <span data-ttu-id="42157-129">Use essa função para interromper qualquer tarefa de processamento em segundo plano iniciada quando o Windows Media Player chamou **CYourProject:: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="42157-129">Use this function to stop any background processing tasks you started when Windows Media Player called **CYourProject::startBackgroundProcessing**.</span></span>

## <a name="working-with-media-and-playlist-objects"></a><span data-ttu-id="42157-130">Trabalhando com objetos de mídia e playlist</span><span class="sxs-lookup"><span data-stu-id="42157-130">Working with Media and Playlist Objects</span></span>

<span data-ttu-id="42157-131">O método **allowPlay** fornece um ponteiro para a interface **IWMPMedia** como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42157-131">The **allowPlay** method provides a pointer to the **IWMPMedia** interface as a parameter.</span></span> <span data-ttu-id="42157-132">Essa interface é a interface do Windows Media Player que representa os objetos de mídia.</span><span class="sxs-lookup"><span data-stu-id="42157-132">This interface is the Windows Media Player interface that represents media objects.</span></span> <span data-ttu-id="42157-133">Ao chamar os métodos nessa interface, você pode trabalhar com os atributos e as propriedades de um item de mídia individual.</span><span class="sxs-lookup"><span data-stu-id="42157-133">By calling the methods on this interface, you can work with the attributes and properties of an individual media item.</span></span>

<span data-ttu-id="42157-134">Os métodos **allowCDBurn** e **allowPDATransfer** fornecem um ponteiro para a interface **IWMPPlaylist** como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42157-134">The **allowCDBurn** and **allowPDATransfer** methods provide a pointer to the **IWMPPlaylist** interface as a parameter.</span></span> <span data-ttu-id="42157-135">Essa interface é a interface do Windows Media Player que representa os objetos da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="42157-135">This interface is the Windows Media Player interface that represents playlist objects.</span></span> <span data-ttu-id="42157-136">Ao chamar os métodos nessa interface, você pode trabalhar com os atributos e as propriedades de uma lista de reprodução, adicionar itens a uma lista de reprodução ou remover itens de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="42157-136">By calling the methods on this interface, you can work with the attributes and properties of a playlist, add items to a playlist, or remove items from a playlist.</span></span>

<span data-ttu-id="42157-137">Para saber como remover um item de uma playlist programaticamente, consulte a implementação de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="42157-137">To learn how to remove an item from a playlist programmatically, see the implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span> <span data-ttu-id="42157-138">Para saber mais sobre como trabalhar com objetos de mídia e playlist, confira [modelo de objeto do Player para linguagens de script](player-object-model-for-scripting-languages.md).</span><span class="sxs-lookup"><span data-stu-id="42157-138">To learn more about working with media and playlist objects, see [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span></span>

## <a name="code-that-can-be-removed"></a><span data-ttu-id="42157-139">Código que pode ser removido</span><span class="sxs-lookup"><span data-stu-id="42157-139">Code That Can Be Removed</span></span>

<span data-ttu-id="42157-140">Provavelmente, você desejará remover o código que abre as caixas de diálogo porque é improvável que você queira que os usuários decidam quais itens de mídia podem ser reproduzidos ou copiados.</span><span class="sxs-lookup"><span data-stu-id="42157-140">You will probably want to remove the code that opens dialog boxes because it is unlikely that you will want users deciding which media items can be played or copied.</span></span> <span data-ttu-id="42157-141">Em seuprojeto. h, remova o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="42157-141">From YourProject.h, remove the following code:</span></span>

-   <span data-ttu-id="42157-142">A declaração de **CAllowBaseDialog**.</span><span class="sxs-lookup"><span data-stu-id="42157-142">The declaration of **CAllowBaseDialog**.</span></span>
-   <span data-ttu-id="42157-143">A declaração de **CAllowBurnDialog**.</span><span class="sxs-lookup"><span data-stu-id="42157-143">The declaration of **CAllowBurnDialog**.</span></span>
-   <span data-ttu-id="42157-144">A declaração de **CAllowTransferDialog**.</span><span class="sxs-lookup"><span data-stu-id="42157-144">The declaration of **CAllowTransferDialog**.</span></span>

<span data-ttu-id="42157-145">Em seuprojeto. cpp, remova o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="42157-145">From YourProject.cpp, remove the following code:</span></span>

-   <span data-ttu-id="42157-146">A implementação de **CAllowBaseDialog <T> :: OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="42157-146">The implementation of **CAllowBaseDialog<T>::OnInitDialog**.</span></span>
-   <span data-ttu-id="42157-147">A implementação de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="42157-147">The implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42157-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42157-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42157-149">**Criando o plug-in para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="42157-149">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




