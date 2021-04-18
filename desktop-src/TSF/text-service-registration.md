---
title: Registro do serviço de texto
description: Além das entradas de registro de servidor no proc padrão, um serviço de texto deve se registrar com a TSF (estrutura de serviços de texto) para que possa estar disponível para uso com um aplicativo.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- TSF (estrutura de serviços de texto), registro
- TSF (estrutura de serviços de texto), registro
- serviços de texto, registro
- TSF (estrutura de serviços de texto), perfis de idioma
- TSF (estrutura de serviços de texto), perfis de idioma
- serviços de texto, perfis de idioma
- TSF (estrutura de serviços de texto), categorias
- TSF (estrutura de serviços de texto), categorias
- serviços de texto, categorias
- registrando serviços de texto
- registrando perfis de idioma
- registrando categorias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454192"
---
# <a name="text-service-registration"></a><span data-ttu-id="0f8e6-115">Registro do serviço de texto</span><span class="sxs-lookup"><span data-stu-id="0f8e6-115">Text Service Registration</span></span>

<span data-ttu-id="0f8e6-116">Além das entradas de registro de servidor no proc padrão, um serviço de texto deve se registrar com a TSF (estrutura de serviços de texto) para que possa estar disponível para uso com um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-116">In addition to the standard COM in-proc server registry entries, a text service must register itself with the Text Services Framework (TSF) so that it can be available for use with an application.</span></span> <span data-ttu-id="0f8e6-117">O TSF fornece a interface [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) e [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) para simplificar o processo de registro.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-117">TSF supplies the [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) and [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) interface to simplify the registration process.</span></span>

<span data-ttu-id="0f8e6-118">Os provedores de serviço de texto também devem fornecer assinaturas digitais com seus executáveis binários.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-118">Text service providers should also provide digital signatures with their binary executables.</span></span> <span data-ttu-id="0f8e6-119">Consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f8e6-119">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="registering-the-text-service"></a><span data-ttu-id="0f8e6-120">Registrando o serviço de texto</span><span class="sxs-lookup"><span data-stu-id="0f8e6-120">Registering the Text Service</span></span>

<span data-ttu-id="0f8e6-121">Um serviço de texto se registra com o TSF chamando [ITfInputProcessorProfiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) com o identificador de classe do serviço de texto.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-121">A text service registers itself with TSF by calling [ITfInputProcessorProfiles::Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) with the class identifier of the text service.</span></span> <span data-ttu-id="0f8e6-122">Uma instância da interface **ITfInputProcessorProfiles** é obtida chamando **CoCreateInstance** com CLSID \_ TF \_ InputProcessorProfiles.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-122">An instance of the **ITfInputProcessorProfiles** interface is obtained by calling **CoCreateInstance** with CLSID\_TF\_InputProcessorProfiles.</span></span>

<span data-ttu-id="0f8e6-123">O exemplo a seguir demonstra como criar um objeto **ITfInputProcessorProfiles** e registrar o serviço de texto.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-123">The following example demonstrates how to create an **ITfInputProcessorProfiles** object and register the text service.</span></span>


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[<span data-ttu-id="0f8e6-124">ITfInputProcessorProfiles:: cancelar registro</span><span class="sxs-lookup"><span data-stu-id="0f8e6-124">ITfInputProcessorProfiles::Unregister</span></span>](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a><span data-ttu-id="0f8e6-125">Registrando perfis de idioma</span><span class="sxs-lookup"><span data-stu-id="0f8e6-125">Registering Language Profiles</span></span>

<span data-ttu-id="0f8e6-126">Um serviço de texto só está disponível quando um aplicativo tem o foco e o idioma apropriado é selecionado na barra de idiomas.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-126">A text service is only available when an application has the focus and the proper language is selected in the language bar.</span></span> <span data-ttu-id="0f8e6-127">Para facilitar isso, o TSF requer que um serviço de texto se registre em todos os idiomas aos quais ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-127">To facilitate this, TSF requires that a text service register itself for all of the languages that it supports.</span></span> <span data-ttu-id="0f8e6-128">O serviço de texto registra seus perfis de idioma chamando [ITfInputProcessorProfiles:: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) com o identificador de classe de serviço de texto, esse identificador de idioma do perfil e um **GUID** de serviço de texto definido que identifica o perfil de idioma.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-128">The text service registers its language profiles by calling [ITfInputProcessorProfiles::AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) with the text service class identifier, that language identifier of the profile, and a text service defined **GUID** that identifies the language profile.</span></span>

<span data-ttu-id="0f8e6-129">Um perfil de idioma pode ser removido chamando [ITfInputProcessorProfiles:: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span><span class="sxs-lookup"><span data-stu-id="0f8e6-129">A language profile can be removed by calling [ITfInputProcessorProfiles::RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span></span> <span data-ttu-id="0f8e6-130">**ITfInputProcessorProfiles:: Unregister** remove todos os perfis de idioma para o serviço de texto; Quando um serviço de texto é desinstalado, ele requer a remoção dos perfis de idioma individuais.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-130">**ITfInputProcessorProfiles::Unregister** removes all language profiles for the text service; when a text service is uninstalled, it does require removal of the individual language profiles.</span></span>

## <a name="registering-categories"></a><span data-ttu-id="0f8e6-131">Registrando categorias</span><span class="sxs-lookup"><span data-stu-id="0f8e6-131">Registering Categories</span></span>

<span data-ttu-id="0f8e6-132">Um serviço de texto também deve registrar a categoria à qual o serviço de texto se aplica.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-132">A text service must also register the category that the text service applies to.</span></span> <span data-ttu-id="0f8e6-133">Por exemplo, se o serviço de texto fornece informações de atributo de exibição, ele deve se registrar como um provedor de atributo de exibição chamando [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) com o identificador de classe do serviço de texto para o primeiro parâmetro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER para o segundo parâmetro e o identificador de classe do serviço de texto novamente para o terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-133">For example, if the text service supplies display attribute information, it must register itself as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span> <span data-ttu-id="0f8e6-134">As categorias possíveis são listadas em [valores de categoria predefinidos](predefined-category-values.md).</span><span class="sxs-lookup"><span data-stu-id="0f8e6-134">The possible categories are listed under [Predefined Category Values](predefined-category-values.md).</span></span>

<span data-ttu-id="0f8e6-135">Remova as categorias registradas anteriormente chamando [ITfCategoryMgr:: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span><span class="sxs-lookup"><span data-stu-id="0f8e6-135">Remove previously registered categories by calling [ITfCategoryMgr::UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span></span> <span data-ttu-id="0f8e6-136">ITfInputProcessorProfiles:: Unregister remove todas as categorias para o serviço de texto; Quando um serviço de texto é desinstalado, ele deve remover as categorias individuais.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-136">ITfInputProcessorProfiles::Unregister removes all categories for the text service; when a text service is uninstalled, it must remove the individual categories.</span></span>

 

 