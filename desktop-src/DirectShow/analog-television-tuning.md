---
description: Ajuste de televisão analógica
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Ajuste de televisão analógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754780"
---
# <a name="analog-television-tuning"></a><span data-ttu-id="8ab7f-103">Ajuste de televisão analógica</span><span class="sxs-lookup"><span data-stu-id="8ab7f-103">Analog Television Tuning</span></span>

<span data-ttu-id="8ab7f-104">O ajuste é controlado pelo filtro de sintonizador de TV, por meio da interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="8ab7f-104">Tuning is controlled by the TV Tuner filter, through the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="8ab7f-105">A interface IAMTVTuner herda IAMTuner.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-105">The IAMTVTuner interface inherits IAMTuner.</span></span> <span data-ttu-id="8ab7f-106">Para obter um ponteiro para a interface, chame o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8ab7f-106">To obtain a pointer to the interface, call the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method as follows:</span></span>


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



<span data-ttu-id="8ab7f-107">O primeiro parâmetro indica a pesquisa de upstream a partir do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-107">The first parameter indicates to search upstream from the capture filter.</span></span>

<span data-ttu-id="8ab7f-108">Tabelas de frequência</span><span class="sxs-lookup"><span data-stu-id="8ab7f-108">Frequency Tables</span></span>

<span data-ttu-id="8ab7f-109">Internamente, o filtro de sintonizador de TV mantém uma lista de tabelas de frequência.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-109">Internally, the TV Tuner filter keeps a list of frequency tables.</span></span> <span data-ttu-id="8ab7f-110">Cada tabela de frequência corresponde à frequência de transmissão ou de cabo para um determinado país/região.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-110">Each frequency table corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="8ab7f-111">Também há uma tabela de frequência "unicable" genérica, que é usada quando um país/região não tem um conjunto padrão de atribuições de frequência.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-111">There is also a generic "Unicable" frequency table, which is used when a country/region does not have a standard set of frequency assignments.</span></span>

<span data-ttu-id="8ab7f-112">Cada tabela Frequency contém uma lista de frequências de ajuste.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-112">Each frequency table contains a list of tuning frequencies.</span></span> <span data-ttu-id="8ab7f-113">Para alguns países/regiões, os índices na tabela correspondem diretamente aos números de canal – em outras palavras, a frequência do canal n é a entrada n-th na tabela.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-113">For some countries/regions, the indexes in the table correspond directly to channel numbers — in other words, the frequency for channel n is the n th entry in the table.</span></span> <span data-ttu-id="8ab7f-114">No entanto, para alguns países/regiões, não há nenhuma correspondência direta entre números de canal e frequências.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-114">For some countries/regions, however, there is no direct correspondence between channel numbers and frequencies.</span></span> <span data-ttu-id="8ab7f-115">Nesse caso, o aplicativo deve manter uma lista que mapeia os números de canal (normalmente escolhidos pelo usuário) para as entradas da tabela de frequência.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-115">In that case, the application must keep a list that maps channel numbers (typically chosen by the user) to frequency table entries.</span></span> <span data-ttu-id="8ab7f-116">Por exemplo, o que o usuário vê como "canal 5" pode ser a entrada número 12 na tabela de frequência.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-116">For example, what the user sees as "channel 5" might be entry number 12 in the frequency table.</span></span>

<span data-ttu-id="8ab7f-117">Para obter detalhes, consulte [ajuste de TV analógica internacional](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="8ab7f-117">For details, see [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span>

<span data-ttu-id="8ab7f-118">Operações básicas de ajuste</span><span class="sxs-lookup"><span data-stu-id="8ab7f-118">Basic Tuning Operations</span></span>

<span data-ttu-id="8ab7f-119">Se o sintonizador der suporte a vários modos de recepção, como televisão e FM Radio, chame [**IAMTuner::p \_ modo UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) para selecionar o modo.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-119">If the tuner supports multiple reception modes, such as television and FM radio, call [**IAMTuner::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) to select the mode.</span></span> <span data-ttu-id="8ab7f-120">O método [**IAMTuner:: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) retorna todos os modos aos quais o sintonizador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-120">The [**IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) method returns all of the modes that the tuner supports.</span></span> <span data-ttu-id="8ab7f-121">Por exemplo, o código a seguir verifica se o sintonizador dá suporte a rádio FM e, em caso afirmativo, alterna para esse modo.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-121">For example, the following code checks whether the tuner supports FM radio, and if so, switches to that mode.</span></span>


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



<span data-ttu-id="8ab7f-122">Para definir o país/região, chame o método [**IAMTuner::p UT \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) .</span><span class="sxs-lookup"><span data-stu-id="8ab7f-122">To set the country/region, call the [**IAMTuner::put\_CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) method.</span></span> <span data-ttu-id="8ab7f-123">O sintonizador usa esse valor para selecionar a tabela de frequência apropriada.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-123">The tuner uses this value to select the appropriate frequency table.</span></span> <span data-ttu-id="8ab7f-124">Confira [atribuições de país/região](country-region-assignments.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-124">See [Country/Region Assignments](country-region-assignments.md) for more information.</span></span>

<span data-ttu-id="8ab7f-125">Para definir o canal, chame o método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) .</span><span class="sxs-lookup"><span data-stu-id="8ab7f-125">To set the channel, call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method.</span></span> <span data-ttu-id="8ab7f-126">O argumento para esse método não é, na verdade, um número de canal, mas sim um índice na tabela de frequência atual.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-126">The argument to this method is actually not a channel number, but rather an index into the current frequency table.</span></span> <span data-ttu-id="8ab7f-127">Conforme descrito anteriormente, o número de índice pode ou não corresponder a um número de canal.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-127">As described previously, the index number may or may not correspond to a channel number.</span></span> <span data-ttu-id="8ab7f-128">O método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) retorna os valores de índice mínimo e máximo para a tabela de frequência atual.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-128">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method returns the minimum and maximum index values for the current frequency table.</span></span>

<span data-ttu-id="8ab7f-129">Substituindo entradas de frequência</span><span class="sxs-lookup"><span data-stu-id="8ab7f-129">Overriding Frequency Entries</span></span>

<span data-ttu-id="8ab7f-130">É possível que algumas entradas nas tabelas Frequency estejam incorretas ou se tornem obsoletas.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-130">It is possible that some entries in the frequency tables might be incorrect or become obsolete.</span></span> <span data-ttu-id="8ab7f-131">Portanto, um mecanismo é fornecido para substituir entradas individuais usando chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-131">Therefore, a mechanism is provided for overriding individual entries using registry keys.</span></span>

<span data-ttu-id="8ab7f-132">As especificações são explicadas no tópico [ajuste de TV analógica internacional](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="8ab7f-132">The specifics are explained in the topic [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span> <span data-ttu-id="8ab7f-133">Cada chave do registro define um "espaço de ajuste" que contém uma ou mais subchaves.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-133">Each registry key defines a "tuning space" which contains one or more subkeys.</span></span> <span data-ttu-id="8ab7f-134">Cada subchave substitui uma entrada de frequência.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-134">Each subkey overrides one frequency entry.</span></span> <span data-ttu-id="8ab7f-135">Para definir o espaço de ajuste atual, use o método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) .</span><span class="sxs-lookup"><span data-stu-id="8ab7f-135">To set the current tuning space, use the [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method.</span></span> <span data-ttu-id="8ab7f-136">Ativar o espaço de ajuste substitui as entradas de frequência na tabela de frequência atual.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-136">Activating the tuning space overrides the frequency entries in the current frequency table.</span></span> <span data-ttu-id="8ab7f-137">Portanto, cabe ao aplicativo manter uma correspondência entre espaços de ajuste e países/regiões.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-137">Therefore, it is up to the application to maintain a correspondence between tuning spaces and countries/regions.</span></span> <span data-ttu-id="8ab7f-138">A melhor abordagem é simplesmente usar o identificador de país/região como o nome do espaço de sintonia.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-138">The best approach is simply to use the country/region identifier as the name of the tuning space.</span></span>

<span data-ttu-id="8ab7f-139">Ajuste fino das entradas de frequência</span><span class="sxs-lookup"><span data-stu-id="8ab7f-139">Fine Tuning the Frequency Entries</span></span>

<span data-ttu-id="8ab7f-140">As frequências de difusão podem ser ajustadas ou reduzidas a vários kHz pela estação de difusão para reduzir a possibilidade de interferência com canais vizinhos.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-140">Broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span> <span data-ttu-id="8ab7f-141">Dada a frequência nominal, o cartão sintonizador pode verificar a frequência exata.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-141">Given the nominal frequency, the tuner card can scan for the exact frequency.</span></span> <span data-ttu-id="8ab7f-142">O filtro de sintonizador de TV tem um mecanismo para salvar as frequências ajustadas no registro.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-142">The TV Tuner filter has a mechanism for saving the adjusted frequencies in the registry.</span></span>

<span data-ttu-id="8ab7f-143">Para cada entrada na tabela Frequency, chame o método Put \_ Channel para ajustar a essa frequência.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-143">For each entry in the frequency table, call the put\_Channel method to tune to that frequency.</span></span> <span data-ttu-id="8ab7f-144">O sintonizador examinará a frequência mais precisa.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-144">The tuner will scan for the most precise frequency.</span></span> <span data-ttu-id="8ab7f-145">Você pode verificar se o sintonizador obteve um bloqueio horizontal chamando [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span><span class="sxs-lookup"><span data-stu-id="8ab7f-145">You can check whether the tuner achieved a horizontal lock by calling [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span></span> <span data-ttu-id="8ab7f-146">O filtro de sintonizador de TV também armazena o resultado internamente.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-146">The TV Tuner filter also stores the result internally.</span></span>

<span data-ttu-id="8ab7f-147">Depois de verificar todas as frequências, chame o método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para gravar os valores atualizados no registro.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-147">After scanning all of the frequencies, call the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method to write the updated values into the registry.</span></span> <span data-ttu-id="8ab7f-148">Os valores atualizados são armazenados na entrada do registro para o espaço de ajuste atual.</span><span class="sxs-lookup"><span data-stu-id="8ab7f-148">The updated values are stored under the registry entry for the current tuning space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ab7f-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ab7f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab7f-150">Televisão analógica</span><span class="sxs-lookup"><span data-stu-id="8ab7f-150">Analog Television</span></span>](analog-television.md)
</dt> </dl>

 

 



