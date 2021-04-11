---
title: Atualizando licenças para lojas que têm o logotipo do PlaysForSure
description: Atualizando licenças para lojas que têm o logotipo do PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Armazenamentos online do Windows Media Player, atualizando licenças
- lojas online, atualização de licenças
- Lojas online do Windows Media Player, atualizando licenças
- lojas online, atualizando licenças
- Lojas online do Windows Media Player, logotipo do PlaysForSure
- lojas online, logotipo do PlaysForSure
- Atualizando licenças
- licenças, atualizando
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084368"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a><span data-ttu-id="cca61-112">Atualizando licenças para lojas que têm o logotipo do PlaysForSure</span><span class="sxs-lookup"><span data-stu-id="cca61-112">Refreshing Licenses for Stores That Have the PlaysForSure Logo</span></span>

<span data-ttu-id="cca61-113">Algumas lojas de música online têm o logotipo do PlaysForSure, mas não estão integradas ao Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="cca61-113">Certain online music stores have the PlaysForSure logo but are not integrated with Windows Media Player 11.</span></span> <span data-ttu-id="cca61-114">Esses armazenamentos devem fornecer um documento de informações e um componente leve para que o Windows Media Player 11 possa obter e atualizar licenças para seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cca61-114">Those stores must provide a ServiceInfo document and a lightweight component so that Windows Media Player 11 can obtain and update licenses for their content.</span></span>

<span data-ttu-id="cca61-115">O exemplo a seguir ilustra como o processo de atualização de licença funciona.</span><span class="sxs-lookup"><span data-stu-id="cca61-115">The following example illustrates how the license updating process works.</span></span>

1.  <span data-ttu-id="cca61-116">O usuário obtém faixas de música de 50 da loja online da Proseware.</span><span class="sxs-lookup"><span data-stu-id="cca61-116">The user obtains 50 music tracks from the Proseware online store.</span></span> <span data-ttu-id="cca61-117">Cada faixa é um arquivo com a extensão de nome de arquivo. WMA.</span><span class="sxs-lookup"><span data-stu-id="cca61-117">Each track is a file with the .wma file name extension.</span></span> <span data-ttu-id="cca61-118">Juntamente com as faixas, o usuário obtém licenças para reproduzir as faixas.</span><span class="sxs-lookup"><span data-stu-id="cca61-118">Along with the tracks, the user obtains licenses to play the tracks.</span></span>
2.  <span data-ttu-id="cca61-119">O usuário copia as faixas 50 para um novo computador que tem o Windows Media Player 11 instalado e adiciona as faixas à biblioteca do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cca61-119">The user copies the 50 tracks to a new computer that has Windows Media Player 11 installed and adds the tracks to the Windows Media Player library.</span></span>
3.  <span data-ttu-id="cca61-120">Em algum momento posterior, o módulo de atualização de licença (LRM), que faz parte do Windows Media Player 11, inspeciona os metadados nas faixas 50 e determina que o Proseware é o provedor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cca61-120">At some later time, the License Refresh Module (LRM), which is part of Windows Media Player 11, inspects the metadata in the fifty tracks and determines that Proseware is the content provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="cca61-121">O Windows Media Player é capaz de identificar o provedor de conteúdo inspecionando o atributo **ContentDistributor** em um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cca61-121">Windows Media Player is able to identify the content provider by inspecting the **ContentDistributor** attribute in a media file.</span></span> <span data-ttu-id="cca61-122">Se uma loja online que tem o logotipo do PlaysForSure fornecer um arquivo de mídia que usa o Windows Media Digital Rights Management (WMDRM), o repositório online deverá posicionar o atributo **ContentDistributor** no arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cca61-122">If an online store that has the PlaysForSure logo provides a media file that uses Windows Media Digital Rights Management (WMDRM), the online store must place the **ContentDistributor** attribute in the media file.</span></span> <span data-ttu-id="cca61-123">Para obter mais informações, consulte Adicionando o atributo de distribuidor de conteúdo no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cca61-123">For more information, see Adding the Content Distributor Attribute in the Windows Media Player SDK.</span></span>

     

4.  <span data-ttu-id="cca61-124">O LRM pesquisa a URL do documento de informações da Proseware, baixa o documento e inspeciona o elemento de **instalação** do documento para obter a URL de um pacote que o LRM pode usar para instalar o componente da Proseware.</span><span class="sxs-lookup"><span data-stu-id="cca61-124">The LRM looks up the URL of Proseware's ServiceInfo document, downloads the document, and inspects the document's **Install** element to obtain the URL of a package that the LRM can use to install Proseware's component.</span></span> <span data-ttu-id="cca61-125">O LRM instala e carrega o componente.</span><span class="sxs-lookup"><span data-stu-id="cca61-125">The LRM installs and loads the component.</span></span>
5.  <span data-ttu-id="cca61-126">Para cada uma das faixas 50, o LRM chama o método [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) do componente da Proseware.</span><span class="sxs-lookup"><span data-stu-id="cca61-126">For each of the 50 tracks, the LRM calls the Proseware component's [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) method.</span></span> <span data-ttu-id="cca61-127">O método **allowPlay** coloca uma licença para a faixa individual no novo computador e retorna **true** no parâmetro *pfAllowPlay* .</span><span class="sxs-lookup"><span data-stu-id="cca61-127">The **allowPlay** method places a license for the individual track on the new computer and returns **TRUE** in the *pfAllowPlay* parameter.</span></span>
    > [!Note]  
    > <span data-ttu-id="cca61-128">O componente Proseware deve fornecer todas as licenças necessárias para reproduzir a faixa individual. Ou seja, o componente deve fornecer uma licença raiz e uma folha, se necessário.</span><span class="sxs-lookup"><span data-stu-id="cca61-128">The Proseware component must provide all licenses required to play the individual track. That is, the component must provide both a root license and a leaf license if needed.</span></span>

     

    <span data-ttu-id="cca61-129">Durante a primeira chamada para o método **allowPlay** , o componente Proseware deve exibir uma caixa de diálogo para verificar se o usuário atual tem uma conta de Proseware e tem o direito de reproduzir o controle. Durante as chamadas subsequentes para **allowPlay**, o componente pode usar as credenciais que ele obteve na primeira chamada para verificar se o usuário tem o direito de reproduzir as faixas restantes.</span><span class="sxs-lookup"><span data-stu-id="cca61-129">During the first call to the **allowPlay** method, the Proseware component must display a dialog box to verify that the current user has a Proseware account and has the right to play the track. During subsequent calls to **allowPlay**, the component can use the credentials that it obtained in the first call to verify that the user has the right to play the remaining tracks.</span></span>

<span data-ttu-id="cca61-130">O componente, que é gravado pela loja online, deve implementar o método **allowPlay** da interface **IWMPSubscriptionService** .</span><span class="sxs-lookup"><span data-stu-id="cca61-130">The component, which is written by the online store, must implement the **allowPlay** method of the **IWMPSubscriptionService** interface.</span></span> <span data-ttu-id="cca61-131">O componente deve retornar E \_ NOTIMPL de cada um dos três métodos: **allowCDBurn**, **allowPDATransfer** e **startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="cca61-131">The component must return E\_NOTIMPL from each of the other three methods: **allowCDBurn**, **allowPDATransfer**, and **startBackgroundProcessing**.</span></span> <span data-ttu-id="cca61-132">Além disso, o componente deve definir o valor da entrada de registro **Capabilities** como 1; ou seja, o \_ sinalizador de recurso ALLOWPLAY de limite de assinatura \_ deve ser definido e todos os outros sinalizadores de funcionalidade devem ser limpos.</span><span class="sxs-lookup"><span data-stu-id="cca61-132">Also, the component must set the value of the **Capabilities** registry entry to 1; that is, the SUBSCRIPTION\_CAP\_ALLOWPLAY capability flag must be set, and all other capability flags must be cleared.</span></span> <span data-ttu-id="cca61-133">Para obter mais informações sobre como registrar o componente, consulte [chaves e entradas do registro para uma loja online tipo 2](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="cca61-133">For more information about registering the component, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="cca61-134">Para obter informações sobre como criar um componente que implementa a interface **IWMPSubscriptionService** , consulte [criando o plug-in para uma loja online tipo 2](building-the-plug-in-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="cca61-134">For information about creating a component that implements the **IWMPSubscriptionService** interface, see [Building the Plug-in for a Type 2 Online Store](building-the-plug-in-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="cca61-135">Para obter informações sobre como fornecer um documento de informações da Microsoft, envie um email para a equipe de serviços virtuais do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cca61-135">For information about providing Microsoft with a ServiceInfo document, send email to the Windows Media Player Virtual Services team.</span></span> <span data-ttu-id="cca61-136">O endereço de email da equipe é mpsvctm@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="cca61-136">The team's email address is mpsvctm@microsoft.com.</span></span>

<span data-ttu-id="cca61-137">Para obter orientações técnicas sobre como usar uma variedade de SDKs do Windows Media para criar um serviço que oferece conteúdo de mídia digital licenciado, vá para o [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) e procure "criando uma assinatura online do Windows Media Player 10".</span><span class="sxs-lookup"><span data-stu-id="cca61-137">For technical guidance on using a variety of Windows Media SDKs to create a service that offers licensed digital media content, go to the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) and search for "Creating a Windows Media Player 10 Subscription Online Store".</span></span>

## <a name="related-topics"></a><span data-ttu-id="cca61-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cca61-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cca61-139">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="cca61-139">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="cca61-140">**Lojas online do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="cca61-140">**Windows Media Player Online Stores**</span></span>](windows-media-player-online-stores.md)
</dt> </dl>

 

 




