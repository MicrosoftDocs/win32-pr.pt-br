---
description: Usar funções de CryptoAPI para gerenciar repositórios de certificados e certificados, listas de certificados revogados e listas de certificados confiáveis nessas lojas.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Gerenciando certificados com repositórios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570966"
---
# <a name="managing-certificates-with-certificate-stores"></a><span data-ttu-id="f5470-103">Gerenciando certificados com repositórios de certificados</span><span class="sxs-lookup"><span data-stu-id="f5470-103">Managing Certificates with Certificate Stores</span></span>

<span data-ttu-id="f5470-104">Durante um período de tempo, os [*certificados*](../secgloss/c-gly.md) serão acumulados no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="f5470-104">Over a period of time, [*certificates*](../secgloss/c-gly.md) will accumulate on a user's computer.</span></span> <span data-ttu-id="f5470-105">As ferramentas são necessárias para gerenciar esses certificados.</span><span class="sxs-lookup"><span data-stu-id="f5470-105">Tools are required to manage these certificates.</span></span> <span data-ttu-id="f5470-106">O [*CryptoAPI*](../secgloss/c-gly.md) fornece essas ferramentas como funções para armazenar, recuperar, excluir, listar (enumerar) e verificar certificados.</span><span class="sxs-lookup"><span data-stu-id="f5470-106">[*CryptoAPI*](../secgloss/c-gly.md) provides those tools as functions to store, retrieve, delete, list (enumerate), and verify certificates.</span></span> <span data-ttu-id="f5470-107">O CryptoAPI também fornece os meios para anexar certificados a mensagens.</span><span class="sxs-lookup"><span data-stu-id="f5470-107">CryptoAPI also provides the means to attach certificates to messages.</span></span>

<span data-ttu-id="f5470-108">A CryptoAPI oferece duas categorias principais de funções para gerenciar certificados: funções que gerenciam [*repositórios de certificados*](../secgloss/c-gly.md)e funções que funcionam com certificados, CRLs ( [*listas de certificados revogados*](../secgloss/c-gly.md) ) e [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) nesses armazenamentos.</span><span class="sxs-lookup"><span data-stu-id="f5470-108">CryptoAPI offers two main categories of functions for managing certificates: functions that manage [*certificate stores*](../secgloss/c-gly.md), and functions that work with the certificates, [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) within those stores.</span></span>

<span data-ttu-id="f5470-109">As funções que gerenciam os [*repositórios de certificados*](../secgloss/c-gly.md) incluem funções para trabalhar com [*repositórios*](../secgloss/v-gly.md)lógicos ou virtuais, [*repositórios remotos*](../secgloss/r-gly.md), [*repositórios externos*](../secgloss/e-gly.md)e repositórios que podem ser realocados.</span><span class="sxs-lookup"><span data-stu-id="f5470-109">The functions that manage [*certificate stores*](../secgloss/c-gly.md) include functions for working with logical or [*virtual stores*](../secgloss/v-gly.md), [*remote stores*](../secgloss/r-gly.md), [*external stores*](../secgloss/e-gly.md), and stores that can be relocated.</span></span>

<span data-ttu-id="f5470-110">Certificados, [*CRLs*](../secgloss/c-gly.md)e [*CTLs*](../secgloss/c-gly.md) podem ser mantidos e mantidos em [*repositórios de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f5470-110">Certificates, [*CRLs*](../secgloss/c-gly.md), and [*CTLs*](../secgloss/c-gly.md) can be kept and maintained in [*certificate stores*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="f5470-111">Eles podem ser recuperados de uma loja em que foram persistidos para uso em processos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="f5470-111">They can be retrieved from a store where they have been persisted for use in authentication processes.</span></span>

<span data-ttu-id="f5470-112">O [*repositório de certificados*](../secgloss/c-gly.md) é fundamental para toda a funcionalidade de certificado.</span><span class="sxs-lookup"><span data-stu-id="f5470-112">The [*certificate store*](../secgloss/c-gly.md) is central to all certificate functionality.</span></span> <span data-ttu-id="f5470-113">Os certificados são gerenciados no armazenamento usando funções com um prefixo "CERT".</span><span class="sxs-lookup"><span data-stu-id="f5470-113">The certificates are managed in the store using functions with a "Cert" prefix.</span></span> <span data-ttu-id="f5470-114">Um repositório de certificados típico é uma lista vinculada de [*certificados*](../secgloss/c-gly.md) , conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5470-114">A typical certificate store is a linked list of [*certificates*](../secgloss/c-gly.md) as shown in the following illustration.</span></span>

![repositório de certificados](images/certstore1.png)

<span data-ttu-id="f5470-116">A ilustração anterior mostra:</span><span class="sxs-lookup"><span data-stu-id="f5470-116">The preceding illustration shows:</span></span>

-   <span data-ttu-id="f5470-117">Cada [*repositório de certificados*](../secgloss/c-gly.md) tem um ponteiro para o primeiro bloco de certificado nesse armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f5470-117">Each [*certificate store*](../secgloss/c-gly.md) has a pointer to the first certificate block in that store.</span></span>
-   <span data-ttu-id="f5470-118">Um bloco de certificado inclui um ponteiro para os dados desse certificado e um ponteiro "próximo" para o próximo bloco de certificado no repositório.</span><span class="sxs-lookup"><span data-stu-id="f5470-118">A certificate block includes a pointer to that certificate's data and a "next" pointer to the next certificate block in the store.</span></span>
-   <span data-ttu-id="f5470-119">O ponteiro "Next" no último bloco de certificado é definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f5470-119">The "next" pointer in the last certificate block is set to **NULL**.</span></span>
-   <span data-ttu-id="f5470-120">O bloco de dados de um certificado contém o contexto de certificado somente leitura e todas as propriedades estendidas do certificado.</span><span class="sxs-lookup"><span data-stu-id="f5470-120">The data block of a certificate contains the read-only certificate context and any extended properties of the certificate.</span></span>
-   <span data-ttu-id="f5470-121">O bloco de dados de cada certificado contém uma [*contagem de referência*](../secgloss/r-gly.md) que controla o número de ponteiros para o certificado existente.</span><span class="sxs-lookup"><span data-stu-id="f5470-121">The data block of each certificate contains a [*reference count*](../secgloss/r-gly.md) that keeps track of the number of pointers to the certificate that exist.</span></span>

<span data-ttu-id="f5470-122">Os certificados em um [*repositório de certificados*](../secgloss/c-gly.md) normalmente são mantidos em algum tipo de armazenamento permanente, como um arquivo de disco ou o registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="f5470-122">Certificates in a [*certificate store*](../secgloss/c-gly.md) are normally kept in some kind of permanent storage such as a disk file or the system registry.</span></span> <span data-ttu-id="f5470-123">Os repositórios de certificados também podem ser criados e abertos estritamente na memória.</span><span class="sxs-lookup"><span data-stu-id="f5470-123">Certificate stores can also be created and opened strictly in memory.</span></span> <span data-ttu-id="f5470-124">Um armazenamento de memória fornece armazenamento de certificado temporário para trabalhar com certificados que não precisam ser mantidos.</span><span class="sxs-lookup"><span data-stu-id="f5470-124">A memory store provides temporary certificate storage for working with certificates that do not need to be kept.</span></span>

<span data-ttu-id="f5470-125">Locais de armazenamento adicionais permitem que as lojas sejam mantidas e pesquisadas em várias partes do registro de um computador local ou, com as permissões adequadas definidas, no registro em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="f5470-125">Additional store locations allow stores to be kept and searched in various parts of a local computer's registry or, with proper permissions set, in the registry on a remote computer.</span></span>

<span data-ttu-id="f5470-126">Cada usuário tem uma minha loja pessoal na qual os certificados desse usuário estão armazenados.</span><span class="sxs-lookup"><span data-stu-id="f5470-126">Each user has a personal My store where that user's certificates are stored.</span></span> <span data-ttu-id="f5470-127">O meu repositório pode estar em qualquer um dos vários locais físicos, incluindo o registro em um computador local ou remoto, um arquivo de disco, um banco de dados, um serviço de diretório, um [*cartão inteligente*](../secgloss/s-gly.md)ou outro local.</span><span class="sxs-lookup"><span data-stu-id="f5470-127">The My store can be at any one of many physical locations, including the registry on a local or remote computer, a disk file, a database, directory service, a [*smart card*](../secgloss/s-gly.md), or another location.</span></span> <span data-ttu-id="f5470-128">Embora qualquer certificado possa ser armazenado no meu repositório, esse armazenamento deve ser reservado para os certificados pessoais de um usuário: os certificados usados para assinar e descriptografar as mensagens desse usuário.</span><span class="sxs-lookup"><span data-stu-id="f5470-128">While any certificate can be stored in the My store, this store should be reserved for a user's personal certificates: those certificates used for signing and decrypting that user's messages.</span></span>

<span data-ttu-id="f5470-129">O uso de certificados para autenticação depende de ter certificados emitidos por algum emissor de certificado confiável.</span><span class="sxs-lookup"><span data-stu-id="f5470-129">Using certificates for authentication depends on having certificates issued by some trusted certificate issuer.</span></span> <span data-ttu-id="f5470-130">Certificados para emissores de certificados confiáveis normalmente são mantidos no armazenamento raiz, que é persistido atualmente em uma subchave do registro.</span><span class="sxs-lookup"><span data-stu-id="f5470-130">Certificates for trusted certificate issuers are typically kept in the Root store, which is currently persisted to a registry subkey.</span></span> <span data-ttu-id="f5470-131">No contexto de CryptoAPI, o armazenamento raiz é protegido e as caixas de diálogo da interface do usuário lembram o usuário para posicionar apenas os certificados confiáveis nesse armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f5470-131">In the CryptoAPI context, the Root store is protected, and user interface dialog boxes remind the user to place only trusted certificates into that store.</span></span> <span data-ttu-id="f5470-132">Em situações de rede corporativa, os certificados podem ser enviados por push (copiados) por um administrador do sistema do computador do controlador de domínio para os armazenamentos raiz em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="f5470-132">In enterprise network situations, certificates might be pushed (copied) by a system administrator from the domain controller computer to the Root stores on client computers.</span></span> <span data-ttu-id="f5470-133">Esse processo fornece todos os membros de um domínio com listas de confiança semelhantes.</span><span class="sxs-lookup"><span data-stu-id="f5470-133">This process provides all members of a domain with similar trust lists.</span></span>

<span data-ttu-id="f5470-134">Outros certificados podem ser armazenados no repositório do sistema de [*autoridade de certificação*](../secgloss/c-gly.md) (CA) ou em armazenamentos baseados em arquivo, criados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f5470-134">Other certificates can be stored in the [*certification authority*](../secgloss/c-gly.md) (CA) system store or in user-created, file-based stores.</span></span>

<span data-ttu-id="f5470-135">Para obter listas de funções para usar e manter repositórios de certificados, consulte [funções de repositório de certificados](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f5470-135">For lists of functions for using and maintaining certificate stores, see [Certificate Store Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="f5470-136">Para obter um exemplo que usa algumas dessas funções, consulte [exemplo C programa: operações de repositório de certificados](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f5470-136">For an example that uses some of these functions, see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5470-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5470-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5470-138">Gerenciando um estado de repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="f5470-138">Managing a Certificate Store State</span></span>](managing-a-certificate-store-state.md)
</dt> <dt>

[<span data-ttu-id="f5470-139">Trabalhando com certificados em repositórios de certificados</span><span class="sxs-lookup"><span data-stu-id="f5470-139">Working with Certificates in Certificate Stores</span></span>](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[<span data-ttu-id="f5470-140">Links de certificado</span><span class="sxs-lookup"><span data-stu-id="f5470-140">Certificate Links</span></span>](certificate-links.md)
</dt> <dt>

[<span data-ttu-id="f5470-141">Repositórios de coleta</span><span class="sxs-lookup"><span data-stu-id="f5470-141">Collection Stores</span></span>](collection-stores.md)
</dt> <dt>

[<span data-ttu-id="f5470-142">Repositórios lógicos e físicos</span><span class="sxs-lookup"><span data-stu-id="f5470-142">Logical and Physical Stores</span></span>](logical-and-physical-stores.md)
</dt> <dt>

[<span data-ttu-id="f5470-143">Locais de armazenamento do sistema</span><span class="sxs-lookup"><span data-stu-id="f5470-143">System Store Locations</span></span>](system-store-locations.md)
</dt> <dt>

[<span data-ttu-id="f5470-144">Migração do repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="f5470-144">Certificate Store Migration</span></span>](certificate-store-migration.md)
</dt> </dl>

 

 
