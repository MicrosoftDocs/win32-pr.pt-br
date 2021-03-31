---
description: Etapa 3 implementar a função Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Etapa 3 implementar a função Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829374"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Etapa 3: implementar a função Frame-Grabbing

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Este tópico é a etapa 3 de [captar um quadro de cartaz](grabbing-a-poster-frame.md).

A próxima etapa é implementar a função getbitmap, que usa o detector de mídia para pegar um quadro de pôster. Dentro dessa função, execute as seguintes etapas:

1.  Crie o detector de mídia.
2.  Especifique um arquivo de mídia.
3.  Examine cada fluxo no arquivo. Se for um fluxo de vídeo, obtenha as dimensões nativas do vídeo.
4.  Obtenha um quadro de cartaz, especificando o tempo de busca e a dimensão de destino.

Crie o objeto do detector de mídia chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Especifique um nome de arquivo, usando o método [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) . Esse método usa um parâmetro **BSTR** .


```C++
hr = pDet->put_Filename(bstrFilename);
```



Obtenha o número de fluxos e execute um loop em cada fluxo verificando o tipo de mídia. O método [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) recupera o número de fluxos e o método [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) especifica qual fluxo examinar. Saia do loop no primeiro fluxo de vídeo.


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



Se nenhum fluxo de vídeo for encontrado, a função será encerrada.

No código anterior, o método [**\_ streamtype IMediaDet:: Get**](imediadet-get-streamtype.md) retorna apenas o GUID de tipo principal. Isso é conveniente se você não precisar examinar o tipo de mídia completo. No entanto, para obter as dimensões de vídeo, é necessário examinar o bloco de formato para que o tipo de mídia completo seja necessário. Você pode recuperar isso chamando o método [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md) , que preenche uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . O detector de mídia converte todos os fluxos de vídeo em formato descompactado, com um bloco de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



O método [**Get \_ StreamMediaType**](imediadet-get-streammediatype.md) aloca o bloco de formato, que o chamador deve liberar. Este exemplo usa a função [**FreeMediaType**](freemediatype.md) da biblioteca de classes base.

Agora você está pronto para obter o quadro do pôster. Primeiro, chame o método [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) com um ponteiro **nulo** para o buffer:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Essa chamada retorna o tamanho de buffer necessário no parâmetro *lSize* . O primeiro parâmetro especifica o tempo de transmissão a ser buscado; Este exemplo usa o tempo zero. Para a largura e a altura, este exemplo usa as dimensões de vídeo nativa obtidas anteriormente. Se você especificar outros valores, o detector de mídia irá alongar o bitmap para corresponder.

Se o método for bem sucedido, aloque o buffer e chame [**GetBitmapBits**](imediadet-getbitmapbits.md) novamente:


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



Esta é a função completa, com tratamento de erros um pouco melhor.


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



Em seguida: [etapa 4: desenhar o bitmap na área do cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando um quadro de cartaz](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
