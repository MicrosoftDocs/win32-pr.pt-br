---
description: Coletando informações de Fine-Tuning
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Coletando informações de Fine-Tuning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105787398"
---
# <a name="collecting-fine-tuning-information"></a><span data-ttu-id="010cc-103">Coletando informações de Fine-Tuning</span><span class="sxs-lookup"><span data-stu-id="010cc-103">Collecting Fine-Tuning Information</span></span>

<span data-ttu-id="010cc-104">Embora as frequências de cabos geralmente sejam exatas, as frequências de difusão podem ser ajustadas ou reduzidas em vários kHz pela estação de difusão para reduzir a interferência potencial com canais vizinhos.</span><span class="sxs-lookup"><span data-stu-id="010cc-104">Although cable frequencies are generally expected to be exact, broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span>

<span data-ttu-id="010cc-105">Quando o filtro de sintonizador de TV se ajusta a um canal, ele examina o sinal mais preciso.</span><span class="sxs-lookup"><span data-stu-id="010cc-105">When the TV Tuner filter tunes to a channel, it scans for the most precise signal.</span></span> <span data-ttu-id="010cc-106">Para salvar essas informações no registro para operações de ajuste posteriores, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="010cc-106">To save this information in the registry for subsequent tuning operations, do the following:</span></span>

1.  <span data-ttu-id="010cc-107">Chame [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) para determinar o intervalo de entradas de frequência na tabela de frequência atual.</span><span class="sxs-lookup"><span data-stu-id="010cc-107">Call [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) to determine the range of frequency entries in the current frequency table.</span></span>
2.  <span data-ttu-id="010cc-108">Chame o método [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) uma vez para cada índice de frequência no intervalo.</span><span class="sxs-lookup"><span data-stu-id="010cc-108">Call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method once for each frequency index in the range.</span></span>
3.  <span data-ttu-id="010cc-109">Chame [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para salvar as informações de ajuste fino no registro.</span><span class="sxs-lookup"><span data-stu-id="010cc-109">Call [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) to save the fine-tuning information in the registry.</span></span> <span data-ttu-id="010cc-110">As informações são armazenadas na chave do registro para o espaço de ajuste atual.</span><span class="sxs-lookup"><span data-stu-id="010cc-110">The information is stored under the registry key for the current tuning space.</span></span>

<span data-ttu-id="010cc-111">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="010cc-111">The following code shows these steps:</span></span>


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



<span data-ttu-id="010cc-112">Com versões anteriores do filtro de sintonizador de TV, o método [**IAMTVTuner:: AutoAjuste**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) era recomendado para ajuste fino.</span><span class="sxs-lookup"><span data-stu-id="010cc-112">With earlier versions of the TV Tuner filter, the [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method was recommended for fine-tuning.</span></span> <span data-ttu-id="010cc-113">No entanto, esse método ignora qualquer substituição de frequência, portanto, seu uso não é mais recomendado.</span><span class="sxs-lookup"><span data-stu-id="010cc-113">However, this method ignores any frequency overrides, so its use is no longer recommended.</span></span> <span data-ttu-id="010cc-114">O código a seguir é equivalente ao método **AutoAjuste** , mas funciona corretamente com substituições de frequência:</span><span class="sxs-lookup"><span data-stu-id="010cc-114">The following code is equivalent to the **AutoTune** method, but works correctly with frequency overrides:</span></span>


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



<span data-ttu-id="010cc-115">Com a recepção de difusão, nem sempre é possível obter um bloqueio horizontal, embora a imagem esteja visível.</span><span class="sxs-lookup"><span data-stu-id="010cc-115">With broadcast reception, it is not always possible to get a horizontal lock, although the picture is viewable.</span></span> <span data-ttu-id="010cc-116">Nesses casos, o hardware do sintonizador terá um bloqueio de frequência, mas o decodificador não terá o bloqueio horizontal.</span><span class="sxs-lookup"><span data-stu-id="010cc-116">In these cases, the tuner hardware will have a frequency lock, but the decoder will not have horizontal lock.</span></span> <span data-ttu-id="010cc-117">Essa condição pode ser detectada ao usar [**Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) ou [**AutoAjuste**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) examinando o código de retorno.</span><span class="sxs-lookup"><span data-stu-id="010cc-117">This condition can be detected when using [**put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) or [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) by examining the return code.</span></span>



| <span data-ttu-id="010cc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="010cc-118">Value</span></span>    | <span data-ttu-id="010cc-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="010cc-119">Description</span></span>                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010cc-120">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="010cc-120">S\_OK</span></span>    | <span data-ttu-id="010cc-121">A operação de ajuste foi bem-sucedida e o sintonizador obteve um bloqueio de frequência.</span><span class="sxs-lookup"><span data-stu-id="010cc-121">The tune operation succeeded and the tuner got a frequency lock.</span></span>                                                                                                                          |
| <span data-ttu-id="010cc-122">\_falso</span><span class="sxs-lookup"><span data-stu-id="010cc-122">S\_FALSE</span></span> | <span data-ttu-id="010cc-123">Não houve erros durante a operação de ajuste, mas o sintonizador não conseguiu obter um bloqueio de frequência.</span><span class="sxs-lookup"><span data-stu-id="010cc-123">There were no errors during the tune operation, but the tuner was not able to get a frequency lock.</span></span> <span data-ttu-id="010cc-124">É muito improvável que haja um canal visível resultante dessa operação.</span><span class="sxs-lookup"><span data-stu-id="010cc-124">It is highly unlikely that there is a viewable channel resulting from this operation.</span></span> |



 

<span data-ttu-id="010cc-125">Qualquer outro código de retorno indica que ocorreu algum erro.</span><span class="sxs-lookup"><span data-stu-id="010cc-125">Any other return code indicates that some error occurred.</span></span>

<span data-ttu-id="010cc-126">Um valor de retorno de S \_ OK não garante que o decodificador tenha um bloqueio horizontal.</span><span class="sxs-lookup"><span data-stu-id="010cc-126">A return value of S\_OK does not guarantee that the decoder has a horizontal lock.</span></span> <span data-ttu-id="010cc-127">O método [**AutoAjuste**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) atualiza o parâmetro *FoundSignal* para indicar se o bloqueio horizontal foi atingido ou não.</span><span class="sxs-lookup"><span data-stu-id="010cc-127">The [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method updates the *FoundSignal* parameter to indicate whether or not horizontal lock was achieved.</span></span> <span data-ttu-id="010cc-128">O método [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) retorna as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="010cc-128">The [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) method returns the same information.</span></span>

<span data-ttu-id="010cc-129">No entanto, quando o valor de retorno é S \_ OK, o aplicativo tem a opção de ignorar o parâmetro *FoundSignal* , pois o sintonizador está relatando um bloqueio de frequência.</span><span class="sxs-lookup"><span data-stu-id="010cc-129">When the return value is S\_OK, however, the application has the option of ignoring the *FoundSignal* parameter, because the tuner is reporting a frequency lock.</span></span> <span data-ttu-id="010cc-130">Há a possibilidade de um bloqueio de frequência em ruído, mas essa possibilidade deve ser avaliada em relação à possibilidade de ignorar canais visíveis.</span><span class="sxs-lookup"><span data-stu-id="010cc-130">There is the possibility of a frequency lock on noise, but this possibility should be weighed against the possibility of skipping viewable channels.</span></span>

## <a name="registry-conversion"></a><span data-ttu-id="010cc-131">Conversão de registro</span><span class="sxs-lookup"><span data-stu-id="010cc-131">Registry Conversion</span></span>

<span data-ttu-id="010cc-132">Para dar suporte a substituições de frequência, o formato interno da chave do registro que contém informações de ajuste fino foi alterado.</span><span class="sxs-lookup"><span data-stu-id="010cc-132">To support frequency overrides, the internal format of the registry key that holds fine-tuning information has changed.</span></span> <span data-ttu-id="010cc-133">O formato original ainda tem suporte para compatibilidade com versões anteriores, mas não oferece suporte a substituições de frequência.</span><span class="sxs-lookup"><span data-stu-id="010cc-133">The original format is still supported for backward compatibility, but it does not support frequency overrides.</span></span>

<span data-ttu-id="010cc-134">O formato antigo do registro é convertido para o novo formato sempre que o método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) é chamado.</span><span class="sxs-lookup"><span data-stu-id="010cc-134">The old registry format is converted to the new format whenever the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method is called.</span></span> <span data-ttu-id="010cc-135">Se seu aplicativo adicionar substituições de frequência, ele deve chamar o método **StoreAutoTune** para converter para o novo formato de registro.</span><span class="sxs-lookup"><span data-stu-id="010cc-135">If your application adds frequency overrides, it should call the **StoreAutoTune** method to convert to the new registry format.</span></span> <span data-ttu-id="010cc-136">Não é necessário coletar informações de ajuste fino antes de chamar **StoreAutoTune**.</span><span class="sxs-lookup"><span data-stu-id="010cc-136">It is not necessary to collect any fine-tuning information before calling **StoreAutoTune**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="010cc-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="010cc-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="010cc-138">Ajuste de TV analógica internacional</span><span class="sxs-lookup"><span data-stu-id="010cc-138">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



