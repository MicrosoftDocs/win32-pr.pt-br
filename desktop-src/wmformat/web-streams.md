---
title: Fluxos da Web
description: Fluxos da Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- SDK do Windows Media Format, Web streams
- ASF (Advanced Systems Format), fluxos da Web
- ASF (formato de sistemas avançados), fluxos da Web
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- Fluxos da Web, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005447"
---
# <a name="web-streams"></a><span data-ttu-id="679dd-110">Fluxos da Web</span><span class="sxs-lookup"><span data-stu-id="679dd-110">Web Streams</span></span>

<span data-ttu-id="679dd-111">Um fluxo da Web é como um fluxo de arquivos, pois ele contém arquivos de dados.</span><span class="sxs-lookup"><span data-stu-id="679dd-111">A Web stream is like a file stream in that it contains data files.</span></span> <span data-ttu-id="679dd-112">Em um fluxo da Web, esses arquivos normalmente são páginas HTML e elementos gráficos associados no formato GIF ou JPEG.</span><span class="sxs-lookup"><span data-stu-id="679dd-112">In a Web stream, these files are typically HTML pages and associated graphics in GIF or JPEG format.</span></span>

<span data-ttu-id="679dd-113">Os fluxos da Web podem ser particularmente úteis para arquivos ASF que são usados como apresentações.</span><span class="sxs-lookup"><span data-stu-id="679dd-113">Web streams can be particularly useful for ASF files that are used as presentations.</span></span> <span data-ttu-id="679dd-114">Antes do suporte de fluxos da Web, as apresentações teriam URLs em fluxos de script em um arquivo para que uma página da Web fosse carregada em um tempo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="679dd-114">Prior to the support of Web streams, presentations would have URLs in script streams within a file so that a Web page would load at a predetermined time.</span></span> <span data-ttu-id="679dd-115">A dificuldade era que o congestionamento da rede poderia causar atrasos e criar uma experiência de exibição ruim.</span><span class="sxs-lookup"><span data-stu-id="679dd-115">The difficulty was that network congestion could cause delays and create a poor viewing experience.</span></span>

<span data-ttu-id="679dd-116">Com os fluxos da Web, as partes constituintes de páginas da Web podem ser incluídas no arquivo ASF como um fluxo.</span><span class="sxs-lookup"><span data-stu-id="679dd-116">With Web streams, the constituent parts of Web pages can be included in the ASF file as a stream.</span></span> <span data-ttu-id="679dd-117">À medida que os arquivos são recebidos, eles podem ser armazenados em cache para que, quando o comando para exibir (ou renderizar) uma URL seja entregue, eles possam ser acessados instantaneamente por um navegador.</span><span class="sxs-lookup"><span data-stu-id="679dd-117">As the files are received, they can be cached so that, when the command to display (or render) a URL is delivered, they can be instantly accessed by a browser.</span></span> <span data-ttu-id="679dd-118">Isso permite uma reprodução uniforme e consistente.</span><span class="sxs-lookup"><span data-stu-id="679dd-118">This enables smooth, consistent playback.</span></span> <span data-ttu-id="679dd-119">O comando render é entregue no fluxo da Web em si, não como um comando de script em um fluxo separado.</span><span class="sxs-lookup"><span data-stu-id="679dd-119">The render command is delivered in the Web stream itself, not as a script command in a separate stream.</span></span>

<span data-ttu-id="679dd-120">É recomendável que os fluxos da Web criados usando o SDK da série Windows Media Format 9 Series ou posterior recebam o número de versão 1.</span><span class="sxs-lookup"><span data-stu-id="679dd-120">It is recommended that Web streams created by using the Windows Media Format 9 Series SDK, or later be given the version number 1.</span></span> <span data-ttu-id="679dd-121">Esse valor é especificado na estrutura [**de \_ \_ formato webstream do WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) no membro **wVersion** .</span><span class="sxs-lookup"><span data-stu-id="679dd-121">This value is specified in the [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure in the **wVersion** member.</span></span> <span data-ttu-id="679dd-122">O próprio SDK não faz nada para impor essa versão.</span><span class="sxs-lookup"><span data-stu-id="679dd-122">The SDK itself does nothing to enforce this version.</span></span>

> [!Note]  
> <span data-ttu-id="679dd-123">Ao se conectar a fluxos de transmissão ao vivo que têm fluxos da Web, é possível que o usuário receba um comando render antes que o arquivo especificado esteja realmente no cache local.</span><span class="sxs-lookup"><span data-stu-id="679dd-123">When connecting to live broadcast streams that have Web streams, it is possible that the user may receive a render command before the specified file is actually in the local cache.</span></span> <span data-ttu-id="679dd-124">A menos que seu aplicativo manipule essa condição, o navegador exibirá um erro "página não encontrada".</span><span class="sxs-lookup"><span data-stu-id="679dd-124">Unless your application handles this condition, the browser will display a "Page not found" error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="679dd-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="679dd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="679dd-126">**Fluxos arbitrários**</span><span class="sxs-lookup"><span data-stu-id="679dd-126">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="679dd-127">**Configurando fluxos da Web**</span><span class="sxs-lookup"><span data-stu-id="679dd-127">**Configuring Web Streams**</span></span>](configuring-web-streams.md)
</dt> </dl>

 

 




