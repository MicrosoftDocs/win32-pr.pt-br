---
description: Trabalhando com buffers de mídia
ms.assetid: c7e079e0-99f3-4bff-9163-1c5a022c14ae
title: Trabalhando com buffers de mídia (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63843ded32be6b1baa9c62e21a33f6563a43d5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837652"
---
# <a name="working-with-media-buffers-microsoft-media-foundation"></a>Trabalhando com buffers de mídia (Microsoft Media Foundation)

Este tópico descreve como usar a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) para acessar os dados em um buffer de mídia. Todos os buffers de mídia expõem **IMFMediaBuffer**, que é projetado para qualquer tipo de dados. Quadros de vídeo descompactados são um caso especial, descritos no tópico [buffers de vídeo descompactados](uncompressed-video-buffers.md).

## <a name="buffer-size"></a>Tamanho do Buffer

Um buffer de mídia tem dois tamanhos associados a ele:

-   O *comprimento máximo* é o tamanho físico da memória que é alocada para o buffer. Esse valor é definido quando o buffer é criado e não é alterado durante o tempo de vida do buffer. O comprimento máximo indica a quantidade de dados que pode ser armazenada no buffer. Para localizar o tamanho máximo, chame [**IMFMediaBuffer:: GetMaxLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getmaxlength).

-   O *comprimento atual* é a quantidade de dados válidos que estão atualmente no buffer. Quando o buffer é alocado pela primeira vez, o comprimento atual é zero, porque não há dados válidos no buffer. Se você gravar dados no buffer, deverá atualizar o comprimento atual chamando [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength). Por exemplo, se você gravar 100 bytes de dados no buffer, chame **SetCurrentLength** com o valor 100. Se você ler dados de um buffer de mídia, chame [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) para descobrir a quantidade de dados atualmente no buffer. Não ler após o comprimento atual. O comprimento atual nunca pode exceder o comprimento máximo do buffer.

## <a name="accessing-the-buffer-memory"></a>Acessando a memória de buffer

Para acessar a memória no buffer, chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock). Esse método retorna um ponteiro para o início do bloco de memória. Ele também retorna o comprimento máximo e o comprimento atual. Quando terminar de usar o ponteiro, chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Para gravar dados em um buffer de mídia:

1.  Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para a memória. O método também retorna o comprimento máximo do buffer.
2.  Grave seus dados na memória, até o comprimento máximo do buffer.
3.  Chame [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) para atualizar o comprimento atual. Defina o comprimento atual igual à quantidade de dados que você escreveu na etapa 2.
4.  Chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o buffer.

Para ler dados de um buffer de mídia:

1.  Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para obter um ponteiro para a memória. O método também retorna o comprimento atual do buffer (a quantidade de dados válidos no buffer).
2.  Ler o conteúdo da memória, até o comprimento atual.
3.  Chame [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear o buffer.

## <a name="creating-system-memory-buffers"></a>Criando buffers de memória do sistema

O buffer de memória do sistema é um buffer de mídia que gerencia um bloco de memória do sistema. Para criar uma instância desse objeto, chame [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) ou [**MFCreateAlignedMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatealignedmemorybuffer) e especifique um tamanho de buffer. Ambas as funções alocam um bloco de memória e retornam um ponteiro [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . A memória é liberada automaticamente quando a contagem de referência do buffer de mídia atinge zero e o objeto é destruído.

O exemplo a seguir mostra como criar um buffer de memória do sistema e gravar no buffer.


```C++
HRESULT CreateSystemMemoryBuffer(
    BYTE *pSrc, 
    DWORD cbData, 
    IMFMediaBuffer **ppBuffer
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer.
    hr = MFCreateMemoryBuffer(
        cbData,   // Amount of memory to allocate, in bytes.
        &pBuffer        
        );

    // Lock the buffer to get a pointer to the memory.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    if (SUCCEEDED(hr))
    {
        memcpy_s(pData, cbData, pSrc, cbData);
    }

    // Update the current length.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbData);
    }

    // Unlock the buffer.
    if (pData)
    {
        hr = pBuffer->Unlock();
    }

    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de mídia](media-buffers.md)
</dt> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



