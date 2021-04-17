---
title: Criando e inicializando um gravador de DRM
description: Criando e inicializando um gravador de DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- SDK do Windows Media Format, gravadores DRM
- DRM (gerenciamento de direitos digitais), criando gravadores de DRM
- DRM (gerenciamento de direitos digitais), criando gravadores de DRM
- DRM (gerenciamento de direitos digitais), inicializando gravadores DRM
- DRM (gerenciamento de direitos digitais), inicializando gravadores DRM
- APIs estendidas do cliente DRM, gravadores DRM
- APIs estendidas do cliente, gravadores DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105763102"
---
# <a name="creating-and-initializing-a-drm-writer"></a><span data-ttu-id="28571-110">Criando e inicializando um gravador de DRM</span><span class="sxs-lookup"><span data-stu-id="28571-110">Creating and Initializing a DRM Writer</span></span>

<span data-ttu-id="28571-111">As etapas a seguir são necessárias para inicializar um objeto do gravador ASF para importar exemplos de mídia criptografada no Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="28571-111">The following steps are required to initialize an ASF writer object for importing encrypted media samples in Windows Media DRM.</span></span>

1.  <span data-ttu-id="28571-112">Siga as etapas 1 a 4 da [importação de licença e material de chave](importing-license-and-key-material.md).</span><span class="sxs-lookup"><span data-stu-id="28571-112">Follow steps 1 to 4 of [Importing License and Key Material](importing-license-and-key-material.md).</span></span>
2.  <span data-ttu-id="28571-113">Crie e inicialize um objeto do gravador ASF usando o material da chave DRM do Windows Media apropriado.</span><span class="sxs-lookup"><span data-stu-id="28571-113">Create and initialize an ASF writer object using the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="28571-114">Para obter mais informações, consulte [habilitando o suporte a DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="28571-114">For more information, see [Enabling DRM Support](enabling-drm-support.md).</span></span>
3.  <span data-ttu-id="28571-115">Defina cada um dos seguintes atributos chamando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span><span class="sxs-lookup"><span data-stu-id="28571-115">Set each of the following attributes by calling [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span></span>
    -   <span data-ttu-id="28571-116">\_HEADERSIGNPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="28571-116">DRM\_HeaderSignPrivKey</span></span>
    -   <span data-ttu-id="28571-117">\_V1LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="28571-117">DRM\_V1LicenseAcqURL</span></span>
    -   <span data-ttu-id="28571-118">\_Keyid DRM</span><span class="sxs-lookup"><span data-stu-id="28571-118">DRM\_KeyID</span></span>
    -   <span data-ttu-id="28571-119">\_LICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="28571-119">DRM\_LicenseAcqURL</span></span>
4.  <span data-ttu-id="28571-120">Se uma versão licenciada do Windows Media Rights Manager não estiver instalada no computador que executa o software, os quatro atributos a seguir também deverão ser definidos:</span><span class="sxs-lookup"><span data-stu-id="28571-120">If a licensed version of Windows Media Rights Manager is not installed on the computer running your software, then the following four attributes must also be set:</span></span>
    -   <span data-ttu-id="28571-121">\_LASIGNATUREROOTCERT DRM</span><span class="sxs-lookup"><span data-stu-id="28571-121">DRM\_LASignatureRootCert</span></span>
    -   <span data-ttu-id="28571-122">\_LASIGNATURECERT DRM</span><span class="sxs-lookup"><span data-stu-id="28571-122">DRM\_LASignatureCert</span></span>
    -   <span data-ttu-id="28571-123">\_LASIGNATURELICSRVCERT DRM</span><span class="sxs-lookup"><span data-stu-id="28571-123">DRM\_LASignatureLicSrvCert</span></span>
    -   <span data-ttu-id="28571-124">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="28571-124">DRM\_LASignaturePrivKey</span></span>
    -   <span data-ttu-id="28571-125">O aplicativo para os certificados de criptografia necessários pode ser concluído preenchendo o [contrato de licenciamento do Windows Media (WMLA)](https://www.microsoft.com/licensing/default) online.</span><span class="sxs-lookup"><span data-stu-id="28571-125">Application for the necessary encryption certificates can be completed by filling out the [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.</span></span>
5.  <span data-ttu-id="28571-126">Crie uma chave de sessão e preencha uma estrutura de [**\_ chave de \_ sessão \_ de importação WMDRM**](wmdrm-import-session-key.md) .</span><span class="sxs-lookup"><span data-stu-id="28571-126">Create a session key and fill out a [**WMDRM\_IMPORT\_SESSION\_KEY**](wmdrm-import-session-key.md) structure.</span></span> <span data-ttu-id="28571-127">A chave de sessão será usada para criptografar uma chave de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="28571-127">The session key will be used for encrypting a content key.</span></span> <span data-ttu-id="28571-128">Para obter um exemplo, consulte o [exemplo de Create Session Key](create-session-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="28571-128">For an example, see [Create Session Key Example](create-session-key-example.md).</span></span>
6.  <span data-ttu-id="28571-129">Crie uma chave de conteúdo de um vetor de inicialização RC4 aleatório e preencha uma estrutura de [**chave de conteúdo de importação do WMDRM \_ \_ \_**](wmdrm-import-content-key.md) .</span><span class="sxs-lookup"><span data-stu-id="28571-129">Create a content key from a random RC4 initialization vector, and fill out a [**WMDRM\_IMPORT\_CONTENT\_KEY**](wmdrm-import-content-key.md) structure.</span></span> <span data-ttu-id="28571-130">A chave de conteúdo é usada para criptografar os exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="28571-130">The content key is used for encrypting the media samples.</span></span> <span data-ttu-id="28571-131">Para obter um exemplo, consulte [criar exemplo de chave de conteúdo](create-content-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="28571-131">For an example, see [Create Content Key Example](create-content-key-example.md).</span></span>
7.  <span data-ttu-id="28571-132">Criptografe a chave de conteúdo com a chave de sessão usando a criptografia RC4.</span><span class="sxs-lookup"><span data-stu-id="28571-132">Encrypt the content key with the session key, using RC4 encryption.</span></span>
8.  <span data-ttu-id="28571-133">Extraia a chave de coleção de certificados do computador.</span><span class="sxs-lookup"><span data-stu-id="28571-133">Extract the machine certificate collection key.</span></span> <span data-ttu-id="28571-134">Para obter um exemplo, consulte [obter o exemplo de certificado de máquina](get-machine-certificate-example.md).</span><span class="sxs-lookup"><span data-stu-id="28571-134">For an example, see [Get Machine Certificate Example](get-machine-certificate-example.md).</span></span>
9.  <span data-ttu-id="28571-135">Criptografe a chave de sessão com a chave pública extraída do certificado.</span><span class="sxs-lookup"><span data-stu-id="28571-135">Encrypt the session key with the public key extracted from the certificate.</span></span>
10. <span data-ttu-id="28571-136">Preencha uma estrutura [**de \_ \_ \_ struct init de importação do WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="28571-136">Fill out a [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>
11. <span data-ttu-id="28571-137">Chame o método [**IWMDRMWriter3:: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) para notificar o SDK de que as amostras que chegam no gravador já estão protegidas e devem ser enviadas diretamente para o cliente DRM do Windows Media para importação.</span><span class="sxs-lookup"><span data-stu-id="28571-137">Call the [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) method to notify the SDK that samples coming into the writer are already protected and should be sent directly to the Windows Media DRM client for import.</span></span>
12. <span data-ttu-id="28571-138">Chame [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="28571-138">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="28571-139">As etapas restantes para criar um arquivo protegido por DRM são documentadas no guia de programação do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="28571-139">The remaining steps for creating a DRM-protected file are documented in the Windows Media Format SDK Programming Guide.</span></span> <span data-ttu-id="28571-140">Para obter mais informações, consulte [criando arquivos protegidos](creating-protected-files.md).</span><span class="sxs-lookup"><span data-stu-id="28571-140">For more information, see [Creating Protected Files](creating-protected-files.md).</span></span>

<span data-ttu-id="28571-141">A próxima etapa é iterar por meio de cada exemplo de mídia, criptografá-la e passá-la para o objeto do gravador.</span><span class="sxs-lookup"><span data-stu-id="28571-141">The next step is to iterate through each media sample, encrypt it, and pass it to the writer object.</span></span> <span data-ttu-id="28571-142">Para obter mais informações, consulte a [criptografia e a importação de amostras de mídia](encrypting-and-importing-media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="28571-142">For more information, see the [Encrypting and Importing Media Samples](encrypting-and-importing-media-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28571-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28571-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28571-144">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="28571-144">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="28571-145">**Importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="28571-145">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




