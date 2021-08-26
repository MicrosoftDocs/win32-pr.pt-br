---
description: Etapa 3 Implementar a função Frame-Grabbing função
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Etapa 3 Implementar a função Frame-Grabbing função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75410c48765e9437cd328a220ccbecf2c207bdaae5242a9e41060bc13fa02eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904087"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Etapa 3: Implementar a função Frame-Grabbing função

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Este tópico é a Etapa 3 de [Como segurar um quadro de cartaz.](grabbing-a-poster-frame.md)

A próxima etapa é implementar a função GetBitmap, que usa o Detector de Mídia para obter um quadro de cartaz. Dentro dessa função, execute as seguintes etapas:

1.  Crie o Detector de Mídia.
2.  Especifique um arquivo de mídia.
3.  Examine cada fluxo no arquivo. Se for um fluxo de vídeo, obter as dimensões nativas do vídeo.
4.  Obtenha um quadro de cartaz, especificando a hora da busca e a dimensão de destino.

Crie o objeto Detector de Mídia chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Especifique um nome de arquivo usando [**o método \_ Filename IMediaDet::p ut.**](imediadet-put-filename.md) Esse método aceita um **parâmetro BSTR.**


```C++
hr = pDet->put_Filename(bstrFilename);
```



Obter o número de fluxos e fazer um loop em cada fluxo verificando o tipo de mídia. O [**método IMediaDet::get \_ OutputStreams**](imediadet-get-outputstreams.md) recupera o número de fluxos e o método [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md) especifica qual fluxo examinar. Saia do loop no primeiro fluxo de vídeo.


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



Se nenhum fluxo de vídeo tiver sido encontrado, a função será saída.

No código anterior, o [**método IMediaDet::get \_ StreamType**](imediadet-get-streamtype.md) retorna apenas o GUID do tipo principal. Isso será conveniente se você não precisar examinar o tipo de mídia completo. No entanto, para obter as dimensões de vídeo, é necessário examinar o bloco de formato, portanto, o tipo de mídia completo é necessário. Você pode recuperá-lo chamando o [**método IMediaDet::get \_ StreamMediaType,**](imediadet-get-streammediatype.md) que preenche uma estrutura [**AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) O Detector de Mídia converte todos os fluxos de vídeo em formato descompactado, com um [**bloco de formato VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)


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



O [**método \_ get StreamMediaType**](imediadet-get-streammediatype.md) aloca o bloco de formato, que o chamador deve liberar. Este exemplo usa a [**função FreeMediaType**](freemediatype.md) da biblioteca de classes base.

Agora você está pronto para obter o quadro de cartaz. Primeiro, chame [**o método IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) com um **ponteiro NULL** para o buffer:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Essa chamada retorna o tamanho do buffer necessário no *parâmetro lSize.* O primeiro parâmetro especifica o tempo de fluxo a ser buscado; este exemplo usa a hora zero. Para a largura e a altura, este exemplo usa as dimensões de vídeo nativas obtidas anteriormente. Se você especificar outros valores, o Detector de Mídia ampliará o bitmap para corresponder.

Se o método for bem-sucedido, aloce o buffer e [**chame GetBitmapBits**](imediadet-getbitmapbits.md) novamente:


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



Aqui está a função completa, com um tratamento de erro um pouco melhor.


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



Próximo: [Etapa 4: Desenhar o bitmap na área do cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pegar um quadro de cartaz](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
