---
title: Falha de liberação de D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Uma chamada de liberação por um destino de renderização falhou
keywords:
- D1110 de falha de liberação de Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 721fb27e8cfd5e83f94b93079ee66e4a1c35992d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549921"
---
# <a name="d1110-flush-failure"></a>D1110: falha de liberação

Uma chamada de liberação por um recurso com falha de destino de renderização \[  \] . Marcas \[ *da tag1*, *tag2* \] .

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Kit*
</dt> <dd>

O endereço do destino de renderização.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*da tag1*
</dt> <dd>

O primeiro valor de marca. Consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obter mais informações.

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

O valor da segunda marca. Consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obter mais informações.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nível de erro | Aviso |



 

## <a name="examples"></a>Exemplos

**Exemplo 1:** O código a seguir mostra que uma chamada de desenho está em um estado inválido. Para evitar a mensagem de aviso, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para definir o modo AntiAlias de d2d1 \_ \_ \_ AntiAlias antes de uma chamada [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





Este exemplo produz a seguinte mensagem de depuração:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Exemplo 2:** O código a seguir mostra que a [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) é chamada após a chamada [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



Este exemplo produz a seguinte mensagem de depuração:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Possíveis causas

A [**chamada Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) pode falhar por um dos dois motivos. Ele pode falhar porque o método foi chamado fora da chamada [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)EndDraw ou pode falhar porque houve um erro produzido por uma das operações de destino de renderização que foram processadas desde a última chamada flush ou / [](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) **EndDraw.**  Para corrigir o problema, o aplicativo deve determinar a causa do erro e tomar a ação apropriada.

## <a name="fixes"></a>Correções

Há muitos motivos pelos quais uma [**chamada flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) pode falhar. O aplicativo deve determinar a causa do erro e tomar a ação apropriada.

 

 