---
description: O campo assunto de uma \# solicitação de certificado PKCS 10 contém o nome distinto da entidade que solicita o certificado.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Nomes de Entidades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756160"
---
# <a name="subject-names"></a><span data-ttu-id="fc140-103">Nomes de Entidades</span><span class="sxs-lookup"><span data-stu-id="fc140-103">Subject Names</span></span>

<span data-ttu-id="fc140-104">O campo **assunto** de uma \# solicitação de certificado PKCS 10 contém o nome distinto da entidade que solicita o certificado.</span><span class="sxs-lookup"><span data-stu-id="fc140-104">The **subject** field of a PKCS \#10 certificate request contains the distinguished name of the entity requesting the certificate.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

<span data-ttu-id="fc140-105">O nome distinto consiste em uma sequência de nomes distintos relativos (RDNs).</span><span class="sxs-lookup"><span data-stu-id="fc140-105">The distinguished name consists of a sequence of relative distinguished names (RDNs).</span></span> <span data-ttu-id="fc140-106">Cada RDN consiste em um conjunto de atributos, e cada atributo consiste em um identificador de objeto e um valor.</span><span class="sxs-lookup"><span data-stu-id="fc140-106">Each RDN consists of a set of attributes, and each attribute consists of an object identifier and a value.</span></span> <span data-ttu-id="fc140-107">O tipo de dados do valor é identificado pela estrutura **directorystring** .</span><span class="sxs-lookup"><span data-stu-id="fc140-107">The data type of the value is identified by the **DirectoryString** structure.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="fc140-108">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="fc140-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="fc140-109">Criando um nome de entidade</span><span class="sxs-lookup"><span data-stu-id="fc140-109">Creating a Subject Name</span></span>](creating-a-subject-name.md)
-   [<span data-ttu-id="fc140-110">Codificando um nome de entidade</span><span class="sxs-lookup"><span data-stu-id="fc140-110">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)

## <a name="related-topics"></a><span data-ttu-id="fc140-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc140-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc140-112">Solicitações</span><span class="sxs-lookup"><span data-stu-id="fc140-112">Requests</span></span>](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
