---
description: Definindo propriedades de compactação de vídeo
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Definindo propriedades de compactação de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3f1d73d27acb99e5a197ec4501411669278a6fd5c7b857875141d8831c7173f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583276"
---
# <a name="setting-video-compression-properties"></a>Definindo propriedades de compactação de vídeo

Os filtros de compactação de vídeo podem dar suporte à interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) em seus pinos de saída. Use essa interface para definir propriedades de compactação, como a taxa de quadros-chave, o número de quadros previstos (P) por quadro-chave e a qualidade de compactação relativa.

Primeiro, chame o [**método IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) para encontrar o pino de saída do filtro e consulte o pino para a interface. Alguns filtros podem não dar suporte à interface. Outros podem expor a interface, mas não dar suporte a todas as propriedades de compactação. Para determinar quais propriedades têm suporte, chame [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Esse método retorna várias informações:

-   Um conjunto de sinalizadores de funcionalidades
-   Uma cadeia de caracteres descritiva e uma cadeia de caracteres de número de versão
-   Valores padrão para taxa de quadros-chave, taxa de quadros P e qualidade (quando há suporte)

O método tem a seguinte sintaxe:


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



Os *parâmetros pszVersion* e *pszDesc* são buffers de caractere largo que recebem a cadeia de caracteres de versão e a cadeia de caracteres de descrição. Os *parâmetros cbVersion* e *cbDesc* recebem os tamanhos de buffer necessários em bytes (não caracteres). Os *parâmetros lKeyFrame,* *lPFrame* e *dblQuality* recebem os valores padrão para a taxa de quadros-chave, a taxa de quadros P e a qualidade. A qualidade é expressa como um número de ponto flutuante de 0,0 a 1,0. O *parâmetro lCap* recebe um **OR** bit a bit dos sinalizadores de funcionalidades, que são definidos pelo tipo enumerado [**CompressionCaps.**](/windows/desktop/api/strmif/ne-strmif-compressioncaps)

Qualquer um desses parâmetros pode ser **NULL,** caso em que o método ignora esse parâmetro. Por exemplo, para alocar buffers para as cadeias de caracteres de versão e descrição, primeiro chame o método com **NULL** no primeiro e no terceiro parâmetros. Use os valores retornados para *cbVersion* e *cbDesc* para alocar os buffers e, em seguida, chame o método novamente:


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



O valor *de lCap* indica a quais dos outros **métodos IAMVideoCompression** o filtro dá suporte. Por exemplo, se *lCap* contiver o sinalizador CompressionCaps CanKeyFrame, você poderá chamar \_ [**IAMVideoCompression::get \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) para obter a taxa de quadros-chave e [**IAMVideoCompression::p ut \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) para definir a taxa de quadros-chave. Um valor negativo indica que o filtro usará o valor padrão, conforme obtido de [**IAMVideoCompression::GetInfo.**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo) Por exemplo:


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



O exemplo de código a seguir tenta encontrar a interface **IAMVideoCompression** no pino de saída. Se for bem-sucedido, ele recuperará os valores padrão e real para as propriedades de compactação:


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> Se você estiver usando a interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) para criar o grafo, poderá obter a interface **IAMVideoCompression** chamando [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), em vez de usar **IBaseFilter::EnumPins**. O **método FindInterface** é um método auxiliar que pesquisa filtros e pinos no grafo para uma interface especificada.

 

 

 



