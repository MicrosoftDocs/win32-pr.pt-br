---
description: Exemplo de filtro do analisador PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Exemplo de filtro do analisador PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551191"
---
# <a name="psi-parser-filter-sample"></a><span data-ttu-id="840ab-103">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="840ab-103">PSI Parser Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="840ab-104">Description</span><span class="sxs-lookup"><span data-stu-id="840ab-104">Description</span></span>

<span data-ttu-id="840ab-105">O filtro do analisador PSI recebe informações específicas do programa (PSI) de um fluxo de transporte MPEG-2 e extrai informações do programa da PAT (tabela de associação de programa) e do pgto (tabelas de mapa do programa).</span><span class="sxs-lookup"><span data-stu-id="840ab-105">The PSI Parser filter receives Program Specific Information (PSI) from an MPEG-2 transport stream and extracts program information from the Program Association Table (PAT) and Program Map Tables (PMT).</span></span> <span data-ttu-id="840ab-106">Essas informações permitem que um aplicativo configure o demultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="840ab-106">This information enables an application to configure the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="840ab-107">O filtro oferece suporte a uma interface personalizada, [**IMpeg2PsiParser**](impeg2psiparser.md), para recuperar as informações de psi.</span><span class="sxs-lookup"><span data-stu-id="840ab-107">The filter supports a custom interface, [**IMpeg2PsiParser**](impeg2psiparser.md), for retrieving the PSI information.</span></span>

<span data-ttu-id="840ab-108">Esse filtro foi projetado para dispositivos MPEG-2, como IEEE 1394 MPEG-2 camcorders e dispositivos D-VHS.</span><span class="sxs-lookup"><span data-stu-id="840ab-108">This filter is designed for MPEG-2 devices, such as IEEE 1394 MPEG-2 camcorders and D-VHS devices.</span></span> <span data-ttu-id="840ab-109">Consulte o [Driver MSTape](mstape-driver.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="840ab-109">See [MSTape Driver](mstape-driver.md) for more information.</span></span> <span data-ttu-id="840ab-110">As fontes de difusão de televisão digital devem usar um filtro TIF para obter informações sobre o programa.</span><span class="sxs-lookup"><span data-stu-id="840ab-110">Digital television broadcast sources should use a TIF filter to get program information.</span></span>

## <a name="usage"></a><span data-ttu-id="840ab-111">Uso</span><span class="sxs-lookup"><span data-stu-id="840ab-111">Usage</span></span>

<span data-ttu-id="840ab-112">Você pode testar o filtro do analisador PSI no GraphEdit da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="840ab-112">You can test the PSI Parser filter in GraphEdit as follows:</span></span>

1.  <span data-ttu-id="840ab-113">Inicie o GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="840ab-113">Launch GraphEdit.</span></span>
2.  <span data-ttu-id="840ab-114">Insira uma fonte de transporte MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="840ab-114">Insert an MPEG-2 transport source.</span></span> <span data-ttu-id="840ab-115">Os dispositivos de camcorder MPEG-2 e D-VHS aparecem como "dispositivo de subunidade de fita AV/C da Microsoft" na categoria fontes de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="840ab-115">MPEG-2 camcorders and D-VHS devices appear as "Microsoft AV/C Tape Subunit Device" in the Video Capture Sources category.</span></span>
3.  <span data-ttu-id="840ab-116">Conecte o filtro de origem ao filtro de Desmultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="840ab-116">Connect the source filter to the MPEG-2 Demultiplexer filter.</span></span>
4.  <span data-ttu-id="840ab-117">Use a página de propriedades no Demux para criar um pino de saída com um tipo de mídia "MPEG-2 PSI".</span><span class="sxs-lookup"><span data-stu-id="840ab-117">Use the property page on the demux to create an output pin with an "MPEG-2 PSI" media type.</span></span> <span data-ttu-id="840ab-118">Esse PIN fornecerá as seções PAT e pgto.</span><span class="sxs-lookup"><span data-stu-id="840ab-118">This pin will deliver the PAT and PMT sections.</span></span>
5.  <span data-ttu-id="840ab-119">Use a página de propriedades Demux para mapear o PID 0x00 para o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="840ab-119">Use the demux property page to map PID 0x00 to the output pin.</span></span> <span data-ttu-id="840ab-120">Defina o tipo de conteúdo como "seções PSI do MPEG2".</span><span class="sxs-lookup"><span data-stu-id="840ab-120">Set the content type to "MPEG2 PSI Sections".</span></span>
6.  <span data-ttu-id="840ab-121">Conecte o pino de saída Demux ao analisador PSI, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="840ab-121">Connect the demux output pin to PSI Parser, as shown in the following diagram.</span></span>

    ![Grafo de filtro do analisador psi](images/psi-parser.png)

7.  <span data-ttu-id="840ab-123">Execute o grafo para alimentar dados PSI ao filtro do analisador PSI.</span><span class="sxs-lookup"><span data-stu-id="840ab-123">Run the graph, in order to feed PSI data to the PSI Parser filter.</span></span> <span data-ttu-id="840ab-124">Como o filtro decodifica as seções PAT, ele mapeia automaticamente os PIDs de PGTO para o mesmo pino de saída no Demux, para que ele receba as seções pgto.</span><span class="sxs-lookup"><span data-stu-id="840ab-124">As the filter decodes the PAT sections, it automatically maps the PMT PIDs to the same output pin on the demux, so that it receives the PMT sections.</span></span>
8.  <span data-ttu-id="840ab-125">Use a página de propriedades do analisador PSI para selecionar um número de programa.</span><span class="sxs-lookup"><span data-stu-id="840ab-125">Use the PSI Parser property page to select a program number.</span></span> <span data-ttu-id="840ab-126">A lista de fluxos elementares na página de propriedades mostrará a PID e o tipo de fluxo associados a cada fluxo elementar no programa selecionado.</span><span class="sxs-lookup"><span data-stu-id="840ab-126">The elementary stream list in the property page will show the PID and stream type associated with each elementary stream in the selected program.</span></span> <span data-ttu-id="840ab-127">A página de propriedades foi projetada para reconhecer os tipos de fluxo definidos no ISO/IEC 13818-1.</span><span class="sxs-lookup"><span data-stu-id="840ab-127">The property page is designed to recognize stream types defined in ISO/IEC 13818-1.</span></span>
9.  <span data-ttu-id="840ab-128">Insira o número da PID de áudio na caixa de edição **pid de áudio** e o número de PID do vídeo na caixa de edição **pid do vídeo** .</span><span class="sxs-lookup"><span data-stu-id="840ab-128">Enter the audio PID number in the **Audio PID** edit box, and the video PID number in the **Video PID** edit box.</span></span>
10. <span data-ttu-id="840ab-129">Clique no botão **Exibir programa** .</span><span class="sxs-lookup"><span data-stu-id="840ab-129">Click the **View Program** button.</span></span> <span data-ttu-id="840ab-130">O analisador PSI configurará os Pins de saída no Demux para corresponder às informações de fluxo do programa e renderizar os Pins.</span><span class="sxs-lookup"><span data-stu-id="840ab-130">The PSI Parser will configure the output pins on the demux to match the program stream information and render the pins.</span></span>

> [!Note]  
> <span data-ttu-id="840ab-131">A página de propriedades do analisador PSI é fornecida para facilitar o teste e fornecer um código de exemplo que configure o demultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="840ab-131">The PSI Parser property page is provided to make testing easier, and to provide sample code that configures the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="840ab-132">Não é recomendável que os aplicativos usem.</span><span class="sxs-lookup"><span data-stu-id="840ab-132">It is not recommended for applications to use.</span></span> <span data-ttu-id="840ab-133">Os aplicativos devem configurar o Demux de forma programática.</span><span class="sxs-lookup"><span data-stu-id="840ab-133">Applications should configure the demux programmatically.</span></span>

 

<span data-ttu-id="840ab-134">Para usar o filtro do analisador PSI em um aplicativo, comece criando o grafo de filtro da origem MPEG-2 para o Demux MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="840ab-134">To use the PSI Parser filter in an application, start by building the filter graph from the MPEG-2 source to the MPEG-2 demux.</span></span> <span data-ttu-id="840ab-135">O código desta etapa não é mostrado aqui, pois a configuração exata do grafo dependerá da origem.</span><span class="sxs-lookup"><span data-stu-id="840ab-135">Code for this step is not shown here, because the exact graph configuration will depend on the source.</span></span>

<span data-ttu-id="840ab-136">Em seguida, crie um PIN de saída no Demux para os dados PSI.</span><span class="sxs-lookup"><span data-stu-id="840ab-136">Next, create an output pin on the demux for the PSI data.</span></span> <span data-ttu-id="840ab-137">MAP PID 0x00, que é reservado para seções PAT, para esse PIN, conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="840ab-137">Map PID 0x00, which is reserved for PAT sections, to this pin, as shown in the following code:</span></span>


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



<span data-ttu-id="840ab-138">Para obter mais informações, consulte [usando o demultiplexador MPEG-2](using-the-mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="840ab-138">For more information, see [Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span></span>

<span data-ttu-id="840ab-139">Adicione o filtro do analisador PSI ao grafo e conecte-o ao pino de saída no Demux.</span><span class="sxs-lookup"><span data-stu-id="840ab-139">Add the PSI Parser filter to the graph and connect it to the output pin on the demux.</span></span> <span data-ttu-id="840ab-140">Consulte o analisador PSI para a interface [**IMpeg2PsiParser**](impeg2psiparser.md) .</span><span class="sxs-lookup"><span data-stu-id="840ab-140">Query the PSI Parser for the [**IMpeg2PsiParser**](impeg2psiparser.md) interface.</span></span> <span data-ttu-id="840ab-141">Agora, execute o grafo e aguarde os \_ eventos de alteração do programa do EC \_ , que sinalizam uma nova seção Pat ou pgto.</span><span class="sxs-lookup"><span data-stu-id="840ab-141">Now run the graph and wait for EC\_PROGRAM\_CHANGED events, which signal a new PAT or PMT section.</span></span> <span data-ttu-id="840ab-142">Esse evento é um evento personalizado definido pelo filtro do analisador PSI.</span><span class="sxs-lookup"><span data-stu-id="840ab-142">This event is a custom event defined by the PSI Parser filter.</span></span> <span data-ttu-id="840ab-143">Ao receber um evento de \_ alteração de programa do EC \_ , você pode obter as informações de psi disponíveis chamando métodos **IMpeg2PsiParser** .</span><span class="sxs-lookup"><span data-stu-id="840ab-143">When you receive an EC\_PROGRAM\_CHANGED event, you can get the available PSI information by calling **IMpeg2PsiParser** methods.</span></span> <span data-ttu-id="840ab-144">Esta seção descreve os métodos que serão necessários com mais frequência.</span><span class="sxs-lookup"><span data-stu-id="840ab-144">This section describes the methods you will need most often.</span></span>

<span data-ttu-id="840ab-145">Para obter o número de programas, use o método [**IMpeg2PsiParser:: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :</span><span class="sxs-lookup"><span data-stu-id="840ab-145">To get the number of programs, use the [**IMpeg2PsiParser::GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) method:</span></span>


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



<span data-ttu-id="840ab-146">Para obter o número do programa para um programa específico, use o método [**IMpeg2PsiParser:: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :</span><span class="sxs-lookup"><span data-stu-id="840ab-146">To get the program number for a specific program, use the [**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) method:</span></span>


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



<span data-ttu-id="840ab-147">O número do programa é usado para obter as entradas de PGTO para programas individuais.</span><span class="sxs-lookup"><span data-stu-id="840ab-147">The program number is used to obtain the PMT entries for individual programs.</span></span> <span data-ttu-id="840ab-148">Para obter o número de fluxos elementares em um programa, use o método [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :</span><span class="sxs-lookup"><span data-stu-id="840ab-148">To get the number of elementary streams in a program, use the [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) method:</span></span>


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



<span data-ttu-id="840ab-149">Para cada fluxo elementar, o método [**IMpeg2PsiParser:: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) retorna o PID e o método [**IMpeg2PsiParser:: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) retorna o tipo de fluxo:</span><span class="sxs-lookup"><span data-stu-id="840ab-149">For each elementary stream, the [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) method returns the PID, and the [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) method returns the stream type:</span></span>


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



<span data-ttu-id="840ab-150">A PID e o tipo de fluxo permitem configurar novos PINs de saída no demultiplexador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="840ab-150">The PID and the stream type enable you to configure new output pins on the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="840ab-151">Isso pode exigir algum conhecimento da fonte original.</span><span class="sxs-lookup"><span data-stu-id="840ab-151">This may require some knowledge of the original source.</span></span> <span data-ttu-id="840ab-152">Por exemplo, o ISO/IEC 13818-1 define os tipos de fluxo 0x80 por meio de 0xFF como "particular do usuário", mas outros padrões baseados em MPEG-2 podem atribuir outros significados a esses tipos.</span><span class="sxs-lookup"><span data-stu-id="840ab-152">For example, ISO/IEC 13818-1 defines stream types 0x80 through 0xFF as "user private," but other standards that are based on MPEG-2 may assign other meanings to these types.</span></span>

<span data-ttu-id="840ab-153">O demultiplexador MPEG-2 pode criar novos PINs e novos mapeamentos de PID enquanto o grafo está em execução, mas você deve parar o grafo para conectar Pins.</span><span class="sxs-lookup"><span data-stu-id="840ab-153">The MPEG-2 Demultiplexer can create new pins and new PID mappings while the graph is running, but you must stop the graph to connect pins.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="840ab-154">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="840ab-154">Downloading the Sample</span></span>

<span data-ttu-id="840ab-155">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="840ab-155">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="840ab-156">Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ amostras de multimídia do \\ \\ DirectShow \\ \\ PSIParser.</span><span class="sxs-lookup"><span data-stu-id="840ab-156">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PSIParser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="840ab-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="840ab-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="840ab-158">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="840ab-158">DirectShow Samples</span></span>](directshow-samples.md)
</dt> <dt>

[<span data-ttu-id="840ab-159">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="840ab-159">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> </dl>

 

 
