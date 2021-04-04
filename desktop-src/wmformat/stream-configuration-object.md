---
title: Objeto de configuração de fluxo
description: Objeto de configuração de fluxo
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- SDK do Windows Media Format, objetos de configuração de fluxo
- ASF (Advanced Systems Format), objetos de configuração de fluxo
- ASF (formato de sistemas avançados), objetos de configuração de fluxo
- objetos, objetos de configuração de fluxo
- objetos de configuração de fluxo
- fluxos, objetos de configuração de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084397"
---
# <a name="stream-configuration-object"></a><span data-ttu-id="2c640-109">Objeto de configuração de fluxo</span><span class="sxs-lookup"><span data-stu-id="2c640-109">Stream Configuration Object</span></span>

<span data-ttu-id="2c640-110">Um objeto de configuração de fluxo é usado para especificar as propriedades de um fluxo de mídia em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="2c640-110">A stream configuration object is used to specify the properties of a media stream in an ASF file.</span></span> <span data-ttu-id="2c640-111">Os objetos de configuração de fluxo podem ser criados para fluxos existentes em um perfil ou podem ser criados em branco, prontos para receber novos dados.</span><span class="sxs-lookup"><span data-stu-id="2c640-111">Stream configuration objects can be created for existing streams in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="2c640-112">Os objetos de configuração de fluxo não podem existir independentemente de um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="2c640-112">Stream configuration objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="2c640-113">Para salvar o conteúdo de um objeto de configuração de fluxo, você deve chamar [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para adicionar um novo fluxo ou [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para salvar as alterações feitas em um fluxo existente.</span><span class="sxs-lookup"><span data-stu-id="2c640-113">To save the contents of a stream configuration object, you must call either [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add a new stream or [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to save changes made to an existing stream.</span></span>

<span data-ttu-id="2c640-114">Para criar um objeto de configuração de fluxo, use um dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c640-114">To create a stream configuration object, use one of the following methods.</span></span>



| <span data-ttu-id="2c640-115">Método</span><span class="sxs-lookup"><span data-stu-id="2c640-115">Method</span></span>                                                                | <span data-ttu-id="2c640-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c640-116">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c640-117">**IWMProfile::CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="2c640-117">**IWMProfile::CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | <span data-ttu-id="2c640-118">Cria um objeto de configuração de fluxo sem nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="2c640-118">Creates a stream configuration object without any data.</span></span>                                                                          |
| [<span data-ttu-id="2c640-119">**IWMProfile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="2c640-119">**IWMProfile::GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | <span data-ttu-id="2c640-120">Cria um objeto de configuração de fluxo populado com dados de um perfil.</span><span class="sxs-lookup"><span data-stu-id="2c640-120">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="2c640-121">Usa o índice de fluxo para identificar o fluxo desejado.</span><span class="sxs-lookup"><span data-stu-id="2c640-121">Uses the stream index to identify the desired stream.</span></span>  |
| [<span data-ttu-id="2c640-122">**IWMProfile::GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="2c640-122">**IWMProfile::GetStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | <span data-ttu-id="2c640-123">Cria um objeto de configuração de fluxo populado com dados de um perfil.</span><span class="sxs-lookup"><span data-stu-id="2c640-123">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="2c640-124">Usa o número de fluxo para identificar o fluxo desejado.</span><span class="sxs-lookup"><span data-stu-id="2c640-124">Uses the stream number to identify the desired stream.</span></span> |



 

<span data-ttu-id="2c640-125">Todos os métodos na tabela anterior definiram um ponteiro para uma interface **IWMStreamConfig** .</span><span class="sxs-lookup"><span data-stu-id="2c640-125">All of the methods in the preceding table set a pointer to an **IWMStreamConfig** interface.</span></span> <span data-ttu-id="2c640-126">As outras interfaces do objeto de configuração de fluxo podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="2c640-126">The other interfaces of the stream configuration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="2c640-127">As interfaces a seguir têm suporte do objeto de configuração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2c640-127">The following interfaces are supported by the stream configuration object.</span></span>



| <span data-ttu-id="2c640-128">Interface</span><span class="sxs-lookup"><span data-stu-id="2c640-128">Interface</span></span>                                        | <span data-ttu-id="2c640-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c640-129">Description</span></span>                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c640-130">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="2c640-130">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="2c640-131">Define e recupera a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="2c640-131">Sets and retrieves the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream.</span></span>                                    |
| [<span data-ttu-id="2c640-132">**IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="2c640-132">**IWMPropertyVault**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | <span data-ttu-id="2c640-133">Define e recupera propriedades que não são necessárias para todos os fluxos, como configurações de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="2c640-133">Sets and retrieves properties that are not required for all streams, like variable bit rate (VBR) settings.</span></span>                  |
| [<span data-ttu-id="2c640-134">**IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="2c640-134">**IWMStreamConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | <span data-ttu-id="2c640-135">Define e recupera todas as informações básicas sobre um fluxo.</span><span class="sxs-lookup"><span data-stu-id="2c640-135">Sets and retrieves all of the basic information about a stream.</span></span>                                                              |
| [<span data-ttu-id="2c640-136">**IWMStreamConfig2**</span><span class="sxs-lookup"><span data-stu-id="2c640-136">**IWMStreamConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | <span data-ttu-id="2c640-137">Configura os tipos de extensões de unidade de dados associadas ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="2c640-137">Configures the types of data unit extensions associated with the stream.</span></span> <span data-ttu-id="2c640-138">Herda todos os métodos de **IWMStreamConfig**.</span><span class="sxs-lookup"><span data-stu-id="2c640-138">Inherits all of the methods of **IWMStreamConfig**.</span></span> |
| [<span data-ttu-id="2c640-139">**IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="2c640-139">**IWMStreamConfig3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | <span data-ttu-id="2c640-140">Define e recupera o idioma para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="2c640-140">Sets and retrieves the language for the stream.</span></span> <span data-ttu-id="2c640-141">Herda todos os métodos de **IWMStreamConfig** e **IWMStreamConfig2**.</span><span class="sxs-lookup"><span data-stu-id="2c640-141">Inherits all of the methods of **IWMStreamConfig** and **IWMStreamConfig2**.</span></span> |
| [<span data-ttu-id="2c640-142">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="2c640-142">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="2c640-143">Gerencia as propriedades de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2c640-143">Manages the properties of a video stream.</span></span> <span data-ttu-id="2c640-144">Essa é uma interface opcional e está disponível apenas para fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2c640-144">This is an optional interface, and is available only for video streams.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="2c640-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c640-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c640-146">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="2c640-146">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="2c640-147">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="2c640-147">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="2c640-148">**Objeto do gerenciador de perfis**</span><span class="sxs-lookup"><span data-stu-id="2c640-148">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




