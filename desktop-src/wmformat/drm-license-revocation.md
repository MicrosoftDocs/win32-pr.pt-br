---
title: Revogação de licença (cliente Microsoft Windows Media DRM)
description: Revogação de licença (cliente Microsoft Windows Media DRM)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- SDK do Windows Media Format, licenças
- SDK do Windows Media Format, revogação de licença
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), revogação de licença
- DRM (gerenciamento de direitos digitais), revogação de licença
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, revogação de licença
- APIs estendidas do cliente, revogação de licença
- licenças, revogação
- revogação de licença, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172416"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a><span data-ttu-id="aadf1-115">Revogação de licença (cliente Microsoft Windows Media DRM)</span><span class="sxs-lookup"><span data-stu-id="aadf1-115">License Revocation (Microsoft Windows Media DRM Client)</span></span>

<span data-ttu-id="aadf1-116">A revogação de licença refere-se à remoção de licenças de um repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="aadf1-116">License revocation refers to the removal of licenses from a local license store.</span></span> <span data-ttu-id="aadf1-117">Um cenário comum para a revogação de licença ocorre quando um provedor de serviços, como um serviço de assinatura musical, deve desativar o serviço no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="aadf1-117">A common scenario for license revocation occurs when a service provider, such as a music subscription service, must deactivate the service on a user's computer.</span></span>

<span data-ttu-id="aadf1-118">O processo de revogação de licença é iniciado por um serviço fornecido pelo emissor da licença.</span><span class="sxs-lookup"><span data-stu-id="aadf1-118">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="aadf1-119">Seu aplicativo pode hospedar esse serviço ou pode ser um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="aadf1-119">Your application can host this service or it can be a Web application.</span></span> <span data-ttu-id="aadf1-120">Em ambos os casos, seu aplicativo deve ser capaz de receber um desafio de licença criado pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="aadf1-120">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="aadf1-121">Para remover licenças do repositório de licenças, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aadf1-121">To remove licenses from the license store, do the following:</span></span>

1.  <span data-ttu-id="aadf1-122">Após receber um desafio de licença do emissor da licença, crie um desafio de revogação usando o método [**IWMDRMLicenseManagement:: CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .</span><span class="sxs-lookup"><span data-stu-id="aadf1-122">Upon receiving a license challenge from the license issuer, create a revocation challenge using the [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) method.</span></span> <span data-ttu-id="aadf1-123">Esse método alocará um buffer contendo dados de desafio de revogação, que são passados para seu aplicativo por meio do parâmetro *ppbChallengeOutput* .</span><span class="sxs-lookup"><span data-stu-id="aadf1-123">This method will allocate a buffer containing a revocation challenge data, which is passed to your application through the *ppbChallengeOutput* parameter.</span></span>
2.  <span data-ttu-id="aadf1-124">Enviar o desafio de revogação de licença para um serviço de revogação de licença.</span><span class="sxs-lookup"><span data-stu-id="aadf1-124">Send the license revocation challenge to a license revocation service.</span></span> <span data-ttu-id="aadf1-125">O servidor irá gerar um BLOB de revogação de licença (LRB) em resposta.</span><span class="sxs-lookup"><span data-stu-id="aadf1-125">The server will generate a license revocation BLOB (LRB) in response.</span></span>
3.  <span data-ttu-id="aadf1-126">Remova a licença do armazenamento local usando o método [**IWMDRMLicenseManagement::P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , passando o LRB retornado pelo servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="aadf1-126">Remove the license from the local store using the [**IWMDRMLicenseManagement::ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) method, passing the LRB returned by license server.</span></span>
4.  <span data-ttu-id="aadf1-127">Desaloque o buffer alocado por **CreateLicenseRevocationChallenge** usando a função **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="aadf1-127">Deallocate the buffer allocated by **CreateLicenseRevocationChallenge** by using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="aadf1-128">Para obter mais informações sobre como a revogação de licença funciona ou sobre como escrever um serviço de revogação, consulte [implementando a revogação de licenças](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span><span class="sxs-lookup"><span data-stu-id="aadf1-128">For more information on how license revocation works or on how to write a revocation service, see [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aadf1-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aadf1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aadf1-130">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="aadf1-130">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="aadf1-131">**Repositório de licenças local**</span><span class="sxs-lookup"><span data-stu-id="aadf1-131">**Local License Store**</span></span>](local-license-store.md)
</dt> <dt>

[<span data-ttu-id="aadf1-132">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="aadf1-132">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 