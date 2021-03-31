---
title: Verificando revogação de certificado
description: Verificando revogação de certificado
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, revogação de certificado
- SDK do Windows Media Format, revogação de certificados
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), revogação de certificado
- DRM (gerenciamento de direitos digitais), revogação de certificado
- DRM (gerenciamento de direitos digitais), revogação de certificados
- DRM (gerenciamento de direitos digitais), revogação de certificados
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, revogação de certificado
- APIs estendidas do cliente, revogação de certificado
- APIs estendidas do cliente DRM, revogação de certificados
- APIs estendidas do cliente, revogação de certificados
- certificados, revogação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635813"
---
# <a name="checking-certificate-revocation"></a><span data-ttu-id="86cad-120">Verificando revogação de certificado</span><span class="sxs-lookup"><span data-stu-id="86cad-120">Checking Certificate Revocation</span></span>

<span data-ttu-id="86cad-121">Ao importar o conteúdo para o Windows Media DRM, você deve garantir que nenhum certificado em uma coleção de certificados tenha sido revogado verificando se nenhum certificado na coleção está na lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="86cad-121">When importing content into Windows Media DRM, you must ensure that no certificate in a certificate collection has been revoked by verifying that no certificate in the collection is in the revocation list.</span></span> <span data-ttu-id="86cad-122">A lista de revogação é extraída usando o método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="86cad-122">The revocation list is extracted by using the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>

<span data-ttu-id="86cad-123">Em seguida, você usa o método [**IWMDRMSecurity:: CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) para verificar se o certificado não foi revogado.</span><span class="sxs-lookup"><span data-stu-id="86cad-123">You then use the [**IWMDRMSecurity::CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) method to verify that the certificate is not revoked.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86cad-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86cad-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86cad-125">**Importação de DRM**</span><span class="sxs-lookup"><span data-stu-id="86cad-125">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




