---
description: Usando o protocolo COPP (certificado de proteção de saída)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Usando o protocolo COPP (certificado de proteção de saída)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786963"
---
# <a name="using-certified-output-protection-protocol-copp"></a><span data-ttu-id="fb773-103">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="fb773-103">Using Certified Output Protection Protocol (COPP)</span></span>

<span data-ttu-id="fb773-104">O protocolo COPP (certificado de proteção de saída) permite que um aplicativo proteja um fluxo de vídeo à medida que ele viaja do adaptador gráfico para o dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb773-104">Certified Output Protection Protocol (COPP) enables an application to protect a video stream as it travels from the graphics adapter to the display device.</span></span> <span data-ttu-id="fb773-105">Um aplicativo pode usar COPP para descobrir que tipo de conector físico está anexado ao dispositivo de vídeo e quais tipos de proteção de saída estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fb773-105">An application can use COPP to discover what kind of physical connector is attached to the display device, and what types of output protection are available.</span></span> <span data-ttu-id="fb773-106">Os mecanismos de proteção incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fb773-106">Protection mechanisms include the following:</span></span>

-   <span data-ttu-id="fb773-107">Proteção de Conteúdo Digital High-Bandwidth (HDCP)</span><span class="sxs-lookup"><span data-stu-id="fb773-107">High-Bandwidth Digital Content Protection (HDCP)</span></span>
-   <span data-ttu-id="fb773-108">Sistema de gerenciamento de geração de cópia — analógico (CGMS-A)</span><span class="sxs-lookup"><span data-stu-id="fb773-108">Copy Generation Management System — Analog (CGMS-A)</span></span>
-   <span data-ttu-id="fb773-109">Proteção de cópia analógica (ACP)</span><span class="sxs-lookup"><span data-stu-id="fb773-109">Analog Copy Protection (ACP)</span></span>

<span data-ttu-id="fb773-110">Se o adaptador gráfico oferecer suporte a um desses mecanismos, o aplicativo poderá usar COPP para definir o nível de proteção.</span><span class="sxs-lookup"><span data-stu-id="fb773-110">If the graphics adapter supports one of these mechanisms, the application can use COPP to set the protection level.</span></span>

<span data-ttu-id="fb773-111">COPP define um protocolo que é usado para estabelecer um canal de comunicações seguro com o driver de gráficos.</span><span class="sxs-lookup"><span data-stu-id="fb773-111">COPP defines a protocol that is used to establish a secure communications channel with the graphics driver.</span></span> <span data-ttu-id="fb773-112">Ele usa MACs (códigos de autenticação de mensagens) para verificar a integridade dos comandos COPP que são passados entre o aplicativo e o driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fb773-112">It uses Message Authentication Codes (MACs) to verify the integrity of the COPP commands that are passed between the application and the display driver.</span></span> <span data-ttu-id="fb773-113">O aplicativo usa COPP chamando métodos na interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) do filtro de processador de mixagem de vídeo do DIRECTSHOW (VMR-7 ou VMR-9).</span><span class="sxs-lookup"><span data-stu-id="fb773-113">The application uses COPP by calling methods on the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface of the DirectShow Video Mixing Renderer filter (VMR-7 or VMR-9).</span></span>

<span data-ttu-id="fb773-114">A COPP não define nada sobre as políticas de direitos digitais que podem ser aplicadas ao conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="fb773-114">COPP does not define anything about the digital rights policies that might apply to digital media content.</span></span> <span data-ttu-id="fb773-115">Além disso, a própria COPP não implementa sistemas de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="fb773-115">Also, COPP itself does not implement any output protection systems.</span></span> <span data-ttu-id="fb773-116">O protocolo COPP simplesmente fornece uma maneira de definir e consultar os níveis de proteção no adaptador gráfico, usando os sistemas de proteção fornecidos pelo adaptador.</span><span class="sxs-lookup"><span data-stu-id="fb773-116">The COPP protocol simply provides a way to set and query protection levels on the graphics adapter, using the protection systems provided by the adapter.</span></span>

<span data-ttu-id="fb773-117">Esta seção pressupõe que você esteja familiarizado com as seguintes tecnologias:</span><span class="sxs-lookup"><span data-stu-id="fb773-117">This section assumes that you are familiar with the following technologies:</span></span>

-   <span data-ttu-id="fb773-118">DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb773-118">DirectShow</span></span>
-   <span data-ttu-id="fb773-119">SDK do Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="fb773-119">Windows Media Format SDK</span></span>
-   <span data-ttu-id="fb773-120">XML</span><span class="sxs-lookup"><span data-stu-id="fb773-120">XML</span></span>
-   <span data-ttu-id="fb773-121">Criptografia de chave pública e criptografia simétrica</span><span class="sxs-lookup"><span data-stu-id="fb773-121">Public-key cryptography and symmetric cryptography</span></span>

<span data-ttu-id="fb773-122">Os exemplos de código nesta seção usam o CryptoAPI da Microsoft para executar operações criptográficas.</span><span class="sxs-lookup"><span data-stu-id="fb773-122">The code examples in this section use Microsoft's CryptoAPI to perform cryptographic operations.</span></span> <span data-ttu-id="fb773-123">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="fb773-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fb773-124">Visão geral de COPP</span><span class="sxs-lookup"><span data-stu-id="fb773-124">Overview of COPP</span></span>](overview-of-copp.md)
-   [<span data-ttu-id="fb773-125">Obtendo a cadeia de certificados do driver</span><span class="sxs-lookup"><span data-stu-id="fb773-125">Obtaining the Driver's Certificate Chain</span></span>](obtaining-the-drivers-certificate-chain.md)
-   [<span data-ttu-id="fb773-126">Validando a cadeia de certificados</span><span class="sxs-lookup"><span data-stu-id="fb773-126">Validating the Certificate Chain</span></span>](validating-the-certificate-chain.md)
-   [<span data-ttu-id="fb773-127">Listas de certificados revogados</span><span class="sxs-lookup"><span data-stu-id="fb773-127">Certificate Revocation Lists</span></span>](certificate-revocation-lists.md)
-   [<span data-ttu-id="fb773-128">Importando a chave pública do driver</span><span class="sxs-lookup"><span data-stu-id="fb773-128">Importing the Driver's Public Key</span></span>](importing-the-drivers-public-key.md)
-   [<span data-ttu-id="fb773-129">Iniciando uma sessão COPP</span><span class="sxs-lookup"><span data-stu-id="fb773-129">Initiating a COPP Session</span></span>](initiating-a-copp-session.md)
-   [<span data-ttu-id="fb773-130">Enviando solicitações de status COPP</span><span class="sxs-lookup"><span data-stu-id="fb773-130">Sending COPP Status Requests</span></span>](sending-copp-status-requests.md)
-   [<span data-ttu-id="fb773-131">Enviando comandos COPP</span><span class="sxs-lookup"><span data-stu-id="fb773-131">Sending COPP Commands</span></span>](sending-copp-commands.md)
-   [<span data-ttu-id="fb773-132">Testando se um driver gráfico dá suporte a COPP</span><span class="sxs-lookup"><span data-stu-id="fb773-132">Testing Whether a Graphics Driver Supports COPP</span></span>](testing-whether-a-graphics-driver-supports-copp.md)
-   [<span data-ttu-id="fb773-133">Referência de consulta COPP</span><span class="sxs-lookup"><span data-stu-id="fb773-133">COPP Query Reference</span></span>](copp-query-reference.md)
-   [<span data-ttu-id="fb773-134">Referência de comando COPP</span><span class="sxs-lookup"><span data-stu-id="fb773-134">COPP Command Reference</span></span>](copp-command-reference.md)

## <a name="related-topics"></a><span data-ttu-id="fb773-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb773-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb773-136">Usando o processador de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="fb773-136">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



