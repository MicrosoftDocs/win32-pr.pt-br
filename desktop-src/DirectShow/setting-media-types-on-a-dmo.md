---
description: Definindo tipos de mídia em um DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Definindo tipos de mídia em um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fd437ae54d2e5baec35eb415dd8d04e4d3a3fe5992b8ba73f6d25c77f0475a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904246"
---
# <a name="setting-media-types-on-a-dmo"></a>Definindo tipos de mídia em um DMO

Antes que um DMO possa processar dados, o cliente deve definir o tipo de mídia para cada fluxo. (Há uma exceção secundária a essa regra; consulte [Opcional Fluxos](optional-streams.md).) Para encontrar o número de fluxos, chame o [**método IMediaObject::GetStreamCount:**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount)


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Esse método retorna dois valores, o número de entradas e o número de saídas. Esses valores são fixos durante o tempo de vida do DMO.

**Tipos preferenciais**

Para cada fluxo, o DMO atribui uma lista de possíveis tipos de mídia, em ordem de preferência. Por exemplo, os tipos preferenciais podem ser RGB de 32 RGB, RGB de 24 bits e RGB de 16 bits, nessa ordem. Quando o cliente define os tipos de mídia, ele pode usar essas listas como uma dica. Para recuperar um tipo preferencial para um fluxo, chame o método [**IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) ou o método [**IMediaObject::GetOutputType.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) Especifique o número de fluxo e um valor de índice para o tipo (começando do zero). Por exemplo, o código a seguir recupera o primeiro tipo preferencial do primeiro fluxo de entrada:


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



Para enumerar todos os tipos de mídia preferenciais em um determinado fluxo, use um loop que incrementa o índice de tipo até que o método retorne DMO E NO MORE ITEMS, conforme mostrado no exemplo a \_ \_ \_ \_ seguir:


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



Você deve observar os seguintes pontos sobre tipos preferenciais:

-   O DMO pode retornar um tipo que não tem nenhum bloco de formato. Por exemplo, um DMO pode especificar um tipo de vídeo, como RGB de 24 bits, sem fornecer a largura e a altura da imagem. No entanto, ao definir o tipo, você deve fornecer um bloco de formato completo. (Alguns tipos de mídia, como MIDI, nunca exigem um bloco de formato; nesse caso, esse comentário não se aplica.)
-   O DMO é necessário para dar suporte a cada combinação de tipos preferenciais que ele retorna. Por exemplo, se um DMO tiver dois fluxos e cada fluxo tiver quatro tipos preferenciais, haverá 16 combinações possíveis, mas nem todos eles serão válidos.
-   Quando o cliente define o tipo de mídia para um fluxo, o DMO pode atualizar os tipos preferenciais de outros fluxos para refletir o novo estado. No entanto, não é necessário fazer isso.
-   Para alguns fluxos, o DMO pode não oferecer nenhum tipo preferencial. Normalmente, um DMO deve oferecer pelo menos alguns tipos preferenciais em alguns fluxos.
-   O DMO é necessário para oferecer uma lista completa dos tipos de mídia que ele pode aceitar. Pode haver tipos "não revertidos" aos quais o DMO dá suporte, mas não oferece como tipos preferenciais.

Em resumo, o cliente deve tratar os tipos preferenciais apenas como diretrizes. A única maneira de saber com certeza quais tipos têm suporte é testá-los, conforme descrito na próxima seção.

**Definindo o tipo de mídia em um fluxo**

Use os [**métodos IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) para definir o tipo para cada fluxo. Você deve fornecer uma **estrutura DMO \_ MEDIA \_ TYPE** que contenha uma descrição completa do tipo de mídia. O exemplo a seguir define o tipo de mídia no fluxo de entrada 0, usando áudio PCM estéreo de 16 bits de 44,1 kHz:


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



Para testar um tipo de mídia sem defini-lo, chame **SetInputType** ou **SetOutputType** com o sinalizador \_ DMO SET \_ TYPEF TEST \_ \_ ONLY. O método retornará S \_ OK se o tipo for aceitável ou S FALSE caso \_ contrário:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Como as configurações em um fluxo podem afetar outro fluxo, talvez seja necessário limpar o tipo de mídia de um fluxo. Para fazer isso, chame **SetInputType ou** **SetOutputType** com o DMO \_ SET \_ TYPEF \_ CLEAR.

Para um decodificador DMO, o cliente normalmente definiria o tipo de entrada primeiro e, em seguida, escolheria um tipo de saída. Para um DMO codificador, o cliente definiria o tipo de saída primeiro e, em seguida, o tipo de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



