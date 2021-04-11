---
title: Objeto de exclusão mútua
description: Objeto de exclusão mútua
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- SDK do Windows Media Format, objetos de exclusão mútua
- ASF (Advanced Systems Format), objetos de exclusão mútua
- ASF (formato de sistemas avançados), objetos de exclusão mútua
- objetos, objetos de exclusão mútua
- exclusão mútua, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084389"
---
# <a name="mutual-exclusion-object"></a><span data-ttu-id="2036e-108">Objeto de exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="2036e-108">Mutual Exclusion Object</span></span>

<span data-ttu-id="2036e-109">Um objeto de exclusão mútua é usado para especificar um número de fluxos, dos quais apenas um pode ser entregue de cada vez.</span><span class="sxs-lookup"><span data-stu-id="2036e-109">A mutual exclusion object is used to specify a number of streams, of which only one can be delivered at a time.</span></span> <span data-ttu-id="2036e-110">Isso pode ser usado de várias maneiras, como fornecer um fluxo de áudio em várias linguagens como a trilha sonora de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2036e-110">This can be used in several ways, such as providing an audio stream in several languages as the soundtrack for one video stream.</span></span>

<span data-ttu-id="2036e-111">A exclusão mútua é uma parte opcional de um perfil.</span><span class="sxs-lookup"><span data-stu-id="2036e-111">Mutual exclusion is an optional part of a profile.</span></span> <span data-ttu-id="2036e-112">Os objetos de exclusão mútua podem ser criados para informações de exclusão mútua existentes em um perfil ou podem ser criados em branco, prontos para receber novos dados.</span><span class="sxs-lookup"><span data-stu-id="2036e-112">Mutual exclusion objects can be created for existing mutual exclusion information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="2036e-113">Os objetos de exclusão mútua não podem existir independentemente de um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="2036e-113">Mutual exclusion objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="2036e-114">Para salvar o conteúdo de um objeto de exclusão mútua, você deve chamar [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="2036e-114">To save the contents of a mutual exclusion object, you must call [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

<span data-ttu-id="2036e-115">Para criar um objeto de exclusão mútua, use um dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2036e-115">To create a mutual exclusion object, use one of the following methods.</span></span>



| <span data-ttu-id="2036e-116">Método</span><span class="sxs-lookup"><span data-stu-id="2036e-116">Method</span></span>                                                                              | <span data-ttu-id="2036e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2036e-117">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2036e-118">**IWMProfile::CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="2036e-118">**IWMProfile::CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="2036e-119">Cria um objeto de exclusão mútua sem nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="2036e-119">Creates a mutual exclusion object without any data.</span></span>                                                                                                         |
| [<span data-ttu-id="2036e-120">**IWMProfile::GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="2036e-120">**IWMProfile::GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="2036e-121">Cria um objeto de exclusão mútua populado com dados de um perfil.</span><span class="sxs-lookup"><span data-stu-id="2036e-121">Creates a mutual exclusion object populated with data from a profile.</span></span> <span data-ttu-id="2036e-122">Usa o índice de exclusão mútua para identificar as informações de exclusão mútua desejada.</span><span class="sxs-lookup"><span data-stu-id="2036e-122">Uses the mutual exclusion index to identify the desired mutual exclusion information.</span></span> |



 

<span data-ttu-id="2036e-123">Os dois métodos na tabela anterior definiram um ponteiro para uma interface **IWMMutualExclusion** .</span><span class="sxs-lookup"><span data-stu-id="2036e-123">Both methods in the preceding table set a pointer to an **IWMMutualExclusion** interface.</span></span> <span data-ttu-id="2036e-124">A interface **IWMStreamList** é herdada por **IWMMutualExclusion** e nunca precisa ser acessada diretamente.</span><span class="sxs-lookup"><span data-stu-id="2036e-124">The **IWMStreamList** interface is inherited by **IWMMutualExclusion** and never needs to be accessed directly.</span></span> <span data-ttu-id="2036e-125">A outra interface do objeto de exclusão mútua pode ser obtida chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="2036e-125">The other interface of the mutual exclusion object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="2036e-126">As interfaces a seguir têm suporte de cada objeto de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="2036e-126">The following interfaces are supported by every mutual exclusion object.</span></span>



| <span data-ttu-id="2036e-127">Interface</span><span class="sxs-lookup"><span data-stu-id="2036e-127">Interface</span></span>                                          | <span data-ttu-id="2036e-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="2036e-128">Description</span></span>                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2036e-129">**IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="2036e-129">**IWMMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | <span data-ttu-id="2036e-130">Define e recupera o tipo de exclusão mútua a ser usado.</span><span class="sxs-lookup"><span data-stu-id="2036e-130">Sets and retrieves the type of mutual exclusion to be used.</span></span>                                                                                            |
| [<span data-ttu-id="2036e-131">**IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="2036e-131">**IWMMutualExclusion2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | <span data-ttu-id="2036e-132">Organiza fluxos em registros, que podem ser usados para criar cenários complexos de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="2036e-132">Organizes streams into records, which can be used to create complex mutual exclusion scenarios.</span></span> <span data-ttu-id="2036e-133">Herda todos os métodos de **IWMMutualExclusion**.</span><span class="sxs-lookup"><span data-stu-id="2036e-133">Inherits all of the methods of **IWMMutualExclusion**.</span></span> |
| [<span data-ttu-id="2036e-134">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="2036e-134">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="2036e-135">Gerencia a lista de fluxos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="2036e-135">Manages the list of mutually exclusive streams.</span></span>                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2036e-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2036e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2036e-137">**Exclusão mútua**</span><span class="sxs-lookup"><span data-stu-id="2036e-137">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="2036e-138">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="2036e-138">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="2036e-139">**Objeto do gerenciador de perfis**</span><span class="sxs-lookup"><span data-stu-id="2036e-139">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




