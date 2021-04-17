---
title: Interface IWMProfile
description: A interface IWMProfile é a interface primária para um objeto de perfil.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Formato de mídia do Windows da interface IWMProfile
- Formato de mídia do Windows da interface IWMProfile, descrito
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "105811895"
---
# <a name="iwmprofile-interface"></a><span data-ttu-id="f20ce-105">Interface IWMProfile</span><span class="sxs-lookup"><span data-stu-id="f20ce-105">IWMProfile interface</span></span>

<span data-ttu-id="f20ce-106">A interface **IWMProfile** é a interface primária para um objeto de [*perfil*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="f20ce-106">The **IWMProfile** interface is the primary interface for a [*profile*](wmformat-glossary.md) object.</span></span> <span data-ttu-id="f20ce-107">Um objeto de perfil é usado para configurar perfis personalizados.</span><span class="sxs-lookup"><span data-stu-id="f20ce-107">A profile object is used to configure custom profiles.</span></span> <span data-ttu-id="f20ce-108">Você pode usar **IWMProfile** para criar, excluir ou modificar objetos de configuração de fluxo e objetos de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="f20ce-108">You can use **IWMProfile** to create, delete, or modify stream configuration objects and mutual exclusion objects.</span></span> <span data-ttu-id="f20ce-109">Você também pode definir e recuperar informações gerais sobre o perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-109">You can also set and retrieve general information about the profile.</span></span> <span data-ttu-id="f20ce-110">Para acessar todos os recursos do objeto de perfil, você deve usar [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), que herda de **IWMProfile** e [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span><span class="sxs-lookup"><span data-stu-id="f20ce-110">To access all the features of the profile object, you should use [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), which inherits from **IWMProfile** and [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span></span>

<span data-ttu-id="f20ce-111">O **IWMProfile** também é acessível por meio do objeto leitor, onde você pode usá-lo para obter informações sobre os fluxos de um arquivo que é carregado no leitor.</span><span class="sxs-lookup"><span data-stu-id="f20ce-111">**IWMProfile** is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader.</span></span> <span data-ttu-id="f20ce-112">Ao acessar o **IWMProfile** do leitor, você pode fazer alterações no perfil, mas nenhuma das alterações pode ser salva no arquivo.</span><span class="sxs-lookup"><span data-stu-id="f20ce-112">When accessing **IWMProfile** from the reader, you can make changes to the profile, but none of the changes can be saved to the file.</span></span> <span data-ttu-id="f20ce-113">Geralmente, é útil usar o perfil de um arquivo existente como a base de um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-113">It is often handy to use the profile of an existing file as the foundation of a new profile.</span></span> <span data-ttu-id="f20ce-114">O leitor síncrono dá suporte a **IWMProfile** da mesma maneira que o leitor.</span><span class="sxs-lookup"><span data-stu-id="f20ce-114">The synchronous reader supports **IWMProfile** in the same way as the reader.</span></span>

<span data-ttu-id="f20ce-115">As informações de perfil obtidas por meio do leitor ou leitor síncrono não são provenientes de um arquivo. prx.</span><span class="sxs-lookup"><span data-stu-id="f20ce-115">The profile information obtained through the reader or synchronous reader does not come from a .prx file.</span></span> <span data-ttu-id="f20ce-116">O leitor usa as informações no arquivo ASF para montar as configurações de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f20ce-116">The reader uses the information in the ASF file to assemble the stream configurations.</span></span> <span data-ttu-id="f20ce-117">Assim, determinadas informações de perfil, como o nome e a descrição, não estão disponíveis por meio do leitor.</span><span class="sxs-lookup"><span data-stu-id="f20ce-117">Thus certain profile information, like the name and description, are not available through the reader.</span></span>

<span data-ttu-id="f20ce-118">Há várias maneiras de obter um ponteiro para uma interface **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="f20ce-118">There are several ways to obtain a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="f20ce-119">O Gerenciador de perfis tem métodos para criar um novo perfil e acessar perfis existentes.</span><span class="sxs-lookup"><span data-stu-id="f20ce-119">The profile manager has methods to create a new profile and to access existing profiles.</span></span> <span data-ttu-id="f20ce-120">Todos esses métodos definem um ponteiro **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="f20ce-120">All of these methods set an **IWMProfile** pointer.</span></span> <span data-ttu-id="f20ce-121">Ao ler um arquivo, um ponteiro para **IWMProfile** pode ser obtido chamando o método **QueryInterface** de qualquer interface de leitor.</span><span class="sxs-lookup"><span data-stu-id="f20ce-121">When reading a file, a pointer to **IWMProfile** can be obtained by calling the **QueryInterface** method of any reader interface.</span></span> <span data-ttu-id="f20ce-122">Da mesma forma, qualquer interface do objeto leitor síncrono pode obter um ponteiro com uma chamada para **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span><span class="sxs-lookup"><span data-stu-id="f20ce-122">Likewise, any interface of the synchronous reader object can obtain a pointer with a call to **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span></span>

## <a name="members"></a><span data-ttu-id="f20ce-123">Membros</span><span class="sxs-lookup"><span data-stu-id="f20ce-123">Members</span></span>

<span data-ttu-id="f20ce-124">A interface **IWMProfile** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f20ce-124">The **IWMProfile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f20ce-125">**IWMProfile** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f20ce-125">**IWMProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="f20ce-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="f20ce-126">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f20ce-127">Métodos</span><span class="sxs-lookup"><span data-stu-id="f20ce-127">Methods</span></span>

<span data-ttu-id="f20ce-128">A interface **IWMProfile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f20ce-128">The **IWMProfile** interface has these methods.</span></span>



| <span data-ttu-id="f20ce-129">Método</span><span class="sxs-lookup"><span data-stu-id="f20ce-129">Method</span></span>                                                                  | <span data-ttu-id="f20ce-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="f20ce-130">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f20ce-131">**AddMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="f20ce-131">**AddMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | <span data-ttu-id="f20ce-132">Adiciona um objeto de exclusão mútua ao perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-132">Adds a mutual exclusion object to the profile.</span></span><br/>                                   |
| [<span data-ttu-id="f20ce-133">**AddStream**</span><span class="sxs-lookup"><span data-stu-id="f20ce-133">**AddStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | <span data-ttu-id="f20ce-134">Adiciona um fluxo ao perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-134">Adds a stream to the profile.</span></span><br/>                                                    |
| [<span data-ttu-id="f20ce-135">**CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="f20ce-135">**CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="f20ce-136">Cria um objeto de exclusão mútua para o perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-136">Creates a mutual exclusion object for the profile.</span></span><br/>                               |
| [<span data-ttu-id="f20ce-137">**CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="f20ce-137">**CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | <span data-ttu-id="f20ce-138">Cria um objeto de configuração de fluxo para o perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-138">Creates a stream configuration object for the profile.</span></span><br/>                           |
| [<span data-ttu-id="f20ce-139">**GetDescription**</span><span class="sxs-lookup"><span data-stu-id="f20ce-139">**GetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | <span data-ttu-id="f20ce-140">Recupera a descrição do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-140">Retrieves the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="f20ce-141">**GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="f20ce-141">**GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="f20ce-142">Recupera um objeto de exclusão mútua do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-142">Retrieves a mutual exclusion object from the profile.</span></span><br/>                            |
| [<span data-ttu-id="f20ce-143">**GetMutualExclusionCount**</span><span class="sxs-lookup"><span data-stu-id="f20ce-143">**GetMutualExclusionCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | <span data-ttu-id="f20ce-144">Recupera o número de objetos de exclusão mútua no perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-144">Retrieves the number of mutual exclusion objects in the profile.</span></span><br/>                 |
| [<span data-ttu-id="f20ce-145">**GetName**</span><span class="sxs-lookup"><span data-stu-id="f20ce-145">**GetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | <span data-ttu-id="f20ce-146">Recupera o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-146">Retrieves the name of the profile.</span></span><br/>                                               |
| [<span data-ttu-id="f20ce-147">**GetStream**</span><span class="sxs-lookup"><span data-stu-id="f20ce-147">**GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | <span data-ttu-id="f20ce-148">Recupera um fluxo, usando um número de índice, do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-148">Retrieves a stream, using an index number, from the profile.</span></span><br/>                     |
| [<span data-ttu-id="f20ce-149">**GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="f20ce-149">**GetStreamByNumber**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | <span data-ttu-id="f20ce-150">Recupera um fluxo, usando o número do fluxo, do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-150">Retrieves a stream, using the number of the stream, from the profile.</span></span><br/>            |
| [<span data-ttu-id="f20ce-151">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="f20ce-151">**GetStreamCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | <span data-ttu-id="f20ce-152">Recupera o número de fluxos no perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-152">Retrieves the number of streams in the profile.</span></span><br/>                                  |
| [<span data-ttu-id="f20ce-153">**Obter versão**</span><span class="sxs-lookup"><span data-stu-id="f20ce-153">**GetVersion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | <span data-ttu-id="f20ce-154">Recupera o número de versão do Microsoft Windows Media Services no perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-154">Retrieves the version number of Microsoft Windows Media Services in the profile.</span></span><br/> |
| [<span data-ttu-id="f20ce-155">**ReconfigStream**</span><span class="sxs-lookup"><span data-stu-id="f20ce-155">**ReconfigStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | <span data-ttu-id="f20ce-156">Permite que as alterações feitas em uma configuração de fluxo sejam incluídas no perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-156">Enables changes made to a stream configuration to be included in the profile.</span></span><br/>    |
| [<span data-ttu-id="f20ce-157">**RemoveMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="f20ce-157">**RemoveMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | <span data-ttu-id="f20ce-158">Remove um objeto de exclusão mútua do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-158">Removes a mutual exclusion object from the profile.</span></span><br/>                              |
| [<span data-ttu-id="f20ce-159">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="f20ce-159">**RemoveStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | <span data-ttu-id="f20ce-160">Remove um fluxo do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-160">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="f20ce-161">**RemoveStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="f20ce-161">**RemoveStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | <span data-ttu-id="f20ce-162">Remove um fluxo do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-162">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="f20ce-163">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="f20ce-163">**SetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | <span data-ttu-id="f20ce-164">Especifica a descrição do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-164">Specifies the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="f20ce-165">**SetName**</span><span class="sxs-lookup"><span data-stu-id="f20ce-165">**SetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | <span data-ttu-id="f20ce-166">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20ce-166">Specifies the name of the profile.</span></span><br/>                                               |



 

<span data-ttu-id="f20ce-167">Para obter informações sobre quais interfaces podem ser obtidas usando o método QueryInterface dessa interface, consulte o tópico para o objeto no qual essa interface é implementada.</span><span class="sxs-lookup"><span data-stu-id="f20ce-167">For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.</span></span>

## <a name="see-also"></a><span data-ttu-id="f20ce-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="f20ce-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20ce-169">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="f20ce-169">**Interfaces**</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="f20ce-170">**Interface IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="f20ce-170">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="f20ce-171">**Objeto do gerenciador de perfis**</span><span class="sxs-lookup"><span data-stu-id="f20ce-171">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="f20ce-172">**Objeto de leitor**</span><span class="sxs-lookup"><span data-stu-id="f20ce-172">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="f20ce-173">**Objeto de leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="f20ce-173">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="f20ce-174">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="f20ce-174">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

