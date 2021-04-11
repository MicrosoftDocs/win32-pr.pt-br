---
title: Protegendo arquivos com DRM versão 1
description: Protegendo arquivos com DRM versão 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- SDK do Windows Media Format, criando arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), criando arquivos protegidos
- ASF (formato de sistemas avançados), criando arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (formato de sistemas avançados), WMStubDRM. lib
- WMStubDRM. lib, criando arquivos protegidos
- WMStubDRM. lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104293853"
---
# <a name="protecting-files-with-drm-version-1"></a><span data-ttu-id="183b0-115">Protegendo arquivos com DRM versão 1</span><span class="sxs-lookup"><span data-stu-id="183b0-115">Protecting Files with DRM Version 1</span></span>

<span data-ttu-id="183b0-116">Quando esse tipo de proteção é aplicado, é gerada uma licença do DRM versão 1 que é válida somente no computador do qual a solicitação de licença foi feita.</span><span class="sxs-lookup"><span data-stu-id="183b0-116">When this kind of protection is applied, a DRM version 1 license is generated that is valid only on the machine from which the license request was made.</span></span> <span data-ttu-id="183b0-117">Como nenhuma semente de chave ou chave está definida, não há como gerar licenças portáteis para conteúdo protegido usando essa técnica.</span><span class="sxs-lookup"><span data-stu-id="183b0-117">Because no key or key seed is set, there is no way to generate portable licenses for content protected using this technique.</span></span> <span data-ttu-id="183b0-118">No entanto, ao usar o Windows Media Format SDK 7,1 ou posterior, as licenças são recuperáveis no serviço de migração de licença da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="183b0-118">However, when using the Windows Media Format SDK 7.1 or later, the licenses are recoverable at the Microsoft License Migration service.</span></span>

<span data-ttu-id="183b0-119">Para proteger os arquivos ASF usando o DRM versão 1, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="183b0-119">To protect ASF files using DRM version 1, perform the following steps:</span></span>

1.  <span data-ttu-id="183b0-120">Vincule o arquivo WMStubDRM. lib ao seu projeto e, se necessário, desvincule o WMVCORE. lib.</span><span class="sxs-lookup"><span data-stu-id="183b0-120">Link the WMStubDRM.lib file to your project and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="183b0-121">Chame a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para criar o gravador.</span><span class="sxs-lookup"><span data-stu-id="183b0-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the writer.</span></span> <span data-ttu-id="183b0-122">O primeiro argumento é reservado e deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="183b0-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="183b0-123">Defina um perfil para o gravador a ser usado chamando [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span><span class="sxs-lookup"><span data-stu-id="183b0-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="183b0-124">Você deve definir um perfil no gravador antes de definir qualquer atributo DRM.</span><span class="sxs-lookup"><span data-stu-id="183b0-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="183b0-125">Somente há suporte para DRM para perfis que usam os codecs de vídeo do Windows Media Audio ou Windows Media.</span><span class="sxs-lookup"><span data-stu-id="183b0-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs.</span></span>
4.  <span data-ttu-id="183b0-126">Usando o método [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , defina as seguintes propriedades de DRM.</span><span class="sxs-lookup"><span data-stu-id="183b0-126">Using the [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) method, set the following DRM properties.</span></span> <span data-ttu-id="183b0-127">A propriedade **usar \_ DRM** INSTRUI os componentes DRM para proteger o conteúdo usando o DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="183b0-127">The **Use\_DRM** property instructs the DRM components to protect the content using DRM version 1.</span></span> <span data-ttu-id="183b0-128">A propriedade de **\_ sinalizadores DRM** especifica os direitos a serem incluídos na licença local que será criada para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="183b0-128">The **DRM\_Flags** property specifies the rights to be included in the local license that will be created for the content.</span></span> <span data-ttu-id="183b0-129">O valor de **\_ nível de DRM** também é armazenado na licença; ele especifica o nível mínimo necessário para acessar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="183b0-129">The **DRM\_LEVEL** value is also stored in the license; it specifies the minimum level required to access the content.</span></span> <span data-ttu-id="183b0-130">150 é o nível recomendado para conteúdo DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="183b0-130">150 is the recommended level for DRM version 1 content.</span></span>

    | <span data-ttu-id="183b0-131">Atributo</span><span class="sxs-lookup"><span data-stu-id="183b0-131">Attribute</span></span>      | <span data-ttu-id="183b0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="183b0-132">Value</span></span>                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | <span data-ttu-id="183b0-133">**Usar \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="183b0-133">**Use\_DRM**</span></span>   | <span data-ttu-id="183b0-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="183b0-134">**TRUE**</span></span>                                                                                    |
    | <span data-ttu-id="183b0-135">**Sinalizadores de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="183b0-135">**DRM\_Flags**</span></span> | <span data-ttu-id="183b0-136">WMT \_ de \_ reprodução \| direita \_ WMT \_ copiar \_ para \_ \_ dispositivo não \_ SDMI \| WMT \_ copiar à direita \_ \_ para \_ CD</span><span class="sxs-lookup"><span data-stu-id="183b0-136">WMT\_RIGHT\_PLAYBACK \| WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE \| WMT\_RIGHT\_COPY\_TO\_CD</span></span> |
    | <span data-ttu-id="183b0-137">**nível de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="183b0-137">**DRM\_LEVEL**</span></span> | <span data-ttu-id="183b0-138">150</span><span class="sxs-lookup"><span data-stu-id="183b0-138">150</span></span>                                                                                         |

    

     

<span data-ttu-id="183b0-139">O código de exemplo a seguir mostra como criar um gravador habilitado para DRM para DRM versão 1 e definir as propriedades de DRM.</span><span class="sxs-lookup"><span data-stu-id="183b0-139">The following example code shows how to create a DRM-enabled writer for DRM version 1 and set the DRM properties.</span></span> <span data-ttu-id="183b0-140">A verificação de erros foi omitida por questão de Clarify.</span><span class="sxs-lookup"><span data-stu-id="183b0-140">Error checking has been omitted for the sake of clarify.</span></span>


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




