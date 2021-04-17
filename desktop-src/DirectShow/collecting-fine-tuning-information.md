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
# <a name="collecting-fine-tuning-information"></a>Coletando informações de Fine-Tuning

Embora as frequências de cabos geralmente sejam exatas, as frequências de difusão podem ser ajustadas ou reduzidas em vários kHz pela estação de difusão para reduzir a interferência potencial com canais vizinhos.

Quando o filtro de sintonizador de TV se ajusta a um canal, ele examina o sinal mais preciso. Para salvar essas informações no registro para operações de ajuste posteriores, faça o seguinte:

1.  Chame [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) para determinar o intervalo de entradas de frequência na tabela de frequência atual.
2.  Chame o método [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) uma vez para cada índice de frequência no intervalo.
3.  Chame [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para salvar as informações de ajuste fino no registro. As informações são armazenadas na chave do registro para o espaço de ajuste atual.

O código a seguir mostra estas etapas:


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



Com versões anteriores do filtro de sintonizador de TV, o método [**IAMTVTuner:: AutoAjuste**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) era recomendado para ajuste fino. No entanto, esse método ignora qualquer substituição de frequência, portanto, seu uso não é mais recomendado. O código a seguir é equivalente ao método **AutoAjuste** , mas funciona corretamente com substituições de frequência:


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



Com a recepção de difusão, nem sempre é possível obter um bloqueio horizontal, embora a imagem esteja visível. Nesses casos, o hardware do sintonizador terá um bloqueio de frequência, mas o decodificador não terá o bloqueio horizontal. Essa condição pode ser detectada ao usar [**Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) ou [**AutoAjuste**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) examinando o código de retorno.



| Valor    | Descrição                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK    | A operação de ajuste foi bem-sucedida e o sintonizador obteve um bloqueio de frequência.                                                                                                                          |
| \_falso | Não houve erros durante a operação de ajuste, mas o sintonizador não conseguiu obter um bloqueio de frequência. É muito improvável que haja um canal visível resultante dessa operação. |



 

Qualquer outro código de retorno indica que ocorreu algum erro.

Um valor de retorno de S \_ OK não garante que o decodificador tenha um bloqueio horizontal. O método [**AutoAjuste**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) atualiza o parâmetro *FoundSignal* para indicar se o bloqueio horizontal foi atingido ou não. O método [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) retorna as mesmas informações.

No entanto, quando o valor de retorno é S \_ OK, o aplicativo tem a opção de ignorar o parâmetro *FoundSignal* , pois o sintonizador está relatando um bloqueio de frequência. Há a possibilidade de um bloqueio de frequência em ruído, mas essa possibilidade deve ser avaliada em relação à possibilidade de ignorar canais visíveis.

## <a name="registry-conversion"></a>Conversão de registro

Para dar suporte a substituições de frequência, o formato interno da chave do registro que contém informações de ajuste fino foi alterado. O formato original ainda tem suporte para compatibilidade com versões anteriores, mas não oferece suporte a substituições de frequência.

O formato antigo do registro é convertido para o novo formato sempre que o método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) é chamado. Se seu aplicativo adicionar substituições de frequência, ele deve chamar o método **StoreAutoTune** para converter para o novo formato de registro. Não é necessário coletar informações de ajuste fino antes de chamar **StoreAutoTune**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ajuste de TV analógica internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



