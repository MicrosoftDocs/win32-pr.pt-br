---
description: Visão geral de COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Visão geral de COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779838"
---
# <a name="overview-of-copp"></a><span data-ttu-id="13ea4-103">Visão geral de COPP</span><span class="sxs-lookup"><span data-stu-id="13ea4-103">Overview of COPP</span></span>

<span data-ttu-id="13ea4-104">Aqui estão as etapas básicas que um aplicativo deve executar para usar o protocolo de proteção de saída certificado (COPP).</span><span class="sxs-lookup"><span data-stu-id="13ea4-104">Here are the basic steps that an application must perform to use Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="13ea4-105">**Obter a cadeia de certificados do driver**</span><span class="sxs-lookup"><span data-stu-id="13ea4-105">**Get the driver's certificate chain**</span></span>

1.  <span data-ttu-id="13ea4-106">Crie um grafo de reprodução do DirectShow que renderiza o vídeo usando o processador de mixagem de vídeo (VMR-7 ou VMR-9) ou o filtro de [**processador de vídeo aprimorado**](enhanced-video-renderer-filter.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="13ea4-106">Build a DirectShow playback graph that renders video using the Video Mixing Renderer (VMR-7 or VMR-9) or the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) filter (EVR).</span></span>
2.  <span data-ttu-id="13ea4-107">Consulte o VMR para a interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .</span><span class="sxs-lookup"><span data-stu-id="13ea4-107">Query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface.</span></span>
3.  <span data-ttu-id="13ea4-108">Chame [**IAMCertifiedOutputProtection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="13ea4-108">Call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="13ea4-109">Esse método retorna um número aleatório de 128 bits do driver, juntamente com uma cadeia de certificados que contém a chave pública RSA de 2048 bits do driver.</span><span class="sxs-lookup"><span data-stu-id="13ea4-109">This method returns a 128-bit random number from the driver, along with a certificate chain that contains the driver's 2048-bit RSA public key.</span></span>

<span data-ttu-id="13ea4-110">**Validar a cadeia de certificados**</span><span class="sxs-lookup"><span data-stu-id="13ea4-110">**Validate the certificate chain**</span></span>

1.  <span data-ttu-id="13ea4-111">Valide a cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="13ea4-111">Validate the certificate chain.</span></span> <span data-ttu-id="13ea4-112">Se a cadeia de certificados não for válida, pare.</span><span class="sxs-lookup"><span data-stu-id="13ea4-112">If the certificate chain is not valid, stop.</span></span>
2.  <span data-ttu-id="13ea4-113">Verifique a CRL (lista de certificados revogados).</span><span class="sxs-lookup"><span data-stu-id="13ea4-113">Check the certificate revocation list (CRL).</span></span> <span data-ttu-id="13ea4-114">Se qualquer um dos certificados na cadeia de certificados aparecer na lista de revogação, pare.</span><span class="sxs-lookup"><span data-stu-id="13ea4-114">If any of the certificates in the certificate chain appears in the revocation list, stop.</span></span>
3.  <span data-ttu-id="13ea4-115">Obtenha a chave pública RSA da cadeia de certificados.</span><span class="sxs-lookup"><span data-stu-id="13ea4-115">Get the RSA public key from the certificate chain.</span></span>

<span data-ttu-id="13ea4-116">**Inicializar a sessão COPP**</span><span class="sxs-lookup"><span data-stu-id="13ea4-116">**Initialize the COPP Session**</span></span>

1.  <span data-ttu-id="13ea4-117">Gere uma chave de sessão AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="13ea4-117">Generate a 128-bit AES session key.</span></span> <span data-ttu-id="13ea4-118">Essa chave é usada para assinar dados e verificar se os dados assinados não foram adulterados.</span><span class="sxs-lookup"><span data-stu-id="13ea4-118">This key is used to sign data and to verify that signed data has not been tampered with.</span></span>
2.  <span data-ttu-id="13ea4-119">Gere dois números aleatórios de 32 bits seguros criptograficamente.</span><span class="sxs-lookup"><span data-stu-id="13ea4-119">Generate two cryptographically secure 32-bit random numbers.</span></span> <span data-ttu-id="13ea4-120">O primeiro é um número de sequência de status e o segundo é um número de sequência de comando.</span><span class="sxs-lookup"><span data-stu-id="13ea4-120">The first is a status sequence number, and the second is a command sequence number.</span></span> <span data-ttu-id="13ea4-121">Cada vez que o aplicativo envia um comando ou uma solicitação de status, ele incrementa o número de sequência correspondente e inclui esse número no comando COPP ou nos dados de solicitação.</span><span class="sxs-lookup"><span data-stu-id="13ea4-121">Each time the application sends a command or status request, it increments the corresponding sequence number, and includes this number in the COPP command or request data.</span></span>
3.  <span data-ttu-id="13ea4-122">Concatene o número aleatório de 128 bits do driver de gráficos, a chave de sessão AES, o número de sequência de status e o número de sequência de comando.</span><span class="sxs-lookup"><span data-stu-id="13ea4-122">Concatenate the 128-bit random number from the graphics driver, the AES session key, the status sequence number, and the command sequence number.</span></span> <span data-ttu-id="13ea4-123">Criptografe esta matriz de bytes usando a chave pública do driver e passe o resultado para [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span><span class="sxs-lookup"><span data-stu-id="13ea4-123">Encrypt this byte array using the driver's public key and pass the result to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span></span>

<span data-ttu-id="13ea4-124">**Enviar comandos COPP e solicitações de status**</span><span class="sxs-lookup"><span data-stu-id="13ea4-124">**Send COPP Commands and Status Requests**</span></span>

1.  <span data-ttu-id="13ea4-125">Consulte os tipos de proteção disponíveis e outras informações chamando [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span><span class="sxs-lookup"><span data-stu-id="13ea4-125">Query for the available protection types and other information by calling [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span></span>
2.  <span data-ttu-id="13ea4-126">Defina os níveis de proteção desejados chamando [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span><span class="sxs-lookup"><span data-stu-id="13ea4-126">Set the desired protection levels by calling [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span></span>
3.  <span data-ttu-id="13ea4-127">Consulte periodicamente o nível de proteção local atual.</span><span class="sxs-lookup"><span data-stu-id="13ea4-127">Periodically query for the current local protection level.</span></span> <span data-ttu-id="13ea4-128">Pare a reprodução se o nível de proteção local for alterado inesperadamente ou se um problema for detectado.</span><span class="sxs-lookup"><span data-stu-id="13ea4-128">Stop playback if the local protection level changes unexpectedly or if a problem is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13ea4-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13ea4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13ea4-130">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="13ea4-130">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



