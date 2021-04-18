---
title: Perfis
description: Perfis
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- SDK do Windows Media Format, perfis
- ASF (Advanced Systems Format), perfis
- ASF (formato de sistemas avançados), perfis
- SDK do Windows Media Format, arquivos. prx
- Formato de sistema avançado (ASF), arquivos. prx
- ASF (formato de sistemas avançados), arquivos. prx
- SDK do Windows Media Format, editor de perfil
- ASF (Advanced Systems Format), editor de perfil
- ASF (formato de sistemas avançados), editor de perfil
- arquivos. prx
- arquivos PRX
- Editor de perfil
- Codificador de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de244445a7c1301c7a14ef273b81ac9fd9cbfb62
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105781629"
---
# <a name="profiles"></a><span data-ttu-id="62cac-116">Perfis</span><span class="sxs-lookup"><span data-stu-id="62cac-116">Profiles</span></span>

<span data-ttu-id="62cac-117">Um perfil é uma coleção de dados que descreve a configuração de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="62cac-117">A profile is a collection of data that describes the configuration of an ASF file.</span></span> <span data-ttu-id="62cac-118">No mínimo, um perfil deve conter definições de configuração para um único fluxo.</span><span class="sxs-lookup"><span data-stu-id="62cac-118">At a minimum, a profile must contain configuration settings for a single stream.</span></span>

<span data-ttu-id="62cac-119">As informações de fluxo em um perfil contêm a taxa de bits, a janela de buffer e as propriedades de mídia para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="62cac-119">The stream information in a profile contains the bit rate, buffer window, and media properties for the stream.</span></span> <span data-ttu-id="62cac-120">As informações de fluxo para áudio e vídeo descrevem exatamente como a mídia é configurada no arquivo, incluindo qual codec (se houver) será usado para compactar os dados.</span><span class="sxs-lookup"><span data-stu-id="62cac-120">The stream information for audio and video describes exactly how the media is configured in the file, including which codec (if any) will be used to compress the data.</span></span>

<span data-ttu-id="62cac-121">Um perfil também contém informações sobre os vários recursos de arquivo ASF que serão usados em arquivos criados com ele.</span><span class="sxs-lookup"><span data-stu-id="62cac-121">A profile also contains information about the various ASF file features that will be used in files created with it.</span></span> <span data-ttu-id="62cac-122">Isso inclui [exclusão mútua](mutual-exclusion.md), [priorização de fluxo](stream-prioritization.md), [compartilhamento de largura de banda](bandwidth-sharing.md)e extensões de unidade de [dados](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="62cac-122">These include [Mutual Exclusion](mutual-exclusion.md), [Stream Prioritization](stream-prioritization.md), [Bandwidth Sharing](bandwidth-sharing.md), and [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="62cac-123">As versões anteriores do SDK do Windows Media Format forneciam perfis de sistema pré-configurados, que poderiam ser usados para criar tipos comuns de arquivos ou alterados um pouco para atender às necessidades do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="62cac-123">Previous versions of the Windows Media Format SDK provided preconfigured system profiles, which could be used to create common types of files, or altered slightly to suit the needs of your application.</span></span> <span data-ttu-id="62cac-124">Os perfis do sistema não têm suporte para os codecs da série Windows Media 9.</span><span class="sxs-lookup"><span data-stu-id="62cac-124">System profiles are not supported for the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="62cac-125">Isso ocorre porque o número de tipos "comuns" de arquivos cresceu exponencialmente com a adição de novos recursos.</span><span class="sxs-lookup"><span data-stu-id="62cac-125">This is because the number of "common" types of files has grown exponentially with the addition of new features.</span></span> <span data-ttu-id="62cac-126">Espera-se que praticamente todo criador de conteúdo precise que vá além das soluções simples fornecidas por perfis de sistema.</span><span class="sxs-lookup"><span data-stu-id="62cac-126">It is expected that virtually every content creator has needs that go beyond the simple solutions provided by system profiles.</span></span> <span data-ttu-id="62cac-127">Você ainda pode usar os perfis de sistema antigos como um local inicial.</span><span class="sxs-lookup"><span data-stu-id="62cac-127">You can still use the old system profiles as a starting place.</span></span> <span data-ttu-id="62cac-128">Para obter mais informações, consulte [usando perfis de sistema](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="62cac-128">For more information, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="62cac-129">Você deve fornecer ao gravador um perfil para cada arquivo que você escrever.</span><span class="sxs-lookup"><span data-stu-id="62cac-129">You must supply the writer with a profile for every file you write.</span></span> <span data-ttu-id="62cac-130">Você pode especificar um perfil a ser usado com o gravador chamando [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="62cac-130">You can specify a profile to use with the writer by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>

<span data-ttu-id="62cac-131">Os dados de perfil existem em várias formas diferentes que podem ser usadas pelo Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="62cac-131">Profile data exists in several different forms that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="62cac-132">As informações de perfil também podem ser acessadas de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="62cac-132">Profile information can also be accessed in several ways.</span></span> <span data-ttu-id="62cac-133">Isso pode levar à confusão sobre o que é um perfil e como ele é usado.</span><span class="sxs-lookup"><span data-stu-id="62cac-133">This can lead to confusion about what a profile is and how it is used.</span></span>

<span data-ttu-id="62cac-134">O diagrama a seguir mostra como os dados de perfil são usados no SDK.</span><span class="sxs-lookup"><span data-stu-id="62cac-134">The following diagram shows how profile data is used in the SDK.</span></span>

![diagrama mostrando o fluxo de informações de perfil.](images/formatsdk01.png)

<span data-ttu-id="62cac-136">Os dados de perfil assumem três formas diferentes: dados contidos em um objeto de perfil em um aplicativo, um arquivo XML em disco e dados no cabeçalho de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="62cac-136">Profile data takes three different forms: data contained within a profile object in an application, an XML file on disk, and data in the header of an ASF file.</span></span> <span data-ttu-id="62cac-137">Cada uma dessas formas de dados é mostrada como um retângulo sombreado no diagrama.</span><span class="sxs-lookup"><span data-stu-id="62cac-137">Each of these forms of data is shown as a shaded rectangle in the diagram.</span></span>

## <a name="data-in-a-profile-object"></a><span data-ttu-id="62cac-138">Dados em um objeto de perfil</span><span class="sxs-lookup"><span data-stu-id="62cac-138">Data in a Profile Object</span></span>

<span data-ttu-id="62cac-139">Ao editar um perfil, você usa um objeto de perfil, que encapsula todos os dados de perfil.</span><span class="sxs-lookup"><span data-stu-id="62cac-139">When you are editing a profile, you use a profile object, which encapsulates all of the profile data.</span></span> <span data-ttu-id="62cac-140">Você pode criar um objeto de perfil vazio usando o objeto do Gerenciador de perfis.</span><span class="sxs-lookup"><span data-stu-id="62cac-140">You can create an empty profile object by using the profile manager object.</span></span> <span data-ttu-id="62cac-141">Você também pode usar o objeto do Gerenciador de perfis para carregar dados de perfil existentes em um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="62cac-141">You can also use the profile manager object to load existing profile data into a profile object.</span></span>

<span data-ttu-id="62cac-142">A maioria dos dados de perfil deve ser adicionada e manipulada por meio do uso de objetos que representam partes individuais do perfil.</span><span class="sxs-lookup"><span data-stu-id="62cac-142">Most profile data must be added and manipulated through the use of objects representing individual parts of the profile.</span></span> <span data-ttu-id="62cac-143">Isso inclui objetos de configuração de fluxo, objetos de exclusão mútua, objetos de compartilhamento de largura de banda e um objeto de priorização de fluxo.</span><span class="sxs-lookup"><span data-stu-id="62cac-143">These include stream configuration objects, mutual exclusion objects, bandwidth sharing objects, and a stream prioritization object.</span></span> <span data-ttu-id="62cac-144">Cada um desses tipos de objeto pode ser criado usando métodos no objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="62cac-144">Each of these object types can be created using methods in the profile object.</span></span> <span data-ttu-id="62cac-145">Fazer alterações nesses objetos não afetará o objeto de perfil até que você use um método no objeto de perfil para incluir os dados atualizados do outro objeto.</span><span class="sxs-lookup"><span data-stu-id="62cac-145">Making changes to these objects does not affect the profile object until you use a method in the profile object to include the updated data from the other object.</span></span>

## <a name="data-in-an-xml-file"></a><span data-ttu-id="62cac-146">Dados em um arquivo XML</span><span class="sxs-lookup"><span data-stu-id="62cac-146">Data in an XML File</span></span>

<span data-ttu-id="62cac-147">Os dados de perfil são armazenados em disco na forma de um arquivo XML com a extensão de nome de arquivo. prx.</span><span class="sxs-lookup"><span data-stu-id="62cac-147">Profile data is stored on disk in the form of an XML file with the .prx file name extension.</span></span> <span data-ttu-id="62cac-148">Incluído no Windows Media Format SDK há uma coleção de perfis chamada perfis de sistema que abrangem os tipos mais comuns de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="62cac-148">Included with the Windows Media Format SDK is a collection of profiles called system profiles that cover the most common types of ASF files.</span></span> <span data-ttu-id="62cac-149">Os perfis de sistema são armazenados em um arquivo chamado WMSysPr9. prx.</span><span class="sxs-lookup"><span data-stu-id="62cac-149">System profiles are stored in a file named WMSysPr9.prx.</span></span> <span data-ttu-id="62cac-150">(Observe que esse arquivo realmente não contém perfis de sistema para o Windows Media 9 Series porque o conceito de perfis de sistema não é mais usado.) Ao salvar seus próprios perfis personalizados, você deve salvá-los em seus próprios arquivos.</span><span class="sxs-lookup"><span data-stu-id="62cac-150">(Note that this file actually contains no system profiles for Windows Media 9 Series because the concept of system profiles is no longer used.) When you save your own custom profiles, you must save them to your own files.</span></span>

<span data-ttu-id="62cac-151">Você pode usar o objeto do Gerenciador de perfis para salvar os dados de um objeto de perfil em uma cadeia de caracteres de texto XML.</span><span class="sxs-lookup"><span data-stu-id="62cac-151">You can use the profile manager object to save the data from a profile object to a string of XML text.</span></span> <span data-ttu-id="62cac-152">Em seguida, você pode usar quaisquer funções de e/s de arquivo que gosta de salvar a cadeia de caracteres em um arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="62cac-152">You can then use whatever file I/O functions you like to save the string to a file on disk.</span></span>

## <a name="data-in-the-header-of-an-asf-file"></a><span data-ttu-id="62cac-153">Dados no cabeçalho de um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="62cac-153">Data in the Header of an ASF File</span></span>

<span data-ttu-id="62cac-154">O gravador pega as informações do perfil e as usa para criar os fluxos que vão para a seção de dados do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="62cac-154">The writer takes the information from the profile and uses it to create the streams that go into the data section of the ASF file.</span></span> <span data-ttu-id="62cac-155">A massa dos dados do perfil é armazenada na seção de cabeçalho do arquivo quando um arquivo é gravado.</span><span class="sxs-lookup"><span data-stu-id="62cac-155">The bulk of the profile data is stored in the header section of the file when a file is written.</span></span> <span data-ttu-id="62cac-156">Na reprodução, o objeto leitor (ou o objeto leitor síncrono) pode acessar as informações no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="62cac-156">At playback, the reader object (or the synchronous reader object) can access the information in the header of the file.</span></span> <span data-ttu-id="62cac-157">Nesse caso, o objeto de leitura cria um objeto de perfil e o popula com os dados do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="62cac-157">In this case, the reading object creates a profile object and populates it with the data from the header.</span></span>

<span data-ttu-id="62cac-158">Ao acessar os dados de perfil usando o leitor (ou leitor síncrono), você pode fazer alterações nas informações de perfil, mas não há como aplicar essas alterações ao arquivo no leitor.</span><span class="sxs-lookup"><span data-stu-id="62cac-158">When you access the profile data by using the reader (or synchronous reader), you can make changes to the profile information, but there is no way to apply those changes to the file in the reader.</span></span> <span data-ttu-id="62cac-159">Você pode aplicar as informações de perfil de um arquivo em um leitor a um perfil em um gravador para criar um novo arquivo com as mesmas configurações do arquivo no leitor.</span><span class="sxs-lookup"><span data-stu-id="62cac-159">You can apply the profile information from a file in a reader to a profile in a writer to create a new file with the same settings as the file in the reader.</span></span> <span data-ttu-id="62cac-160">Nesse caso, quaisquer alterações feitas nas informações de perfil antes de definir o perfil no gravador serão refletidas nas informações de perfil registradas pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="62cac-160">In this case, any changes you make to the profile information prior to setting the profile in the writer will be reflected in the profile information registered by the writer.</span></span>

## <a name="using-profile-editor"></a><span data-ttu-id="62cac-161">Usando o editor de perfil</span><span class="sxs-lookup"><span data-stu-id="62cac-161">Using Profile Editor</span></span>

<span data-ttu-id="62cac-162">Em vez de criar perfis usando o Windows Media Format SDK, você pode usar o editor de perfil, um utilitário que está incluído no codificador de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="62cac-162">Rather than creating profiles by using the Windows Media Format SDK, you can use Profile Editor, a utility that is included with Windows Media Encoder.</span></span> <span data-ttu-id="62cac-163">No seu aplicativo de codificação, use o método **IWMProfileManager:: LoadProfileByData** para carregar o perfil salvo.</span><span class="sxs-lookup"><span data-stu-id="62cac-163">In your encoding application, use the **IWMProfileManager::LoadProfileByData** method to load the saved profile.</span></span> <span data-ttu-id="62cac-164">Em alguns cenários, por exemplo, se você usar um número limitado de perfis que nunca são modificados dinamicamente, talvez seja mais conveniente usar o editor de perfil para criar seus perfis.</span><span class="sxs-lookup"><span data-stu-id="62cac-164">In some scenarios, for example if you use a limited number of profiles that are never modified dynamically, it might be more convenient to use the Profile Editor to create your profiles.</span></span>

<span data-ttu-id="62cac-165">No entanto, se você usar o editor de perfil, é recomendável não usar a configuração "tamanho do vídeo: igual à entrada de vídeo".</span><span class="sxs-lookup"><span data-stu-id="62cac-165">However, if you do use Profile Editor, it is recommended that you do not use the "Video Size: Same As Video Input" setting.</span></span> <span data-ttu-id="62cac-166">Quando essa caixa de seleção estiver marcada, o editor de perfil criará um perfil com a altura e a largura de saída do vídeo definida como zero.</span><span class="sxs-lookup"><span data-stu-id="62cac-166">When this check box is checked, Profile Editor will create a profile with the video output height and width set to zero.</span></span> <span data-ttu-id="62cac-167">Quando o codificador do Windows Media encontra esses perfis, ele define os valores corretos para corresponder à entrada de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62cac-167">When Windows Media Encoder encounters these profiles, it sets the correct values to match its video input.</span></span> <span data-ttu-id="62cac-168">No entanto, o gravador no Windows Media Format SDK não faz isso automaticamente, portanto, você deve garantir que seu aplicativo defina o tamanho do quadro de vídeo em casos em que o perfil tenha nenhum.</span><span class="sxs-lookup"><span data-stu-id="62cac-168">However, the Writer in the Windows Media Format SDK does not do so automatically, so you must ensure that your application sets the video frame size in cases where the profile has none.</span></span>

<span data-ttu-id="62cac-169">**Observação** Alguns itens de configuração de fluxo não são armazenados no perfil.</span><span class="sxs-lookup"><span data-stu-id="62cac-169">**Note** Some stream configuration items are not stored in the profile.</span></span> <span data-ttu-id="62cac-170">Os dados no perfil descrevem o formato do arquivo ASF concluído.</span><span class="sxs-lookup"><span data-stu-id="62cac-170">The data in the profile describes the format of the finished ASF file.</span></span> <span data-ttu-id="62cac-171">As propriedades de mídia de entrada e outros dados de configuração usados pelo objeto gravador para configurar os codecs não são salvos no perfil.</span><span class="sxs-lookup"><span data-stu-id="62cac-171">Input media properties and other configuration data used by the writer object to configure the codecs are not saved in the profile.</span></span> <span data-ttu-id="62cac-172">Isso inclui todas as propriedades definidas usando o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="62cac-172">This includes all properties set by using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62cac-173">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62cac-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62cac-174">**Objeto de compartilhamento de largura de banda**</span><span class="sxs-lookup"><span data-stu-id="62cac-174">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="62cac-175">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="62cac-175">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="62cac-176">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="62cac-176">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="62cac-177">**Interface IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="62cac-177">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="62cac-178">**Objeto de exclusão mútua**</span><span class="sxs-lookup"><span data-stu-id="62cac-178">**Mutual Exclusion Object**</span></span>](mutual-exclusion-object.md)
</dt> <dt>

[<span data-ttu-id="62cac-179">**Objeto do gerenciador de perfis**</span><span class="sxs-lookup"><span data-stu-id="62cac-179">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="62cac-180">**Objeto de configuração de fluxo**</span><span class="sxs-lookup"><span data-stu-id="62cac-180">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="62cac-181">**Objeto de priorização de fluxo**</span><span class="sxs-lookup"><span data-stu-id="62cac-181">**Stream Prioritization Object**</span></span>](stream-prioritization-object.md)
</dt> <dt>

[<span data-ttu-id="62cac-182">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="62cac-182">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




