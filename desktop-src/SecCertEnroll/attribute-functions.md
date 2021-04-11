---
description: Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma autoridade de certificação (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado.
ms.assetid: 3eba5a2f-eeac-4e38-8705-b12bc183b7eb
title: Funções de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6413da0d43c142373e6f3cabe3d8e31636b82ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169361"
---
# <a name="attribute-functions"></a><span data-ttu-id="3760c-103">Funções de atributo</span><span class="sxs-lookup"><span data-stu-id="3760c-103">Attribute Functions</span></span>

<span data-ttu-id="3760c-104">Os atributos podem ser adicionados a uma solicitação de certificado para fornecer uma [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA) com informações adicionais que podem ser usadas ao criar e emitir um certificado.</span><span class="sxs-lookup"><span data-stu-id="3760c-104">Attributes can be added to a certificate request to provide a [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) with additional information that it can use when creating and issuing a certificate.</span></span>

<span data-ttu-id="3760c-105">CertEnroll.dll implementa as seguintes interfaces para definir atributos e coleções de atributos:</span><span class="sxs-lookup"><span data-stu-id="3760c-105">CertEnroll.dll implements the following interfaces to define attributes and attribute collections:</span></span>

-   [<span data-ttu-id="3760c-106">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="3760c-106">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [<span data-ttu-id="3760c-107">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="3760c-107">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [<span data-ttu-id="3760c-108">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="3760c-108">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [<span data-ttu-id="3760c-109">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="3760c-109">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
-   [<span data-ttu-id="3760c-110">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="3760c-110">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [<span data-ttu-id="3760c-111">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="3760c-111">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [<span data-ttu-id="3760c-112">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="3760c-112">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [<span data-ttu-id="3760c-113">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="3760c-113">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [<span data-ttu-id="3760c-114">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="3760c-114">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [<span data-ttu-id="3760c-115">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="3760c-115">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [<span data-ttu-id="3760c-116">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="3760c-116">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

<span data-ttu-id="3760c-117">As seções a seguir identificam as funções exportadas por Xenroll.dll para associar atributos criptográficos a solicitações de certificado e discutir como usar CertEnroll.dll para substituir a função ou indicar que não existe mapeamento entre as duas bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="3760c-117">The following sections identify functions exported by Xenroll.dll to associate cryptographic attributes with certificate requests and discuss how to use CertEnroll.dll to replace the function or indicate that no mapping between the two libraries exists:</span></span>

-   [<span data-ttu-id="3760c-118">addAttributeToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="3760c-118">addAttributeToRequestWStr</span></span>](#addattributetorequestwstr)
-   [<span data-ttu-id="3760c-119">AddAuthenticatedAttributesToPKCS7Request</span><span class="sxs-lookup"><span data-stu-id="3760c-119">AddAuthenticatedAttributesToPKCS7Request</span></span>](#addauthenticatedattributestopkcs7request)
-   [<span data-ttu-id="3760c-120">addNameValuePairToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="3760c-120">addNameValuePairToRequestWStr</span></span>](#addnamevaluepairtorequestwstr)
-   [<span data-ttu-id="3760c-121">AddNameValuePairToSignatureWStr</span><span class="sxs-lookup"><span data-stu-id="3760c-121">AddNameValuePairToSignatureWStr</span></span>](#addnamevaluepairtosignaturewstr)
-   [<span data-ttu-id="3760c-122">ClientId</span><span class="sxs-lookup"><span data-stu-id="3760c-122">ClientId</span></span>](#clientid)
-   [<span data-ttu-id="3760c-123">RenewalCertificate</span><span class="sxs-lookup"><span data-stu-id="3760c-123">RenewalCertificate</span></span>](#renewalcertificate)
-   [<span data-ttu-id="3760c-124">redefinirattributes</span><span class="sxs-lookup"><span data-stu-id="3760c-124">resetAttributes</span></span>](#resetattributes)
-   [<span data-ttu-id="3760c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3760c-125">Related topics</span></span>](#related-topics)

## <a name="addattributetorequestwstr"></a><span data-ttu-id="3760c-126">addAttributeToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="3760c-126">addAttributeToRequestWStr</span></span>

<span data-ttu-id="3760c-127">A função [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) no Xenroll.dll adiciona um atributo a uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="3760c-127">The [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) function in Xenroll.dll adds an attribute to a certificate request.</span></span>

<span data-ttu-id="3760c-128">Em geral, para adicionar um atributo a uma solicitação usando os objetos implementados no CertEnroll.dll, você pode executar as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="3760c-128">In general, to add an attribute to a request by using the objects implemented in CertEnroll.dll, you can perform the following actions:</span></span>

1.  <span data-ttu-id="3760c-129">Crie um objeto de coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .</span><span class="sxs-lookup"><span data-stu-id="3760c-129">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection object.</span></span>
2.  <span data-ttu-id="3760c-130">Crie um objeto [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) e chame o método [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) para criar um atributo a partir de um identificador de objeto e um valor de atributo ou use qualquer uma das interfaces listadas anteriormente para definir um dos atributos mais comuns.</span><span class="sxs-lookup"><span data-stu-id="3760c-130">Create an [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) object and call the [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attribute-initialize) method to create an attribute from an object identifier and attribute value or use any of the interfaces listed earlier to define one of the more common attributes.</span></span>
3.  <span data-ttu-id="3760c-131">Adicione cada novo atributo criado na etapa anterior à coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) usando o método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) .</span><span class="sxs-lookup"><span data-stu-id="3760c-131">Add each new attribute created in the preceding step to the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection by using the [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-add) method.</span></span>
4.  <span data-ttu-id="3760c-132">Crie um objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) e inicialize-o chamando o método [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) e especificando a coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) na entrada.</span><span class="sxs-lookup"><span data-stu-id="3760c-132">Create an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object and initialize it by calling the [**InitializeFromValues**](/windows/desktop/api/CertEnroll/nf-certenroll-icryptattribute-initializefromvalues) method and specifying the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection on input.</span></span>
5.  <span data-ttu-id="3760c-133">Recupere um objeto de coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) chamando a propriedade [**cript**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) . de um objeto de solicitação [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) ou [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) existente.</span><span class="sxs-lookup"><span data-stu-id="3760c-133">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection object by calling the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes) property on an existing [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) or [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) request object.</span></span>
6.  <span data-ttu-id="3760c-134">Adicione o objeto [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à coleção [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .</span><span class="sxs-lookup"><span data-stu-id="3760c-134">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="addauthenticatedattributestopkcs7request"></a><span data-ttu-id="3760c-135">AddAuthenticatedAttributesToPKCS7Request</span><span class="sxs-lookup"><span data-stu-id="3760c-135">AddAuthenticatedAttributesToPKCS7Request</span></span>

<span data-ttu-id="3760c-136">Os atributos autenticados são pares de nome-valor que são assinados e adicionados a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3760c-136">Authenticated attributes are name-value pairs that are signed by and added to a signature.</span></span> <span data-ttu-id="3760c-137">A função [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) no Xenroll.dll adiciona uma matriz de atributos autenticados a uma solicitação [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="3760c-137">The [**AddAuthenticatedAttributesToPKCS7Request**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request) function in Xenroll.dll adds an array of authenticated attributes to a [*PKCS \#7*](/windows/desktop/SecGloss/p-gly) request.</span></span>

<span data-ttu-id="3760c-138">Conforme discutido acima para a função [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) , você pode usar CertEnroll.dll para definir e adicionar facilmente uma coleção de atributos a uma solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="3760c-138">As discussed above for the [**addAttributeToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addattributetorequestwstr) function, you can use CertEnroll.dll to easily define and add a collection of attributes to a certificate request.</span></span> <span data-ttu-id="3760c-139">No entanto, você não pode escolher se o atributo é autenticado.</span><span class="sxs-lookup"><span data-stu-id="3760c-139">You cannot, however, choose whether the attribute is authenticated.</span></span> <span data-ttu-id="3760c-140">O processo de registro toma essa decisão automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3760c-140">The enrollment process automatically makes this decision.</span></span>

## <a name="addnamevaluepairtorequestwstr"></a><span data-ttu-id="3760c-141">addNameValuePairToRequestWStr</span><span class="sxs-lookup"><span data-stu-id="3760c-141">addNameValuePairToRequestWStr</span></span>

<span data-ttu-id="3760c-142">A função [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) no Xenroll.dll adiciona um par de nome-valor não autenticado a uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="3760c-142">The [**addNameValuePairToRequestWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addnamevaluepairtorequestwstr) function in Xenroll.dll adds an unauthenticated name-value pair to a request.</span></span>

<span data-ttu-id="3760c-143">Você pode usar a interface [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) em CertEnroll.dll para definir um par de nome-valor e pode adicionar uma coleção de pares de nome-valor a um objeto de solicitação CMC executando as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="3760c-143">You can use the [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) interface in CertEnroll.dll to define a name-value pair, and you can add a collection of name-value pairs to a CMC request object by performing the following actions:</span></span>

1.  <span data-ttu-id="3760c-144">Crie e inicialize um objeto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="3760c-144">Create and initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="3760c-145">O processo de inicialização cria uma coleção [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) vazia.</span><span class="sxs-lookup"><span data-stu-id="3760c-145">The initialization process creates an empty [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection.</span></span>
2.  <span data-ttu-id="3760c-146">Chame a propriedade [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) em um objeto de solicitação CMC existente para recuperar a coleção.</span><span class="sxs-lookup"><span data-stu-id="3760c-146">Call the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property on an existing CMC request object to retrieve the collection.</span></span>
3.  <span data-ttu-id="3760c-147">Crie e inicialize um objeto [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="3760c-147">Create and initialize an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object.</span></span>
4.  <span data-ttu-id="3760c-148">Adicione cada novo par nome-valor à coleção [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) chamando o método [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) .</span><span class="sxs-lookup"><span data-stu-id="3760c-148">Add each new name-value pair to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection by calling the [**Add**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509namevaluepairs-add) method.</span></span>

<span data-ttu-id="3760c-149">O processo de registro coloca a coleção de pares nome-valor na estrutura **taggedattribute** da solicitação CMC.</span><span class="sxs-lookup"><span data-stu-id="3760c-149">The enrollment process places the collection of name-value pairs in the **TaggedAttribute** structure of the CMC request.</span></span>

## <a name="addnamevaluepairtosignaturewstr"></a><span data-ttu-id="3760c-150">AddNameValuePairToSignatureWStr</span><span class="sxs-lookup"><span data-stu-id="3760c-150">AddNameValuePairToSignatureWStr</span></span>

<span data-ttu-id="3760c-151">A função [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) no Xenroll.dll adiciona um par nome-valor autenticado a uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="3760c-151">The [**AddNameValuePairToSignatureWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr) function in Xenroll.dll adds an authenticated name-value pair to a request.</span></span> <span data-ttu-id="3760c-152">Normalmente, isso é usado para especificar o nome do solicitante em uma solicitação de registro em nome de (EOBO).</span><span class="sxs-lookup"><span data-stu-id="3760c-152">This is typically used to specify the requester name in an enroll-on-behalf-of (EOBO) request.</span></span>

<span data-ttu-id="3760c-153">Em CertEnroll.dll, use a propriedade [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) para especificar o nome em uma solicitação EOBO.</span><span class="sxs-lookup"><span data-stu-id="3760c-153">In CertEnroll.dll, use the [**RequesterName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_requestername) property to specify the name in an EOBO request.</span></span>

## <a name="clientid"></a><span data-ttu-id="3760c-154">ClientId</span><span class="sxs-lookup"><span data-stu-id="3760c-154">ClientId</span></span>

<span data-ttu-id="3760c-155">A função [**ClientID**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) no Xenroll.dll especifica ou recupera um atributo **ClientID** .</span><span class="sxs-lookup"><span data-stu-id="3760c-155">The [**ClientId**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_clientid) function in Xenroll.dll specifies or retrieves a **ClientId** attribute.</span></span>

<span data-ttu-id="3760c-156">Use a propriedade [**ClientID**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) em CertEnroll.dll para adicionar esse atributo a uma solicitação CMC ou PKCS \# 10.</span><span class="sxs-lookup"><span data-stu-id="3760c-156">Use the [**ClientId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_clientid) property in CertEnroll.dll to add this attribute to a CMC or PKCS \#10 request.</span></span>

## <a name="renewalcertificate"></a><span data-ttu-id="3760c-157">RenewalCertificate</span><span class="sxs-lookup"><span data-stu-id="3760c-157">RenewalCertificate</span></span>

<span data-ttu-id="3760c-158">A função [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) em Xenroll.dll especifica ou recupera um atributo **RenewalCertificate** .</span><span class="sxs-lookup"><span data-stu-id="3760c-158">The [**RenewalCertificate**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate) function in Xenroll.dll specifies or retrieves a **RenewalCertificate** attribute.</span></span>

<span data-ttu-id="3760c-159">No CertEnroll.dll, quando você chama [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) em um \# objeto PKCS 7 ou Pkcs) é criado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3760c-159">In CertEnroll.dll, when you call [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) on a PKCS \#7 or PKCS ) object is automatically created.</span></span>

## <a name="resetattributes"></a><span data-ttu-id="3760c-160">redefinirattributes</span><span class="sxs-lookup"><span data-stu-id="3760c-160">resetAttributes</span></span>

<span data-ttu-id="3760c-161">A função [**resetattributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) no Xenroll.dll remove a coleção de atributos de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="3760c-161">The [**resetAttributes**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-resetattributes) function in Xenroll.dll removes the attribute collection from a request.</span></span>

<span data-ttu-id="3760c-162">Para remover um atributo de uma solicitação por índice usando CertEnroll.dll, chame o método [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) na coleção [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) .</span><span class="sxs-lookup"><span data-stu-id="3760c-162">To remove an attribute from a request by index using CertEnroll.dll, call the [**Remove**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-remove) method on the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection.</span></span> <span data-ttu-id="3760c-163">Para remover todos os atributos de uma solicitação, chame o método [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) .</span><span class="sxs-lookup"><span data-stu-id="3760c-163">To remove all attributes from a request, call the [**Clear**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509attributes-clear) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3760c-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3760c-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3760c-165">Mapeando Xenroll.dll para CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="3760c-165">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="3760c-166">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="3760c-166">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[<span data-ttu-id="3760c-167">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="3760c-167">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[<span data-ttu-id="3760c-168">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="3760c-168">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[<span data-ttu-id="3760c-169">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="3760c-169">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> <dt>

[<span data-ttu-id="3760c-170">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="3760c-170">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)
</dt> <dt>

[<span data-ttu-id="3760c-171">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="3760c-171">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)
</dt> </dl>

 

 
