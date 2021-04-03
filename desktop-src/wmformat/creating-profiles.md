---
title: Criando perfis
description: Criando perfis
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- SDK do Windows Media Format, perfis
- perfis, criando
- perfis, interface IWMProfileManager
- IWMProfileManager, criando perfis
- perfis, função WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007083"
---
# <a name="creating-profiles"></a><span data-ttu-id="d5c58-109">Criando perfis</span><span class="sxs-lookup"><span data-stu-id="d5c58-109">Creating Profiles</span></span>

<span data-ttu-id="d5c58-110">Em muitos casos, você desejará criar um perfil vazio para configurar suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="d5c58-110">In many cases, you will want to create an empty profile to configure for your needs.</span></span> <span data-ttu-id="d5c58-111">Em outros casos, é mais fácil editar um perfil existente, como um perfil do sistema.</span><span class="sxs-lookup"><span data-stu-id="d5c58-111">In other cases it is easier to edit an existing profile, like a system profile.</span></span> <span data-ttu-id="d5c58-112">Para obter mais informações sobre como usar perfis de sistema, consulte [usando perfis de sistema](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="d5c58-112">For more information about using system profiles, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="d5c58-113">A criação de um perfil vazio, pronto para configuração, requer um objeto do Gerenciador de perfis.</span><span class="sxs-lookup"><span data-stu-id="d5c58-113">Creating an empty profile, ready for you to configure, requires a profile manager object.</span></span> <span data-ttu-id="d5c58-114">Para obter a interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de um objeto do Gerenciador de perfis, chame a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="d5c58-114">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>

<span data-ttu-id="d5c58-115">Para criar um perfil vazio, chame [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span><span class="sxs-lookup"><span data-stu-id="d5c58-115">To create an empty profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span> <span data-ttu-id="d5c58-116">Quando você cria um perfil vazio, a única coisa que você especifica é a versão do SDK do Windows Media Format com a qual o perfil está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="d5c58-116">When you create an empty profile, the only thing you specify is the version of the Windows Media Format SDK with which the profile complies.</span></span> <span data-ttu-id="d5c58-117">A menos que você tenha uma necessidade específica de usar uma versão anterior, você sempre deve usar a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="d5c58-117">Unless you have a specific need to use a previous version, you should always use the latest version.</span></span> <span data-ttu-id="d5c58-118">A versão determina a estrutura do perfil; as versões anteriores não davam suporte a algumas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d5c58-118">The version dictates the structure of the profile; previous versions did not support some properties.</span></span>

<span data-ttu-id="d5c58-119">O código de exemplo a seguir mostra como criar um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="d5c58-119">The following example code shows how to create a new profile.</span></span> <span data-ttu-id="d5c58-120">Para compilar esse código em seu aplicativo, inclua stdio. h.</span><span class="sxs-lookup"><span data-stu-id="d5c58-120">To compile this code in your application, include stdio.h.</span></span> <span data-ttu-id="d5c58-121">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="d5c58-121">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="d5c58-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5c58-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5c58-123">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="d5c58-123">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="d5c58-124">**Interface IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="d5c58-124">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="d5c58-125">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="d5c58-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




