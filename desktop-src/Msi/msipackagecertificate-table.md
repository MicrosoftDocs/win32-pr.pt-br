---
description: A tabela MsiPackageCertificate lista os certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem essa Multiple-Package instalação.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabela MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172020"
---
# <a name="msipackagecertificate-table"></a><span data-ttu-id="77546-103">Tabela MsiPackageCertificate</span><span class="sxs-lookup"><span data-stu-id="77546-103">MsiPackageCertificate Table</span></span>

<span data-ttu-id="77546-104">A tabela MsiPackageCertificate lista os certificados de assinatura digital usados para verificar a identidade dos pacotes de instalação que fazem essa [instalação de vários pacotes](multiple-package-installations.md).</span><span class="sxs-lookup"><span data-stu-id="77546-104">The MsiPackageCertificate Table lists digital signature certificates used to verify the identity of the installation packages that make this [Multiple-Package Installation](multiple-package-installations.md).</span></span>

<span data-ttu-id="77546-105">Use esta tabela para criar uma [instalação de vários pacotes](multiple-package-installations.md) para um produto que contém vários pacotes de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="77546-105">Use this table to author a [multiple-package installation](multiple-package-installations.md) for a product containing multiple Windows Installer packages.</span></span> <span data-ttu-id="77546-106">Se o primeiro pacote for assinado digitalmente e contiver uma tabela MsiPackageCertificate especificando certificados digitais para todos os pacotes restantes do produto, o administrador precisará aceitar apenas o prompt do [*controle de conta de usuário*](u-gly.md) (UAC) exibido para o primeiro pacote.</span><span class="sxs-lookup"><span data-stu-id="77546-106">If the first package is digitally signed, and contains a MsiPackageCertificate Table specifying digital certificates for all the remaining packages in the product, the administrator needs only accept the [*User Account Control*](u-gly.md) (UAC) prompt displayed for the first package.</span></span> <span data-ttu-id="77546-107">Depois de aceitar o prompt do UAC para o primeiro pacote, as funções definidas pelo usuário na [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) podem então unir os pacotes restantes à instalação de vários pacotes sem exibir um prompt do UAC e exigir uma resposta de administrador para cada pacote.</span><span class="sxs-lookup"><span data-stu-id="77546-107">After accepting the UAC's prompt for the first package, the user-defined functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) can then join the remaining packages to the multiple-package installation without displaying a UAC prompt and requiring an administrator response for each package.</span></span>

<span data-ttu-id="77546-108">Se uma ou mais das funções na [tabela MsiEmbeddedChainer](msiembeddedchainer-table.md) solicitarem um pacote não assinado, outro prompt do UAC que exigir a interação do administrador será exibido para cada pacote não assinado.</span><span class="sxs-lookup"><span data-stu-id="77546-108">If one or more of the functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) request an unsigned package, another UAC prompt requiring administrator interaction is displayed for each unsigned package.</span></span> <span data-ttu-id="77546-109">Se o administrador aceitar esse prompt do UAC, a instalação de vários pacotes continuará.</span><span class="sxs-lookup"><span data-stu-id="77546-109">If the administrator accepts this UAC prompt, the multi-package installation continues.</span></span> <span data-ttu-id="77546-110">Depois que um administrador tiver fornecido credenciais para um pacote, nenhum prompt do UAC será exibido novamente para esse pacote durante a instalação de vários pacotes.</span><span class="sxs-lookup"><span data-stu-id="77546-110">Once an administrator has provided credentials for a package, no UAC prompt will again be displayed for that package during this multi-package installation.</span></span> <span data-ttu-id="77546-111">Se o administrador rejeitar um prompt de UAC para um pacote, o Windows Installer reverterá a instalação de vários pacotes antes de confirmar a instalação de todos os pacotes pertencentes ao produto.</span><span class="sxs-lookup"><span data-stu-id="77546-111">If the administrator rejects a UAC prompt for a package, the Windows installer rolls back the multi-package installation before it commits to install any packages belonging to the product.</span></span>

<span data-ttu-id="77546-112">**[Windows Installer 4,0 ou anterior](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="77546-112">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="77546-113">Esta tabela está disponível a partir do Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="77546-113">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="77546-114">A tabela MsiPackageCertificate tem as seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="77546-114">The MsiPackageCertificate Table has the following columns:</span></span>



| <span data-ttu-id="77546-115">Coluna</span><span class="sxs-lookup"><span data-stu-id="77546-115">Column</span></span>               | <span data-ttu-id="77546-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="77546-116">Type</span></span>                         | <span data-ttu-id="77546-117">Chave</span><span class="sxs-lookup"><span data-stu-id="77546-117">Key</span></span> | <span data-ttu-id="77546-118">Nullable</span><span class="sxs-lookup"><span data-stu-id="77546-118">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="77546-119">PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="77546-119">PackageCertificate</span></span>   | [<span data-ttu-id="77546-120">Identificador</span><span class="sxs-lookup"><span data-stu-id="77546-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="77546-121">S</span><span class="sxs-lookup"><span data-stu-id="77546-121">Y</span></span>   | <span data-ttu-id="77546-122">N</span><span class="sxs-lookup"><span data-stu-id="77546-122">N</span></span>        |
| <span data-ttu-id="77546-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="77546-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="77546-124">Identificador</span><span class="sxs-lookup"><span data-stu-id="77546-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="77546-125">N</span><span class="sxs-lookup"><span data-stu-id="77546-125">N</span></span>   | <span data-ttu-id="77546-126">N</span><span class="sxs-lookup"><span data-stu-id="77546-126">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="77546-127">Colunas</span><span class="sxs-lookup"><span data-stu-id="77546-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="77546-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="77546-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span></span>
</dt> <dd>

<span data-ttu-id="77546-129">O identificador exclusivo para esta linha na tabela MsiPackageCertificate.</span><span class="sxs-lookup"><span data-stu-id="77546-129">The unique identifier for this row in the MsiPackageCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="77546-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="77546-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="77546-131">Uma chave externa na primeira coluna da [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="77546-131">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="77546-132">A linha indicada na tabela MsiDigitalCertificate contém a representação binária do certificado de signatário.</span><span class="sxs-lookup"><span data-stu-id="77546-132">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="77546-133">Validação</span><span class="sxs-lookup"><span data-stu-id="77546-133">Validation</span></span>

<dl>

[<span data-ttu-id="77546-134">ICE39</span><span class="sxs-lookup"><span data-stu-id="77546-134">ICE39</span></span>](ice39.md)  
[<span data-ttu-id="77546-135">ICE81</span><span class="sxs-lookup"><span data-stu-id="77546-135">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="77546-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77546-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77546-137">MsiEmbeddedChainer</span><span class="sxs-lookup"><span data-stu-id="77546-137">MsiEmbeddedChainer</span></span>](msiembeddedchainer-table.md)
</dt> <dt>

[<span data-ttu-id="77546-138">Tabela MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="77546-138">MsiDigitalCertificate Table</span></span>](msidigitalcertificate-table.md)
</dt> </dl>

 

 



