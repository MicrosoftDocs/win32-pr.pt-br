---
description: Windows Installer pode usar assinaturas digitais para detectar recursos corrompidos.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Assinaturas digitais e arquivos de gabinete externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828999"
---
# <a name="digital-signatures-and-external-cabinet-files"></a><span data-ttu-id="008bf-103">Assinaturas digitais e arquivos de gabinete externo</span><span class="sxs-lookup"><span data-stu-id="008bf-103">Digital Signatures and External Cabinet Files</span></span>

<span data-ttu-id="008bf-104">Windows Installer pode usar assinaturas digitais para detectar recursos corrompidos.</span><span class="sxs-lookup"><span data-stu-id="008bf-104">Windows Installer can use digital signatures to detect corrupted resources.</span></span> <span data-ttu-id="008bf-105">Ao instalar um recurso externo, o certificado de signatário pertencente ao recurso pode ser verificado em relação a um certificado de signatário de referência criado no pacote.</span><span class="sxs-lookup"><span data-stu-id="008bf-105">When installing an external resource, the signer certificate belonging to the resource may be verified against a reference signer certificate authored in the package.</span></span> <span data-ttu-id="008bf-106">O instalador não pode verificar assinaturas para gabinetes internos.</span><span class="sxs-lookup"><span data-stu-id="008bf-106">The installer cannot verify signatures for internal cabinets.</span></span> <span data-ttu-id="008bf-107">Ele só pode verificar assinaturas digitais usando a [tabela MsiDigitalSignature](msidigitalsignature-table.md) e a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="008bf-107">It can only verify digital signatures by using the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>

<span data-ttu-id="008bf-108">Windows Installer faz o seguinte ao instalar um arquivo armazenado em um gabinete externo:</span><span class="sxs-lookup"><span data-stu-id="008bf-108">Windows Installer does the following when installing a file stored in an external cabinet:</span></span>

-   <span data-ttu-id="008bf-109">O instalador verifica se a entrada de mídia para esse gabinete externo está listada na [tabela MsiDigitalSignature](msidigitalsignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="008bf-109">The installer checks to see whether the media entry for that external cabinet is listed in the [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span> <span data-ttu-id="008bf-110">Um arquivo armazenado em um gabinete externo é identificado por ter uma entrada na coluna de gabinete da [tabela de mídia](media-table.md) que não é prefixada por um \# caractere ' '.</span><span class="sxs-lookup"><span data-stu-id="008bf-110">A file stored in an external cabinet is identified by having an entry in the Cabinet column of the [Media table](media-table.md) that is not prefixed by a '\#' character.</span></span>
-   <span data-ttu-id="008bf-111">Antes de abrir o gabinete externo, o instalador chama WinVerifyTrust para extrair o certificado atual e as informações de hash.</span><span class="sxs-lookup"><span data-stu-id="008bf-111">Before opening the external cabinet, the installer calls WinVerifyTrust to extract the current certificate and hash information.</span></span> <span data-ttu-id="008bf-112">Se houver uma incompatibilidade entre as informações de assinatura atuais no gabinete e as informações de assinatura criadas no pacote, a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="008bf-112">If there is a mismatch between the current signature information on the cabinet and the signature information authored in the package, the installation fails.</span></span> <span data-ttu-id="008bf-113">A instalação falha porque o gabinete pode ter sido comprometido e não pode ser confiável.</span><span class="sxs-lookup"><span data-stu-id="008bf-113">The installation fails because the cabinet may have been compromised and cannot be trusted.</span></span>

<span data-ttu-id="008bf-114">Para obter mais informações sobre o uso de assinaturas digitais, certificados digitais e [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consulte a seção [segurança](https://msdn.microsoft.com/library/cc527452.aspx) do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="008bf-114">For more information regarding the use of digital signatures, digital certificates, and [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), see the [Security](https://msdn.microsoft.com/library/cc527452.aspx) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="008bf-115">Para obter mais informações, consulte [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate Table](msidigitalcertificate-table.md)e [MsiDigitalSignature Table](msidigitalsignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="008bf-115">For more information, see [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate table](msidigitalcertificate-table.md), and [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span>

 

 
