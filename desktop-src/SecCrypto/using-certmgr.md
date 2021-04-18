---
description: Use o CertMgr para exibir certificados, CRLs e CTLs de um arquivo ou de um repositório de certificados, para copiar certificados em um repositório de certificados, para excluir certificados de um repositório de certificados e para salvar certificados em arquivos.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Usando CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753389"
---
# <a name="using-certmgr"></a><span data-ttu-id="64d8d-103">Usando CertMgr</span><span class="sxs-lookup"><span data-stu-id="64d8d-103">Using CertMgr</span></span>

<span data-ttu-id="64d8d-104">O [certmgr](certmgr.md) pode ser usado para exibir [*certificados*](../secgloss/c-gly.md), [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs) e listas de [*certificados confiáveis*](../secgloss/c-gly.md) (CTLs) de um arquivo ou de um repositório de certificados, para copiar certificados em um [*repositório de certificados*](../secgloss/c-gly.md), para excluir certificados de um repositório de certificados e para salvar certificados em arquivos.</span><span class="sxs-lookup"><span data-stu-id="64d8d-104">[CertMgr](certmgr.md) can be used to view [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) from a file or a certificate store, to copy certificates into a [*certificate store*](../secgloss/c-gly.md), to delete certificates from a certificate store, and to save certificates to files.</span></span>

<span data-ttu-id="64d8d-105">Quando [certmgr](certmgr.md) é usado sem opções, um assistente de certmgr é exibido para orientar o usuário durante a operação.</span><span class="sxs-lookup"><span data-stu-id="64d8d-105">When [CertMgr](certmgr.md) is used without options, a CertMgr wizard appears to guide the user through the operation.</span></span>

<span data-ttu-id="64d8d-106">O arquivo deve ser um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="64d8d-106">The file must be one of the following types:</span></span>

-   <span data-ttu-id="64d8d-107">Um arquivo de certificado, CRL ou CTL codificado (pode ser codificado em base-64)</span><span class="sxs-lookup"><span data-stu-id="64d8d-107">An encoded CTL, CRL, or certificate file (could be base-64 encoded)</span></span>
-   <span data-ttu-id="64d8d-108">Um \# arquivo PKCS 7</span><span class="sxs-lookup"><span data-stu-id="64d8d-108">A PKCS \#7 file</span></span>
-   <span data-ttu-id="64d8d-109">Um arquivo SPC</span><span class="sxs-lookup"><span data-stu-id="64d8d-109">An SPC file</span></span>
-   <span data-ttu-id="64d8d-110">Um documento assinado</span><span class="sxs-lookup"><span data-stu-id="64d8d-110">A signed document</span></span>
-   <span data-ttu-id="64d8d-111">Um StoreFile serializado</span><span class="sxs-lookup"><span data-stu-id="64d8d-111">A serialized storeFile</span></span>

<span data-ttu-id="64d8d-112">Os exemplos a seguir usam comandos [certmgr](certmgr.md) para executar tarefas comuns de certificado.</span><span class="sxs-lookup"><span data-stu-id="64d8d-112">The following examples use [CertMgr](certmgr.md) commands to perform common certificate tasks.</span></span>

-   <span data-ttu-id="64d8d-113">Exiba os certificados, as CRLs e as CTLs de *MyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="64d8d-113">View the certificates, CRLs, and CTLs from *MyFile.ext*.</span></span>

    <span data-ttu-id="64d8d-114">**certmgr** *MyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="64d8d-114">**certmgr** *MyFile.ext*</span></span>

-   <span data-ttu-id="64d8d-115">Exiba os certificados, as CRLs e as CTLs do meu repositório do sistema.</span><span class="sxs-lookup"><span data-stu-id="64d8d-115">View the certificates, CRLs, and CTLs from the MY system store.</span></span>

    <span data-ttu-id="64d8d-116">**Certmgr-s My**</span><span class="sxs-lookup"><span data-stu-id="64d8d-116">**certmgr -s my**</span></span>

-   <span data-ttu-id="64d8d-117">Copie todos os certificados, CRLs e CTLs em um arquivo chamado *MyFile. ext* para um novo arquivo, chamado *newfile. ext*.</span><span class="sxs-lookup"><span data-stu-id="64d8d-117">Copy all the certificates, CRLs, and CTLs in a file named *MyFile.ext* to a new file, called *NewFile.ext*.</span></span>

    <span data-ttu-id="64d8d-118">**certmgr-Add-All-c** *MyFile. ext* *newfile. ext*</span><span class="sxs-lookup"><span data-stu-id="64d8d-118">**certmgr -add -all -c** *MyFile.ext* *NewFile.ext*</span></span>

-   <span data-ttu-id="64d8d-119">Copie todos os certificados, CRLs e CTLs do meu repositório do sistema para um arquivo chamado *NewMyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="64d8d-119">Copy all the certificates, CRLs, and CTLs from the MY system store to a file called *NewMyFile.ext*.</span></span>

    <span data-ttu-id="64d8d-120">**certmgr-adicionar-tudo-c-s My** *NewMyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="64d8d-120">**certmgr -add -all -c -s my** *NewMyFile.ext*</span></span>

-   <span data-ttu-id="64d8d-121">Copie um certificado com o nome comum *MyCert* no meu armazenamento do sistema para um arquivo chamado *NewCert. cer*.</span><span class="sxs-lookup"><span data-stu-id="64d8d-121">Copy a certificate with the common name *MyCert* in the MY system store to a file called *NewCert.cer*.</span></span>

    <span data-ttu-id="64d8d-122">**certmgr-Add-c-n** *MyCert* **-s minha** *NewCert. cer*</span><span class="sxs-lookup"><span data-stu-id="64d8d-122">**certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*</span></span>

-   <span data-ttu-id="64d8d-123">Exclua todos os certificados do meu repositório do sistema.</span><span class="sxs-lookup"><span data-stu-id="64d8d-123">Delete all the certificates from the MY system store.</span></span>

    <span data-ttu-id="64d8d-124">**Certmgr-del-All-c-s meu**</span><span class="sxs-lookup"><span data-stu-id="64d8d-124">**certmgr -del -all -c -s my**</span></span>

-   <span data-ttu-id="64d8d-125">Exclua todas as CTLs do meu repositório do sistema e salve o repositório resultante em um arquivo chamado *NewStore. Str*.</span><span class="sxs-lookup"><span data-stu-id="64d8d-125">Delete all the CTLs from the MY system store and save the resulting store to a file called *NewStore.str*.</span></span>

    <span data-ttu-id="64d8d-126">**certmgr-del-All-CTL-s My** *NewStore. Str*</span><span class="sxs-lookup"><span data-stu-id="64d8d-126">**certmgr -del -all -ctl -s my** *NewStore.str*</span></span>

-   <span data-ttu-id="64d8d-127">Salve, em um arquivo chamado *NewCert. cer*, um certificado que é um certificado codificado [*X. 509*](../secgloss/x-gly.md) , que tem o nome comum *MyCert* e que está localizado no repositório de certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="64d8d-127">Save, to a file called *NewCert.cer*, a certificate that is an [*X.509*](../secgloss/x-gly.md) encoded certificate, that has the common name *MyCert*, and that is located in the Root certificate store.</span></span>

    <span data-ttu-id="64d8d-128">**certmgr-Put-c-n** *MyCert* **-s raiz** *NewCert. cer*</span><span class="sxs-lookup"><span data-stu-id="64d8d-128">**certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*</span></span>

## <a name="related-topics"></a><span data-ttu-id="64d8d-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64d8d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d8d-130">CertMgr</span><span class="sxs-lookup"><span data-stu-id="64d8d-130">CertMgr</span></span>](certmgr.md)
</dt> </dl>

 

 
