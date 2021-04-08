---
description: Instala um certificado registrado de um arquivo de troca de informações pessoais (PFX) no repositório de certificados.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922444"
---
# <a name="installresponsefrompfx"></a><span data-ttu-id="872d5-103">installResponseFromPFX</span><span class="sxs-lookup"><span data-stu-id="872d5-103">installResponseFromPFX</span></span>

<span data-ttu-id="872d5-104">O exemplo installResponseFromPFX instala um certificado registrado de um arquivo de troca de informações pessoais (PFX) no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="872d5-104">The installResponseFromPFX sample installs an enrolled certificate from a Personal Information Exchange (PFX) file to the certificate store.</span></span>

## <a name="location"></a><span data-ttu-id="872d5-105">Local</span><span class="sxs-lookup"><span data-stu-id="872d5-105">Location</span></span>

<span data-ttu-id="872d5-106">Quando você instala o SDK (Software Development Kit) do Microsoft Windows, o exemplo é instalado, por padrão, na pasta *% ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registro \\ vc \\ installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="872d5-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\installResponseFromPFX folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="872d5-107">Discussão</span><span class="sxs-lookup"><span data-stu-id="872d5-107">Discussion</span></span>

<span data-ttu-id="872d5-108">O exemplo de installResponseFromPFX:</span><span class="sxs-lookup"><span data-stu-id="872d5-108">The installResponseFromPFX sample:</span></span>

1.  <span data-ttu-id="872d5-109">Processa os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="872d5-109">Processes the command line arguments.</span></span> <span data-ttu-id="872d5-110">A linha de comando deve conter:</span><span class="sxs-lookup"><span data-stu-id="872d5-110">The command line should contain:</span></span>
    -   <span data-ttu-id="872d5-111">O nome do exemplo.</span><span class="sxs-lookup"><span data-stu-id="872d5-111">The name of the sample.</span></span>
    -   <span data-ttu-id="872d5-112">O nome do arquivo PFX que contém o certificado registrado.</span><span class="sxs-lookup"><span data-stu-id="872d5-112">The name of the PFX file that contains the enrolled certificate.</span></span>
    -   <span data-ttu-id="872d5-113">Uma senha associada ao arquivo PFX.</span><span class="sxs-lookup"><span data-stu-id="872d5-113">A password associated with the PFX file.</span></span>
2.  <span data-ttu-id="872d5-114">Lê o arquivo PFX, experimentando o formato Base64 primeiro e o formato binário se a base64 falhar.</span><span class="sxs-lookup"><span data-stu-id="872d5-114">Reads the PFX file, trying the base64 format first and the binary format if base64 fails.</span></span> <span data-ttu-id="872d5-115">A função DecodeFileW () é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="872d5-115">The DecodeFileW() function is defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="872d5-116">Converte o certificado registrado em um **BSTR** e o usa para inicializar um objeto [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .</span><span class="sxs-lookup"><span data-stu-id="872d5-116">Converts the enrolled certificate to a **BSTR** and uses it to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="872d5-117">A função convertWszToBstr é definida em enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="872d5-117">The convertWszToBstr function is defined in enrollCommon.cpp.</span></span>
4.  <span data-ttu-id="872d5-118">Instala o certificado no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="872d5-118">Installs the certificate in the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="872d5-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="872d5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872d5-120">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="872d5-120">enrollEOBOCMC</span></span>](enrolleobocmc.md)
</dt> <dt>

[<span data-ttu-id="872d5-121">Usando os exemplos incluídos</span><span class="sxs-lookup"><span data-stu-id="872d5-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



