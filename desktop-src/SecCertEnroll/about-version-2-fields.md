---
description: Um certificado X.509 versão 2 contém os campos básicos definidos na versão 1 e adiciona os campos a seguir.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Campos da versão 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164250"
---
# <a name="version-2-fields"></a><span data-ttu-id="23c65-103">Campos da versão 2</span><span class="sxs-lookup"><span data-stu-id="23c65-103">Version 2 Fields</span></span>

<span data-ttu-id="23c65-104">Um certificado X.509 versão 2 contém os campos básicos definidos na versão 1 e adiciona os campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="23c65-104">An X.509 version 2 certificate contains the basic fields defined in version 1 and adds the following fields.</span></span>

## <a name="issuer-unique-identifier"></a><span data-ttu-id="23c65-105">Identificador Exclusivo de Emissor</span><span class="sxs-lookup"><span data-stu-id="23c65-105">Issuer Unique Identifier</span></span>

<span data-ttu-id="23c65-106">Contém um valor exclusivo que pode ser usado para tornar o nome X.500 da AC não ambíguo quando reutilizado por entidades diferentes com o tempo.</span><span class="sxs-lookup"><span data-stu-id="23c65-106">Contains a unique value that can be used to make the X.500 name of the CA unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a><span data-ttu-id="23c65-107">Identificador Exclusivo de Entidade</span><span class="sxs-lookup"><span data-stu-id="23c65-107">Subject Unique Identifier</span></span>

<span data-ttu-id="23c65-108">Contém um valor exclusivo que pode ser usado para tornar o nome X.500 da entidade do certificado não ambíguo quando reutilizado por entidades diferentes com o tempo.</span><span class="sxs-lookup"><span data-stu-id="23c65-108">Contains a unique value that can be used to make the X.500 name of the certificate subject unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a><span data-ttu-id="23c65-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23c65-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c65-110">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="23c65-110">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="23c65-111">Extensões da versão 3</span><span class="sxs-lookup"><span data-stu-id="23c65-111">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="23c65-112">Certificados de chave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="23c65-112">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



