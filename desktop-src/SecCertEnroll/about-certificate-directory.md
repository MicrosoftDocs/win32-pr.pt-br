---
description: Uma PKI (infraestrutura de chave pública) do Windows salva certificados no servidor que hospeda a autoridade de certificação (CA) e no computador ou dispositivo local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Certificar o diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172154"
---
# <a name="certificate-directory"></a><span data-ttu-id="7885f-103">Certificar o diretório</span><span class="sxs-lookup"><span data-stu-id="7885f-103">Certificate Directory</span></span>

<span data-ttu-id="7885f-104">Uma PKI (infraestrutura de chave pública) do Windows salva certificados no servidor que hospeda a autoridade de certificação (CA) e no computador ou dispositivo local.</span><span class="sxs-lookup"><span data-stu-id="7885f-104">A Windows public key infrastructure (PKI) saves certificates on the server that hosts the certification authority (CA) and on the local computer or device.</span></span> <span data-ttu-id="7885f-105">O armazenamento de CA é normalmente chamado de banco de dados de certificado, e o armazenamento local é conhecido como o repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="7885f-105">CA storage is typically referred to as the certificate database, and local storage is known as the certificate store.</span></span>

## <a name="certificate-database"></a><span data-ttu-id="7885f-106">Banco de dados de certificados</span><span class="sxs-lookup"><span data-stu-id="7885f-106">Certificate Database</span></span>

<span data-ttu-id="7885f-107">Quando você adiciona os serviços de certificados em um servidor Windows e configura uma AC, um banco de dados de certificado é criado.</span><span class="sxs-lookup"><span data-stu-id="7885f-107">When you add Certificate Services on a Windows server and configure a CA, a certificate database is created.</span></span> <span data-ttu-id="7885f-108">Por padrão, o banco de dados está contido na pasta *% systemroot%* \\ System32 \\ Certlog e o nome é baseado no nome da autoridade de certificação com uma extensão. edb.</span><span class="sxs-lookup"><span data-stu-id="7885f-108">By default, the database is contained in the *%SystemRoot%*\\System32\\Certlog folder, and the name is based on the CA name with an .edb extension.</span></span> <span data-ttu-id="7885f-109">O banco de dados pode conter:</span><span class="sxs-lookup"><span data-stu-id="7885f-109">The database can contain:</span></span>

-   <span data-ttu-id="7885f-110">Certificados emitidos</span><span class="sxs-lookup"><span data-stu-id="7885f-110">Issued certificates</span></span>
-   <span data-ttu-id="7885f-111">Certificados revogados</span><span class="sxs-lookup"><span data-stu-id="7885f-111">Revoked certificates</span></span>
-   <span data-ttu-id="7885f-112">Chaves privadas arquivadas</span><span class="sxs-lookup"><span data-stu-id="7885f-112">Archived private keys</span></span>
-   <span data-ttu-id="7885f-113">Solicitações de certificado</span><span class="sxs-lookup"><span data-stu-id="7885f-113">Certificate requests</span></span>

<span data-ttu-id="7885f-114">Você não pode usar a API de registro de certificado para manipular o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7885f-114">You cannot use the Certificate Enrollment API to manipulate the database.</span></span> <span data-ttu-id="7885f-115">O processo de registro cria automaticamente as entradas necessárias.</span><span class="sxs-lookup"><span data-stu-id="7885f-115">The enrollment process automatically creates the necessary entries.</span></span>

## <a name="certificate-stores"></a><span data-ttu-id="7885f-116">Repositórios de certificados</span><span class="sxs-lookup"><span data-stu-id="7885f-116">Certificate Stores</span></span>

<span data-ttu-id="7885f-117">Os serviços de certificados da Microsoft copiam certificados emitidos e solicitações pendentes ou rejeitadas para computadores e dispositivos locais.</span><span class="sxs-lookup"><span data-stu-id="7885f-117">Microsoft Certificate Services copies issued certificates and pending or rejected requests to local computers and devices.</span></span> <span data-ttu-id="7885f-118">O local de armazenamento é chamado de repositório de certificados e consiste nos repositórios lógicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7885f-118">The storage location is called the certificate store and consists of the following logical stores.</span></span>

| <span data-ttu-id="7885f-119">Repositório lógico</span><span class="sxs-lookup"><span data-stu-id="7885f-119">Logical store</span></span>                                         | <span data-ttu-id="7885f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="7885f-120">Description</span></span>                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7885f-121">Pessoal</span><span class="sxs-lookup"><span data-stu-id="7885f-121">Personal</span></span><br/>                                   | <span data-ttu-id="7885f-122">Contém certificados associados a uma chave privada controlada pelo usuário ou computador.</span><span class="sxs-lookup"><span data-stu-id="7885f-122">Contains certificates associated with a private key controlled by the user or computer.</span></span><br/>                     |
| <span data-ttu-id="7885f-123">Autoridades de Certificação Confiáveis</span><span class="sxs-lookup"><span data-stu-id="7885f-123">Trusted Root Certification Authorities</span></span><br/>     | <span data-ttu-id="7885f-124">Contém certificados de CAs (autoridades de certificação) implicitamente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7885f-124">Contains certificates from implicitly trusted certification authorities (CAs).</span></span><br/>                              |
| <span data-ttu-id="7885f-125">Confiabilidade Empresarial</span><span class="sxs-lookup"><span data-stu-id="7885f-125">Enterprise Trust</span></span><br/>                           | <span data-ttu-id="7885f-126">Contém listas de certificados confiáveis normalmente usadas para confiar em certificados autoassinados de outras organizações.</span><span class="sxs-lookup"><span data-stu-id="7885f-126">Contains certificate trust lists typically used to trust self-signed certificates from other organizations.</span></span><br/> |
| <span data-ttu-id="7885f-127">Autoridades de Certificação Intermediárias</span><span class="sxs-lookup"><span data-stu-id="7885f-127">Intermediate Certification Authorities</span></span><br/>     | <span data-ttu-id="7885f-128">Contém certificados emitidos para ACs subordinadas na hierarquia de certificação.</span><span class="sxs-lookup"><span data-stu-id="7885f-128">Contains certificates issued to subordinate CAs in the certification hierarchy.</span></span><br/>                             |
| <span data-ttu-id="7885f-129">Objeto de Usuário do Active Directory</span><span class="sxs-lookup"><span data-stu-id="7885f-129">Active Directory User Object</span></span><br/>               | <span data-ttu-id="7885f-130">Contém o certificado de objeto do usuário ou os certificados publicados no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7885f-130">Contains the user object certificate or certificates published in Active Directory.</span></span><br/>                         |
| <span data-ttu-id="7885f-131">Editores Confiáveis</span><span class="sxs-lookup"><span data-stu-id="7885f-131">Trusted Publishers</span></span><br/>                         | <span data-ttu-id="7885f-132">Contém certificados de CAs confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7885f-132">Contains certificates from trusted CAs.</span></span><br/>                                                                     |
| <span data-ttu-id="7885f-133">Certificados Não Confiáveis</span><span class="sxs-lookup"><span data-stu-id="7885f-133">Untrusted Certificates</span></span><br/>                     | <span data-ttu-id="7885f-134">Contém certificados que foram identificados explicitamente como não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7885f-134">Contains certificates that have been explicitly identified as untrusted.</span></span><br/>                                    |
| <span data-ttu-id="7885f-135">Autoridades de Certificação Raiz de Terceiros</span><span class="sxs-lookup"><span data-stu-id="7885f-135">Third-Party Root Certification Authorities</span></span><br/> | <span data-ttu-id="7885f-136">Contém certificados raiz confiáveis de CAs fora da hierarquia de certificados internos.</span><span class="sxs-lookup"><span data-stu-id="7885f-136">Contains trusted root certificates from CAs outside the internal certificate hierarchy.</span></span><br/>                     |
| <span data-ttu-id="7885f-137">Pessoas de Confiança</span><span class="sxs-lookup"><span data-stu-id="7885f-137">Trusted People</span></span><br/>                             | <span data-ttu-id="7885f-138">Contém certificados emitidos para usuários ou entidades que foram explicitamente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7885f-138">Contains certificates issued to users or entities that have been explicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="7885f-139">Outras pessoas</span><span class="sxs-lookup"><span data-stu-id="7885f-139">Other People</span></span><br/>                               | <span data-ttu-id="7885f-140">Contém certificados emitidos para usuários ou entidades que foram implicitamente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="7885f-140">Contains certificates issued to users or entities that have been implicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="7885f-141">Solicitações de registro de certificado</span><span class="sxs-lookup"><span data-stu-id="7885f-141">Certificate Enrollment Requests</span></span><br/>            | <span data-ttu-id="7885f-142">Contém solicitações de certificado pendentes ou rejeitadas.</span><span class="sxs-lookup"><span data-stu-id="7885f-142">Contains pending or rejected certificate requests.</span></span><br/>                                                          |



 

<span data-ttu-id="7885f-143">Você não pode usar a API de registro de certificado para especificar ou recuperar propriedades de armazenamento ou copiar certificados para repositórios específicos.</span><span class="sxs-lookup"><span data-stu-id="7885f-143">You cannot use the Certificate Enrollment API to specify or retrieve store properties or copy certificates to specific stores.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7885f-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7885f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7885f-145">Elementos PKI</span><span class="sxs-lookup"><span data-stu-id="7885f-145">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 




