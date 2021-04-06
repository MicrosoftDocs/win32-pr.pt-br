---
description: A tabela MsiDigitalCertificate armazena certificados no formato de fluxo binário e associa cada certificado a uma chave primária.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Tabela MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661860"
---
# <a name="msidigitalcertificate-table"></a><span data-ttu-id="0faa1-103">Tabela MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="0faa1-103">MsiDigitalCertificate Table</span></span>

<span data-ttu-id="0faa1-104">A tabela MsiDigitalCertificate armazena certificados no formato de fluxo binário e associa cada certificado a uma chave primária.</span><span class="sxs-lookup"><span data-stu-id="0faa1-104">The MsiDigitalCertificate table stores certificates in binary stream format and associates each certificate with a primary key.</span></span> <span data-ttu-id="0faa1-105">A chave primária é usada para compartilhar certificados entre vários objetos assinados digitalmente.</span><span class="sxs-lookup"><span data-stu-id="0faa1-105">The primary key is used to share certificates among multiple digitally signed objects.</span></span> <span data-ttu-id="0faa1-106">Um certificado digital é uma credencial que fornece um meio para verificar a identidade.</span><span class="sxs-lookup"><span data-stu-id="0faa1-106">A digital certificate is a credential that provides a means to verify identity.</span></span> <span data-ttu-id="0faa1-107">Para obter mais informações, consulte [certificados digitais](../seccrypto/digital-certificates.md) na seção [criptografia](../seccrypto/cryptography-portal.md) do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0faa1-107">For more information, see [Digital Certificates](../seccrypto/digital-certificates.md) in the [Cryptography](../seccrypto/cryptography-portal.md) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="0faa1-108">As tabelas [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate estão disponíveis a partir da versão Windows Installer 2,0.</span><span class="sxs-lookup"><span data-stu-id="0faa1-108">The [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="0faa1-109">Windows Installer pode usar assinaturas digitais como um meio de detectar recursos corrompidos.</span><span class="sxs-lookup"><span data-stu-id="0faa1-109">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="0faa1-110">Windows Installer versão 2,0 só pode verificar as assinaturas digitais de gabinetes externos e apenas pelo uso das tabelas [MsiDigitalSignature](msidigitalsignature-table.md) e MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="0faa1-110">Windows Installer version 2.0 can only verify the digital signatures of external cabinets, and only by the use of the [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables.</span></span>

<span data-ttu-id="0faa1-111">A partir do Windows Installer versão 3,0, o Windows Installer pode verificar as assinaturas digitais de patches (arquivos. msp) usando as tabelas [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="0faa1-111">Beginning with Windows Installer version 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="0faa1-112">Para obter mais informações, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md) e [aplicação de patches de UAC (controle de conta de usuário)](user-account-control--uac--patching.md).</span><span class="sxs-lookup"><span data-stu-id="0faa1-112">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="0faa1-113">A tabela MsiDigitalCertificate tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0faa1-113">The MsiDigitalCertificate table has the following columns.</span></span>



| <span data-ttu-id="0faa1-114">Coluna</span><span class="sxs-lookup"><span data-stu-id="0faa1-114">Column</span></span>             | <span data-ttu-id="0faa1-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="0faa1-115">Type</span></span>                         | <span data-ttu-id="0faa1-116">Chave</span><span class="sxs-lookup"><span data-stu-id="0faa1-116">Key</span></span> | <span data-ttu-id="0faa1-117">Nullable</span><span class="sxs-lookup"><span data-stu-id="0faa1-117">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="0faa1-118">DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="0faa1-118">DigitalCertificate</span></span> | [<span data-ttu-id="0faa1-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="0faa1-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="0faa1-120">S</span><span class="sxs-lookup"><span data-stu-id="0faa1-120">Y</span></span>   | <span data-ttu-id="0faa1-121">N</span><span class="sxs-lookup"><span data-stu-id="0faa1-121">N</span></span>        |
| <span data-ttu-id="0faa1-122">CertData</span><span class="sxs-lookup"><span data-stu-id="0faa1-122">CertData</span></span>           | [<span data-ttu-id="0faa1-123">Binary</span><span class="sxs-lookup"><span data-stu-id="0faa1-123">Binary</span></span>](binary.md)         | <span data-ttu-id="0faa1-124">N</span><span class="sxs-lookup"><span data-stu-id="0faa1-124">N</span></span>   | <span data-ttu-id="0faa1-125">N</span><span class="sxs-lookup"><span data-stu-id="0faa1-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0faa1-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="0faa1-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0faa1-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="0faa1-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="0faa1-128">Identifica o certificado de assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="0faa1-128">Identifies the digital signature certificate.</span></span> <span data-ttu-id="0faa1-129">Chave primária da tabela.</span><span class="sxs-lookup"><span data-stu-id="0faa1-129">Primary key of table.</span></span>

</dd> <dt>

<span data-ttu-id="0faa1-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span><span class="sxs-lookup"><span data-stu-id="0faa1-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span></span>
</dt> <dd>

<span data-ttu-id="0faa1-131">A representação binária do certificado digital.</span><span class="sxs-lookup"><span data-stu-id="0faa1-131">The binary representation of the digital certificate.</span></span> <span data-ttu-id="0faa1-132">A coluna CertData contém a matriz de bytes codificada de um contexto de certificado.</span><span class="sxs-lookup"><span data-stu-id="0faa1-132">The CertData column contains the encoded byte array of a certificate context.</span></span> <span data-ttu-id="0faa1-133">Esse é o membro **pbCertEncoded** da estrutura [**de \_ contexto do certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="0faa1-133">This is the **pbCertEncoded** member of the [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="0faa1-134">O contexto do certificado pode ser obtido chamando [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)ou importando um arquivo. cer.</span><span class="sxs-lookup"><span data-stu-id="0faa1-134">The certificate context can be obtained by calling [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), or by importing a .cer file.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="0faa1-135">Validação</span><span class="sxs-lookup"><span data-stu-id="0faa1-135">Validation</span></span>

<dl>

[<span data-ttu-id="0faa1-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="0faa1-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0faa1-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="0faa1-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0faa1-138">ICE29</span><span class="sxs-lookup"><span data-stu-id="0faa1-138">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="0faa1-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="0faa1-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0faa1-140">ICE66</span><span class="sxs-lookup"><span data-stu-id="0faa1-140">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="0faa1-141">ICE81</span><span class="sxs-lookup"><span data-stu-id="0faa1-141">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="0faa1-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0faa1-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0faa1-143">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="0faa1-143">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="0faa1-144">Tabela MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="0faa1-144">MsiDigitalSignature table</span></span>](msidigitalsignature-table.md)
</dt> <dt>

[<span data-ttu-id="0faa1-145">Assinaturas digitais e Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0faa1-145">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
