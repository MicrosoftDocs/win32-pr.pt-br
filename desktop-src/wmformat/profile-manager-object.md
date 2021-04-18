---
title: Objeto do gerenciador de perfis
description: Objeto do gerenciador de perfis
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- SDK do Windows Media Format, objetos do Gerenciador de perfis
- ASF (Advanced Systems Format), objetos do Gerenciador de perfis
- ASF (formato de sistemas avançados), objetos do Gerenciador de perfis
- objetos, objetos do Gerenciador de perfis
- perfis, objetos
- perfis, objetos do Gerenciador de perfis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105780684"
---
# <a name="profile-manager-object"></a><span data-ttu-id="f2caf-109">Objeto do gerenciador de perfis</span><span class="sxs-lookup"><span data-stu-id="f2caf-109">Profile Manager Object</span></span>

<span data-ttu-id="f2caf-110">Um perfil é um conjunto de parâmetros de mídia usados para criar um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="f2caf-110">A profile is a set of media parameters used to create an ASF file.</span></span> <span data-ttu-id="f2caf-111">O objeto Gerenciador de perfis cria objetos de perfil para edição.</span><span class="sxs-lookup"><span data-stu-id="f2caf-111">The profile manager object creates profile objects for editing.</span></span> <span data-ttu-id="f2caf-112">Os objetos de perfil podem ser criados sem dados ou criados a partir de dados de perfil existentes.</span><span class="sxs-lookup"><span data-stu-id="f2caf-112">Profile objects can be created without any data in them or built from existing profile data.</span></span> <span data-ttu-id="f2caf-113">O objeto Gerenciador de perfis também fornece métodos para enumerar codecs com suporte e consultar esses codecs para obter informações.</span><span class="sxs-lookup"><span data-stu-id="f2caf-113">The profile manager object also provides methods for enumerating supported codecs and querying those codecs for information.</span></span>

<span data-ttu-id="f2caf-114">O objeto Gerenciador de perfis é criado pela função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , que define um ponteiro para uma interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="f2caf-114">The profile manager object is created by the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function, which sets a pointer to an [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="f2caf-115">As outras interfaces do objeto do Gerenciador de perfis podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="f2caf-115">The other interfaces of the profile manager object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="f2caf-116">As interfaces a seguir têm suporte do objeto Gerenciador de perfis.</span><span class="sxs-lookup"><span data-stu-id="f2caf-116">The following interfaces are supported by the profile manager object.</span></span>



| <span data-ttu-id="f2caf-117">Interface</span><span class="sxs-lookup"><span data-stu-id="f2caf-117">Interface</span></span>                                                      | <span data-ttu-id="f2caf-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2caf-118">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2caf-119">**IWMCodecInfo**</span><span class="sxs-lookup"><span data-stu-id="f2caf-119">**IWMCodecInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | <span data-ttu-id="f2caf-120">Recupera informações sobre os codecs com suporte e seus formatos.</span><span class="sxs-lookup"><span data-stu-id="f2caf-120">Retrieves information about supported codecs and their formats.</span></span>                                                                              |
| [<span data-ttu-id="f2caf-121">**IWMCodecInfo2**</span><span class="sxs-lookup"><span data-stu-id="f2caf-121">**IWMCodecInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | <span data-ttu-id="f2caf-122">Recupera os nomes dos codecs com suporte e as descrições de seus formatos.</span><span class="sxs-lookup"><span data-stu-id="f2caf-122">Retrieves the names of the supported codecs and the descriptions of their formats.</span></span> <span data-ttu-id="f2caf-123">Herda todos os métodos de **IWMCodecInfo**.</span><span class="sxs-lookup"><span data-stu-id="f2caf-123">Inherits all of the methods of **IWMCodecInfo**.</span></span>          |
| [<span data-ttu-id="f2caf-124">**IWMCodecInfo3**</span><span class="sxs-lookup"><span data-stu-id="f2caf-124">**IWMCodecInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | <span data-ttu-id="f2caf-125">Recupera as propriedades do codec e os codecs de consultas para recursos com suporte.</span><span class="sxs-lookup"><span data-stu-id="f2caf-125">Retrieves codec properties and queries codecs for supported features.</span></span> <span data-ttu-id="f2caf-126">Herda todos os métodos de **IWMCodecInfo** e **IWMCodecInfo2**.</span><span class="sxs-lookup"><span data-stu-id="f2caf-126">Inherits all of the methods of **IWMCodecInfo** and **IWMCodecInfo2**.</span></span> |
| [<span data-ttu-id="f2caf-127">**IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="f2caf-127">**IWMProfileManager**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | <span data-ttu-id="f2caf-128">Cria novos perfis, carrega perfis existentes e salva perfis personalizados.</span><span class="sxs-lookup"><span data-stu-id="f2caf-128">Creates new profiles, loads existing profiles, and saves custom profiles.</span></span>                                                                    |
| [<span data-ttu-id="f2caf-129">**IWMProfileManager2**</span><span class="sxs-lookup"><span data-stu-id="f2caf-129">**IWMProfileManager2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | <span data-ttu-id="f2caf-130">Controla a versão dos perfis de sistema enumerados pelo Gerenciador de perfis.</span><span class="sxs-lookup"><span data-stu-id="f2caf-130">Controls the version of system profiles enumerated by the profile manager.</span></span> <span data-ttu-id="f2caf-131">Herda todos os métodos de **IWMProfileManager**.</span><span class="sxs-lookup"><span data-stu-id="f2caf-131">Inherits all of the methods of **IWMProfileManager**.</span></span>             |
| [<span data-ttu-id="f2caf-132">**IWMProfileManagerLanguage**</span><span class="sxs-lookup"><span data-stu-id="f2caf-132">**IWMProfileManagerLanguage**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | <span data-ttu-id="f2caf-133">Controla o idioma dos perfis de sistema analisados pelo Gerenciador de perfis.</span><span class="sxs-lookup"><span data-stu-id="f2caf-133">Controls the language of the system profiles parsed by the profile manager.</span></span>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="f2caf-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2caf-134">Remarks</span></span>

<span data-ttu-id="f2caf-135">Quando um objeto do Gerenciador de perfis é criado, ele analisa todos os perfis de sistema, o que pode levar vários segundos.</span><span class="sxs-lookup"><span data-stu-id="f2caf-135">When a profile manager object is created, it parses all of the system profiles, which can take several seconds.</span></span> <span data-ttu-id="f2caf-136">Criar e liberar um Gerenciador de perfis toda vez que você precisar usá-lo afetará negativamente o desempenho.</span><span class="sxs-lookup"><span data-stu-id="f2caf-136">Creating and releasing a profile manager every time you need to use it will adversely affect performance.</span></span> <span data-ttu-id="f2caf-137">Você deve criar um Gerenciador de perfis uma vez no aplicativo e liberá-lo somente quando não precisar mais usá-lo.</span><span class="sxs-lookup"><span data-stu-id="f2caf-137">You should create a profile manager once in your application and release it only when you no longer need to use it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2caf-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2caf-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2caf-139">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="f2caf-139">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="f2caf-140">**Objeto de perfil**</span><span class="sxs-lookup"><span data-stu-id="f2caf-140">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="f2caf-141">**Perfis**</span><span class="sxs-lookup"><span data-stu-id="f2caf-141">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




