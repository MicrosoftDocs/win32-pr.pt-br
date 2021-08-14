---
title: D1111 usando camada quando o clipe é suficiente
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Uma camada está sendo usada com uma máscara de opacidade nula, 1,0 de opacidade e uma máscara geométrica retangular alinhada ao eixo. A API de clipe Push/pop deve obter os mesmos resultados com melhor desempenho.
keywords:
- D1111 usando camada quando o clipe é suficiente Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b03a6c2a4806724cd7cfdc97354e29e86dc60e0f1729ee9efeca89d971ca0a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758096"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111: usando a camada quando o clipe é suficiente

PERF-uma camada está sendo usada com uma máscara de opacidade **nula** , 1,0 de opacidade e uma máscara geométrica retangular alinhada ao eixo. A API de clipe Push/pop deve obter os mesmos resultados com melhor desempenho.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

O endereço da interface.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Nível de erro | Informações |



 

## <a name="examples"></a>Exemplos

O código a seguir usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) quando a camada contém apenas um primitivo (um retângulo) e os campos da estrutura [**de \_ \_ parâmetros da camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) são definidos como padrões. Para obter os valores padrão da estrutura de **\_ \_ parâmetros de camada d2d1** , consulte [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



Este exemplo produz a seguinte mensagem de depuração:

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Possíveis causas

Uma camada foi usada quando os métodos [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) seriam suficientes.

 

 