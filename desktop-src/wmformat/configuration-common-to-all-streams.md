---
title: Configuração comum a todos os fluxos
description: Configuração comum a todos os fluxos
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- perfis, configurações comuns a todos os fluxos
- fluxos, configurações comuns
- fluxos, nomes
- fluxos, nomes de conexão
- fluxos, números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104365775"
---
# <a name="configuration-common-to-all-streams"></a><span data-ttu-id="89f23-108">Configuração comum a todos os fluxos</span><span class="sxs-lookup"><span data-stu-id="89f23-108">Configuration Common to All Streams</span></span>

<span data-ttu-id="89f23-109">Todos os fluxos, independentemente do tipo, devem ser atribuídos a um nome de fluxo, um nome de conexão e um número de fluxo.</span><span class="sxs-lookup"><span data-stu-id="89f23-109">All streams, regardless of type, should be assigned a stream name, a connection name, and a stream number.</span></span>

<span data-ttu-id="89f23-110">O nome do fluxo é simplesmente um nome descritivo que você atribui ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="89f23-110">The stream name is simply a descriptive name you assign to the stream.</span></span> <span data-ttu-id="89f23-111">Um fluxo não precisa ter um nome de fluxo, mas ajuda a identificar o fluxo ao editar o perfil posteriormente.</span><span class="sxs-lookup"><span data-stu-id="89f23-111">A stream does not need to have a stream name, but it helps you to identify the stream when editing the profile at a later time.</span></span> <span data-ttu-id="89f23-112">Você pode definir um nome para o fluxo chamando [**IWMStreamConfig:: Setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span><span class="sxs-lookup"><span data-stu-id="89f23-112">You can set a name for the stream by calling [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).</span></span>

<span data-ttu-id="89f23-113">Cada fluxo deve ter um nome de conexão, também chamado de nome de entrada.</span><span class="sxs-lookup"><span data-stu-id="89f23-113">Every stream should have a connection name, also called an input name.</span></span> <span data-ttu-id="89f23-114">Quando você define o perfil no objeto do gravador para gravar um arquivo, o gravador associará cada nome de conexão a uma entrada.</span><span class="sxs-lookup"><span data-stu-id="89f23-114">When you set the profile in the writer object to write a file, the writer will associate each connection name with an input.</span></span> <span data-ttu-id="89f23-115">Para identificar as entradas, você deve chamar [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) para recuperar o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="89f23-115">To identify the inputs, you must call [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) to retrieve the connection name.</span></span> <span data-ttu-id="89f23-116">Nomes de conexão típicos são descrições simples do conteúdo, como "áudio".</span><span class="sxs-lookup"><span data-stu-id="89f23-116">Typical connection names are simple descriptions of the content, such as "audio".</span></span> <span data-ttu-id="89f23-117">Se o seu perfil contiver fluxos mutuamente exclusivos por taxa de bits, cada um dos fluxos mutuamente exclusivos deverá ter o mesmo nome de conexão.</span><span class="sxs-lookup"><span data-stu-id="89f23-117">If your profile contains streams that are mutually exclusive by bit rate, each of the mutually exclusive streams must have the same connection name.</span></span> <span data-ttu-id="89f23-118">Se não tiverem, o perfil será inválido e será rejeitado pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="89f23-118">If they do not, the profile is invalid and will be rejected by the writer.</span></span> <span data-ttu-id="89f23-119">Você pode definir um nome de conexão chamando [**IWMStreamConfig:: Setconnectionname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span><span class="sxs-lookup"><span data-stu-id="89f23-119">You can set a connection name by calling [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).</span></span>

<span data-ttu-id="89f23-120">O número do fluxo identifica o fluxo dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="89f23-120">The stream number identifies the stream within the file.</span></span> <span data-ttu-id="89f23-121">Ao contrário dos números de entrada e de saída, os números de fluxo começam em 1, e não 0.</span><span class="sxs-lookup"><span data-stu-id="89f23-121">Unlike input numbers and output numbers, stream numbers start at 1, not 0.</span></span> <span data-ttu-id="89f23-122">Um número de fluxo é diferente de um índice de fluxo, que você usa ao obter fluxos em um perfil usando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="89f23-122">A stream number is different than a stream index, which you use when getting streams in a profile by using [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span> <span data-ttu-id="89f23-123">O índice de fluxo é um número atribuído ao fluxo pelo objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="89f23-123">The stream index is a number assigned to the stream by the profile object.</span></span> <span data-ttu-id="89f23-124">Os índices de fluxo variam entre 0 e um menor que o número de fluxos recuperados por [**IWMProfile:: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span><span class="sxs-lookup"><span data-stu-id="89f23-124">Stream indexes range between 0 and one less than the number of streams retrieved by [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount).</span></span> <span data-ttu-id="89f23-125">Os números de fluxo não precisam ser sequenciais, embora normalmente estejam e podem variar de 1 a 63.</span><span class="sxs-lookup"><span data-stu-id="89f23-125">Stream numbers need not be sequential, though they usually are, and can range from 1 to 63.</span></span> <span data-ttu-id="89f23-126">Você pode definir um número de fluxo chamando [**IWMStreamConfig:: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span><span class="sxs-lookup"><span data-stu-id="89f23-126">You can set a stream number by calling [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89f23-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89f23-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f23-128">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="89f23-128">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="89f23-129">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="89f23-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




