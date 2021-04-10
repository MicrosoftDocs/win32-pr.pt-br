---
title: Verificação e inicialização
description: Verificação e inicialização
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- SDK do Windows Media Format, verificação
- SDK do Windows Media Format, inicialização
- DRM (gerenciamento de direitos digitais), verificação
- DRM (gerenciamento de direitos digitais), verificação
- DRM (gerenciamento de direitos digitais), inicialização
- DRM (gerenciamento de direitos digitais), inicialização
- APIs estendidas do cliente DRM, verificação
- APIs estendidas do cliente, verificação
- APIs estendidas do cliente DRM, inicialização
- APIs estendidas do cliente, inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293784"
---
# <a name="verification-and-initialization"></a><span data-ttu-id="48014-113">Verificação e inicialização</span><span class="sxs-lookup"><span data-stu-id="48014-113">Verification and Initialization</span></span>

<span data-ttu-id="48014-114">Você deve executar as seguintes etapas para verificar se a criptografia é permitida e inicializar um objeto que descriptografará o conteúdo:</span><span class="sxs-lookup"><span data-stu-id="48014-114">You should perform the following steps to verify that transcryption is allowed and to initialize an object that will decrypt the content:</span></span>

1.  <span data-ttu-id="48014-115">Se você já tiver a ID de chave para o conteúdo, pule para a etapa 5.</span><span class="sxs-lookup"><span data-stu-id="48014-115">If you already have the Key ID for the content, skip to step 5.</span></span>
2.  <span data-ttu-id="48014-116">Chame a função [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) para criar um objeto do editor de metadados e obter uma instância da interface [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) do objeto.</span><span class="sxs-lookup"><span data-stu-id="48014-116">Call the [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) function to create a metadata editor object and get an instance of that object's [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) interface.</span></span>
3.  <span data-ttu-id="48014-117">Chame **IWMMetadataEditor:: QueryInterface** para obter uma instância da interface [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .</span><span class="sxs-lookup"><span data-stu-id="48014-117">Call **IWMMetadataEditor::QueryInterface** to get an instance of the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface.</span></span>
4.  <span data-ttu-id="48014-118">Chame [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) para obter a propriedade de **\_ \_ keyid DRMHeader do DRM** .</span><span class="sxs-lookup"><span data-stu-id="48014-118">Call [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) to get the **DRM\_DRMHeader\_KeyID** property.</span></span>
5.  <span data-ttu-id="48014-119">Inicialize as APIs estendidas do cliente DRM do Windows Media chamando a função [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="48014-119">Initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>
6.  <span data-ttu-id="48014-120">Chame a função [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) para criar um objeto de provedor seguro e obter uma instância da interface [**IWMDRMProvider**](iwmdrmprovider.md) do objeto.</span><span class="sxs-lookup"><span data-stu-id="48014-120">Call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function to create a secure provider object and get an instance of that object's [**IWMDRMProvider**](iwmdrmprovider.md) interface.</span></span>
7.  <span data-ttu-id="48014-121">Chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md) para criar um objeto de gerenciamento de licença e obter uma instância de sua interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="48014-121">Call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md) to create a license management object and get an instance of its [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span>
8.  <span data-ttu-id="48014-122">Chame [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando a ID da chave e a direita que governa as ações a serem tomadas com o conteúdo depois que ele é criptografado.</span><span class="sxs-lookup"><span data-stu-id="48014-122">Call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing in the Key ID and the right that governs the actions to be taken with the content after it is transcrypted.</span></span> <span data-ttu-id="48014-123">Essa chamada recuperará uma instância da interface [**IWMDRMLicense**](iwmdrmlicense.md) que pode ser usada para enumerar por meio de qualquer licença correspondente.</span><span class="sxs-lookup"><span data-stu-id="48014-123">This call will retrieve an instance of the [**IWMDRMLicense**](iwmdrmlicense.md) interface that can be used to enumerate through any matching licenses.</span></span>
9.  <span data-ttu-id="48014-124">Chame [**IWMDRMLicense:: inclusionlist**](iwmdrmlicense-getinclusionlist.md) para recuperar a lista de CPS (sistemas de proteção de conteúdo) autorizados conforme especificado pelo emissor da licença.</span><span class="sxs-lookup"><span data-stu-id="48014-124">Call [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) to retrieve the list of authorized content protection systems (CPS) as specified by the license issuer.</span></span>
10. <span data-ttu-id="48014-125">Analise a lista de inclusão para confirmar se o GUID da saída CPS é permitido pela licença.</span><span class="sxs-lookup"><span data-stu-id="48014-125">Parse the inclusion list to confirm that the GUID of the output CPS is allowed by the license.</span></span>
11. <span data-ttu-id="48014-126">Se o GUID de exportação desejado não estiver na lista de inclusão, chame [**IWMDRMLicense:: GetNext**](iwmdrmlicense-getnext.md) para obter a próxima licença aplicável (se houver) e repita as etapas 9 e 10.</span><span class="sxs-lookup"><span data-stu-id="48014-126">If the desired export GUID is not in the inclusion list, call [**IWMDRMLicense::GetNext**](iwmdrmlicense-getnext.md) to get the next applicable license (if any) and repeat steps 9 and 10.</span></span> <span data-ttu-id="48014-127">Se nenhuma licença tiver o GUID desejado em sua lista de inclusão, a exportação não poderá ser executada.</span><span class="sxs-lookup"><span data-stu-id="48014-127">If no license has the desired GUID in its inclusion list, the export cannot be performed.</span></span>
12. <span data-ttu-id="48014-128">Chame [**IWMDRMLicense:: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) para criar um objeto de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="48014-128">Call [**IWMDRMLicense::CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) to create a decryptor object.</span></span> <span data-ttu-id="48014-129">Passe o certificado de aplicativo de exportação.</span><span class="sxs-lookup"><span data-stu-id="48014-129">Pass in the export application certificate.</span></span> <span data-ttu-id="48014-130">Essa chamada fornecerá um ponteiro para uma instância da interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto decodificador e um objeto binário que contém a semente.</span><span class="sxs-lookup"><span data-stu-id="48014-130">This call will provide a pointer to an instance of the decryptor object's [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface and a binary object containing the seed.</span></span> <span data-ttu-id="48014-131">Somente o tipo de proteção do Windows Media DRM Constant é compatível como um argumento para o parâmetro *dwFlags* no momento. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48014-131">Only the Windows Media **DRM\_PROTECTION\_TYPE\_RC4** constant is supported as an argument to the *dwFlags* parameter at this time.</span></span>
13. <span data-ttu-id="48014-132">Use o esquema de criptografia RSA OAEP para descriptografar o vetor de inicialização.</span><span class="sxs-lookup"><span data-stu-id="48014-132">Use the RSA OAEP encryption scheme to decrypt the initialization vector.</span></span>
14. <span data-ttu-id="48014-133">Use a biblioteca de análise de ASF fornecida pela Microsoft quando você entra no contrato de exportação do DRM do Windows Media, para localizar o deslocamento em bytes para cada carga.</span><span class="sxs-lookup"><span data-stu-id="48014-133">Use the ASF parsing library provided by Microsoft when you enter into the Windows Media DRM export agreement, to locate the offset in bytes for each payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48014-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48014-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48014-135">**Exportando conteúdo compactado**</span><span class="sxs-lookup"><span data-stu-id="48014-135">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




