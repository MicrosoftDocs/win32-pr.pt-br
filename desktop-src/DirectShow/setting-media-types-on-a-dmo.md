---
description: Definindo tipos de mídia em um DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Definindo tipos de mídia em um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782835"
---
# <a name="setting-media-types-on-a-dmo"></a>Definindo tipos de mídia em um DMO

Antes que um DMO possa processar quaisquer dados, o cliente deve definir o tipo de mídia para cada fluxo. (Há uma exceção secundária para essa regra; consulte [fluxos opcionais](optional-streams.md).) Para localizar o número de fluxos, chame o método [**IMediaObject:: GetStreamCount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) :


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Esse método retorna dois valores, o número de entradas e o número de saídas. Esses valores são fixos para o tempo de vida do DMO.

**Tipos preferenciais**

Para cada fluxo, o DMO atribui uma lista de tipos de mídia possíveis, em ordem de preferência. Por exemplo, os tipos preferenciais podem ser 32-RGB, RGB de 24 bits e RGB de 16 bits, nessa ordem. Quando o cliente define os tipos de mídia, ele pode usar essas listas como uma dica. Para recuperar um tipo preferencial para um fluxo, chame o método [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) ou [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) . Especifique o número do fluxo e um valor de índice para o tipo (começando de zero). Por exemplo, o código a seguir recupera o primeiro tipo preferencial do primeiro fluxo de entrada:


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



Para enumerar todos os tipos de mídia preferenciais em um determinado fluxo, use um loop que incrementa o índice de tipo até que o método retorne DMO \_ E \_ não \_ mais \_ itens, conforme mostrado no exemplo a seguir:


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



Você deve observar os seguintes pontos sobre os tipos preferenciais:

-   O DMO pode retornar um tipo que não tem nenhum bloco de formato. Por exemplo, um DMO poderia especificar um tipo de vídeo, como RGB de 24 bits, sem fornecer a largura e a altura da imagem. No entanto, quando você define o tipo, deve fornecer um bloco de formato completo. (Alguns tipos de mídia, como MIDI, nunca exigem um bloco de formato; nesse caso, esse comentário não se aplica.)
-   O DMO não é necessário para dar suporte a cada combinação de tipos preferenciais que ele retorna. Por exemplo, se um DMO tiver dois fluxos, e cada fluxo tiver quatro tipos preferenciais, haverá 16 combinações possíveis, mas nem todos eles terão a garantia de serem válidos.
-   Quando o cliente define o tipo de mídia para um fluxo, o DMO pode atualizar os tipos preferenciais para outros fluxos para refletir o novo estado. No entanto, não é necessário fazer isso.
-   Para alguns fluxos, o DMO pode não oferecer nenhum tipo preferencial. Normalmente, um DMO deve oferecer pelo menos alguns tipos preferenciais em alguns fluxos.
-   O DMO não precisa oferecer uma lista completa dos tipos de mídia que ele pode aceitar. Pode haver tipos "não anunciados" que o DMO dá suporte, mas não oferece como tipos preferenciais.

Em suma, o cliente deve tratar os tipos preferenciais como somente diretrizes. A única maneira de saber quais tipos têm suporte é testá-los, conforme descrito na próxima seção.

**Configurando o tipo de mídia em um fluxo**

Use os métodos [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) para definir o tipo para cada fluxo. Você deve fornecer uma estrutura de **\_ \_ tipo de mídia DMO** que contém uma descrição completa do tipo de mídia. O exemplo a seguir define o tipo de mídia no fluxo de entrada 0, usando áudio PCM estéreo de 16 bits de 44,1-kHz:


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



Para testar um tipo de mídia sem defini-lo, chame **SetInputType** ou **setoutputtypetype** com o \_ sinalizador do set \_ TYPEF \_ test \_ only. O método retornará S \_ OK se o tipo for aceitável ou, \_ caso contrário, s false:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Como as configurações em um fluxo podem afetar outro fluxo, talvez seja necessário limpar o tipo de mídia de um fluxo. Para fazer isso, chame **SetInputType** ou **setoutputtypetype** com o \_ sinalizador Set \_ TYPEF \_ Clear do DMO.

Para um decodificador DMO, o cliente normalmente definiria o tipo de entrada primeiro e, em seguida, escolheria um tipo de saída. Para um codificador DMO, o cliente definiria o tipo de saída primeiro e, em seguida, o tipo de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



