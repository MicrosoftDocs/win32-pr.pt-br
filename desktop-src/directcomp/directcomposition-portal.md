---
title: DirectComposition
description: Este tópico explica a finalidade do Microsoft DirectComposition, identifica seus requisitos de tempo de execução e descreve o plano de fundo de programação que você precisa para usar o Microsoft DirectComposition com eficiência.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- DirectComposition Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291984"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Finalidade

O Microsoft DirectComposition é um componente do Windows que permite a composição de bitmap de alto desempenho com transformações, efeitos e animações. Os desenvolvedores de aplicativos podem usar a API DirectComposition para criar interfaces do usuário visualmente atraentes que contam com transições animadas avançadas e fluidas de um elemento visual para outro.

O DirectComposition permite transições avançadas e fluintes obtendo uma alta taxa de quadros, usando hardware de gráficos e operando independentemente do thread da interface do usuário. O DirectComposition pode aceitar conteúdo de bitmap desenhado por diferentes bibliotecas de renderização, incluindo bitmaps do Microsoft DirectX e bitmaps renderizados para uma janela (bitmaps HWND). Além disso, o DirectComposition dá suporte a uma variedade de transformações, como transformações de afinidade 2D e transformações de perspectiva 3D, bem como efeitos básicos como recorte e opacidade.

O DirectComposition foi projetado para simplificar o processo de composição de [*visuais*](directcomposition-glossary.md) e criação de transições animadas. Se seu aplicativo já contiver código de renderização ou já usar a API do DirectX recomendada, você só precisará fazer uma quantidade mínima de trabalho para usar o DirectComposition efetivamente.

## <a name="developer-audience"></a>Público de desenvolvedores

A API do DirectComposition destina-se a desenvolvedores de gráficos experientes e altamente compatíveis que conhecem o C/C++, têm uma compreensão sólida do COM (Component Object Model) e estão familiarizados com os conceitos de programação do Windows.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O DirectComposition foi introduzido no Windows 8. Ele está incluído em plataformas de 32 bits, 64 bits e ARM.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                       | Descrição                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Por que usar o DirectComposition?](why-use-directcomposition-.md)<br/>     | Este tópico descreve os recursos e os benefícios do DirectComposition. <br/>                                                                           |
| [Como usar o DirectComposition](how-to-use-directcomposition.md)<br/> | Esta seção descreve as práticas recomendadas para usar a API DirectComposition e demonstra como usar a API para realizar várias tarefas comuns. <br/> |
| [Conceitos de DirectComposition](directcomposition-concepts.md)<br/>     | Esta seção fornece uma visão geral conceitual do DirectComposition.<br/>                                                                                   |
| [Referência de DirectComposition](reference.md)<br/>                     | Esta seção fornece informações de referência detalhadas para os elementos que compõem a API DirectComposition.<br/>                                       |
| [Exemplos de DirectComposition](directcomposition-code-samples.md)<br/>  | Os aplicativos de exemplo a seguir mostram como usar a API DirectComposition e demonstrar seus recursos. <br/>                                      |
| [Glossário do DirectComposition](directcomposition-glossary.md)<br/>     | Este tópico define os termos de DirectComposition. <br/>                                                                                                        |



 

 

 





