---
description: Método virtual puro que as classes derivadas substituem.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Método CBaseControlVideo. GetStaticImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752915"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>Método CBaseControlVideo. GetStaticImage

Método virtual puro que as classes derivadas substituem.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Ponteiro para o tamanho do buffer de saída.

</dd> <dt>

*pDIBImage* 
</dt> <dd>

Ponteiro para o buffer de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , um aplicativo pode solicitar que ele receba uma cópia da imagem atual em um buffer de memória (alguns renderizadores podem retornar E \_ NOTIMPL para isso se não suportarem isso). A classe derivada determina como recuperar a imagem. Quando o aplicativo chama **CBaseControlVideo:: GetStaticImage**, ele chama esse método virtual puro que a classe derivada deve substituir para implementá-lo. Isso também é chamado pela função de membro [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) .

A classe fornece uma função de membro auxiliar, [**CBaseControlVideo:: CopyImage**](cbasecontrolvideo-copyimage.md), que pode receber um exemplo que contém uma imagem, e a função de membro copiará a seção relevante dela (com base no retângulo de origem atual) para o buffer de saída fornecido pelo aplicativo.

O exemplo a seguir demonstra uma implementação dessa função de membro em uma classe derivada. Neste exemplo, m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md).


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




