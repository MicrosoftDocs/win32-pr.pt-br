---
title: Usar perfis com o gravador
description: Usar perfis com o gravador
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, gravando arquivos ASF
- SDK do Windows Media Format, criando arquivos ASF
- SDK do Windows Media Format, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), gravando arquivos
- ASF (formato de sistemas avançados), gravando arquivos
- ASF (Advanced Systems Format), criando arquivos
- ASF (formato de sistemas avançados), criando arquivos
- perfis, criando arquivos ASF
- perfis, gravando arquivos ASF
- perfis, criação de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007233"
---
# <a name="to-use-profiles-with-the-writer"></a><span data-ttu-id="9ae66-113">Usar perfis com o gravador</span><span class="sxs-lookup"><span data-stu-id="9ae66-113">To Use Profiles with the Writer</span></span>

<span data-ttu-id="9ae66-114">O gravador usa dados de perfil para criar arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="9ae66-114">The writer uses profile data to create ASF files.</span></span> <span data-ttu-id="9ae66-115">Você deve especificar um perfil para uso antes de fazer qualquer outra coisa com o gravador.</span><span class="sxs-lookup"><span data-stu-id="9ae66-115">You must specify a profile for use before doing anything else with the writer.</span></span>

<span data-ttu-id="9ae66-116">Você pode definir um perfil do sistema para uso com o gravador passando a ID do perfil para o método [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .</span><span class="sxs-lookup"><span data-stu-id="9ae66-116">You can set a system profile for use with the writer by passing the profile ID to the [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) method.</span></span>

<span data-ttu-id="9ae66-117">Para especificar um perfil personalizado para uso com o gravador, você deve obter uma interface [**IWMProfile**](iwmprofile.md) para um objeto que contém os dados de perfil desejados.</span><span class="sxs-lookup"><span data-stu-id="9ae66-117">To specify a custom profile for use with the writer, you must obtain an [**IWMProfile**](iwmprofile.md) interface to an object containing the desired profile data.</span></span> <span data-ttu-id="9ae66-118">Você pode usar um dos métodos de carregamento da interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="9ae66-118">You can use one of the loading methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface to accomplish this.</span></span> <span data-ttu-id="9ae66-119">Depois de ter uma interface **IWMProfile** válida, você pode passar um ponteiro para ele para o método [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) .</span><span class="sxs-lookup"><span data-stu-id="9ae66-119">After you have a valid **IWMProfile** interface, you can pass a pointer to it to the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method.</span></span> <span data-ttu-id="9ae66-120">Para obter mais informações sobre configurações de perfil, consulte [trabalhando com perfis](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="9ae66-120">For more information about profile settings, see [Working with Profiles](working-with-profiles.md).</span></span>

<span data-ttu-id="9ae66-121">Se você fizer alterações no objeto de perfil usando a interface **IWMProfile** depois de definir o perfil no gravador, deverá chamar **setprofile** novamente ou as alterações não serão refletidas no gravador.</span><span class="sxs-lookup"><span data-stu-id="9ae66-121">If you make changes to the profile object by using the **IWMProfile** interface after setting the profile in the writer, you must call **SetProfile** again, or else the changes will not be reflected in the writer.</span></span> <span data-ttu-id="9ae66-122">No entanto, chamar **Setprofile** redefinirá todos os atributos de cabeçalho, portanto, certifique-se de definir todos os atributos de cabeçalho necessários depois de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="9ae66-122">However, calling **SetProfile** will reset all header attributes, so be sure to set any required header attributes after calling this method.</span></span>

<span data-ttu-id="9ae66-123">A função de exemplo a seguir define o perfil como "Windows Media Video 8 para modems dial-up (56 Kbps)":</span><span class="sxs-lookup"><span data-stu-id="9ae66-123">The following example function sets the profile to "Windows Media Video 8 for Dial-up Modems (56 Kbps)":</span></span>


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> <span data-ttu-id="9ae66-124">Não há nenhum perfil de sistema predefinido que use os codecs de áudio do Windows Media e vídeo 9 Series.</span><span class="sxs-lookup"><span data-stu-id="9ae66-124">There are no predefined system profiles that use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="9ae66-125">Para obter mais informações, consulte [reutilizando configurações de fluxo](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9ae66-125">For more information, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9ae66-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ae66-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae66-127">**IWMWriter::SetProfileByID**</span><span class="sxs-lookup"><span data-stu-id="9ae66-127">**IWMWriter::SetProfileByID**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[<span data-ttu-id="9ae66-128">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="9ae66-128">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> <dt>

[<span data-ttu-id="9ae66-129">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="9ae66-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




