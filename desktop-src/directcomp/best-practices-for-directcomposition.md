---
title: Práticas recomendadas para DirectComposition
description: Este tópico descreve as práticas recomendadas para o uso do Microsoft DirectComposition.
ms.assetid: D3A1ECD4-9358-44B9-8A84-7D901219D5CD
keywords:
- práticas recomendadas para DirectComposition
- práticas recomendadas para DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d19b82b188105c7914e89282c08b12dd4bdc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641749"
---
# <a name="best-practices-for-directcomposition"></a>Práticas recomendadas para DirectComposition

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico descreve as práticas recomendadas para o uso do Microsoft DirectComposition.

-   [Práticas recomendadas](#best-practices-for-directcomposition)
-   [Considerações sobre segurança](#security-considerations)
-   [Tópicos relacionados](#related-topics)

## <a name="best-practices"></a>Melhores práticas

A tabela a seguir apresenta as práticas recomendadas para trabalhar com elementos visuais do Microsoft DirectComposition.



| Prática                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Depois de criar um dispositivo DirectComposition, chame o método [**IDCompositionDevice:: CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) em resposta a cada mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) para garantir que o dispositivo ainda seja válido.<br/> | Se o dispositivo de infraestrutura gráfica do Microsoft DirectX (DXGI) for perdido, o dispositivo DirectComposition associado ao dispositivo DXGI também será perdido. Quando ele detecta um dispositivo perdido, o DirectComposition envia a mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) para todas as janelas. Chamar [**CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) em resposta a cada mensagem do **WM \_ Paint** permite determinar se o objeto de dispositivo do DirectComposition ainda é válido e, caso contrário, tomar medidas para recuperar o conteúdo. <br/> Para obter mais informações, consulte [Device Object](basic-concepts.md).<br/> |
| Crie apenas o número de visuais necessários para uma composição ou animação e destrua os visuais imediatamente após o DirectComposition terminar de usá-los.<br/>                                                                                            | O DirectComposition usa a GPU (unidade de processamento gráfico), um recurso que seu aplicativo compartilha com outros aplicativos e o sistema operacional. Essa prática garante que todos os aplicativos e o sistema operacional recebam recursos de GPU adequados.<br/> Para obter mais informações, consulte [visuais](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                     |
| Não oculte os visuais definindo a opacidade como 0%; em vez disso, remova os visuais da árvore visual.<br/>                                                                                                                                                          | Definir a opacidade como 0% exige mais recursos do sistema do que removê-los da árvore visual.<br/> Para obter mais informações, consulte [opacidade](effects.md) e [árvore visual](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| Não oculte um Visual aplicando um retângulo de clipe vazio (tamanho zero) a um Visual. Em vez disso, remova o Visual da árvore visual. <br/>                                                                                                                 | A remoção de um Visual da árvore visual resulta em um melhor desempenho do que a aplicação de um retângulo de clipe vazio.<br/> Para obter mais informações, consulte [recorte](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Não aplique um retângulo de clipe a um Visual se o clipe retângulo não for necessário, como um retângulo de clipe que inclui todo o conteúdo do bitmap do Visual.<br/>                                                                                       | Retângulos de clipes desnecessários danificam o desempenho do sistema.<br/> Para obter mais informações, consulte [recorte](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Se você precisar de um bitmap grande, de cor única, crie uma superfície de bitmap menor e, em seguida, aplique uma transformação de escala em vez de criar uma superfície de tamanho total. <br/>                                                                                                | A aplicação de uma transformação de escala a uma superfície menor usa menos recursos do sistema do que uma superfície de tamanho total.<br/> Para obter mais informações, consulte [bitmaps](bitmap-surfaces.md) e [transformações](transforms.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| Evite aplicar transformações 3D a vários níveis de uma árvore visual, como a um pai e seus descendentes. <br/>                                                                                                                                        | A aplicação de transformações 3D a vários níveis de uma árvore visual pode produzir resultados indesejados porque as transformações 3D não são multiplicadas na árvore. Por exemplo, uma rotação de 90 graus em volta do eixo y em um filho, e uma rotação de 90 graus em volta do eixo y em um pai, resulta em ambos os visuais sendo girados de forma a nada.<br/> Para obter mais informações, veja [Efeitos](effects.md).<br/>                                                                                                                                                                                                     |



 

## <a name="security-considerations"></a>Considerações de segurança

Os artigos a seguir fornecem diretrizes para escrever código C++ seguro.

-   [Práticas recomendadas de segurança para C++](/cpp/security/security-best-practices-for-cpp?view=vs-2019)
-   [Padrões & práticas de segurança diretrizes para aplicativos](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o DirectComposition](how-to-use-directcomposition.md)
</dt> </dl>

 

