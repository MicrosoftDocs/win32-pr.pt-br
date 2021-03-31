---
description: Os serviços de certificados dão suporte ao uso de certificados, conforme definido na recomendação ITU-T X. 509 (também, ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propriedades do Certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828011"
---
# <a name="certificate-properties"></a><span data-ttu-id="3efce-103">Propriedades do Certificado</span><span class="sxs-lookup"><span data-stu-id="3efce-103">Certificate Properties</span></span>

<span data-ttu-id="3efce-104">Os serviços de certificados dão suporte ao uso de certificados, conforme definido na recomendação ITU-T [*X. 509*](../secgloss/x-gly.md) (também, ISO/IEC 9594-8).</span><span class="sxs-lookup"><span data-stu-id="3efce-104">Certificate Services supports the use of certificates as defined in the ITU-T recommendation [*X.509*](../secgloss/x-gly.md) (also, ISO/IEC 9594-8).</span></span> <span data-ttu-id="3efce-105">Veja a seguir as propriedades contidas em um certificado X. 509 padrão.</span><span class="sxs-lookup"><span data-stu-id="3efce-105">The following are properties that are contained in a standard X.509 certificate.</span></span>



| <span data-ttu-id="3efce-106">Campo</span><span class="sxs-lookup"><span data-stu-id="3efce-106">Field</span></span>                                       | <span data-ttu-id="3efce-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3efce-107">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3efce-108">Versão</span><span class="sxs-lookup"><span data-stu-id="3efce-108">Version</span></span>                                     | <span data-ttu-id="3efce-109">Número de versão do formato do certificado.</span><span class="sxs-lookup"><span data-stu-id="3efce-109">Version number of the certificate format.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="3efce-110">Número de Série</span><span class="sxs-lookup"><span data-stu-id="3efce-110">Serial Number</span></span>                               | <span data-ttu-id="3efce-111">Número de série do certificado.</span><span class="sxs-lookup"><span data-stu-id="3efce-111">Serial number of the certificate.</span></span> <span data-ttu-id="3efce-112">Esse número é atribuído pelo emissor e é exclusivo na lista de certificados emitidos do emissor.</span><span class="sxs-lookup"><span data-stu-id="3efce-112">This number is assigned by the issuer and is unique within the issuer's list of issued certificates.</span></span>                                                                          |
| <span data-ttu-id="3efce-113">Identificador e parâmetros do algoritmo</span><span class="sxs-lookup"><span data-stu-id="3efce-113">Algorithm Identifier and Parameters</span></span>         | <span data-ttu-id="3efce-114">Algoritmo de assinatura e quaisquer parâmetros usados pelo emissor.</span><span class="sxs-lookup"><span data-stu-id="3efce-114">Signature algorithm and any parameters used by the issuer.</span></span>                                                                                                                                                      |
| <span data-ttu-id="3efce-115">Emissor</span><span class="sxs-lookup"><span data-stu-id="3efce-115">Issuer</span></span>                                      | <span data-ttu-id="3efce-116">Nome da [*autoridade de certificação*](../secgloss/c-gly.md) que emitiu o certificado.</span><span class="sxs-lookup"><span data-stu-id="3efce-116">Name of the [*certification authority*](../secgloss/c-gly.md) which issued the certificate.</span></span>                                               |
| <span data-ttu-id="3efce-117">Não antes (Data)</span><span class="sxs-lookup"><span data-stu-id="3efce-117">Not Before (Date)</span></span>                           | <span data-ttu-id="3efce-118">O certificado não é válido antes desta data.</span><span class="sxs-lookup"><span data-stu-id="3efce-118">Certificate not valid before this date.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="3efce-119">Não após (Data)</span><span class="sxs-lookup"><span data-stu-id="3efce-119">Not After (Date)</span></span>                            | <span data-ttu-id="3efce-120">Certificado inválido após esta data.</span><span class="sxs-lookup"><span data-stu-id="3efce-120">Certificate not valid after this date.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="3efce-121">Nome do assunto</span><span class="sxs-lookup"><span data-stu-id="3efce-121">Subject Name</span></span>                                | <span data-ttu-id="3efce-122">Nome da pessoa ou entidade para a qual o certificado está sendo emitido.</span><span class="sxs-lookup"><span data-stu-id="3efce-122">Name of the person or entity to whom the certificate is being issued.</span></span> <span data-ttu-id="3efce-123">Esse campo também pode incluir a organização do destinatário do certificado, a unidade organizacional, a localidade, o estado ou a província e o país/região.</span><span class="sxs-lookup"><span data-stu-id="3efce-123">This field can also include the certificate recipient's organization, organization unit, locality, state or province, and country/region.</span></span> |
| <span data-ttu-id="3efce-124">Algoritmo e parâmetros de chave pública da entidade</span><span class="sxs-lookup"><span data-stu-id="3efce-124">Subject Public Key Algorithm and Parameters</span></span> | <span data-ttu-id="3efce-125">O algoritmo e os parâmetros usados para a [*chave pública*](../secgloss/p-gly.md)da entidade.</span><span class="sxs-lookup"><span data-stu-id="3efce-125">The algorithm and any parameters used for the subject's [*public key*](../secgloss/p-gly.md).</span></span>                                                                       |
| <span data-ttu-id="3efce-126">Chave pública de assunto</span><span class="sxs-lookup"><span data-stu-id="3efce-126">Subject Public Key</span></span>                          | <span data-ttu-id="3efce-127">A chave pública real (uma cadeia de caracteres de bits).</span><span class="sxs-lookup"><span data-stu-id="3efce-127">The actual public key (a bit string).</span></span>                                                                                                                                                                           |
| <span data-ttu-id="3efce-128">Assinatura</span><span class="sxs-lookup"><span data-stu-id="3efce-128">Signature</span></span>                                   | <span data-ttu-id="3efce-129">Assinatura conforme fornecida pelo emissor.</span><span class="sxs-lookup"><span data-stu-id="3efce-129">Signature as provided by the issuer.</span></span>                                                                                                                                                                            |



 

<span data-ttu-id="3efce-130">Um certificado pode conter os seguintes itens, dependendo da versão [*X. 509*](../secgloss/x-gly.md) do certificado.</span><span class="sxs-lookup"><span data-stu-id="3efce-130">A certificate can contain the following items, depending on the [*X.509*](../secgloss/x-gly.md) version of the certificate.</span></span>



| <span data-ttu-id="3efce-131">Campo opcional</span><span class="sxs-lookup"><span data-stu-id="3efce-131">Optional field</span></span>    | <span data-ttu-id="3efce-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="3efce-132">Description</span></span>                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3efce-133">ID exclusiva do emissor</span><span class="sxs-lookup"><span data-stu-id="3efce-133">Issuer Unique ID</span></span>  | <span data-ttu-id="3efce-134">Usado para tornar o nome do emissor inambíguo se ele tiver sido usado por mais de uma entidade.</span><span class="sxs-lookup"><span data-stu-id="3efce-134">Used to make the issuer name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="3efce-135">Presente somente nas versões [*X. 509*](../secgloss/x-gly.md) 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3efce-135">Present only in versions [*X.509*](../secgloss/x-gly.md) 2.0 or later.</span></span><br/> |
| <span data-ttu-id="3efce-136">ID exclusiva da entidade</span><span class="sxs-lookup"><span data-stu-id="3efce-136">Subject unique ID</span></span> | <span data-ttu-id="3efce-137">Usado para tornar o nome da entidade inequívoca se ele tiver sido usado por mais de uma entidade.</span><span class="sxs-lookup"><span data-stu-id="3efce-137">Used to make the subject name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="3efce-138">Presente somente em X. 509 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3efce-138">Present only in X.509 2.0 or later.</span></span><br/>                                                                     |
| <span data-ttu-id="3efce-139">Extensões</span><span class="sxs-lookup"><span data-stu-id="3efce-139">Extensions</span></span>        | <span data-ttu-id="3efce-140">Para especificar as propriedades personalizadas desejadas.</span><span class="sxs-lookup"><span data-stu-id="3efce-140">For specifying any desired custom properties.</span></span> <span data-ttu-id="3efce-141">Qualquer número de campos de extensão pode ser incluído no certificado.</span><span class="sxs-lookup"><span data-stu-id="3efce-141">Any number of extension fields can be included in the certificate.</span></span> <span data-ttu-id="3efce-142">Presente somente na versão X. 509 3,0.</span><span class="sxs-lookup"><span data-stu-id="3efce-142">Present only in version X.509 3.0.</span></span><br/>                                            |



 

> [!Note]  
> <span data-ttu-id="3efce-143">O Microsoft Certificate Services emite certificados X. 509 versão 3.</span><span class="sxs-lookup"><span data-stu-id="3efce-143">Microsoft Certificate Services issues X.509 version 3 certificates.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3efce-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3efce-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3efce-145">Propriedades do nome</span><span class="sxs-lookup"><span data-stu-id="3efce-145">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
