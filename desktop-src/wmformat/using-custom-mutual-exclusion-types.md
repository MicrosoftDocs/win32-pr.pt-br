---
title: Usando tipos de exclusão mútua personalizada
description: Usando tipos de exclusão mútua personalizada
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- exclusão mútua, interface IWMMutualExclusion
- exclusão mútua, tipos personalizados
- perfis, tipos de exclusão mútua personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084354"
---
# <a name="using-custom-mutual-exclusion-types"></a><span data-ttu-id="52508-107">Usando tipos de exclusão mútua personalizada</span><span class="sxs-lookup"><span data-stu-id="52508-107">Using Custom Mutual Exclusion Types</span></span>

<span data-ttu-id="52508-108">Você pode usar objetos de exclusão mútua em um perfil para atender às necessidades de cenários personalizados.</span><span class="sxs-lookup"><span data-stu-id="52508-108">You can use mutual exclusion objects in a profile to meet the needs of custom scenarios.</span></span> <span data-ttu-id="52508-109">Ao passar o valor de GUID CLSID \_ WMMUTEX \_ desconhecido para [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), você informa ao objeto de exclusão mútua que está usando um cenário personalizado.</span><span class="sxs-lookup"><span data-stu-id="52508-109">By passing the GUID value CLSID\_WMMUTEX\_Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), you inform the mutual exclusion object that you are using a custom scenario.</span></span>

<span data-ttu-id="52508-110">Você deve controlar manualmente a seleção de fluxo ao ler um arquivo com um valor de exclusão mútua personalizado.</span><span class="sxs-lookup"><span data-stu-id="52508-110">You must manually control stream selection when you read a file with a custom mutual exclusion value.</span></span> <span data-ttu-id="52508-111">O objeto leitor usará o primeiro fluxo que você adicionar à exclusão mútua como padrão.</span><span class="sxs-lookup"><span data-stu-id="52508-111">The reader object will use the first stream you add to the mutual exclusion as the default.</span></span>

<span data-ttu-id="52508-112">Use as etapas a seguir para criar um objeto de exclusão mútua personalizada e adicioná-lo a um perfil:</span><span class="sxs-lookup"><span data-stu-id="52508-112">Use the following steps to create a custom mutual exclusion object and add it to a profile:</span></span>

1.  <span data-ttu-id="52508-113">Crie um Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="52508-113">Create a profile manager by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="52508-114">Inicie o com um perfil existente ou crie um totalmente novo.</span><span class="sxs-lookup"><span data-stu-id="52508-114">Either start with an existing profile, or create an entirely new one.</span></span>
    -   <span data-ttu-id="52508-115">Se você estiver usando um perfil existente, chame um dos métodos de carga da interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="52508-115">If you are using an existing profile, call one of the load methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="52508-116">Em seguida, pule para a etapa 4.</span><span class="sxs-lookup"><span data-stu-id="52508-116">Then skip to step 4.</span></span>
    -   <span data-ttu-id="52508-117">Se você estiver criando um perfil totalmente novo, chame [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="52508-117">If you are creating an entirely new profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span>
3.  <span data-ttu-id="52508-118">Adicione fluxos ao novo perfil chamando [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span><span class="sxs-lookup"><span data-stu-id="52508-118">Add streams to the new profile by calling [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span></span> <span data-ttu-id="52508-119">Configure os fluxos conforme necessário usando os métodos de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="52508-119">Configure the streams as needed using the methods of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span> <span data-ttu-id="52508-120">Você também pode chamar **QueryInterface** para acessar outras interfaces no objeto de configuração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="52508-120">You can also call **QueryInterface** to access other interfaces in the stream configuration object.</span></span>

    <span data-ttu-id="52508-121">**CreateNewStream** cria apenas um objeto de configuração de fluxo e não afeta o perfil.</span><span class="sxs-lookup"><span data-stu-id="52508-121">**CreateNewStream** creates only a stream configuration object, and does not affect the profile.</span></span> <span data-ttu-id="52508-122">Depois que um fluxo é configurado corretamente, você deve chamar [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para adicionar o fluxo ao perfil.</span><span class="sxs-lookup"><span data-stu-id="52508-122">After a stream is configured properly, you must call [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add the stream to the profile.</span></span>

4.  <span data-ttu-id="52508-123">Crie um objeto de exclusão mútua chamando [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="52508-123">Create a mutual exclusion object by calling [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span></span>
5.  <span data-ttu-id="52508-124">Adicione os fluxos desejados ao objeto de exclusão mútua chamando [**IWMStreamList:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponível diretamente de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), que herda de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span><span class="sxs-lookup"><span data-stu-id="52508-124">Add the desired streams to the mutual exclusion object by calling [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (available directly from [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), which inherits from [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span></span>
6.  <span data-ttu-id="52508-125">Defina o tipo de exclusão mútua para personalizado chamando [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="52508-125">Set the type of mutual exclusion to custom by calling [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span> <span data-ttu-id="52508-126">Passe o CLSID \_ WMMUTEX \_ desconhecido como o tipo Guid.</span><span class="sxs-lookup"><span data-stu-id="52508-126">Pass the CLSID\_WMMUTEX\_Unknown as the type GUID.</span></span>
7.  <span data-ttu-id="52508-127">Adicione o objeto de exclusão mútua configurado ao perfil chamando [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="52508-127">Add the configured mutual exclusion object to the profile by calling [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52508-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52508-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52508-129">**Interface IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="52508-129">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="52508-130">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="52508-130">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="52508-131">**Interface IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="52508-131">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="52508-132">**Interface IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="52508-132">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="52508-133">**Interface IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="52508-133">**IWMStreamList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[<span data-ttu-id="52508-134">**Usando a exclusão mútua**</span><span class="sxs-lookup"><span data-stu-id="52508-134">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="52508-135">**WMCreateProfileManager**</span><span class="sxs-lookup"><span data-stu-id="52508-135">**WMCreateProfileManager**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




