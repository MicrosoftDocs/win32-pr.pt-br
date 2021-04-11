---
description: Um certificado X.509 versão 3 contém os campos definidos na versão 1 e 2, e adiciona extensões de certificado. A sintaxe ASN. 1 das extensões de certificado é mostrada no exemplo a seguir.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Extensões da versão 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169487"
---
# <a name="version-3-extensions"></a><span data-ttu-id="abb86-104">Extensões da versão 3</span><span class="sxs-lookup"><span data-stu-id="abb86-104">Version 3 Extensions</span></span>

<span data-ttu-id="abb86-105">Um certificado X.509 versão 3 contém os campos definidos na versão 1 e 2, e adiciona extensões de certificado.</span><span class="sxs-lookup"><span data-stu-id="abb86-105">An X.509 version 3 certificate contains the fields defined in version 1 and version 2 and adds certificate extensions.</span></span> <span data-ttu-id="abb86-106">A sintaxe ASN. 1 das extensões de certificado é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="abb86-106">The ASN.1 syntax of certificate extensions is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

<span data-ttu-id="abb86-107">As extensões padrão da versão 3 e seus identificadores de objeto (OIDs) são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="abb86-107">The standard version 3 extensions and their object identifiers (OIDs) are listed in the following table.</span></span> <span data-ttu-id="abb86-108">A Microsoft oferece suporte a eles e inclui extensões personalizadas adicionais.</span><span class="sxs-lookup"><span data-stu-id="abb86-108">Microsoft supports these and includes additional custom extensions.</span></span> <span data-ttu-id="abb86-109">Para obter mais informações, consulte [extensões](extensions.md).</span><span class="sxs-lookup"><span data-stu-id="abb86-109">For more information, see [Extensions](extensions.md).</span></span>

| <span data-ttu-id="abb86-110">Extensão</span><span class="sxs-lookup"><span data-stu-id="abb86-110">Extension</span></span>                                         | <span data-ttu-id="abb86-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="abb86-111">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb86-112">Identificador de chave de autoridade (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="abb86-112">Authority Key Identifier(2.5.29.19)</span></span><br/>    | <span data-ttu-id="abb86-113">Identifica a chave pública da autoridade de certificação (AC) que corresponde à chave privada da AC usada para assinar o certificado.</span><span class="sxs-lookup"><span data-stu-id="abb86-113">Identifies the certification authority (CA) public key that corresponds to the CA private key used to sign the certificate.</span></span>                                                                              |
| <span data-ttu-id="abb86-114">Restrições básicas (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="abb86-114">Basic Constraints(2.5.29.35)</span></span><br/>           | <span data-ttu-id="abb86-115">Especifica se a entidade pode ser usada como AC e, em caso afirmativo, o número de ACs subordinadas que podem existir abaixo dela na cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="abb86-115">Specifies whether the entity can be used as a CA and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>                                                           |
| <span data-ttu-id="abb86-116">Políticas de certificado (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="abb86-116">Certificate Policies(2.5.29.32)</span></span><br/>        | <span data-ttu-id="abb86-117">Especifica as políticas sob as quais o certificado foi emitido e as finalidades para as quais ele pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="abb86-117">Specifies the policies under which the certificate has been issued and the purposes for which it can be used.</span></span>                                                                                            |
| <span data-ttu-id="abb86-118">Pontos de distribuição de CRL (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="abb86-118">CRL Distribution Points(2.5.29.31)</span></span><br/>     | <span data-ttu-id="abb86-119">Contém o URI da CRL ( [*lista de certificados revogados*](/windows/desktop/SecGloss/c-gly) ) base.</span><span class="sxs-lookup"><span data-stu-id="abb86-119">Contains the URI of the base [*certificate revocation list*](/windows/desktop/SecGloss/c-gly) (CRL).</span></span>                                  |
| <span data-ttu-id="abb86-120">Uso avançado de chave (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="abb86-120">Enhanced Key Usage(2.5.29.46)</span></span><br/>          | <span data-ttu-id="abb86-121">Especifica a maneira na qual a chave pública contida no certificado pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="abb86-121">Specifies the manner in which the public key contained in the certificate can be used.</span></span>                                                                                                                   |
| <span data-ttu-id="abb86-122">Nome alternativo do emissor (2.5.29.8)</span><span class="sxs-lookup"><span data-stu-id="abb86-122">Issuer Alternative Name(2.5.29.8)</span></span><br/>      | <span data-ttu-id="abb86-123">Especifica uma ou mais formas de nome alternativas para o emissor da solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="abb86-123">Specifies one or more alternative name forms for the issuer of the certificate request.</span></span>                                                                                                                  |
| <span data-ttu-id="abb86-124">Uso de chave (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="abb86-124">Key Usage(2.5.29.15)</span></span><br/>                   | <span data-ttu-id="abb86-125">Especifica restrições nas operações que podem ser executadas pela chave pública contida no certificado.</span><span class="sxs-lookup"><span data-stu-id="abb86-125">Specifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                           |
| <span data-ttu-id="abb86-126">Restrições de nome (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="abb86-126">Name Constraints(2.5.29.30)</span></span><br/>            | <span data-ttu-id="abb86-127">Especifica o namespace dentro do qual todos os nomes de entidades em uma hierarquia de certificados devem estar localizados.</span><span class="sxs-lookup"><span data-stu-id="abb86-127">Specifies the namespace within which all subject names in a certificate hierarchy must be located.</span></span> <span data-ttu-id="abb86-128">A extensão é usada somente em um certificado de AC.</span><span class="sxs-lookup"><span data-stu-id="abb86-128">The extension is used only in a CA certificate.</span></span>                                                       |
| <span data-ttu-id="abb86-129">Restrições de política (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="abb86-129">Policy Constraints(2.5.29.36)</span></span><br/>          | <span data-ttu-id="abb86-130">Restringe a validação do caminho, proibindo o mapeamento de política ou exigindo que cada certificado na hierarquia contenha um identificador de política aceitável.</span><span class="sxs-lookup"><span data-stu-id="abb86-130">Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span> <span data-ttu-id="abb86-131">A extensão é usada somente em um certificado de AC.</span><span class="sxs-lookup"><span data-stu-id="abb86-131">The extension is used only in a CA certificate.</span></span> |
| <span data-ttu-id="abb86-132">Mapeamentos de política (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="abb86-132">Policy Mappings(2.5.29.33)</span></span><br/>             | <span data-ttu-id="abb86-133">Especifica as políticas em uma AC subordinada que correspondem às políticas na AC emissora.</span><span class="sxs-lookup"><span data-stu-id="abb86-133">Specifies the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span>                                                                                                                |
| <span data-ttu-id="abb86-134">Período de uso de chave privada (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="abb86-134">Private Key Usage Period(2.5.29.16)</span></span><br/>    | <span data-ttu-id="abb86-135">Especifica um período de validade para a chave privada diferente do período para o certificado com o qual a chave privada está associada.</span><span class="sxs-lookup"><span data-stu-id="abb86-135">Specifies a different validity period for the private key than for the certificate with which the private key is associated.</span></span>                                                                             |
| <span data-ttu-id="abb86-136">Nome alternativo da entidade (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="abb86-136">Subject Alternative Name(2.5.29.17)</span></span><br/>    | <span data-ttu-id="abb86-137">Especifica uma ou mais formas de nome alternativas para a entidade da solicitação de certificado.</span><span class="sxs-lookup"><span data-stu-id="abb86-137">Specifies one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="abb86-138">Dentre os exemplos de formas alternativas incluem-se endereços de email, nomes DNS, endereços IP e URIs.</span><span class="sxs-lookup"><span data-stu-id="abb86-138">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>                           |
| <span data-ttu-id="abb86-139">Atributos de diretório de assunto (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="abb86-139">Subject Directory Attributes(2.5.29.9)</span></span><br/> | <span data-ttu-id="abb86-140">Expressa atributos de identificação, como a nacionalidade da entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="abb86-140">Conveys identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="abb86-141">O valor da extensão é uma sequência de pares de valores OID.</span><span class="sxs-lookup"><span data-stu-id="abb86-141">The extension value is a sequence of OID-value pairs.</span></span>                                                              |
| <span data-ttu-id="abb86-142">Identificador de chave de entidade (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="abb86-142">Subject Key Identifier(2.5.29.14)</span></span><br/>      | <span data-ttu-id="abb86-143">Diferencia entre várias chaves públicas mantidas pela entidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="abb86-143">Differentiates between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="abb86-144">O valor da extensão é geralmente um hash SHA-1 da chave.</span><span class="sxs-lookup"><span data-stu-id="abb86-144">The extension value is typically a SHA-1 hash of the key.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="abb86-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abb86-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abb86-146">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="abb86-146">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="abb86-147">Campos da versão 2</span><span class="sxs-lookup"><span data-stu-id="abb86-147">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="abb86-148">Certificados de chave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="abb86-148">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

