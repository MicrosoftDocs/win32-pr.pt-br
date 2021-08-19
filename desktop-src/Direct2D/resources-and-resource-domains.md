---
title: Visão geral de recursos
description: Descreve Direct2D recursos e como eles podem ser compartilhados.
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D, recursos
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 67dc8c34703c834dbf0f1b651e3c118831d88abe1676feaba68ac53ecb603565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825107"
---
# <a name="resources-overview"></a>Visão geral de recursos

Um Direct2D é um objeto usado para desenhar e é representado por uma interface Direct2D, como [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) ou [**ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Este tópico descreve os tipos de recursos Direct2D e como eles podem ser compartilhados.

Este tópico contém as seguintes seções:

-   [Sobre Direct2D recursos](#about-direct2d-resources)
-   [Recursos independentes de dispositivo](#device-independent-resources)
-   [Recursos dependentes do dispositivo](#device-dependent-resources)
-   [Compartilhamento de recursos de fábrica](#sharing-factory-resources)
-   [Compartilhamento de recursos de destino de renderização](#sharing-render-target-resources)
    -   [Destinos de renderização de hardware](#hardware-render-targets)
    -   [Destinos de renderização do DXGI Surface](#dxgi-surface-render-targets)
    -   [Destinos de renderização compatíveis e bitmaps compartilhados](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>Sobre Direct2D recursos

Muitas APIs 2D aceleradas por hardware são projetadas em torno de um modelo de recurso voltado para CPU e um conjunto de operações de renderização que funcionam bem em CPUs. Em seguida, alguma parte da API é acelerada por hardware. Implementar essas APIs requer um gerenciador de recursos para mapear recursos de CPU para recursos na GPU. Devido a limitações de GPU, algumas operações podem não ser aceleradas em todas as circunstâncias. Nesses casos, o gerenciador de recursos deve se comunicar entre a CPU e a GPU (que é cara) para que ele possa fazer a transição para a renderização da CPU. Em alguns casos, pode forçar a renderização de forma imprevisível a fazer fall back completamente para a CPU. Além disso, as operações de renderização que parecem simples podem exigir etapas de renderização intermediárias temporárias que não são expostas na API e que exigem recursos adicionais de GPU.

Direct2D fornece um mapeamento mais direto para fazer uso completo da GPU. Ele fornece duas categorias de recursos: independente de dispositivo e dependente de dispositivo.

-   Recursos independentes de dispositivo, como [**ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)são mantidos na CPU.
-   Recursos dependentes do dispositivo, como [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)mapeiam diretamente para recursos na GPU (quando a aceleração de hardware está disponível). As chamadas de renderização são executadas combinando informações de vértice e cobertura de uma geometria com informações de texting produzidas pelos recursos dependentes do dispositivo.

Quando você cria recursos dependentes do dispositivo, os recursos do sistema (a GPU, se disponível ou a CPU) são alocados quando o dispositivo é criado e não mudam de uma operação de renderização para outra. Essa situação elimina a necessidade de um gerenciador de recursos. Além das melhorias gerais de desempenho fornecidas pela eliminação de um gerenciador de recursos, esse modelo permite controlar diretamente qualquer renderização intermediária.

Como Direct2D fornece tanto controle sobre os recursos, você deve entender os diferentes tipos de recursos e quando eles podem ser usados juntos.

## <a name="device-independent-resources"></a>Device-Independent recursos

Conforme descrito na seção anterior, os recursos independentes de dispositivo sempre residem na CPU e nunca estão associados a um dispositivo de renderização de hardware. A seguir estão os recursos independentes de dispositivo:

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) e as interfaces que herdam dela.
-   [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) e [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrkeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

Use um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), um recurso independente de dispositivo, para criar recursos independentes de dispositivo. (Para criar uma fábrica, use a [**função CreateFactory.)**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)

Exceto para destinos de renderização, todos os recursos criados por uma fábrica são independentes de dispositivo. Um destino de renderização é um recurso dependente do dispositivo.

## <a name="device-dependent-resources"></a>Device-Dependent recursos

Qualquer recurso que não seja nomeado na lista anterior é um recurso dependente do dispositivo. Os recursos dependentes do dispositivo são associados a um dispositivo de renderização específico. Quando a aceleração de hardware está disponível, esse dispositivo é a GPU. Em outros casos, é a CPU.

Para criar a maioria dos recursos dependentes do dispositivo, use um destino de renderização. Na maioria dos casos, use uma fábrica para criar um destino de renderização.

Veja a seguir exemplos de recursos dependentes do dispositivo:

-   [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) e as interfaces que herdam dele. Use um destino de renderização para criar pincéis.
-   [**ID2D1Layer.**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) Use um destino de renderização para criar camadas.
-   [**ID2D1RenderTarget e**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) as interfaces que herdam dele. Para criar um destino de renderização, use uma fábrica ou outro destino de renderização.

> [!Note]  
> Começando com Windows 8, há novas interfaces que criam recursos dependentes do dispositivo. Um [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) e [**um ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) poderão compartilhar um recurso se o contexto do dispositivo e o recurso são criados a partir do mesmo **ID2D1Device**.

 

Os recursos dependentes do dispositivo tornam-se inutilizáveis quando os dispositivos de renderização associados ficam indisponíveis. Isso significa que, quando você receber o erro [**D2DERR \_ RECREATE \_ TARGET**](direct2d-error-codes.md) para um destino de renderização, deverá recriar o destino de renderização e todos os seus recursos.

## <a name="sharing-factory-resources"></a>Compartilhamento de recursos de fábrica

Você pode compartilhar todos os recursos independentes de dispositivo criados por uma fábrica com todos os outros recursos (independentes de dispositivo ou dependentes de dispositivo) criados pela mesma fábrica. Por exemplo, você pode usar dois [**objetos ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) para desenhar o mesmo [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) se ambos os **objetos ID2D1RenderTarget** foram criados pela mesma fábrica.

As interfaces de sink ([**ID2D1SimplifiedGeometrySink,**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) podem ser compartilhadas com recursos criados por qualquer fábrica. Ao contrário de outras interfaces Direct2D, qualquer implementação de uma interface de sink pode ser usada. Por exemplo, você pode usar sua própria implementação de **ID2D1SimplifiedGeometrySink.**

## <a name="sharing-render-target-resources"></a>Compartilhamento de recursos de destino de renderização

Sua capacidade de compartilhar recursos criados por um destino de renderização depende do tipo de destino de renderização. Quando você cria um destino de renderização do tipo [**D2D1 \_ RENDER TARGET TYPE \_ \_ \_ DEFAULT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type), os recursos criados por esse destino de renderização só podem ser usados por esse destino de renderização (a menos que o destino de renderização se ajuste a uma das categorias descritas nas seções a seguir). Isso ocorre porque você não sabe qual dispositivo o destino de renderização acabará usando– ele pode acabar sendo renderização para hardware local, software ou hardware de um cliente remoto. Por exemplo, você pode escrever um programa que para de funcionar quando ele é exibido remotamente ou quando o destino de renderização é aumentado de tamanho além do tamanho máximo com suporte pelo hardware de renderização.

As seções a seguir descrevem as circunstâncias nas quais um recurso criado por um destino de renderização pode ser compartilhado com outro destino de renderização.

### <a name="hardware-render-targets"></a>Destinos de renderização de hardware

Você pode compartilhar recursos entre qualquer destino de renderização que use explicitamente o hardware, desde que o modo de remoção seja compatível. O modo de remoting só tem a garantia de ser compatível quando ambos os destinos de renderização usam o sinalizador de uso [**D2D1 \_ RENDER TARGET FORCE \_ \_ \_ \_ BITMAP \_ REMOTING**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) ou **D2D1 \_ RENDER TARGET USAGE \_ \_ \_ GDI \_ COMPATIBLE** ou se nenhum sinalizador for especificado. Essas configurações garantem que os recursos sempre estarão localizados no mesmo computador. Para especificar um modo  de uso, de definido o campo de uso da estrutura PROPRIEDADES DE DESTINO RENDERIZAÇÃO [**D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) que você usou para criar o destino de renderização com um ou mais sinalizadores DE USO DE DESTINO DE RENDERIZAÇÃO **D2D1. \_ \_ \_**

Para criar um destino de renderização que  usa explicitamente a renderização de hardware, de definido o campo de tipo da estrutura [**D2D1 \_ RENDER \_ TARGET \_ PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) que você usou para criar o destino de renderização para HARDWARE DE TIPO DE DESTINO RENDERIZAÇÃO [**D2D1 \_ \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="dxgi-surface-render-targets"></a>Destinos de renderização do DXGI Surface

Você pode compartilhar recursos criados por um destino de renderização de superfície DXGI com qualquer outro destino de renderização da superfície DXGI que está usando o mesmo dispositivo Direct3D subjacente.

### <a name="compatible-render-targets-and-shared-bitmaps"></a>Destinos de renderização compatíveis e bitmaps compartilhados

Você pode compartilhar recursos entre um destino de renderização e destinos de renderização compatíveis criados por esse destino de renderização. Para criar um destino de renderização compatível, use o [**método ID2D1RenderTarget::CreateCompatibleRenderTarget.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))

Você pode usar o método [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para criar um [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que pode ser compartilhado entre os dois destinos de renderização especificados na chamada de método, se o método for bem-sucedido. Esse método terá êxito desde que os dois destinos de renderização usem o mesmo dispositivo subjacente para renderização.

 

 
