---
title: Aquisição de licença não silenciosa
description: Aquisição de licença não silenciosa
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- SDK do Windows Media Format, aquisição de licença não silenciosa
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), aquisição de licença não silenciosa
- DRM (gerenciamento de direitos digitais), aquisição de licença não silenciosa
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, aquisição de licença não silenciosa
- APIs estendidas do cliente, aquisição de licença não silenciosa
- aquisição de licença não silenciosa
- licenças, aquisição de licença não silenciosa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498800"
---
# <a name="non-silent-license-acquisition"></a><span data-ttu-id="98d30-113">Aquisição de licença não silenciosa</span><span class="sxs-lookup"><span data-stu-id="98d30-113">Non-Silent License Acquisition</span></span>

<span data-ttu-id="98d30-114">A aquisição de licença não silenciosa permite que o provedor de licenças interaja com o usuário final por meio de uma página da Web, como uma etapa intermediária no processo de aquisição de licença.</span><span class="sxs-lookup"><span data-stu-id="98d30-114">Non-silent license acquisition enables the license provider to interact with the end user through a Web page, as an intermediate step in the license acquisition process.</span></span> <span data-ttu-id="98d30-115">A aquisição de licença não silenciosa é iniciada em resposta a um usuário que está tentando acessar o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="98d30-115">Non-silent license acquisition is initiated in response to a user trying to access protected content.</span></span>

<span data-ttu-id="98d30-116">Para executar a aquisição de licença não silenciosa, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="98d30-116">To perform non-silent license acquisition, use the following steps:</span></span>

1.  <span data-ttu-id="98d30-117">Chame o método [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="98d30-117">Call the [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span> <span data-ttu-id="98d30-118">Passe o cabeçalho DRM do arquivo protegido como o parâmetro *bstrHeaderData* .</span><span class="sxs-lookup"><span data-stu-id="98d30-118">Pass in the DRM header from the protected file as the *bstrHeaderData* parameter.</span></span> <span data-ttu-id="98d30-119">Especifique quais direitos você deseja que a licença conceda no parâmetro *bstrActions* .</span><span class="sxs-lookup"><span data-stu-id="98d30-119">Specify what rights you want the license to grant in the *bstrActions* parameter.</span></span> <span data-ttu-id="98d30-120">Por fim, defina o parâmetro *dwFlags* como WMDRM \_ adquirir licença não \_ \_ silenciosa.</span><span class="sxs-lookup"><span data-stu-id="98d30-120">Finally, set the *dwFlags* parameter to WMDRM\_ACQUIRE\_LICENSE\_NONSILENT.</span></span>
2.  <span data-ttu-id="98d30-121">Interceptar eventos para a interface **IWMDRMLicenseManagement** .</span><span class="sxs-lookup"><span data-stu-id="98d30-121">Trap events for the **IWMDRMLicenseManagement** interface.</span></span> <span data-ttu-id="98d30-122">Quando você receber o evento **MEWMDRMLicenseAcquisitionCompleted** , obtenha seu valor associado chamando **IMFMediaEvent:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="98d30-122">When you receive the **MEWMDRMLicenseAcquisitionCompleted** event, get its associated value by calling **IMFMediaEvent::GetValue**.</span></span> <span data-ttu-id="98d30-123">O valor deve ser do tipo VT \_ desconhecido, um ponteiro para uma interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="98d30-123">The value should be of type VT\_UNKNOWN, a pointer to an **IUnknown** interface.</span></span>
3.  <span data-ttu-id="98d30-124">Chame o método **QueryInterface** da interface **IUnknown** recuperada na etapa 2 para obter a interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="98d30-124">Call the **QueryInterface** method of the **IUnknown** interface retrieved in step 2 to get the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>
4.  <span data-ttu-id="98d30-125">Chame [**IWMDRMNonSilentLicenseAquisition:: Getdesafiator**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) para recuperar o desafio de licença.</span><span class="sxs-lookup"><span data-stu-id="98d30-125">Call [**IWMDRMNonSilentLicenseAquisition::GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) to retrieve the license challenge.</span></span> <span data-ttu-id="98d30-126">Além disso, chame [**IWMDRMNonSilentLicenseAquisition:: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) se você ainda não tiver a URL do servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="98d30-126">Also call [**IWMDRMNonSilentLicenseAquisition::GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) if you do not have the URL of the license server already.</span></span>
5.  <span data-ttu-id="98d30-127">Envie o desafio para a página da Web especificada pela URL.</span><span class="sxs-lookup"><span data-stu-id="98d30-127">Send the challenge to the Web page specified by the URL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98d30-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98d30-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98d30-129">**Adquirindo licenças**</span><span class="sxs-lookup"><span data-stu-id="98d30-129">**Acquiring Licenses**</span></span>](acquiring-licenses.md)
</dt> <dt>

[<span data-ttu-id="98d30-130">**Usando o modelo de evento Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="98d30-130">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> </dl>

 

 




