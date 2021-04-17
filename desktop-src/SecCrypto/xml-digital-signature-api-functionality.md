---
description: O CryptXML fornece um conjunto de APIs de baixo nível que permite que os aplicativos criem e verifiquem assinaturas envelopadas, enveloping e desanexadas. Você pode usar o CryptXML para criar e verificar o conteúdo armazenado em elementos de objeto de assinatura, incluindo manifestos.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Funcionalidade de API de assinatura digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755034"
---
# <a name="xml-digital-signature-api-functionality"></a><span data-ttu-id="19265-104">Funcionalidade de API de assinatura digital XML</span><span class="sxs-lookup"><span data-stu-id="19265-104">XML Digital Signature API Functionality</span></span>

<span data-ttu-id="19265-105">O CryptXML fornece um conjunto de APIs de baixo nível que permite que os aplicativos criem e verifiquem assinaturas envelopadas, enveloping e desanexadas.</span><span class="sxs-lookup"><span data-stu-id="19265-105">CryptXML provides a low level set of APIs that allow applications to create and verify enveloped, enveloping, and detached signatures.</span></span> <span data-ttu-id="19265-106">Você pode usar o CryptXML para criar e verificar o conteúdo armazenado em elementos de objeto de assinatura, incluindo manifestos.</span><span class="sxs-lookup"><span data-stu-id="19265-106">You can use CryptXML to create and verify content stored in signature object elements, including manifests.</span></span> <span data-ttu-id="19265-107">Uma chave pública/privada, compartilhada ou um certificado [*X. 509*](../secgloss/x-gly.md) ou uma cadeia de certificados pode ser usada para assinar e verificar a [*assinatura digital*](../secgloss/d-gly.md)XML.</span><span class="sxs-lookup"><span data-stu-id="19265-107">A public/private, shared key, or an [*X.509*](../secgloss/x-gly.md) certificate or certificate chain can be used to sign and verify the XML [*digital signature*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="19265-108">Os aplicativos que usam CryptXML para verificar referências externas (referências que se destinam a um documento ou arquivo externo fora do contexto do documento) devem resolver os URIs externos e recuperar os dados a serem resumidos.</span><span class="sxs-lookup"><span data-stu-id="19265-108">Applications that use CryptXML to verify external references (references that target an external document or file outside of the document context) must resolve the external URIs and retrieve the data to be digested.</span></span>

<span data-ttu-id="19265-109">Para obter informações sobre os algoritmos de criptografia com suporte do CryptXML, consulte [algoritmos criptográficos de assinatura digital XML](xml-digital-signature-cryptographic-algorithms.md).</span><span class="sxs-lookup"><span data-stu-id="19265-109">For information about the cryptographic algorithms supported by CryptXML, see [XML Digital Signature Cryptographic Algorithms](xml-digital-signature-cryptographic-algorithms.md).</span></span>

<span data-ttu-id="19265-110">O CryptXML fornece suporte para os algoritmos de canonização com os seguintes identificadores.</span><span class="sxs-lookup"><span data-stu-id="19265-110">CryptXML provides support for the canonicalization algorithms with the following identifiers.</span></span>



| <span data-ttu-id="19265-111">Constante</span><span class="sxs-lookup"><span data-stu-id="19265-111">Constant</span></span>                                              | <span data-ttu-id="19265-112">Valor do URI</span><span class="sxs-lookup"><span data-stu-id="19265-112">URI value</span></span>                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="19265-113">\_c14n de canonização wszURI \_</span><span class="sxs-lookup"><span data-stu-id="19265-113">wszURI\_CANONICALIZATION\_C14N</span></span><br/>             | <span data-ttu-id="19265-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span><span class="sxs-lookup"><span data-stu-id="19265-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span></span><br/>               |
| <span data-ttu-id="19265-115">\_C14NC de canonização wszURI \_</span><span class="sxs-lookup"><span data-stu-id="19265-115">wszURI\_CANONICALIZATION\_C14NC</span></span><br/>            | <span data-ttu-id="19265-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="19265-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span></span><br/> |
| <span data-ttu-id="19265-117">wszURI \_ canonização \_ EXSLUSIVE \_ c14n</span><span class="sxs-lookup"><span data-stu-id="19265-117">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14N</span></span><br/>  | <span data-ttu-id="19265-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span><span class="sxs-lookup"><span data-stu-id="19265-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span></span><br/>                      |
| <span data-ttu-id="19265-119">wszURI \_ canonização \_ EXSLUSIVE \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="19265-119">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14NC</span></span><br/> | <span data-ttu-id="19265-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="19265-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span></span><br/>          |



 

<span data-ttu-id="19265-121">CryptXML fornece suporte para a transformação de assinatura envelopada.</span><span class="sxs-lookup"><span data-stu-id="19265-121">CryptXML provides support for the enveloped signature transform.</span></span>



| <span data-ttu-id="19265-122">Constante</span><span class="sxs-lookup"><span data-stu-id="19265-122">Constant</span></span>                                       | <span data-ttu-id="19265-123">Valor do URI</span><span class="sxs-lookup"><span data-stu-id="19265-123">URI value</span></span>                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="19265-124">\_transformação xmlns \_ wszURI \_ envelopada</span><span class="sxs-lookup"><span data-stu-id="19265-124">wszURI\_XMLNS\_TRANSFORM\_ENVELOPED</span></span><br/> | <span data-ttu-id="19265-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span><span class="sxs-lookup"><span data-stu-id="19265-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span></span><br/> |



 

<span data-ttu-id="19265-126">Por padrão, o CryptXML não oferece suporte a transformações XPath ou XSLT.</span><span class="sxs-lookup"><span data-stu-id="19265-126">By default, CryptXML does not support XPath or XSLT transforms.</span></span> <span data-ttu-id="19265-127">Se necessário, os aplicativos podem implementar essas transformações sobre CryptXML.</span><span class="sxs-lookup"><span data-stu-id="19265-127">If required, applications can implement these transforms on top of CryptXML.</span></span>

 

 
