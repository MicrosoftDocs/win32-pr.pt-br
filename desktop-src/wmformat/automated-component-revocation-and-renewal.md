---
title: Revogação e renovação de componentes automatizados
description: Revogação e renovação de componentes automatizados
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- SDK do Windows Media Format, revogação e renovação automatizadas
- SDK do Windows Media Format, revogação
- SDK do Windows Media Format, renovação
- DRM (gerenciamento de direitos digitais), revogação automatizada e renovação
- DRM (gerenciamento de direitos digitais), revogação e renovação automatizadas
- DRM (gerenciamento de direitos digitais), revogação
- DRM (gerenciamento de direitos digitais), revogação
- DRM (gerenciamento de direitos digitais), renovação
- DRM (gerenciamento de direitos digitais), renovação
- APIs estendidas do cliente DRM, revogação e renovação automatizadas
- APIs estendidas do cliente, revogação e renovação automatizadas
- APIs estendidas do cliente DRM, revogação
- APIs estendidas do cliente, revogação
- APIs estendidas do cliente DRM, renovação
- APIs estendidas do cliente, renovação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294348"
---
# <a name="automated-component-revocation-and-renewal"></a><span data-ttu-id="a47db-118">Revogação e renovação de componentes automatizados</span><span class="sxs-lookup"><span data-stu-id="a47db-118">Automated Component Revocation and Renewal</span></span>

<span data-ttu-id="a47db-119">Os aplicativos ou componentes de software considerados comprometidos podem ser revogados pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a47db-119">Software applications or components that are considered compromised can be revoked by Microsoft.</span></span> <span data-ttu-id="a47db-120">A API estendida do cliente do Windows Media Format fornece um mecanismo para a revogação automatizada e a renovação de componentes.</span><span class="sxs-lookup"><span data-stu-id="a47db-120">The Windows Media Format Client Extended API provides a mechanism for the automated revocation and renewal of components.</span></span>

<span data-ttu-id="a47db-121">Os componentes revogados são listados em uma lista de certificados revogados, que é publicada pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a47db-121">Revoked components are listed in a certificate revocation list, which is published by Microsoft.</span></span> <span data-ttu-id="a47db-122">Quando um componente é revogado, seu certificado é adicionado à lista de certificados revogados e o BLOB de informações de revogação ( \_ info Rev) é atualizado nos servidores da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a47db-122">When a component is revoked, its certificate is added to the certificate revocation list, and the revocation information BLOB (REV\_INFO) is updated on the Microsoft servers.</span></span>

<span data-ttu-id="a47db-123">Para executar a revogação automatizada e a renovação quando um usuário tenta processar o conteúdo protegido por DRM do Windows Media, seu aplicativo deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a47db-123">To perform automated revocation and renewal when a user attempts to process Windows Media DRM protected content, your application must do the following:</span></span>

1.  <span data-ttu-id="a47db-124">Extraia a \_ versão de informações de Rev da licença.</span><span class="sxs-lookup"><span data-stu-id="a47db-124">Extract the REV\_INFO version from the license.</span></span> <span data-ttu-id="a47db-125">O número de versão de informações de REV \_ está localizado no seguinte local em uma licença do XMR:</span><span class="sxs-lookup"><span data-stu-id="a47db-125">The REV\_INFO version number is located in the following location in an XMR license:</span></span>
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  <span data-ttu-id="a47db-126">Compare o \_ número de versão de informações Rev da licença com o \_ número de versão da info Rev no repositório local chamando o método [**IWMDRMSecurity:: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .</span><span class="sxs-lookup"><span data-stu-id="a47db-126">Compare the REV\_INFO version number of the license with the REV\_INFO version number in the local store by calling the [**IWMDRMSecurity::GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) method.</span></span>
3.  <span data-ttu-id="a47db-127">Se a \_ versão de informações Rev não estiver atualizada, chame o método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , passando o \_ sinalizador segurança WMDRM \_ executar \_ atualização de revogação \_ no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="a47db-127">If the REV\_INFO version is not up to date, call the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, passing the WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH flag in the *dwFlags* parameter.</span></span>
4.  <span data-ttu-id="a47db-128">Recupere a lista de certificados revogados do armazenamento local chamando o método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="a47db-128">Retrieve the certificate revocation list from the local store by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
5.  <span data-ttu-id="a47db-129">Analise a lista de revogação e verifique as revogações do Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="a47db-129">Parse the revocation list, and check for Windows Media DRM revocations.</span></span> <span data-ttu-id="a47db-130">Para obter mais informações, consulte [verificando revogação de certificado](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="a47db-130">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
6.  <span data-ttu-id="a47db-131">Se houver qualquer revogação do Windows Media DRM:</span><span class="sxs-lookup"><span data-stu-id="a47db-131">If there are any Windows Media DRM revocations:</span></span>
    1.  <span data-ttu-id="a47db-132">Crie um habilitador de conteúdo para renovar os componentes revogados chamando o método [**IWMDRMSecurity:: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .</span><span class="sxs-lookup"><span data-stu-id="a47db-132">Create a content enabler to renew the revoked components by calling the [**IWMDRMSecurity::GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) method.</span></span>
    2.  <span data-ttu-id="a47db-133">Chame **IMFContentEnabler:: AutomaticEnable** que direciona o usuário para uma URL que contém informações de renovação de componentes.</span><span class="sxs-lookup"><span data-stu-id="a47db-133">Call **IMFContentEnabler::AutomaticEnable** which directs the user to a URL that contains component renewal information.</span></span> <span data-ttu-id="a47db-134">Esse método está documentado no [SDK do Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="a47db-134">This method is documented in the [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx).</span></span>
        > [!Note]  
        > <span data-ttu-id="a47db-135">Você deve esclarecer esse processo para o usuário por meio do uso de uma declaração de privacidade, pois o processo de atualização envia informações do computador cliente para um site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a47db-135">You must clarify this process to the user through the use of a privacy statement because the update process sends information from the client computer to a Microsoft Web site.</span></span>

         

    3.  <span data-ttu-id="a47db-136">Se possível, o usuário renovará o componente da URL, seja automaticamente ou seguindo instruções específicas.</span><span class="sxs-lookup"><span data-stu-id="a47db-136">If possible, the user will renew the component from the URL, either automatically or by following specific instructions.</span></span> <span data-ttu-id="a47db-137">Haverá algumas situações em que o componente não pode ser renovado.</span><span class="sxs-lookup"><span data-stu-id="a47db-137">There will be some situations in which the component cannot be renewed.</span></span>
    4.  <span data-ttu-id="a47db-138">Tente acessar o conteúdo novamente até que não haja mais revogações ou o processo seja interrompido por algum motivo.</span><span class="sxs-lookup"><span data-stu-id="a47db-138">Try to access the content again until there are no more revocations, or the process is halted for some reason.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a47db-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a47db-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a47db-140">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="a47db-140">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 