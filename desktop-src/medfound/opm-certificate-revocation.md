---
description: Revogação de certificado OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revogação de certificado OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092724"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="5cbd8-103">Revogação de certificado OPM</span><span class="sxs-lookup"><span data-stu-id="5cbd8-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="5cbd8-104">Um certificado do Gerenciador de proteção de saída (OPM) pode ser revogado pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="5cbd8-105">A lista de certificados revogados é armazenada em uma lista de revogação global (GRL).</span><span class="sxs-lookup"><span data-stu-id="5cbd8-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="5cbd8-106">O GRL tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="5cbd8-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cbd8-107">Seção</span><span class="sxs-lookup"><span data-stu-id="5cbd8-107">Section</span></span></th>
<th><span data-ttu-id="5cbd8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cbd8-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5cbd8-109">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5cbd8-109">Header</span></span></td>
<td><span data-ttu-id="5cbd8-110">Uma estrutura de <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5cbd8-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cbd8-111">Core</span><span class="sxs-lookup"><span data-stu-id="5cbd8-111">Core</span></span></td>
<td><span data-ttu-id="5cbd8-112">Contém as seguintes listas de revogação:</span><span class="sxs-lookup"><span data-stu-id="5cbd8-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="5cbd8-113">Revogações binárias de kernel</span><span class="sxs-lookup"><span data-stu-id="5cbd8-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="5cbd8-114">Revogações binárias de modo de usuário</span><span class="sxs-lookup"><span data-stu-id="5cbd8-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="5cbd8-115">Revogações de certificado</span><span class="sxs-lookup"><span data-stu-id="5cbd8-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="5cbd8-116">Raízes confiáveis (reservadas)</span><span class="sxs-lookup"><span data-stu-id="5cbd8-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="5cbd8-117">A lista de raízes confiáveis não é usada no momento e é reservada para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cbd8-118">Entradas extensível</span><span class="sxs-lookup"><span data-stu-id="5cbd8-118">Extensible entries</span></span></td>
<td><span data-ttu-id="5cbd8-119">Contém informações usadas por outros componentes.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-119">Contains information used by other components.</span></span> <span data-ttu-id="5cbd8-120">Esta seção não é relevante para OPM.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cbd8-121">Renovações</span><span class="sxs-lookup"><span data-stu-id="5cbd8-121">Renewals:</span></span></td>
<td><span data-ttu-id="5cbd8-122">Contém GUIDs que definem Windows Update identificadores.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="5cbd8-123">Esta seção contém identificadores para as seguintes listas:</span><span class="sxs-lookup"><span data-stu-id="5cbd8-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="5cbd8-124">Revogações binárias de kernel</span><span class="sxs-lookup"><span data-stu-id="5cbd8-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="5cbd8-125">Revogações binárias de modo de usuário</span><span class="sxs-lookup"><span data-stu-id="5cbd8-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="5cbd8-126">Revogações de certificado</span><span class="sxs-lookup"><span data-stu-id="5cbd8-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="5cbd8-127">Um aplicativo pode usar esses identificadores para solicitar uma versão renovada de um binário revogado, se houver um disponível.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cbd8-128">Assinatura: seção principal</span><span class="sxs-lookup"><span data-stu-id="5cbd8-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="5cbd8-129">Assina as seções de cabeçalho e núcleo.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cbd8-130">Assinatura: seção extensível</span><span class="sxs-lookup"><span data-stu-id="5cbd8-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="5cbd8-131">Assina o cabeçalho e as seções extensíveis.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5cbd8-132">O cabeçalho GRL é uma estrutura de [**\_ cabeçalho grl**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="5cbd8-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="5cbd8-133">O membro **dwSequenceNumber** da estrutura contém o número de versão grl.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="5cbd8-134">Esse número é incrementado sempre que o GRL é atualizado e uma nova versão colocada no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="5cbd8-135">Os certificados OPMs revogados são listados na lista de revogações de certificados da seção principal.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="5cbd8-136">Cada entrada principal no GRL é uma matriz de 20 bytes que contém o hash SHA-1 da chave pública do certificado revogado.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="5cbd8-137">As seções de assinatura contêm assinaturas que podem ser usadas para verificar se o GRL não foi violado.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="5cbd8-138">Cada seção de assinatura contém a estrutura de [**\_ assinatura am MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="5cbd8-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="5cbd8-139">A primeira assinatura assina o cabeçalho mais a seção principal.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="5cbd8-140">A segunda assinatura assina o cabeçalho mais a seção extensível; Essa assinatura não é relevante para OPM.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="5cbd8-141">Para garantir que o próprio GRL não tenha sido adulterado, verifique a assinatura da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5cbd8-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="5cbd8-142">Localize o início da estrutura [**de \_ assinatura MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="5cbd8-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="5cbd8-143">O local da estrutura **de \_ assinatura MF** é fornecido no membro **cbSignatureCoreOffset** da estrutura do [**\_ cabeçalho grl**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="5cbd8-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="5cbd8-144">O local é especificado como um deslocamento em bytes do início do GRL.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="5cbd8-145">Analise a estrutura de [**\_ assinatura MF**](mf-signature.md) como uma \# assinatura PKCS 7 com uma cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="5cbd8-146">Verifique a cadeia de certificados para uma raiz confiável.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="5cbd8-147">Verifique se o certificado de folha tem o seguinte identificador de objeto no EKU: "1.3.6.1.4.1.311.10.5.4".</span><span class="sxs-lookup"><span data-stu-id="5cbd8-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="5cbd8-148">Computar um hash dos bytes que incluem o cabeçalho e as seções principais do GRL.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="5cbd8-149">Verifique se o hash corresponde à assinatura no certificado de folha.</span><span class="sxs-lookup"><span data-stu-id="5cbd8-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cbd8-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cbd8-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cbd8-151">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="5cbd8-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="5cbd8-152">**\_cabeçalho grl**</span><span class="sxs-lookup"><span data-stu-id="5cbd8-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="5cbd8-153">**\_assinatura MF**</span><span class="sxs-lookup"><span data-stu-id="5cbd8-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



