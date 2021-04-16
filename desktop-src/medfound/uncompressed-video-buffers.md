---
description: Buffers de vídeo descompactados
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Buffers de vídeo descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772898"
---
# <a name="uncompressed-video-buffers"></a>Buffers de vídeo descompactados

Este artigo descreve como trabalhar com buffers de mídia que contêm quadros de vídeo descompactados. Em ordem de preferência, as opções a seguir estão disponíveis. Nem todo buffer de mídia dá suporte a cada opção.

1.  Use a superfície do Direct3D subjacente. (Aplica-se somente a quadros de vídeo armazenados em superfícies do Direct3D.)
2.  Use a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
3.  Use a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .

## <a name="use-the-underlying-direct3d-surface"></a>Usar a superfície do Direct3D subjacente

O quadro de vídeo pode ser armazenado dentro de uma superfície do Direct3D. Nesse caso, você pode obter um ponteiro para a superfície chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ou [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) no objeto de buffer de mídia. Use o serviço de buffer do identificador de serviço MR \_ \_ . Essa abordagem é recomendada quando o componente que acessa o quadro de vídeo é projetado para usar o Direct3D. Por exemplo, um decodificador de vídeo que dá suporte à aceleração de vídeo do DirectX deve usar essa abordagem.

O código a seguir mostra como obter o ponteiro **IDirect3DSurface9** de um buffer de mídia.


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



Os seguintes objetos oferecem suporte ao serviço de **\_ \_ buffer do Mr** :

-   [Buffer de superfície DirectX](directx-surface-buffer.md)
-   [Exemplos de vídeo](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a>Usar a interface IMF2DBuffer

Se o quadro de vídeo não estiver armazenado dentro de uma superfície do Direct3D ou se o componente não for projetado para usar o Direct3D, a próxima maneira recomendada para acessar o quadro de vídeo é consultar o buffer para a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Essa interface é projetada especificamente para dados de imagem. Para obter um ponteiro para essa interface, chame **QueryInterface** no buffer de mídia. Nem todos os objetos de buffer de mídia expõem essa interface. Mas se um buffer de mídia expor a interface **IMF2DBuffer** , você deverá usar essa interface para acessar os dados, se possível, em vez de usar [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer). Você ainda pode usar a interface **IMFMediaBuffer** , mas pode ser menos eficiente.

1.  Chame **QueryInterface** no buffer de mídia para obter a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
2.  Chame [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para acessar a memória do buffer. Esse método retorna um ponteiro para o primeiro byte da linha superior de pixels. Ele também retorna o stride da imagem, que é o número de bytes desde o início de uma linha de pixels até o início da próxima linha. O buffer pode conter bytes de preenchimento após cada linha de pixels, portanto, o stride pode ser mais largo do que a largura da imagem em bytes. O stride também pode ser negativo se a imagem for orientada de baixo para cima na memória. Para obter mais informações, consulte [Stride de imagem](image-stride.md).
3.  Mantenha o buffer bloqueado somente enquanto você precisa acessar a memória. Desbloqueie o buffer chamando [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).

Nem todo buffer de mídia implementa a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Se o buffer de mídia não implementar essa interface (ou seja, o objeto de buffer retornará E \_ nointerface na etapa 1), você deverá usar a interface de interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , descrita a seguir.

## <a name="use-the-imfmediabuffer-interface"></a>Usar a interface IMFMediaBuffer

Se um buffer de mídia não expor a interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . A semântica geral dessa interface é descrita no tópico [trabalhando com buffers de mídia](working-with-media-buffers.md).

1.  Chame **QueryInterface** no buffer de mídia para obter a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
2.  Chame [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para acessar a memória do buffer. Esse método retorna um ponteiro para a memória do buffer. Quando o método **Lock** é usado, o stride é sempre o stride mínimo para o formato de vídeo em questão, sem nenhum byte de preenchimento extra.
3.  Mantenha o buffer bloqueado somente enquanto você precisa acessar a memória. Desbloqueie o buffer chamando [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

Você sempre deve evitar chamar [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) se o buffer expõe [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), pois o método **Lock** pode forçar o objeto buffer para o quadro de vídeo em um bloco de memória contíguo e, em seguida, voltar novamente. Por outro lado, se o buffer não oferecer suporte a **IMF2DBuffer**, então **IMFMediaBuffer:: Lock** provavelmente não resultará em uma cópia.

Calcule o stride mínimo do tipo de mídia da seguinte maneira:

-   O stride mínimo pode ser armazenado no atributo [**\_ Stride do \_ padrão \_ MF MT**](mf-mt-default-stride-attribute.md) .
-   Se o **atributo \_ \_ \_ Stride do padrão MF MT** não estiver definido, chame a função [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) para calcular o stride para os formatos de vídeo mais comuns.
-   Se a função [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) não reconhecer o formato, você deverá calcular o stride com base na definição do formato. Nesse caso, não há nenhuma regra geral; Você precisa saber os detalhes da definição de formato.

O código a seguir mostra como obter o stride padrão para os formatos de vídeo mais comuns.


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



Dependendo do seu aplicativo, você pode saber com antecedência se um determinado buffer de mídia dá suporte a [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (por exemplo, se você criou o buffer). Caso contrário, você deve estar preparado para usar qualquer uma das duas interfaces de buffer.

O exemplo a seguir mostra uma classe auxiliar que oculta alguns desses detalhes. Essa classe tem um método LockBuffer que chama [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) ou [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) e retorna um ponteiro para o início da primeira linha de pixels. (Esse comportamento corresponde ao método **Lock2D** .) O método LockBuffer usa o stride padrão como um parâmetro de entrada e retorna a Stride real como um parâmetro de saída.


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Stride da imagem](image-stride.md)
</dt> <dt>

[Buffers de mídia](media-buffers.md)
</dt> </dl>

 

 



