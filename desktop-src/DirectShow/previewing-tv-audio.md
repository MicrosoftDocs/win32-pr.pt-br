---
description: Visualizando áudio de TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Visualizando áudio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6b67e33ffd6f051363e8851afbc31b9f38bed17790687db615b679f6a80a63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748306"
---
# <a name="previewing-tv-audio"></a>Visualizando áudio de TV

Para visualizar o áudio de TV, direcione o PIN do decodificador de áudio no filtro Crossbar para o pino do sintonizador de áudio. Para ativar mudo do áudio, encaminhe o PIN do decodificador de áudio para-1, conforme mostrado no diagrama a seguir. (Os filtros Crossbar são descritos em [trabalhando com Crossbars](working-with-crossbars.md).)

![Roteando o PIN do decodificador de áudio](images/vidcap07.png)

A abordagem básica é a seguinte:

1.  Use o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para localizar o filtro Crossbar.
2.  Use o método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) para enumerar os Pins de entrada e saída do filtro Crossbar. Procure um PIN de saída de decodificador de áudio e um pino de entrada do sintonizador de áudio.
3.  Se você encontrar os Pins corretos, chame [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) para rotear os Pins. Caso contrário, observe upstream para outro Crossbar e repita o processo.
4.  Para ativar mudo do áudio, encaminhe o PIN do decodificador de áudio para-1.

A maioria dos sintonizadores de TV usa um único filtro crossbar, mas alguns usam dois filtros Crossbar. Portanto, talvez seja necessário pesquisar por um segundo Crossbar se o primeiro falhar.

> [!Note]  
> Ao contrário do que você pode esperar, nenhum filtro de captura de áudio ou processador de áudio é necessário para visualizar o áudio, porque há uma conexão física entre a placa de sintonizador e a placa de som.

 

O código a seguir mostra essas etapas mais detalhadamente. Primeiro, aqui está uma função auxiliar que pesquisa um filtro Crossbar para um tipo de PIN especificado:


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



A próxima função tenta ativar ou desativar o áudio, dependendo do valor do parâmetro *bActivate* . Ele pesquisa o filtro Crossbar especificado para os Pins necessários. Se ele não conseguir encontrá-los, ele retornará um código de erro.


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



A próxima função pesquisa o grafo de filtro em busca de um filtro Crossbar. Se encontrar uma, ele tentará ativar ou desativar o áudio (usando a função anterior). Se essa operação falhar, o método pesquisará upstream para um segundo Crossbar e tentará novamente. Para obter uma abordagem mais generalizada para gerenciar vários filtros Crossbar em um grafo, consulte a classe CCrossbar no aplicativo de exemplo AmCap.


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



O código a seguir mostra como chamar essas funções:


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Observe que essas funções de exemplo repetem muitas das mesmas chamadas de função. Por exemplo, eles enumeram os Pins Crossbar a cada vez. Em um aplicativo real, você pode armazenar em cache algumas dessas informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Áudio de televisão analógica](analog-television-audio.md)
</dt> <dt>

[Trabalhando com Crossbars](working-with-crossbars.md)
</dt> </dl>

 

 



