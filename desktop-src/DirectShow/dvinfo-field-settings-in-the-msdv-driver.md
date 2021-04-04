---
description: Configurações de campo DVINFO no driver MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Configurações de campo DVINFO no driver MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645941"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a><span data-ttu-id="6687b-103">Configurações de campo DVINFO no driver MSDV</span><span class="sxs-lookup"><span data-stu-id="6687b-103">DVINFO Field Settings in the MSDV Driver</span></span>

<span data-ttu-id="6687b-104">Esta seção descreve como o driver MSDV preenche a estrutura [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="6687b-104">This section describes how the MSDV driver fills in the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="6687b-105">A `DVINFO` estrutura define o bloco de formato para conexões de PIN entre MSDV e outros filtros.</span><span class="sxs-lookup"><span data-stu-id="6687b-105">The `DVINFO` structure defines the format block for pin connections between MSDV and other filters.</span></span> <span data-ttu-id="6687b-106">Por padrão, o filtro de Splitter de DV é usado durante a captura de um dispositivo DV e o filtro de MUX DV é usado ao transmitir para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6687b-106">By default, the DV Splitter filter is used when capturing from a DV device, and the DV Mux filter is used when transmitting to the device.</span></span> <span data-ttu-id="6687b-107">No entanto, os aplicativos podem fornecer seus próprios filtros personalizados, portanto, é útil entender como o MSDV popula o `DVINFO` bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="6687b-107">However, applications may provide their own custom filters, so it is useful to understand how MSDV populates the `DVINFO` format block.</span></span>

<span data-ttu-id="6687b-108">A `DVINFO` estrutura contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="6687b-108">The `DVINFO` structure contains the following information:</span></span>

-   <span data-ttu-id="6687b-109">Dois pacotes de origem auxiliares de áudio (AAUX), para o primeiro e o segundo blocos de áudio.</span><span class="sxs-lookup"><span data-stu-id="6687b-109">Two audio auxiliary (AAUX) source packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="6687b-110">Dois pacotes de controle do código-fonte AAUX para o primeiro e o segundo blocos de áudio.</span><span class="sxs-lookup"><span data-stu-id="6687b-110">Two AAUX source control packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="6687b-111">Um pacote de origem do VAUX (vídeo auxiliar).</span><span class="sxs-lookup"><span data-stu-id="6687b-111">A video auxiliary (VAUX) source pack.</span></span>
-   <span data-ttu-id="6687b-112">Um pacote de controle do código-fonte VAUX.</span><span class="sxs-lookup"><span data-stu-id="6687b-112">A VAUX source control pack.</span></span>

<span data-ttu-id="6687b-113">Cada quadro em um fluxo de DV contém os pacotes AAUX e VAUX.</span><span class="sxs-lookup"><span data-stu-id="6687b-113">Every frame in a DV stream contains AAUX and VAUX packs.</span></span> <span data-ttu-id="6687b-114">No entanto, o `DVINFO` bloco de formato é estático e é usado somente para estabelecer a conexão do PIN.</span><span class="sxs-lookup"><span data-stu-id="6687b-114">However, the `DVINFO` format block is static, and is only used to establish the pin connection.</span></span> <span data-ttu-id="6687b-115">Quando o driver MSDV se conecta, ele não examina nenhum dos pacotes AAUX ou VAUX no fluxo.</span><span class="sxs-lookup"><span data-stu-id="6687b-115">When the MSDV driver connects, it does not examine any of the AAUX or VAUX packs in the stream.</span></span> <span data-ttu-id="6687b-116">Em vez disso, ele usa um conjunto de valores padrão, com base nas seguintes características do dispositivo DV:</span><span class="sxs-lookup"><span data-stu-id="6687b-116">Instead, it uses a set of default values, based on the following characteristics of the DV device:</span></span>

-   <span data-ttu-id="6687b-117">Se o dispositivo dá suporte a um formato de consumidor (DVCR) ou a um formato profissional (DVCPRO)</span><span class="sxs-lookup"><span data-stu-id="6687b-117">Whether the device supports a consumer format (DVCR) or professional format (DVCPRO)</span></span>
-   <span data-ttu-id="6687b-118">O tipo de sinal</span><span class="sxs-lookup"><span data-stu-id="6687b-118">The signal type</span></span>
-   <span data-ttu-id="6687b-119">Se o formato é NTSC ou PAL.</span><span class="sxs-lookup"><span data-stu-id="6687b-119">Whether the format is NTSC or PAL.</span></span> <span data-ttu-id="6687b-120">(Se o dispositivo não relatar essas informações, MSDV o padrão às configurações de NTSC)</span><span class="sxs-lookup"><span data-stu-id="6687b-120">(If the device does not report this information, MSDV defaults to the NTSC settings)</span></span>

<span data-ttu-id="6687b-121">Quando o streaming começa, é responsabilidade dos filtros do modo de usuário, como o divisor DV, examinar o conteúdo real de cada quadro DV.</span><span class="sxs-lookup"><span data-stu-id="6687b-121">Once streaming begins, it is the responsibility of the user-mode filters, such as the DV Splitter, to examine the actual contents of each DV frame.</span></span> <span data-ttu-id="6687b-122">Como as informações podem mudar de quadro para quadro, o filtro pode precisar executar uma alteração de formato dinâmico.</span><span class="sxs-lookup"><span data-stu-id="6687b-122">Because the information can change from frame to frame, the filter may need to perform a dynamic format change.</span></span> <span data-ttu-id="6687b-123">Por exemplo, se a taxa de áudio for alterada, o filtro poderá precisar renegociar o tipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="6687b-123">For example, if the audio rate changes, the filter might need to renegotiate the audio type.</span></span>

<span data-ttu-id="6687b-124">Se você capturar um arquivo DV tipo-1, a `DVINFO` estrutura será gravada no arquivo como a parte do formato de fluxo (' strf ').</span><span class="sxs-lookup"><span data-stu-id="6687b-124">If you capture a type-1 DV file, the `DVINFO` structure is written into the file as the stream format ('strf') chunk.</span></span> <span data-ttu-id="6687b-125">Esses dados são obtidos diretamente do bloco de formato fornecido pelo MSDV.</span><span class="sxs-lookup"><span data-stu-id="6687b-125">This data is taken directly from the format block provided by MSDV.</span></span> <span data-ttu-id="6687b-126">Como observado, o conteúdo real do fluxo pode ser diferente.</span><span class="sxs-lookup"><span data-stu-id="6687b-126">As noted, the actual content of the stream might be different.</span></span> <span data-ttu-id="6687b-127">É responsabilidade do aplicativo examinar os pacotes AAUX e VAUX em cada quadro.</span><span class="sxs-lookup"><span data-stu-id="6687b-127">It is the application's responsibility to examine the AAUX and VAUX packs in each frame.</span></span>

<span data-ttu-id="6687b-128">Nos tópicos a seguir, você pode encontrar tabelas listando todos os campos usados pelo MSDV.</span><span class="sxs-lookup"><span data-stu-id="6687b-128">In the following topics, you can find tables listing all of the fields used by MSDV.</span></span>

-   [<span data-ttu-id="6687b-129">Pacote de origem do AAUX (AS)</span><span class="sxs-lookup"><span data-stu-id="6687b-129">AAUX Source (AS) Pack</span></span>](aaux-source--as--pack.md)
-   [<span data-ttu-id="6687b-130">Pacote de controle do código-fonte AAUX (ASC)</span><span class="sxs-lookup"><span data-stu-id="6687b-130">AAUX Source Control (ASC) Pack</span></span>](aaux-source-control--asc--pack.md)
-   [<span data-ttu-id="6687b-131">Pacote de origem do VAUX (VS)</span><span class="sxs-lookup"><span data-stu-id="6687b-131">VAUX Source (VS) Pack</span></span>](vaux-source--vs--pack.md)
-   [<span data-ttu-id="6687b-132">Pacote de controle do código-fonte (VSC) VAUX</span><span class="sxs-lookup"><span data-stu-id="6687b-132">VAUX Source Control (VSC) Pack</span></span>](vaux-source-control--vsc--pack.md)

<span data-ttu-id="6687b-133">Ao ler essas tabelas, consulte as especificações a seguir:</span><span class="sxs-lookup"><span data-stu-id="6687b-133">When reading these tables, please consult the following specifications:</span></span>

-   <span data-ttu-id="6687b-134">IEC 61834</span><span class="sxs-lookup"><span data-stu-id="6687b-134">IEC 61834</span></span>
-   <span data-ttu-id="6687b-135">314M SMPTE</span><span class="sxs-lookup"><span data-stu-id="6687b-135">SMPTE 314M</span></span>
-   <span data-ttu-id="6687b-136">SMPTE 370</span><span class="sxs-lookup"><span data-stu-id="6687b-136">SMPTE 370</span></span>

<span data-ttu-id="6687b-137">Em cada tabela, a primeira coluna fornece o código de campo, seguido pelo número de bits (entre parênteses).</span><span class="sxs-lookup"><span data-stu-id="6687b-137">In each table, the first column gives the field code, followed by the number of bits (in parentheses).</span></span> <span data-ttu-id="6687b-138">As colunas restantes fornecem os valores de campo.</span><span class="sxs-lookup"><span data-stu-id="6687b-138">The remaining columns give the field values.</span></span> <span data-ttu-id="6687b-139">Muitos dos campos AAUX e VAUX não são relevantes para a conexão de PIN; nesse caso, MSDV define um valor fictício.</span><span class="sxs-lookup"><span data-stu-id="6687b-139">Many of the AAUX and VAUX fields are not relevant for the pin connection, in which case MSDV sets a dummy value.</span></span> <span data-ttu-id="6687b-140">O valor numérico do pacote inteiro é listado na parte inferior de cada tabela.</span><span class="sxs-lookup"><span data-stu-id="6687b-140">The numeric value of the entire pack is listed at the bottom of each table.</span></span>

<span data-ttu-id="6687b-141">As observações depois de cada tabela fornecem mais informações sobre os campos selecionados.</span><span class="sxs-lookup"><span data-stu-id="6687b-141">The notes after each table give more information about selected fields.</span></span> <span data-ttu-id="6687b-142">Para obter descrições completas, consulte as especificações.</span><span class="sxs-lookup"><span data-stu-id="6687b-142">For complete descriptions, refer to the specifications.</span></span> <span data-ttu-id="6687b-143">Além disso, alguns campos não têm o mesmo significado em SMPTE 314M/SMPTE 370 como no IEC 61834.</span><span class="sxs-lookup"><span data-stu-id="6687b-143">Also, some fields do not have the same meaning in SMPTE 314M/SMPTE 370 as they do in IEC 61834.</span></span>

> [!Note]  
> <span data-ttu-id="6687b-144">Atualmente, o DirectShow não oferece suporte a formatos DVCPRO.</span><span class="sxs-lookup"><span data-stu-id="6687b-144">Currently, DirectShow does not support DVCPRO formats.</span></span> <span data-ttu-id="6687b-145">Os valores listados para os formatos DVCPRO são definidos para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6687b-145">The values listed for the DVCPRO formats are defined for future use.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6687b-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6687b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6687b-147">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="6687b-147">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6687b-148">Dados de DV no formato de arquivo AVI</span><span class="sxs-lookup"><span data-stu-id="6687b-148">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[<span data-ttu-id="6687b-149">Driver MSDV</span><span class="sxs-lookup"><span data-stu-id="6687b-149">MSDV Driver</span></span>](msdv-driver.md)
</dt> </dl>

 

 



