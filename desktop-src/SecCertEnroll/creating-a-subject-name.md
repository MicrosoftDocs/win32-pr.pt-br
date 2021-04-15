---
description: Você pode usar a interface IX500DistinguishedName para criar um nome de entidade a partir de uma cadeia de caracteres de nome distinto.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Criando um nome de entidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501337"
---
# <a name="creating-a-subject-name"></a><span data-ttu-id="2b3dc-103">Criando um nome de entidade</span><span class="sxs-lookup"><span data-stu-id="2b3dc-103">Creating a Subject Name</span></span>

<span data-ttu-id="2b3dc-104">Você pode usar a interface [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) para criar um nome de entidade a partir de uma cadeia de caracteres de nome distinto.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-104">You can use the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) interface to create a subject name from a distinguished name string.</span></span> <span data-ttu-id="2b3dc-105">A cadeia de caracteres consiste em nomes distintos relativos (RDNs) concatenados.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-105">The string consists of concatenated relative distinguished names (RDNs).</span></span> <span data-ttu-id="2b3dc-106">As seguintes chaves RDN são suportadas pela API de registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-106">The following RDN keys are supported by the Certificate Enrollment API.</span></span>

| <span data-ttu-id="2b3dc-107">Chave</span><span class="sxs-lookup"><span data-stu-id="2b3dc-107">Key</span></span>                               | <span data-ttu-id="2b3dc-108">OID</span><span class="sxs-lookup"><span data-stu-id="2b3dc-108">OID</span></span>                                             | <span data-ttu-id="2b3dc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b3dc-109">Description</span></span>                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3dc-110">C</span><span class="sxs-lookup"><span data-stu-id="2b3dc-110">C</span></span><br/>                      | <span data-ttu-id="2b3dc-111">\_nome do \_ país do OID do XCN \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-111">XCN\_OID\_COUNTRY\_NAME</span></span><br/>              | <span data-ttu-id="2b3dc-112">Contém um código de país ou região ISO 3166 de duas letras.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-112">Contains a two-letter ISO 3166 country or region code.</span></span><br/>                                  |
| <span data-ttu-id="2b3dc-113">CN</span><span class="sxs-lookup"><span data-stu-id="2b3dc-113">CN</span></span><br/>                     | <span data-ttu-id="2b3dc-114">\_ \_ nome comum do OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-114">XCN\_OID\_COMMON\_NAME</span></span><br/>               | <span data-ttu-id="2b3dc-115">Contém um nome comum.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-115">Contains a common name.</span></span><br/>                                                                 |
| <span data-ttu-id="2b3dc-116">E</span><span class="sxs-lookup"><span data-stu-id="2b3dc-116">E</span></span><br/> <span data-ttu-id="2b3dc-117">Email</span><span class="sxs-lookup"><span data-stu-id="2b3dc-117">EMAIL</span></span><br/>     | <span data-ttu-id="2b3dc-118">XCN \_ OID \_ RSA \_ emailAddr</span><span class="sxs-lookup"><span data-stu-id="2b3dc-118">XCN\_OID\_RSA\_emailAddr</span></span><br/>             | <span data-ttu-id="2b3dc-119">Contém um endereço de email.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-119">Contains an email address.</span></span><br/>                                                              |
| <span data-ttu-id="2b3dc-120">DC</span><span class="sxs-lookup"><span data-stu-id="2b3dc-120">DC</span></span><br/>                     | <span data-ttu-id="2b3dc-121">componente de domínio do XCN \_ OID \_ \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-121">XCN\_OID\_DOMAIN\_COMPONENT</span></span><br/>          | <span data-ttu-id="2b3dc-122">Contém uma parte de um nome DNS (sistema de nomes de domínio).</span><span class="sxs-lookup"><span data-stu-id="2b3dc-122">Contains one part of a Domain Name System (DNS) name.</span></span><br/>                                   |
| <span data-ttu-id="2b3dc-123">G</span><span class="sxs-lookup"><span data-stu-id="2b3dc-123">G</span></span><br/> <span data-ttu-id="2b3dc-124">GivenName</span><span class="sxs-lookup"><span data-stu-id="2b3dc-124">GivenName</span></span><br/> | <span data-ttu-id="2b3dc-125">\_nome do OID XCN \_ fornecido \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-125">XCN\_OID\_GIVEN\_NAME</span></span><br/>                | <span data-ttu-id="2b3dc-126">Contém a parte do nome de uma pessoa que não é um sobrenome.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-126">Contains the part of a person's name that is not a surname.</span></span><br/>                             |
| <span data-ttu-id="2b3dc-127">I</span><span class="sxs-lookup"><span data-stu-id="2b3dc-127">I</span></span><br/>                      | <span data-ttu-id="2b3dc-128">\_iniciais do OID do XCN \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-128">XCN\_OID\_INITIALS</span></span><br/>                   | <span data-ttu-id="2b3dc-129">Contém as iniciais de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-129">Contains a person's initials.</span></span><br/>                                                           |
| <span data-ttu-id="2b3dc-130">L</span><span class="sxs-lookup"><span data-stu-id="2b3dc-130">L</span></span><br/>                      | <span data-ttu-id="2b3dc-131">\_nome de \_ localidade do OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-131">XCN\_OID\_LOCALITY\_NAME</span></span><br/>             | <span data-ttu-id="2b3dc-132">Contém o nome de localidade que identifica uma cidade, país ou outra região geográfica.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-132">Contains the locality name that identifies a city, country, or other geographic region.</span></span><br/> |
| <span data-ttu-id="2b3dc-133">O</span><span class="sxs-lookup"><span data-stu-id="2b3dc-133">O</span></span><br/>                      | <span data-ttu-id="2b3dc-134">\_nome da \_ organização do OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-134">XCN\_OID\_ORGANIZATION\_NAME</span></span><br/>         | <span data-ttu-id="2b3dc-135">Contém o nome de uma organização.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-135">Contains the name of an organization.</span></span><br/>                                                   |
| <span data-ttu-id="2b3dc-136">OU</span><span class="sxs-lookup"><span data-stu-id="2b3dc-136">OU</span></span><br/>                     | <span data-ttu-id="2b3dc-137">\_nome da \_ \_ unidade organizacional XCN OID \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-137">XCN\_OID\_ORGANIZATIONAL\_UNIT\_NAME</span></span><br/> | <span data-ttu-id="2b3dc-138">Contém o nome de uma subdivisão de unidade em uma organização.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-138">Contains the name of a unit subdivision within an organization.</span></span><br/>                         |
| <span data-ttu-id="2b3dc-139">S</span><span class="sxs-lookup"><span data-stu-id="2b3dc-139">S</span></span><br/> <span data-ttu-id="2b3dc-140">ST</span><span class="sxs-lookup"><span data-stu-id="2b3dc-140">ST</span></span><br/>        | <span data-ttu-id="2b3dc-141">\_ \_ \_ \_ nome ou província \_ do XCN OID</span><span class="sxs-lookup"><span data-stu-id="2b3dc-141">XCN\_OID\_STATE\_OR\_PROVINCE\_NAME</span></span><br/>  | <span data-ttu-id="2b3dc-142">Contém o nome completo de um Estado ou província.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-142">Contains the full name of a state or province.</span></span><br/>                                          |
| <span data-ttu-id="2b3dc-143">RUA</span><span class="sxs-lookup"><span data-stu-id="2b3dc-143">STREET</span></span><br/>                 | <span data-ttu-id="2b3dc-144">\_endereço do OID do XCN \_ \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-144">XCN\_OID\_STREET\_ADDRESS</span></span><br/>            | <span data-ttu-id="2b3dc-145">Contém o endereço físico.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-145">Contains the physical address.</span></span><br/>                                                          |
| <span data-ttu-id="2b3dc-146">SN</span><span class="sxs-lookup"><span data-stu-id="2b3dc-146">SN</span></span><br/>                     | <span data-ttu-id="2b3dc-147">\_nome do \_ sur do OID do XCN \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-147">XCN\_OID\_SUR\_NAME</span></span><br/>                  | <span data-ttu-id="2b3dc-148">Contém o nome da família de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-148">Contains the family name of a person.</span></span><br/>                                                   |
| <span data-ttu-id="2b3dc-149">T</span><span class="sxs-lookup"><span data-stu-id="2b3dc-149">T</span></span><br/> <span data-ttu-id="2b3dc-150">TITLE</span><span class="sxs-lookup"><span data-stu-id="2b3dc-150">TITLE</span></span><br/>     | <span data-ttu-id="2b3dc-151">\_título do OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="2b3dc-151">XCN\_OID\_TITLE</span></span><br/>                      | <span data-ttu-id="2b3dc-152">Contém o título de uma pessoa na organização.</span><span class="sxs-lookup"><span data-stu-id="2b3dc-152">Contains the title of a person in the organization.</span></span><br/>                                     |



 

<span data-ttu-id="2b3dc-153">Ao inicializar um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , você pode identificar o formato do nome distinto especificando um valor do tipo de enumeração [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) .</span><span class="sxs-lookup"><span data-stu-id="2b3dc-153">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, you can identify the format of the distinguished name by specifying a value from the [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) enumeration type.</span></span> <span data-ttu-id="2b3dc-154">Por exemplo, suponha que o nome distinto da entidade consiste no seguinte RDNs:</span><span class="sxs-lookup"><span data-stu-id="2b3dc-154">For example, assume that the subject distinguished name consists of the following RDNs:</span></span><dl> <span data-ttu-id="2b3dc-155">CN = administrador</span><span class="sxs-lookup"><span data-stu-id="2b3dc-155">CN=Administrator</span></span>  
<span data-ttu-id="2b3dc-156">CN = usuários</span><span class="sxs-lookup"><span data-stu-id="2b3dc-156">CN=Users</span></span>  
<span data-ttu-id="2b3dc-157">DC = jdomcsc</span><span class="sxs-lookup"><span data-stu-id="2b3dc-157">DC=jdomcsc</span></span>  
<span data-ttu-id="2b3dc-158">DC = nttest</span><span class="sxs-lookup"><span data-stu-id="2b3dc-158">DC=nttest</span></span>  
<span data-ttu-id="2b3dc-159">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="2b3dc-159">DC=microsoft</span></span>  
<span data-ttu-id="2b3dc-160">DC = com</span><span class="sxs-lookup"><span data-stu-id="2b3dc-160">DC=com</span></span>  
</dl>

<span data-ttu-id="2b3dc-161">Se você concatenar esses RDNs na cadeia de caracteres de nome distinto delimitada por vírgulas a seguir, poderá especificar o valor do **\_ \_ \_ \_ \_ sinalizador de vírgula Str de nome de certificado XCN** ao inicializar um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .</span><span class="sxs-lookup"><span data-stu-id="2b3dc-161">If you concatenate these RDNs into the following comma-delimited distinguished name string, you can specify the **XCN\_CERT\_NAME\_STR\_COMMA\_FLAG** value when initializing an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object.</span></span>

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a><span data-ttu-id="2b3dc-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b3dc-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b3dc-163">Codificando um nome de entidade</span><span class="sxs-lookup"><span data-stu-id="2b3dc-163">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)
</dt> <dt>

[<span data-ttu-id="2b3dc-164">Nomes de Entidades</span><span class="sxs-lookup"><span data-stu-id="2b3dc-164">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 




