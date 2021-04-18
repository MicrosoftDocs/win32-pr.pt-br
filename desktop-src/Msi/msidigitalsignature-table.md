---
description: A tabela MsiDigitalSignature contém as informações de assinatura para cada objeto assinado digitalmente no banco de dados de instalação.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Tabela MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750230"
---
# <a name="msidigitalsignature-table"></a><span data-ttu-id="b1c40-103">Tabela MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="b1c40-103">MsiDigitalSignature Table</span></span>

<span data-ttu-id="b1c40-104">A tabela MsiDigitalSignature contém as informações de assinatura para cada objeto assinado digitalmente no banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="b1c40-104">The MsiDigitalSignature table contains the signature information for every digitally signed object in the installation database.</span></span>

<span data-ttu-id="b1c40-105">As tabelas MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) estão disponíveis a partir da versão Windows Installer 2,0.</span><span class="sxs-lookup"><span data-stu-id="b1c40-105">The MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="b1c40-106">Windows Installer versão pode usar assinaturas digitais como um meio de detectar recursos corrompidos.</span><span class="sxs-lookup"><span data-stu-id="b1c40-106">Windows Installer version can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="b1c40-107">Windows Installer 2,0 só pode verificar as assinaturas digitais de gabinetes externos e somente pelo uso das tabelas MsiDigitalSignature e [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b1c40-107">Windows Installer 2.0 can only verify the digital signatures of external cabinets, and only by the use of the MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="b1c40-108">A partir do Windows Installer 3,0, o Windows Installer pode verificar as assinaturas digitais de patches (arquivos. msp) usando as tabelas [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="b1c40-108">Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="b1c40-109">Para obter mais informações, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md) e [aplicação de patches de UAC (controle de conta de usuário)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="b1c40-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="b1c40-110">A tabela MsiDigitalSignature tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1c40-110">The MsiDigitalSignature table has the following columns.</span></span>



| <span data-ttu-id="b1c40-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="b1c40-111">Column</span></span>               | <span data-ttu-id="b1c40-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1c40-112">Type</span></span>                         | <span data-ttu-id="b1c40-113">Chave</span><span class="sxs-lookup"><span data-stu-id="b1c40-113">Key</span></span> | <span data-ttu-id="b1c40-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="b1c40-114">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="b1c40-115">Tabela</span><span class="sxs-lookup"><span data-stu-id="b1c40-115">Table</span></span>                | [<span data-ttu-id="b1c40-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="b1c40-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="b1c40-117">S</span><span class="sxs-lookup"><span data-stu-id="b1c40-117">Y</span></span>   | <span data-ttu-id="b1c40-118">N</span><span class="sxs-lookup"><span data-stu-id="b1c40-118">N</span></span>        |
| <span data-ttu-id="b1c40-119">Signobject</span><span class="sxs-lookup"><span data-stu-id="b1c40-119">SignObject</span></span>           | [<span data-ttu-id="b1c40-120">Text</span><span class="sxs-lookup"><span data-stu-id="b1c40-120">Text</span></span>](text.md)             | <span data-ttu-id="b1c40-121">S</span><span class="sxs-lookup"><span data-stu-id="b1c40-121">Y</span></span>   | <span data-ttu-id="b1c40-122">N</span><span class="sxs-lookup"><span data-stu-id="b1c40-122">N</span></span>        |
| <span data-ttu-id="b1c40-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="b1c40-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="b1c40-124">Identificador</span><span class="sxs-lookup"><span data-stu-id="b1c40-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="b1c40-125">N</span><span class="sxs-lookup"><span data-stu-id="b1c40-125">N</span></span>   | <span data-ttu-id="b1c40-126">N</span><span class="sxs-lookup"><span data-stu-id="b1c40-126">N</span></span>        |
| <span data-ttu-id="b1c40-127">Hash</span><span class="sxs-lookup"><span data-stu-id="b1c40-127">Hash</span></span>                 | [<span data-ttu-id="b1c40-128">Binary</span><span class="sxs-lookup"><span data-stu-id="b1c40-128">Binary</span></span>](binary.md)         | <span data-ttu-id="b1c40-129">N</span><span class="sxs-lookup"><span data-stu-id="b1c40-129">N</span></span>   | <span data-ttu-id="b1c40-130">S</span><span class="sxs-lookup"><span data-stu-id="b1c40-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b1c40-131">Colunas</span><span class="sxs-lookup"><span data-stu-id="b1c40-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b1c40-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="b1c40-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="b1c40-133">Com a versão Windows Installer 2,0, a entrada nesse campo deve ser "Media" para a [tabela de mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1c40-133">With the Windows Installer version 2.0, the entry in this field must be "Media" for the [Media table](media-table.md).</span></span> <span data-ttu-id="b1c40-134">O instalador só verifica as assinaturas digitais em entradas de mídia de gabinete externo.</span><span class="sxs-lookup"><span data-stu-id="b1c40-134">The installer only verifies the digital signatures on external cabinet media entries.</span></span> <span data-ttu-id="b1c40-135">Essa coluna e a coluna Signobject, juntas, especificam o recurso assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="b1c40-135">This column and the SignObject column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="b1c40-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>Signobject</span><span class="sxs-lookup"><span data-stu-id="b1c40-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span></span>
</dt> <dd>

<span data-ttu-id="b1c40-137">Uma chave estrangeira na chave primária da tabela especificada pela coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="b1c40-137">A foreign key into the primary key of the table specified by the Table column.</span></span> <span data-ttu-id="b1c40-138">Essa coluna e a coluna da tabela juntas especificam o recurso assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="b1c40-138">This column and the Table column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="b1c40-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="b1c40-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span></span>
</dt> <dd>

<span data-ttu-id="b1c40-140">Uma chave estrangeira na [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1c40-140">A foreign key into the [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="b1c40-141">Isso identifica o certificado que deve existir no arquivo para que a ação associada seja realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b1c40-141">This identifies the certificate that must exist on the file for the associated action to succeed.</span></span> <span data-ttu-id="b1c40-142">O recurso (ou objeto) sempre é necessário para corresponder a esse certificado na tabela MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="b1c40-142">The resource (or object) is always required to match this certificate in the MsiDigitalCertificate table.</span></span>

</dd> <dt>

<span data-ttu-id="b1c40-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Tralha</span><span class="sxs-lookup"><span data-stu-id="b1c40-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span></span>
</dt> <dd>

<span data-ttu-id="b1c40-144">Neste campo, insira o hash de referência do recurso (ou objeto) que deve ser verificado em relação ao hash real do recurso (ou objeto) Obtido em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b1c40-144">In this field enter the reference hash of the resource (or object) that is to be checked against the actual hash of the resource (or object) obtained at run-time.</span></span> <span data-ttu-id="b1c40-145">Se apenas o certificado precisar ser verificado, o campo de hash poderá ser nulo.</span><span class="sxs-lookup"><span data-stu-id="b1c40-145">If only the certificate needs to be verified, the Hash field may be null.</span></span> <span data-ttu-id="b1c40-146">Observe que o formato do hash depende do tipo de recurso (ou objeto) que está sendo assinado.</span><span class="sxs-lookup"><span data-stu-id="b1c40-146">Note that the format of the hash depends on the type of the resource (or object) being signed.</span></span>

<span data-ttu-id="b1c40-147">A coluna de hash contém a representação binária do hash.</span><span class="sxs-lookup"><span data-stu-id="b1c40-147">The Hash column contains the binary representation of the hash.</span></span> <span data-ttu-id="b1c40-148">O conteúdo real é o membro **pbData** da estrutura [**de \_ \_ blobs de hash criptd**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , que faz parte da estrutura de **\_ BLOBs do CRYPTOAPI** .</span><span class="sxs-lookup"><span data-stu-id="b1c40-148">The actual content is the **pbData** member of the [**CRYPT\_HASH\_BLOB**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure, which is part of the **CRYPTOAPI\_BLOB** structure.</span></span> <span data-ttu-id="b1c40-149">Isso pode ser obtido chamando [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ou [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span><span class="sxs-lookup"><span data-stu-id="b1c40-149">This may be obtained by calling [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) or [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="b1c40-150">Validação</span><span class="sxs-lookup"><span data-stu-id="b1c40-150">Validation</span></span>

<dl>

[<span data-ttu-id="b1c40-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="b1c40-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b1c40-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="b1c40-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b1c40-153">ICE29</span><span class="sxs-lookup"><span data-stu-id="b1c40-153">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="b1c40-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="b1c40-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b1c40-155">ICE66</span><span class="sxs-lookup"><span data-stu-id="b1c40-155">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="b1c40-156">ICE81</span><span class="sxs-lookup"><span data-stu-id="b1c40-156">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="b1c40-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1c40-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1c40-158">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="b1c40-158">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="b1c40-159">Tabela MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="b1c40-159">MsiDigitalCertificate table</span></span>](msidigitalcertificate-table.md)
</dt> <dt>

[<span data-ttu-id="b1c40-160">Assinaturas digitais e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b1c40-160">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
