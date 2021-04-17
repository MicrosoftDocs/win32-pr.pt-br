---
description: Use estas diretrizes para abranger uma instalação de Windows Installer inteira por uma assinatura digital.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Criando uma instalação assinada totalmente verificada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e76bbfb77eab8b020cb1591847d2a36d09c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768483"
---
# <a name="authoring-a-fully-verified-signed-installation"></a><span data-ttu-id="68eba-103">Criando uma instalação assinada totalmente verificada</span><span class="sxs-lookup"><span data-stu-id="68eba-103">Authoring a Fully Verified Signed Installation</span></span>

<span data-ttu-id="68eba-104">Você pode usar essas diretrizes para cobrir toda a instalação do Windows Installer por uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="68eba-104">You can use these guidelines to cover an entire Windows Installer installation by a digital signature.</span></span>

<span data-ttu-id="68eba-105">Os autores de instalações Windows Installer devem aderir ao seguinte para garantir que todas as partes da instalação sejam cobertas por uma assinatura digital:</span><span class="sxs-lookup"><span data-stu-id="68eba-105">Authors of Windows Installer installations must adhere to the following to ensure that all parts of the installation are covered by a digital signature:</span></span>

-   <span data-ttu-id="68eba-106">Use arquivos de gabinete internos ou use arquivos de gabinete externo assinados e crie corretamente a [tabela MsiDigitalSignature](msidigitalsignature-table.md) e a [tabela MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="68eba-106">Use internal cabinet files, or use signed external cabinet files and correctly author the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>
-   <span data-ttu-id="68eba-107">Use apenas ações personalizadas armazenadas no pacote ou instaladas com o pacote.</span><span class="sxs-lookup"><span data-stu-id="68eba-107">Use only custom actions stored within the package or installed with the package.</span></span>
-   <span data-ttu-id="68eba-108">Assine o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="68eba-108">Sign the installation package.</span></span>
-   <span data-ttu-id="68eba-109">Inclua uma [tabela MsiPatchCertificate](msipatchcertificate-table.md) no pacote.</span><span class="sxs-lookup"><span data-stu-id="68eba-109">Include an [MsiPatchCertificate table](msipatchcertificate-table.md) in the package.</span></span> <span data-ttu-id="68eba-110">Para habilitar a [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md), essa tabela deve conter informações usadas para identificar os certificados de signatário usados para assinar digitalmente os patches.</span><span class="sxs-lookup"><span data-stu-id="68eba-110">To enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md), this table must contain information used to identify the signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="68eba-111">A aplicação de patches do UAC permite que o autor do pacote de instalação identifique patches assinados digitalmente que podem ser aplicados no futuro por usuários não administradores.</span><span class="sxs-lookup"><span data-stu-id="68eba-111">UAC patching enables the author of the installation package to identify digitally-signed patches that can be applied in the future by non-administrator users.</span></span>

<span data-ttu-id="68eba-112">Para obter um exemplo que mostra como criar uma instalação assinada usando a automação, consulte [criando uma instalação assinada totalmente verificada usando a automação](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="68eba-112">For an example showing how to author a signed installation using automation, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

 

 



