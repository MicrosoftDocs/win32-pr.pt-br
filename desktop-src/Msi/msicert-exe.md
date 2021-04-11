---
description: Windows Installer pode usar assinaturas digitais como um meio de detectar recursos corrompidos.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172022"
---
# <a name="msicertexe"></a><span data-ttu-id="9c7ba-103">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="9c7ba-103">Msicert.exe</span></span>

<span data-ttu-id="9c7ba-104">Windows Installer pode usar assinaturas digitais como um meio de detectar recursos corrompidos.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-104">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="9c7ba-105">Um certificado de signatário pode ser comparado ao certificado de assinante de um recurso externo a ser instalado pelo pacote.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="9c7ba-106">Para obter mais informações, consulte [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="9c7ba-106">For more information, see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="9c7ba-107">MsiCert.exe é um utilitário de linha de comando que pode ser usado para popular a [tabela MsiDigitalSignature](msidigitalsignature-table.md) e a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md) com as informações de assinatura digital de um arquivo de gabinete externo.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-107">MsiCert.exe is a command line utility that can be used to populate the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md) with the digital signature information of an external cabinet file.</span></span> <span data-ttu-id="9c7ba-108">O arquivo de gabinete deve ser assinado digitalmente e listado na [tabela de mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="9c7ba-108">The cabinet file must by digitally signed and listed in the [Media table](media-table.md).</span></span> <span data-ttu-id="9c7ba-109">MsiCert.exe usa as informações do certificado de signatário do gabinete assinado digitalmente e criará e adicionará as tabelas MsiDigitalSignature e MsiDigitalCertificate ao banco de dados, se elas ainda não existirem.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-109">MsiCert.exe uses the signer certificate information from the digitally signed cabinet and will create and add the MsiDigitalSignature and MsiDigitalCertificate tables to the database if they do not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c7ba-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c7ba-110">Syntax</span></span>

<span data-ttu-id="9c7ba-111">**msicert-d** *{Database}* **-m** *{entrada de mídia}* **-c** *{Cabinet}* **\[ - \] h**</span><span class="sxs-lookup"><span data-stu-id="9c7ba-111">**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[-h\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="9c7ba-112">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="9c7ba-112">Command Line Options</span></span>

<span data-ttu-id="9c7ba-113">As opções de linha de comando não diferenciam maiúsculas de minúsculas e os delimitadores de barra podem ser usados em vez de um traço.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-113">The command line options are case-insensitive and slash delimiters may be used instead of a dash.</span></span>



| <span data-ttu-id="9c7ba-114">Opção</span><span class="sxs-lookup"><span data-stu-id="9c7ba-114">Option</span></span> | <span data-ttu-id="9c7ba-115">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c7ba-115">Parameter</span></span>        | <span data-ttu-id="9c7ba-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c7ba-116">Description</span></span>                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c7ba-117">-d</span><span class="sxs-lookup"><span data-stu-id="9c7ba-117">-d</span></span>     | <database> | <span data-ttu-id="9c7ba-118">O banco de dados (arquivo. msi) que está sendo atualizado.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-118">The database (.msi file) that is being updated.</span></span>                                                         |
| <span data-ttu-id="9c7ba-119">-M</span><span class="sxs-lookup"><span data-stu-id="9c7ba-119">-m</span></span>     | <media Id> | <span data-ttu-id="9c7ba-120">A entrada no campo DiskId da tabela de [mídia](media-table.md) no registro do arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-120">The entry in the DiskId field of the [Media table](media-table.md) in the record for the cabinet file.</span></span> |
| <span data-ttu-id="9c7ba-121">-c</span><span class="sxs-lookup"><span data-stu-id="9c7ba-121">-c</span></span>     | <cabinet>  | <span data-ttu-id="9c7ba-122">O caminho para o arquivo de gabinete assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-122">The path to the digitally signed cabinet file.</span></span>                                                          |
| <span data-ttu-id="9c7ba-123">-H</span><span class="sxs-lookup"><span data-stu-id="9c7ba-123">-h</span></span>     |                  | <span data-ttu-id="9c7ba-124">Inclua o hash da assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-124">Include the hash of the digital signature.</span></span> <span data-ttu-id="9c7ba-125">Isso é opcional.</span><span class="sxs-lookup"><span data-stu-id="9c7ba-125">This is optional.</span></span>                                            |



 

<span data-ttu-id="9c7ba-126">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="9c7ba-126">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c7ba-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c7ba-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c7ba-128">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="9c7ba-128">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="9c7ba-129">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="9c7ba-129">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



