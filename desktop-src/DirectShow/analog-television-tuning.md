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
# <a name="analog-television-tuning"></a>Ajuste de televisão analógica

O ajuste é controlado pelo filtro de sintonizador de TV, por meio da interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . A interface IAMTVTuner herda IAMTuner. Para obter um ponteiro para a interface, chame o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) da seguinte maneira:


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



O primeiro parâmetro indica a pesquisa de upstream a partir do filtro de captura.

Tabelas de frequência

Internamente, o filtro de sintonizador de TV mantém uma lista de tabelas de frequência. Cada tabela de frequência corresponde à frequência de transmissão ou de cabo para um determinado país/região. Também há uma tabela de frequência "unicable" genérica, que é usada quando um país/região não tem um conjunto padrão de atribuições de frequência.

Cada tabela Frequency contém uma lista de frequências de ajuste. Para alguns países/regiões, os índices na tabela correspondem diretamente aos números de canal – em outras palavras, a frequência do canal n é a entrada n-th na tabela. No entanto, para alguns países/regiões, não há nenhuma correspondência direta entre números de canal e frequências. Nesse caso, o aplicativo deve manter uma lista que mapeia os números de canal (normalmente escolhidos pelo usuário) para as entradas da tabela de frequência. Por exemplo, o que o usuário vê como "canal 5" pode ser a entrada número 12 na tabela de frequência.

Para obter detalhes, consulte [ajuste de TV analógica internacional](international-analog-tv-tuning.md).

Operações básicas de ajuste

Se o sintonizador der suporte a vários modos de recepção, como televisão e FM Radio, chame [**IAMTuner::p \_ modo UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) para selecionar o modo. O método [**IAMTuner:: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) retorna todos os modos aos quais o sintonizador dá suporte. Por exemplo, o código a seguir verifica se o sintonizador dá suporte a rádio FM e, em caso afirmativo, alterna para esse modo.


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



Para definir o país/região, chame o método [**IAMTuner::p UT \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) . O sintonizador usa esse valor para selecionar a tabela de frequência apropriada. Confira [atribuições de país/região](country-region-assignments.md) para obter mais informações.

Para definir o canal, chame o método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) . O argumento para esse método não é, na verdade, um número de canal, mas sim um índice na tabela de frequência atual. Conforme descrito anteriormente, o número de índice pode ou não corresponder a um número de canal. O método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) retorna os valores de índice mínimo e máximo para a tabela de frequência atual.

Substituindo entradas de frequência

É possível que algumas entradas nas tabelas Frequency estejam incorretas ou se tornem obsoletas. Portanto, um mecanismo é fornecido para substituir entradas individuais usando chaves do registro.

As especificações são explicadas no tópico [ajuste de TV analógica internacional](international-analog-tv-tuning.md). Cada chave do registro define um "espaço de ajuste" que contém uma ou mais subchaves. Cada subchave substitui uma entrada de frequência. Para definir o espaço de ajuste atual, use o método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) . Ativar o espaço de ajuste substitui as entradas de frequência na tabela de frequência atual. Portanto, cabe ao aplicativo manter uma correspondência entre espaços de ajuste e países/regiões. A melhor abordagem é simplesmente usar o identificador de país/região como o nome do espaço de sintonia.

Ajuste fino das entradas de frequência

As frequências de difusão podem ser ajustadas ou reduzidas a vários kHz pela estação de difusão para reduzir a possibilidade de interferência com canais vizinhos. Dada a frequência nominal, o cartão sintonizador pode verificar a frequência exata. O filtro de sintonizador de TV tem um mecanismo para salvar as frequências ajustadas no registro.

Para cada entrada na tabela Frequency, chame o método Put \_ Channel para ajustar a essa frequência. O sintonizador examinará a frequência mais precisa. Você pode verificar se o sintonizador obteve um bloqueio horizontal chamando [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent). O filtro de sintonizador de TV também armazena o resultado internamente.

Depois de verificar todas as frequências, chame o método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para gravar os valores atualizados no registro. Os valores atualizados são armazenados na entrada do registro para o espaço de ajuste atual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Televisão analógica](analog-television.md)
</dt> </dl>

 

 



