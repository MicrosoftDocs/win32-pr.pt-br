---
description: Perguntas frequentes do DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: Perguntas frequentes do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500486"
---
# <a name="directshow-faq"></a><span data-ttu-id="73d83-103">Perguntas frequentes do DirectShow</span><span class="sxs-lookup"><span data-stu-id="73d83-103">DirectShow FAQ</span></span>

<span data-ttu-id="73d83-104">Este artigo responde muitas perguntas frequentes sobre o Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="73d83-104">This article answers many frequently asked questions about Microsoft DirectShow.</span></span>

<span data-ttu-id="73d83-105">**A quais sistemas operacionais o DirectShow dá suporte?**</span><span class="sxs-lookup"><span data-stu-id="73d83-105">**What operating systems does DirectShow support?**</span></span>

<span data-ttu-id="73d83-106">O DirectShow está disponível em todas as versões do Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="73d83-106">DirectShow is available in all supported versions of Windows.</span></span>

<span data-ttu-id="73d83-107">**Quanto conhecimento de COM eu preciso para programar com o DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="73d83-107">**How much COM knowledge do I need to program with DirectShow?**</span></span>

<span data-ttu-id="73d83-108">Para o desenvolvimento de aplicativos, você precisa entender as noções básicas do trabalho com objetos COM: como instanciá-los, acessar as interfaces que eles expõem e gerenciar contagens de referência nessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="73d83-108">For application development, you need to understand the basics of working with COM objects: how to instantiate them, access the interfaces they expose, and manage reference counts on those interfaces.</span></span> <span data-ttu-id="73d83-109">O desenvolvimento de filtro requer mais conhecimento COM.</span><span class="sxs-lookup"><span data-stu-id="73d83-109">Filter development requires more COM knowledge.</span></span>

<span data-ttu-id="73d83-110">**A quais formatos o DirectShow dá suporte?**</span><span class="sxs-lookup"><span data-stu-id="73d83-110">**What formats does DirectShow support?**</span></span>

<span data-ttu-id="73d83-111">Consulte [formatos com suporte no DirectShow](supported-formats-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="73d83-111">See [Supported Formats in DirectShow](supported-formats-in-directshow.md).</span></span>

<span data-ttu-id="73d83-112">**Há uma HCL (lista de compatibilidade de hardware) do DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="73d83-112">**Is there a DirectShow Hardware Compatibility List (HCL)?**</span></span>

<span data-ttu-id="73d83-113">Não.</span><span class="sxs-lookup"><span data-stu-id="73d83-113">No.</span></span> <span data-ttu-id="73d83-114">O DirectShow usa o Microsoft DirectDraw e os recursos de hardware do Microsoft DirectSound se eles estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="73d83-114">DirectShow uses Microsoft DirectDraw and Microsoft DirectSound hardware capabilities if they are available.</span></span> <span data-ttu-id="73d83-115">Quando não há nenhum hardware especial disponível, o DirectShow usa GDI para desenhar vídeo e as APIs de multimídia do **WaveOut** \* para reproduzir áudio.</span><span class="sxs-lookup"><span data-stu-id="73d83-115">When no special hardware is available, DirectShow uses GDI to draw video and the **waveOut** \* multimedia APIs to play audio.</span></span>

<span data-ttu-id="73d83-116">**Quais linguagens posso usar para escrever um aplicativo DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="73d83-116">**What languages can I use to write a DirectShow application?**</span></span>

<span data-ttu-id="73d83-117">O DirectShow foi projetado principalmente para desenvolvimento em C++.</span><span class="sxs-lookup"><span data-stu-id="73d83-117">DirectShow is designed primarily for C++ development.</span></span> <span data-ttu-id="73d83-118">Um pequeno subconjunto da API do DirectShow é exposto por meio do Visual Basic 6,0; no entanto, esse recurso foi preterido.</span><span class="sxs-lookup"><span data-stu-id="73d83-118">A small sub-set of the DirectShow API is exposed through Visual Basic 6.0; however, this feature is deprecated.</span></span>

<span data-ttu-id="73d83-119">**O DirectShow nunca estará acessível por meio de código gerenciado?**</span><span class="sxs-lookup"><span data-stu-id="73d83-119">**Will DirectShow ever be accessible through managed code?**</span></span>

<span data-ttu-id="73d83-120">A Microsoft não tem planos atuais para implementar uma API do DirectShow gerenciada.</span><span class="sxs-lookup"><span data-stu-id="73d83-120">Microsoft has no current plans to implement a managed DirectShow API.</span></span>

<span data-ttu-id="73d83-121">**Que compilador preciso para o desenvolvimento do DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="73d83-121">**What compiler do I need for DirectShow development?**</span></span>

<span data-ttu-id="73d83-122">Qualquer compilador capaz de gerar objetos COM (Component Object Model) deve funcionar depois que o ambiente do compilador tiver sido configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="73d83-122">Any compiler capable of generating Component Object Model (COM) objects should work once the compiler's environment has been configured correctly.</span></span>

<span data-ttu-id="73d83-123">**Como o DirectShow se relaciona com o Microsoft DirectX?**</span><span class="sxs-lookup"><span data-stu-id="73d83-123">**How does DirectShow relate to Microsoft DirectX?**</span></span>

<span data-ttu-id="73d83-124">Internamente, o DirectShow usa o DirectSound e o DirectDraw quando o hardware dá suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="73d83-124">Internally, DirectShow uses DirectSound and DirectDraw when the hardware supports it.</span></span> <span data-ttu-id="73d83-125">O processador de vídeo e os filtros de mixagem de sobreposição usam superfícies do DirectDraw 3 e do DirectDraw 5.</span><span class="sxs-lookup"><span data-stu-id="73d83-125">The Video Renderer and Overlay Mixer filters use DirectDraw 3 and DirectDraw 5 surfaces.</span></span> <span data-ttu-id="73d83-126">O processador de mixagem de vídeo 7 (somente Windows XP) usa superfícies do DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="73d83-126">The Video Mixing Renderer 7 (Windows XP only) uses DirectDraw 7 surfaces.</span></span> <span data-ttu-id="73d83-127">O processador de mixagem de vídeo 9 e o processador de vídeo aprimorado usam as APIs mais recentes do Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="73d83-127">The Video Mixing Renderer 9 and the Enhanced Video Renderer use the latest Microsoft Direct3D APIs.</span></span> <span data-ttu-id="73d83-128">Você não precisa usar as outras APIs do DirectX para gravar um aplicativo do DirectShow, embora seja possível combiná-los.</span><span class="sxs-lookup"><span data-stu-id="73d83-128">You do not need to use the other DirectX APIs to write a DirectShow application, although it is possible to combine them.</span></span>

<span data-ttu-id="73d83-129">**Como o DirectShow está relacionado ao Microsoft ActiveMovie?**</span><span class="sxs-lookup"><span data-stu-id="73d83-129">**How does DirectShow relate to Microsoft ActiveMovie?**</span></span>

<span data-ttu-id="73d83-130">O ActiveMovie foi o nome original do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="73d83-130">ActiveMovie was the original name for DirectShow.</span></span> <span data-ttu-id="73d83-131">O termo que o ActiveMovie não é mais usado.</span><span class="sxs-lookup"><span data-stu-id="73d83-131">The term ActiveMovie is no longer used.</span></span>

<span data-ttu-id="73d83-132">**O código-fonte para o utilitário GraphEdit está disponível? GraphEdit pode ser redistribuído?**</span><span class="sxs-lookup"><span data-stu-id="73d83-132">**Is the source code to the GraphEdit utility available? Can GraphEdit be redistributed?**</span></span>

<span data-ttu-id="73d83-133">Não, a origem não está disponível e Graphedt.exe não é redistribuível.</span><span class="sxs-lookup"><span data-stu-id="73d83-133">No, the source is not available, and Graphedt.exe is not redistributable.</span></span>

<span data-ttu-id="73d83-134">**DMOs substituir filtros do DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="73d83-134">**Do DMOs replace DirectShow filters?**</span></span>

<span data-ttu-id="73d83-135">O Microsoft DirectX Media Objects (DMOs) pode ser usado em um aplicativo do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="73d83-135">Microsoft DirectX Media Objects (DMOs) can be used in a DirectShow application.</span></span> <span data-ttu-id="73d83-136">Para codificadores, decodificadores e efeitos, você é incentivado a escrever um DMO em vez de um filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="73d83-136">For encoders, decoders, and effects, you are encouraged to write a DMO instead of a DirectShow filter.</span></span> <span data-ttu-id="73d83-137">(Observação: se você quiser usar a aceleração de vídeo do DirectX em seu decodificador, deverá implementá-lo como um filtro.) Para outras finalidades, um filtro do DirectShow pode ser mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="73d83-137">(Note: If you want to use DirectX Video Acceleration in your decoder, you must implement it as a filter.) For other purposes, a DirectShow filter might be more appropriate.</span></span> <span data-ttu-id="73d83-138">Para obter mais informações sobre DMOs, consulte [DirectX Media Objects](directx-media-objects.md).</span><span class="sxs-lookup"><span data-stu-id="73d83-138">For more information about DMOs, see [DirectX Media Objects](directx-media-objects.md).</span></span>

<span data-ttu-id="73d83-139">**Estou executando um arquivo de formato AVI com o Windows Media Player. Posso ouvir o áudio, mas parece que não há nenhum vídeo, eu simplesmente vejo preto. Qual é o problema?**</span><span class="sxs-lookup"><span data-stu-id="73d83-139">**I'm playing an AVI format file with Windows Media Player. I can hear the audio, but there doesn't seem to be any video-instead, I just see black. What's wrong?**</span></span>

<span data-ttu-id="73d83-140">Provavelmente, o arquivo foi codificado com um codec que não está presente no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="73d83-140">Probably the file was encoded with a codec that is not present on your system.</span></span> <span data-ttu-id="73d83-141">Embora o formato de arquivo AVI seja comum, os arquivos AVI podem ser criados com vários formatos de compactação (codecs) diferentes.</span><span class="sxs-lookup"><span data-stu-id="73d83-141">Although the AVI file format is common, AVI files can be created with many different compression formats (codecs).</span></span> <span data-ttu-id="73d83-142">Se você tentar reproduzir um arquivo AVI que usa um codec sem suporte, poderá ouvir o componente de áudio, mas o vídeo será exibido como uma tela preta ou o conteúdo da tela permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="73d83-142">If you try to play an AVI file that uses an unsupported codec, you might hear the audio component, but the video will display as a black screen or the screen contents will remain unchanged.</span></span>

> [!Note]  
> <span data-ttu-id="73d83-143">O Windows Media Player muitas vezes tenta baixar e instalar um codec, caso ele não esteja presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="73d83-143">Windows Media Player often attempts to download and install a codec if it is not present on your system.</span></span>

 

<span data-ttu-id="73d83-144">**Como fazer compilar meu aplicativo? De quais bibliotecas e arquivos de cabeçalho eu preciso?**</span><span class="sxs-lookup"><span data-stu-id="73d83-144">**How do I build my application? What libraries and header files do I need?**</span></span>

<span data-ttu-id="73d83-145">Consulte [Configurando o ambiente de compilação](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="73d83-145">See [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="73d83-146">**O GraphEdit exibe muitos filtros que não estão documentados. O que são esses filtros?**</span><span class="sxs-lookup"><span data-stu-id="73d83-146">**GraphEdit displays a lot of filters that aren't documented. What are these filters?**</span></span>

<span data-ttu-id="73d83-147">GraphEdit enumera todos os filtros registrados em seu sistema em uma categoria de filtro.</span><span class="sxs-lookup"><span data-stu-id="73d83-147">GraphEdit enumerates all of the filters that are registered on your system in a filter category.</span></span> <span data-ttu-id="73d83-148">Isso pode incluir filtros instalados por aplicativos de terceiros ou instalados por outras tecnologias da Microsoft, como o Windows Media ou o NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="73d83-148">This might include filters installed by third-party applications, or installed by other Microsoft technologies, such as Windows Media or NetMeeting.</span></span> <span data-ttu-id="73d83-149">Além disso, alguns filtros do DirectShow atuam como wrappers para codecs ou dispositivos de hardware, com cada codec ou dispositivo exibido como um filtro distinto.</span><span class="sxs-lookup"><span data-stu-id="73d83-149">Also, some DirectShow filters act as wrappers for codecs or hardware devices, with each codec or device appearing as a distinct filter.</span></span> <span data-ttu-id="73d83-150">O codec de vídeo Microsoft H. 263 é usado pelo NetMeeting e não tem mais suporte no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="73d83-150">The Microsoft H.263 Video Codec is used by NetMeeting and is no longer supported in DirectShow.</span></span> <span data-ttu-id="73d83-151">Para obter mais informações, consulte [enumerando dispositivos e filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="73d83-151">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="73d83-152">**Estou tendo problemas para criar meu gráfico personalizado programaticamente.**</span><span class="sxs-lookup"><span data-stu-id="73d83-152">**I'm having trouble building my custom graph programmatically.**</span></span>

<span data-ttu-id="73d83-153">Primeiro, tente criar o grafo de filtro com GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="73d83-153">First try building the filter graph with GraphEdit.</span></span> <span data-ttu-id="73d83-154">Essa ferramenta permite simular muitas possibilidades rapidamente.</span><span class="sxs-lookup"><span data-stu-id="73d83-154">This tool enables you to simulate lots of possibilities quickly.</span></span> <span data-ttu-id="73d83-155">GraphEdit é sempre um ótimo lugar para testar o grafo antes de tentar compilá-lo com o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="73d83-155">GraphEdit is always a great place to test out the graph before attempting to build it with source code.</span></span>

<span data-ttu-id="73d83-156">Para obter mais informações sobre a criação de gráficos, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="73d83-156">For more information about graph building, see the following articles:</span></span>

-   [<span data-ttu-id="73d83-157">Criando o grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="73d83-157">Building the Filter Graph</span></span>](building-the-filter-graph.md)
-   [<span data-ttu-id="73d83-158">Enumerando objetos em um grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="73d83-158">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)

<span data-ttu-id="73d83-159">**Como posso detectar se o DirectShow está instalado em determinado computador?**</span><span class="sxs-lookup"><span data-stu-id="73d83-159">**How can I detect whether DirectShow is installed on a given machine?**</span></span>

<span data-ttu-id="73d83-160">Chame **CoCreateInstance** para criar uma instância do Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="73d83-160">Call **CoCreateInstance** to create an instance of the Filter Graph Manager.</span></span> <span data-ttu-id="73d83-161">Se essa chamada for realizada com sucesso, o DirectShow será instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="73d83-161">If this call succeeds, DirectShow is installed on the machine.</span></span> <span data-ttu-id="73d83-162">O código a seguir mostra como fazer isso:</span><span class="sxs-lookup"><span data-stu-id="73d83-162">The following code shows how to do this:</span></span>


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



<span data-ttu-id="73d83-163">**Como fazer alterar as configurações de um filtro sem exibir a página de propriedades?**</span><span class="sxs-lookup"><span data-stu-id="73d83-163">**How do I change a filter's settings without displaying the property page?**</span></span>

<span data-ttu-id="73d83-164">A maioria dos filtros expõe uma ou mais interfaces para definir propriedades no filtro.</span><span class="sxs-lookup"><span data-stu-id="73d83-164">Most filters expose one or more interfaces for setting properties on the filter.</span></span> <span data-ttu-id="73d83-165">Consulte a página de referência para o filtro em questão.</span><span class="sxs-lookup"><span data-stu-id="73d83-165">Consult the reference page for the filter in question.</span></span> <span data-ttu-id="73d83-166">(Consulte [filtros do DirectShow](directshow-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="73d83-166">(See [DirectShow Filters](directshow-filters.md).)</span></span>

<span data-ttu-id="73d83-167">**Posso testar meu filtro com o GraphEdit?**</span><span class="sxs-lookup"><span data-stu-id="73d83-167">**Can I test my filter with GraphEdit?**</span></span>

<span data-ttu-id="73d83-168">Enquanto você estiver desenvolvendo um filtro, o GraphEdit poderá ajudá-lo a visualizar as conexões entre os filtros.</span><span class="sxs-lookup"><span data-stu-id="73d83-168">While you are developing a filter, GraphEdit can help you to visualize the connections between filters.</span></span> <span data-ttu-id="73d83-169">Ele também pode fornecer um teste rápido da funcionalidade de um filtro.</span><span class="sxs-lookup"><span data-stu-id="73d83-169">It can also provide a quick test of a filter's functionality.</span></span> <span data-ttu-id="73d83-170">No entanto, ela não se destina como uma plataforma de teste robusta.</span><span class="sxs-lookup"><span data-stu-id="73d83-170">However, it is not meant as a robust test platform.</span></span>

<span data-ttu-id="73d83-171">**Em que os filtros do anel de privilégio são executados?**</span><span class="sxs-lookup"><span data-stu-id="73d83-171">**At what privilege ring do filters run?**</span></span>

<span data-ttu-id="73d83-172">Os filtros são executados no anel 3, embora alguns filtros controlem os dispositivos de streaming executados em anel 0.</span><span class="sxs-lookup"><span data-stu-id="73d83-172">Filters run at ring 3, although some filters control streaming devices that run at ring 0.</span></span> <span data-ttu-id="73d83-173">Para obter mais informações, consulte [como os dispositivos de hardware participam do grafo de filtro](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="73d83-173">For more information, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>

<span data-ttu-id="73d83-174">**Preciso usar um depurador de kernel?**</span><span class="sxs-lookup"><span data-stu-id="73d83-174">**Do I need to use a kernel debugger?**</span></span>

<span data-ttu-id="73d83-175">Isso depende de seu projeto específico.</span><span class="sxs-lookup"><span data-stu-id="73d83-175">That depends on your specific project.</span></span> <span data-ttu-id="73d83-176">A instalação das bibliotecas de tempo de execução de depuração do DirectX significa que você está instalando os drivers de depuração e outros componentes do modo kernel, e que, se seu aplicativo causar uma asserção de depuração em um desses componentes, seu computador será reinicializado automaticamente, a menos que você tenha um depurador de kernel anexado ao seu processo.</span><span class="sxs-lookup"><span data-stu-id="73d83-176">Installing the DirectX debug runtime libraries means that you are installing debug drivers and other kernel mode components, and that if your application causes a debug assert in one of these components, your machine will automatically reboot unless you have a kernel debugger attached to your process.</span></span>

<span data-ttu-id="73d83-177">**Quando executo meu aplicativo no depurador, ele falha.**</span><span class="sxs-lookup"><span data-stu-id="73d83-177">**When I run my application in the debugger, it crashes.**</span></span>

<span data-ttu-id="73d83-178">Alguns decodificadores foram projetados para não funcionar enquanto o aplicativo está anexado ao depurador.</span><span class="sxs-lookup"><span data-stu-id="73d83-178">Some decoders are designed not to work while the application is attached to the debugger.</span></span> <span data-ttu-id="73d83-179">Tente executar o aplicativo fora do depurador.</span><span class="sxs-lookup"><span data-stu-id="73d83-179">Try running the application outside the debugger.</span></span>

<span data-ttu-id="73d83-180">**Como funciona a macro de GUID de definição \_ ?**</span><span class="sxs-lookup"><span data-stu-id="73d83-180">**How does the DEFINE\_GUID macro work?**</span></span>

<span data-ttu-id="73d83-181">A macro **definir \_ GUID** resolve o problema de declaração de `extern` referências a valores GUID em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="73d83-181">The **DEFINE\_GUID** macro solves the problem of declaring `extern` references to GUID values in your source code.</span></span> <span data-ttu-id="73d83-182">Por exemplo, suponha que seu projeto tenha três arquivos de origem, Src1. cpp, Src2. cpp e Src3. cpp, e que todos os três arquivos usem um determinado valor de GUID que você definiu.</span><span class="sxs-lookup"><span data-stu-id="73d83-182">For example, suppose that your project has three source files, Src1.cpp, Src2.cpp, and Src3.cpp, and all three files use a certain GUID value that you have defined.</span></span> <span data-ttu-id="73d83-183">O valor de GUID deve ser definido exatamente uma vez no seu projeto e os outros arquivos de origem devem declarar `extern` referências a ele.</span><span class="sxs-lookup"><span data-stu-id="73d83-183">The GUID value must be defined exactly once in your project, and the other source files must declare `extern` references to it.</span></span> <span data-ttu-id="73d83-184">Com a macro **definir \_ GUID** , você pode usar o mesmo arquivo de cabeçalho para ambas as finalidades.</span><span class="sxs-lookup"><span data-stu-id="73d83-184">With the **DEFINE\_GUID** macro, you can use the same header file for both purposes.</span></span> <span data-ttu-id="73d83-185">No arquivo de cabeçalho, declare o GUID da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="73d83-185">In your header file, declare the GUID as follows:</span></span>


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



<span data-ttu-id="73d83-186">(Em que esse exemplo tem zeros, coloque os valores de GUID reais.) Você pode usar o utilitário Guidgen.exe para criar um novo GUID e colá-lo no arquivo de cabeçalho no formato **definir \_ GUID** .</span><span class="sxs-lookup"><span data-stu-id="73d83-186">(Where this example has zeroes, put the actual GUID values.) You can use the Guidgen.exe utility to create a new GUID and paste it into the header file in the **DEFINE\_GUID** format.</span></span> <span data-ttu-id="73d83-187">Inclua esse arquivo de cabeçalho em todos os arquivos de origem que fazem referência ao GUID.</span><span class="sxs-lookup"><span data-stu-id="73d83-187">Include this header file in every source file that references the GUID.</span></span> <span data-ttu-id="73d83-188">Em exatamente um dos arquivos de origem, inclua o arquivo de cabeçalho Initguid. h antes do arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="73d83-188">In exactly one of the source files, include the header file Initguid.h before your header file.</span></span> <span data-ttu-id="73d83-189">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="73d83-189">For example:</span></span>


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



<span data-ttu-id="73d83-190">Sempre que o arquivo de cabeçalho Initguid. h não for incluído, a macro **definir \_ GUID** criará uma `extern` referência ao valor de GUID.</span><span class="sxs-lookup"><span data-stu-id="73d83-190">Wherever the Initguid.h header file is not included, the **DEFINE\_GUID** macro creates an `extern` reference to the GUID value.</span></span> <span data-ttu-id="73d83-191">Quando o arquivo de cabeçalho Initguid. h é incluído, ele redefine a macro **definir \_ GUID** para que **definir o \_ GUID** crie uma declaração de definição do GUID.</span><span class="sxs-lookup"><span data-stu-id="73d83-191">When the Initguid.h header file is included, it redefines the **DEFINE\_GUID** macro so that **DEFINE\_GUID** creates a defining declaration of the GUID.</span></span>

<span data-ttu-id="73d83-192">Se você não incluir Initguid. h em nenhum dos arquivos de origem, receberá um erro de link "símbolo externo não resolvido".</span><span class="sxs-lookup"><span data-stu-id="73d83-192">If you do not include Initguid.h in any of the source files, you will get a link error "unresolved external symbol."</span></span> <span data-ttu-id="73d83-193">Se você incluir Initguid. h duas vezes para o mesmo GUID, receberá um erro de compilação "redefinição; inicialização múltipla ".</span><span class="sxs-lookup"><span data-stu-id="73d83-193">If you include Initguid.h twice for the same GUID, you will get a compile error "redefinition; multiple initialization."</span></span> <span data-ttu-id="73d83-194">Para resolver esses erros, verifique se Initguid. h está incluído exatamente uma vez.</span><span class="sxs-lookup"><span data-stu-id="73d83-194">To resolve these errors, make sure that Initguid.h is included exactly once.</span></span> <span data-ttu-id="73d83-195">Além disso, não inclua Initguid. h dentro de um arquivo de cabeçalho pré-compilado, pois, em vigor, o cabeçalho pré-compilado é incluído em todos os arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="73d83-195">Also, do not include Initguid.h inside a precompiled header file, because in effect the precompiled header is included in every source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73d83-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73d83-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d83-197">Introdução ao DirectShow</span><span class="sxs-lookup"><span data-stu-id="73d83-197">Introduction to DirectShow</span></span>](introduction-to-directshow.md)
</dt> </dl>

 

 



