---
description: Criando o objeto Multiplexador
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Criando o objeto Multiplexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164208"
---
# <a name="creating-the-multiplexer-object"></a><span data-ttu-id="53791-103">Criando o objeto Multiplexador</span><span class="sxs-lookup"><span data-stu-id="53791-103">Creating the Multiplexer Object</span></span>

<span data-ttu-id="53791-104">O multiplexador de ASF é um objeto de camada WMContainer que funciona com o [objeto de dados ASF](asf-file-structure.md) e dá a um aplicativo a capacidade de gerar pacotes de dados ASF para fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="53791-104">The ASF multiplexer is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for media streams.</span></span>

<span data-ttu-id="53791-105">O objeto multiplexador expõe a interface [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) .</span><span class="sxs-lookup"><span data-stu-id="53791-105">The multiplexer object exposes the [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) interface.</span></span> <span data-ttu-id="53791-106">Para criar o multiplexador, chame [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span><span class="sxs-lookup"><span data-stu-id="53791-106">To create the multiplexer, call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span></span> <span data-ttu-id="53791-107">Essa função retorna um ponteiro para um objeto vazio.</span><span class="sxs-lookup"><span data-stu-id="53791-107">This function returns a pointer to an empty object.</span></span> <span data-ttu-id="53791-108">Se o aplicativo estiver gravando um novo arquivo ASF, o aplicativo deverá inicializar o multiplexador com um objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="53791-108">If the application is writing a new ASF file, the application must initialize the multiplexer with a ContentInfo object.</span></span> <span data-ttu-id="53791-109">Para fazer isso, chame [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="53791-109">To do this, call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span></span> <span data-ttu-id="53791-110">O objeto ContentInfo especificado representa o objeto de cabeçalho ASF do novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="53791-110">The specified ContentInfo object represents the ASF Header Object of the new file.</span></span> <span data-ttu-id="53791-111">Para obter informações sobre como criar e inicializar o objeto ContentInfo para um novo arquivo, consulte [inicializando o objeto ContentInfo de um novo arquivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="53791-111">For information about creating and initializing the ContentInfo object for a new file, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>

<span data-ttu-id="53791-112">O método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analisa o objeto ContentInfo para coletar informações de configuração de fluxo, como o número de fluxos, o tamanho do pacote, a preversão.</span><span class="sxs-lookup"><span data-stu-id="53791-112">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method parses the ContentInfo object to collect stream configuration information such as the number of streams, packet size, preroll.</span></span> <span data-ttu-id="53791-113">Opcionalmente, o multiplexador também pode precisar de parâmetros de Bucket de vazamento e das unidades de extensão de carga.</span><span class="sxs-lookup"><span data-stu-id="53791-113">Optionally, the multiplexer might also need leaky bucket parameters, and the payload extension units.</span></span> <span data-ttu-id="53791-114">Essas informações são necessárias para gerar pacotes de dados que correspondam aos requisitos definidos no objeto de cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="53791-114">This information is required in order to generate data packets that match the requirements defined in the ASF Header Object.</span></span> <span data-ttu-id="53791-115">O método **Initialize** configura o multiplexador com base no tipo de mídia e nas definições de configuração dos fluxos.</span><span class="sxs-lookup"><span data-stu-id="53791-115">The **Initialize** method configures the multiplexer based on the media type and configuration settings of the streams.</span></span> <span data-ttu-id="53791-116">Por exemplo, se um fluxo estiver configurado para ter extensões de carga (consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md)) e, em seguida, o multiplexador será configurado para adicionar esses valores aos pacotes de dados gerados.</span><span class="sxs-lookup"><span data-stu-id="53791-116">For example, if a stream is configured to have payload extensions (see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md)), and then the multiplexer is configured to add those values to the generated data packets.</span></span>

<span data-ttu-id="53791-117">O método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) também obtém um identificador para o objeto de dados inicial que foi criado durante a criação do objeto ContentInfo para gravação.</span><span class="sxs-lookup"><span data-stu-id="53791-117">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method also gets a handle to the initial data object that was created during the creation of the ContentInfo object for writing.</span></span> <span data-ttu-id="53791-118">Durante a geração de pacotes de dados, o multiplexador adiciona pacotes ao objeto de dados e os atualiza adequadamente.</span><span class="sxs-lookup"><span data-stu-id="53791-118">During data packet generation, the multiplexer adds packets to the data object and updates it appropriately.</span></span> <span data-ttu-id="53791-119">Depois que o multiplexador gera todos os pacotes de dados, ele atualiza o objeto ContentInfo fornecido para que determinados valores, como o número de pacotes de dados, sejam atualizados.</span><span class="sxs-lookup"><span data-stu-id="53791-119">After the multiplexer generates all the data packets, it updates the supplied ContentInfo object so that certain values, such as number of data packets, are updated.</span></span>

<span data-ttu-id="53791-120">O exemplo de código a seguir mostra como criar um multiplexador e inicializá-lo com um objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="53791-120">The following code example shows how to create a multiplexer and initialize it with a ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



<span data-ttu-id="53791-121">Para ver essa função usada em um aplicativo completo, consulte [tutorial: copiando fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="53791-121">To see this function used in a complete application, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a><span data-ttu-id="53791-122">Inicialização do Multiplexador e configurações de Bucket de vazamento</span><span class="sxs-lookup"><span data-stu-id="53791-122">Multiplexer Initialization and Leaky Bucket Settings</span></span>

<span data-ttu-id="53791-123">O método [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura o multiplexador para determinar o fluxo de dados do Bucket de vazamento.</span><span class="sxs-lookup"><span data-stu-id="53791-123">The [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method configures the multiplexer to determine the leaky bucket data flow.</span></span> <span data-ttu-id="53791-124">Para configurar esses parâmetros, verifique se os valores de propriedade a seguir estão definidos no objeto ContentInfo especificado.</span><span class="sxs-lookup"><span data-stu-id="53791-124">To configure these parameters, make sure that the following property values are set on the specified ContentInfo object.</span></span> <span data-ttu-id="53791-125">Para obter informações sobre como definir essas propriedades, consulte [definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="53791-125">For information about setting these properties, see [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

-   <span data-ttu-id="53791-126">[**MFPKEY \_ Propriedade de \_ \_ taxa de bits de ajuste**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) automático do ASFMEDIASINK: indica se o multiplexador precisa ajustar a taxa de bits automaticamente para manter o fluxo de dados no Bucket de vazamentos.</span><span class="sxs-lookup"><span data-stu-id="53791-126">[**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) property: This indicates whether the multiplexer needs to adjust the bit rate automatically, to maintain the data flow in the leaky bucket.</span></span> <span data-ttu-id="53791-127">Essa configuração pode ser alterada pelo aplicativo chamando [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) e passando o sinalizador de **taxa de \_ bits de \_ AutoAjuste \_ do Multiplexador MFASF** .</span><span class="sxs-lookup"><span data-stu-id="53791-127">This setting can be changed by the application by calling [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) and passing the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span>

-   <span data-ttu-id="53791-128">[**MFPKEY \_ Propriedade \_ \_ sendtime de base ASFMEDIASINK**](mfpkey-asfmediasink-base-sendtime-property.md) : a hora de envio indica quando a carga dentro do Bucket de vazamento será liberada.</span><span class="sxs-lookup"><span data-stu-id="53791-128">[**MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) property: The send time indicates when the payload inside the leaky bucket will be released.</span></span> <span data-ttu-id="53791-129">Os horários de envio devem ser iguais ou anteriores ao horário da apresentação, pois a carga deve ter tempo para chegar ao destino antes da hora da apresentação.</span><span class="sxs-lookup"><span data-stu-id="53791-129">Send times must be equal to or earlier than the presentation time because the payload must have time to get to the destination before the presentation time.</span></span>

    <span data-ttu-id="53791-130">Esse valor de propriedade é a primeira hora de envio.</span><span class="sxs-lookup"><span data-stu-id="53791-130">This property value is the first send time.</span></span> <span data-ttu-id="53791-131">O multiplexador usa esse valor para calcular os tempos de envio subsequentes para garantir que os dados fluem pelo Bucket constantemente.</span><span class="sxs-lookup"><span data-stu-id="53791-131">The multiplexer uses this value to calculate the subsequent send times to ensure that data flows through the bucket steadily.</span></span> <span data-ttu-id="53791-132">Se o sinalizador de **taxa de bits do MFASF \_ multiplexador \_ AutoAjuste \_** tiver sido definido no Multiplexador, o multiplexador ajustará a taxa de bits para que a carga seja enviada quando a janela do buffer estiver perto de estar cheia.</span><span class="sxs-lookup"><span data-stu-id="53791-132">If the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag has been set on the multiplexer, the multiplexer will adjust the bit rate so that the payload is sent out when the buffer window is close to being full.</span></span> <span data-ttu-id="53791-133">Se o sinalizador não estiver definido, o multiplexador falhará ao gerar pacotes de dados devido à saturação da largura de banda.</span><span class="sxs-lookup"><span data-stu-id="53791-133">If the flag is not set, the multiplexer fails to generate data packets due to bandwidth overrun.</span></span>

<span data-ttu-id="53791-134">O multiplexador Obtém informações de configuração de fluxo do perfil ASF associado ao objeto ContentInfo especificado no método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) .</span><span class="sxs-lookup"><span data-stu-id="53791-134">The multiplexer obtains stream configuration information from the ASF profile associated with the ContentInfo object specified in the [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method.</span></span> <span data-ttu-id="53791-135">As informações de configuração de fluxo incluem parâmetros de Bucket de vazamentos.</span><span class="sxs-lookup"><span data-stu-id="53791-135">The stream configuration information includes leaky bucket parameters.</span></span> <span data-ttu-id="53791-136">Esse valor é exigido pelo multiplexador para gerar pacotes de dados.</span><span class="sxs-lookup"><span data-stu-id="53791-136">This value is required by the multiplexer to generate data packets.</span></span>

<span data-ttu-id="53791-137">Para especificar os parâmetros de Bucket de vazamento, defina os valores no atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) no objeto de configuração de fluxo que representa o fluxo no perfil.</span><span class="sxs-lookup"><span data-stu-id="53791-137">To specify the leaky bucket parameters, set the values in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream configuration object that represents the stream in the profile.</span></span> <span data-ttu-id="53791-138">Para usar o valor da janela buffer, que é usado pelo codificador, chame [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="53791-138">To use the buffer window value, which is used by the encoder, call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span> <span data-ttu-id="53791-139">O valor da janela de buffer real só é conhecido depois de definir o tipo de mídia de saída do codificador.</span><span class="sxs-lookup"><span data-stu-id="53791-139">The actual buffer window value is known only after setting the output media type of the encoder.</span></span> <span data-ttu-id="53791-140">Para obter informações sobre como definir o tipo de mídia de saída, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="53791-140">For information about setting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="53791-141">Os valores de Bucket de vazamento usados pelo codificador podem ser diferentes no objeto ContentInfo que foi fornecido pelo perfil ASF que foi usado para criar o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="53791-141">The leaky bucket values used by the encoder might be different in the ContentInfo object that was provided by the ASF Profile that was used to create the multiplexer.</span></span>

 

<span data-ttu-id="53791-142">O método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) atualiza o objeto ContentInfo para que os valores corretos sejam refletidos no objeto de cabeçalho ASF final.</span><span class="sxs-lookup"><span data-stu-id="53791-142">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method updates the ContentInfo object so that the correct values are reflected in the final ASF Header Object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53791-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53791-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53791-144">Multiplexador ASF</span><span class="sxs-lookup"><span data-stu-id="53791-144">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="53791-145">Gerando novos pacotes de dados ASF</span><span class="sxs-lookup"><span data-stu-id="53791-145">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
