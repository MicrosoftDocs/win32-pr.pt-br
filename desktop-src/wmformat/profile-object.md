---
title: Objeto de perfil
description: Objeto de perfil
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- SDK do Windows Media Format, objetos de perfil
- ASF (Advanced Systems Format), objetos de perfil
- ASF (formato de sistemas avançados), objetos de perfil
- objetos, objetos de perfil
- perfis, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103823601"
---
# <a name="profile-object"></a><span data-ttu-id="5c6c5-108">Objeto de perfil</span><span class="sxs-lookup"><span data-stu-id="5c6c5-108">Profile Object</span></span>

<span data-ttu-id="5c6c5-109">Um objeto de perfil gerencia as configurações de um perfil.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-109">A profile object manages the settings of a profile.</span></span> <span data-ttu-id="5c6c5-110">Os objetos de perfil podem ser criados para os dados de perfil existentes ou podem ser criados em branco, prontos para receber novos dados.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-110">Profile objects can be created for existing profile data or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="5c6c5-111">Um objeto de perfil também é criado pelo objeto leitor (e o objeto leitor síncrono) quando um arquivo é carregado para leitura.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-111">A profile object is also created by the reader object (and the synchronous reader object) when a file is loaded for reading.</span></span> <span data-ttu-id="5c6c5-112">Nesse caso, o objeto é populado com as informações de perfil armazenadas no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-112">In this case the object is populated with the profile information stored in the header of the file.</span></span>

<span data-ttu-id="5c6c5-113">Para salvar o conteúdo de um objeto de perfil, você deve chamar [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span><span class="sxs-lookup"><span data-stu-id="5c6c5-113">To save the contents of a profile object, you must call [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span></span>

<span data-ttu-id="5c6c5-114">Um perfil contém vários objetos que controlam vários aspectos do perfil (como fluxos).</span><span class="sxs-lookup"><span data-stu-id="5c6c5-114">A profile contains multiple objects that control various aspects of the profile (such as streams).</span></span> <span data-ttu-id="5c6c5-115">Todos esses objetos são subordinados ao objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-115">All of these objects are subordinate to the profile object.</span></span> <span data-ttu-id="5c6c5-116">Você não cria esses objetos com funções de criação como faria com os objetos principais desse SDK.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-116">You do not create these objects with creation functions as you would with the major objects of this SDK.</span></span> <span data-ttu-id="5c6c5-117">Em vez disso, as interfaces do objeto de perfil contêm métodos que criam os objetos subordinados.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-117">Instead, the interfaces of the profile object contain methods that create the subordinate objects.</span></span>

<span data-ttu-id="5c6c5-118">Para criar um objeto de perfil, chame um dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-118">To create a profile object, call one of the following methods.</span></span>



| <span data-ttu-id="5c6c5-119">Método</span><span class="sxs-lookup"><span data-stu-id="5c6c5-119">Method</span></span>                                                                                | <span data-ttu-id="5c6c5-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c6c5-120">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c6c5-121">**IWMProfileManager::CreateEmptyProfile**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-121">**IWMProfileManager::CreateEmptyProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | <span data-ttu-id="5c6c5-122">Cria um objeto de perfil sem nenhum dado de perfil.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-122">Creates a profile object without any profile data.</span></span>                                                                                                              |
| [<span data-ttu-id="5c6c5-123">**IWMProfileManager::LoadProfileByData**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-123">**IWMProfileManager::LoadProfileByData**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | <span data-ttu-id="5c6c5-124">Cria um objeto de perfil populado com dados de um perfil salvo como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-124">Creates a profile object populated with data from a profile saved as a string.</span></span> <span data-ttu-id="5c6c5-125">Essa é a única maneira de criar um objeto de perfil com dados de um perfil personalizado.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-125">This is the only way to create a profile object with data from a custom profile.</span></span> |
| [<span data-ttu-id="5c6c5-126">**IWMProfileManager::LoadProfileByID**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-126">**IWMProfileManager::LoadProfileByID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | <span data-ttu-id="5c6c5-127">Cria um objeto de perfil populado com dados de um perfil do sistema.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-127">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="5c6c5-128">Usa o GUID para identificar o perfil do sistema desejado.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-128">Uses the GUID to identify the desired system profile.</span></span>                                       |
| [<span data-ttu-id="5c6c5-129">**IWMProfileManager::LoadSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-129">**IWMProfileManager::LoadSystemProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | <span data-ttu-id="5c6c5-130">Cria um objeto de perfil populado com dados de um perfil do sistema.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-130">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="5c6c5-131">Usa o índice de perfil para identificar o perfil do sistema desejado.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-131">Uses the profile index to identify the desired system profile.</span></span>                              |



 

<span data-ttu-id="5c6c5-132">Todos os métodos na tabela anterior definiram um ponteiro para uma interface **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="5c6c5-132">All of the methods in the preceding table set a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="5c6c5-133">As outras interfaces do objeto de perfil podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="5c6c5-133">The other interfaces of the profile object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="5c6c5-134">As interfaces a seguir têm suporte em todos os objetos de perfil.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-134">The following interfaces are supported by every profile object.</span></span>



| <span data-ttu-id="5c6c5-135">Interface</span><span class="sxs-lookup"><span data-stu-id="5c6c5-135">Interface</span></span>                                  | <span data-ttu-id="5c6c5-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c6c5-136">Description</span></span>                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c6c5-137">**IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-137">**IWMLanguageList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | <span data-ttu-id="5c6c5-138">Gerencia uma lista de idiomas com suporte por um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-138">Manages a list of languages supported by an ASF file.</span></span>                                                                                             |
| [<span data-ttu-id="5c6c5-139">**IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-139">**IWMPacketSize**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | <span data-ttu-id="5c6c5-140">Controla o tamanho máximo de pacotes em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-140">Controls the maximum size of packets in a file.</span></span>                                                                                                   |
| [<span data-ttu-id="5c6c5-141">**IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-141">**IWMPacketSize2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | <span data-ttu-id="5c6c5-142">Controla o tamanho mínimo dos pacotes em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-142">Controls the minimum size of packets in a file.</span></span> <span data-ttu-id="5c6c5-143">Herda todos os métodos de **IWMPacketSize**.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-143">Inherits all of the methods of **IWMPacketSize**.</span></span>                                                 |
| [<span data-ttu-id="5c6c5-144">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-144">**IWMProfile**</span></span>](iwmprofile.md)           | <span data-ttu-id="5c6c5-145">Controla as configurações básicas e os objetos incluídos em um perfil.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-145">Controls the basic settings and objects included in a profile.</span></span>                                                                                    |
| [<span data-ttu-id="5c6c5-146">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-146">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | <span data-ttu-id="5c6c5-147">Recupera o GUID (identificador global exclusivo) associado ao perfil.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-147">Retrieves the globally unique identifier (GUID) associated with the profile.</span></span> <span data-ttu-id="5c6c5-148">Herda todos os métodos de **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-148">Inherits all of the methods of **IWMProfile**.</span></span>                       |
| [<span data-ttu-id="5c6c5-149">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-149">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | <span data-ttu-id="5c6c5-150">Controla o compartilhamento de largura de banda e as informações de priorização de fluxo em um perfil.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-150">Controls bandwidth sharing and stream prioritization information in a profile.</span></span> <span data-ttu-id="5c6c5-151">Herda todos os métodos de **IWMProfile** e **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="5c6c5-151">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5c6c5-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c6c5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c6c5-153">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="5c6c5-154">**Objeto do gerenciador de perfis**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-154">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="5c6c5-155">**Perfis**</span><span class="sxs-lookup"><span data-stu-id="5c6c5-155">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




