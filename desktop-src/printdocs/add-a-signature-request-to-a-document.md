---
description: Este tópico descreve como adicionar uma solicitação de assinatura a um documento XPS.
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: Adicionar uma solicitação de assinatura a um documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788899"
---
# <a name="add-a-signature-request-to-an-xps-document"></a><span data-ttu-id="adf39-103">Adicionar uma solicitação de assinatura a um documento XPS</span><span class="sxs-lookup"><span data-stu-id="adf39-103">Add a Signature Request to an XPS Document</span></span>

<span data-ttu-id="adf39-104">Este tópico descreve como adicionar uma solicitação de assinatura a um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="adf39-104">This topic describes how to add a signature request to an XPS document.</span></span> <span data-ttu-id="adf39-105">Uma solicitação de assinatura solicita que um usuário assine um documento se ele concordar com a intenção de assinatura.</span><span class="sxs-lookup"><span data-stu-id="adf39-105">A signature request prompts a user to sign a document if he or she agrees with the signature intent.</span></span>

<span data-ttu-id="adf39-106">Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de assinatura digital](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="adf39-106">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="adf39-107">Para adicionar uma solicitação de assinatura a um documento XPS:</span><span class="sxs-lookup"><span data-stu-id="adf39-107">To add a signature request to an XPS Document:</span></span>

1.  <span data-ttu-id="adf39-108">Carregue o documento XPS em um Gerenciador de assinatura, conforme descrito em [inicializar o Gerenciador de assinatura](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="adf39-108">Load the XPS document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="adf39-109">Adicione um bloco de assinatura ao Gerenciador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="adf39-109">Add a signature block to the signature manager.</span></span>
3.  <span data-ttu-id="adf39-110">Crie uma solicitação de assinatura no novo bloco de assinatura.</span><span class="sxs-lookup"><span data-stu-id="adf39-110">Create a signature request in the new signature block.</span></span>
4.  <span data-ttu-id="adf39-111">Defina as propriedades da solicitação de assinatura:</span><span class="sxs-lookup"><span data-stu-id="adf39-111">Set the properties of the signature request:</span></span>
    1.  <span data-ttu-id="adf39-112">Defina a intenção de assinatura.</span><span class="sxs-lookup"><span data-stu-id="adf39-112">Set the signature intent.</span></span>
    2.  <span data-ttu-id="adf39-113">Defina o nome da pessoa cuja assinatura é solicitada (o signatário solicitado).</span><span class="sxs-lookup"><span data-stu-id="adf39-113">Set the name of the person whose signature is requested (the requested signer).</span></span>
    3.  <span data-ttu-id="adf39-114">Defina a data em que a assinatura é necessária.</span><span class="sxs-lookup"><span data-stu-id="adf39-114">Set the date the signature is required.</span></span>
    4.  <span data-ttu-id="adf39-115">Defina outras propriedades de assinatura conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="adf39-115">Set other signature properties as required.</span></span>

<span data-ttu-id="adf39-116">O exemplo de código a seguir ilustra como adicionar uma solicitação de assinatura a um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="adf39-116">The following code example illustrates how to add a signature request to an XPS document.</span></span>


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="adf39-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adf39-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="adf39-118">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="adf39-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="adf39-119">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="adf39-119">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[<span data-ttu-id="adf39-120">**IXpsSignatureBlock:: CreateRequest**</span><span class="sxs-lookup"><span data-stu-id="adf39-120">**IXpsSignatureBlock::CreateRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[<span data-ttu-id="adf39-121">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="adf39-121">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="adf39-122">**IXpsSignatureManager::AddSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="adf39-122">**IXpsSignatureManager::AddSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[<span data-ttu-id="adf39-123">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="adf39-123">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[<span data-ttu-id="adf39-124">**IXpsSignatureRequest:: setintenções**</span><span class="sxs-lookup"><span data-stu-id="adf39-124">**IXpsSignatureRequest::SetIntent**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[<span data-ttu-id="adf39-125">**IXpsSignatureRequest::SetRequestedSigner**</span><span class="sxs-lookup"><span data-stu-id="adf39-125">**IXpsSignatureRequest::SetRequestedSigner**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[<span data-ttu-id="adf39-126">**IXpsSignatureRequest::SetRequestSignByDate**</span><span class="sxs-lookup"><span data-stu-id="adf39-126">**IXpsSignatureRequest::SetRequestSignByDate**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

<span data-ttu-id="adf39-127">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="adf39-127">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="adf39-128">Erros de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="adf39-128">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="adf39-129">Erros de documento XPS</span><span class="sxs-lookup"><span data-stu-id="adf39-129">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="adf39-130">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="adf39-130">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



