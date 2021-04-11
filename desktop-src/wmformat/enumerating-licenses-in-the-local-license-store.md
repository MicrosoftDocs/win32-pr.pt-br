---
title: Enumerando licenças no repositório de licenças local
description: Enumerando licenças no repositório de licenças local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- SDK do Windows Media Format, enumerando licenças
- SDK do Windows Media Format, licenças
- SDK do Windows Media Format, armazenamento de licença local
- DRM (gerenciamento de direitos digitais), enumerando licenças
- DRM (gerenciamento de direitos digitais), enumerando licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), repositório de licenças local
- DRM (gerenciamento de direitos digitais), repositório de licenças local
- APIs estendidas do cliente DRM, enumerando licenças
- APIs estendidas do cliente, enumerando licenças
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, repositório de licenças local
- APIs estendidas do cliente, repositório de licenças local
- licenças, enumerando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363818"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a><span data-ttu-id="705e2-119">Enumerando licenças no repositório de licenças local</span><span class="sxs-lookup"><span data-stu-id="705e2-119">Enumerating Licenses in the Local License Store</span></span>

<span data-ttu-id="705e2-120">A enumeração é um processo de obter informações sobre as licenças no repositório de licenças local, percorrendo-as uma a uma.</span><span class="sxs-lookup"><span data-stu-id="705e2-120">Enumeration is a process of getting information about the licenses in the local license store, by stepping through them one by one.</span></span> <span data-ttu-id="705e2-121">Você pode criar uma enumeração de licenças chamando o [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="705e2-121">You can create a license enumeration by calling the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span></span>

<span data-ttu-id="705e2-122">O motivo mais comum para enumerar por meio de licenças no repositório é encontrar uma licença específica para descriptografia de algum conteúdo.</span><span class="sxs-lookup"><span data-stu-id="705e2-122">The most common reason for enumerating through licenses in the store is to find a particular license for decryption of some content.</span></span>

<span data-ttu-id="705e2-123">A interface [**IWMDRMLicense**](iwmdrmlicense.md) serve como um portal para os resultados de licença individuais e como o enumerador.</span><span class="sxs-lookup"><span data-stu-id="705e2-123">The [**IWMDRMLicense**](iwmdrmlicense.md) interface serves as both a portal to the individual license results and as the enumerator.</span></span> <span data-ttu-id="705e2-124">Quando a enumeração de licença é criada, a primeira licença da lista é carregada na interface **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="705e2-124">When the license enumeration is created, the first license in the list is loaded into the **IWMDRMLicense** interface.</span></span> <span data-ttu-id="705e2-125">A maioria dos métodos de **IWMDRMLicense** permite que você obtenha informações sobre a licença ou crie objetos para criptografar ou descriptografar conteúdo com base na licença.</span><span class="sxs-lookup"><span data-stu-id="705e2-125">Most of the methods of **IWMDRMLicense** enable you to get information about the license or to create objects to encrypt or decrypt content based on the license.</span></span> <span data-ttu-id="705e2-126">No entanto, há dois métodos que controlam a enumeração: [**GetNext**](iwmdrmlicense-getnext.md) e [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="705e2-126">However, there are two methods that control the enumeration: [**GetNext**](iwmdrmlicense-getnext.md) and [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span></span> <span data-ttu-id="705e2-127">**GetNext** carrega a próxima licença na lista na interface.</span><span class="sxs-lookup"><span data-stu-id="705e2-127">**GetNext** loads the next license in the list into the interface.</span></span> <span data-ttu-id="705e2-128">**ResetEnumeration** retorna a enumeração para o estado em que estava quando ela foi criada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="705e2-128">**ResetEnumeration** returns the enumeration to the state it was in when it was first created.</span></span> <span data-ttu-id="705e2-129">Quando a enumeração é redefinida, a primeira licença na lista é carregada de volta para a interface **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="705e2-129">When the enumeration is reset, the first license in the list is loaded back into the **IWMDRMLicense** interface.</span></span>

<span data-ttu-id="705e2-130">Quando você tiver atingido a última licença na lista, a próxima chamada para **GetNext** retornará um erro \_ sem \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="705e2-130">When you have reached the last license in the list, the next call to **GetNext** returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="705e2-131">Se seu aplicativo executar uma ação com o conteúdo coberto pelo DRM, você deverá verificar as licenças no repositório de licenças local para obter os direitos e outros fatores de limitação, como OPLs (níveis de proteção de saída).</span><span class="sxs-lookup"><span data-stu-id="705e2-131">If your application performs an action with the content that is covered by DRM, you should check the licenses in the local license store for the rights and for other limiting factors, such as output protection levels (OPLs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="705e2-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="705e2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="705e2-133">**Obtendo informações de licenças no repositório de licenças local**</span><span class="sxs-lookup"><span data-stu-id="705e2-133">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




