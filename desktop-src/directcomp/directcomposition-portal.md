---
title: DirectComposition
description: Este tópico explica a finalidade do Microsoft DirectComposition, identifica seus requisitos de tempo de run-time e descreve o plano de fundo de programação que você precisa para usar o Microsoft DirectComposition com eficiência.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- DirectComposition API
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1b13dbd0ee4893f1b208cd88d7fd1251b5fb7ece2400b7e0b195e84865b2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985406"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> Para aplicativos Windows 10, recomendamos o uso de APIs Windows.UI.Composition em vez de DirectComposition. Para obter mais informações, consulte [Modernizar seu aplicativo da área de trabalho usando a camada visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Finalidade

O Microsoft DirectComposition é um Windows que permite a composição de bitmap de alto desempenho com transformações, efeitos e animações. Os desenvolvedores de aplicativos podem usar a API DirectComposition para criar interfaces do usuário visualmente atraentes que contam com transições animadas avançadas e fluidas de um elemento visual para outro.

O DirectComposition permite transições sofisticadas e fluidas, obtendo uma taxa de quadros alta, usando hardware gráfico e operando independentemente do thread da interface do usuário. DirectComposition pode aceitar conteúdo de bitmap desenhado por diferentes bibliotecas de renderização, incluindo bitmaps do Microsoft DirectX e bitmaps renderizados em uma janela (bitmaps HWND). Além disso, o DirectComposition dá suporte a uma variedade de transformações, como transformações de afinidade 2D e transformações de perspectiva 3D, bem como efeitos básicos, como recorte e opacidade.

DirectComposition foi projetado para simplificar o processo de composição [*de visuais*](directcomposition-glossary.md) e criação de transições animadas. Se seu aplicativo já contiver código de renderização ou já usar a API do DirectX recomendada, você só precisará fazer uma quantidade mínima de trabalho para usar o DirectComposition com eficiência.

## <a name="developer-audience"></a>Público de desenvolvedores

A API directComposition destina-se a desenvolvedores gráficos experientes e altamente capacitados que conhecem C/C++, têm uma compreensão sólida do COM (Component Object Model) e estão familiarizados com Windows conceitos de programação.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

DirectComposition foi introduzido no Windows 8. Ele está incluído nas plataformas ARM de 32 bits, 64 bits e .

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                       | Descrição                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Por que usar DirectComposition?](why-use-directcomposition-.md)<br/>     | Este tópico descreve os recursos e os benefícios do DirectComposition. <br/>                                                                           |
| [Como usar o DirectComposition](how-to-use-directcomposition.md)<br/> | Esta seção descreve as práticas recomendadas para usar a API directComposition e demonstra como usar a API para realizar várias tarefas comuns. <br/> |
| [Conceitos do DirectComposition](directcomposition-concepts.md)<br/>     | Esta seção fornece uma visão geral conceitual do DirectComposition.<br/>                                                                                   |
| [Referência do DirectComposition](reference.md)<br/>                     | Esta seção fornece informações de referência detalhadas para os elementos que comem a API directComposition.<br/>                                       |
| [Exemplos de DirectComposition](directcomposition-code-samples.md)<br/>  | Os aplicativos de exemplo a seguir mostram como usar a API directComposition e demonstrar suas funcionalidades. <br/>                                      |
| [Glossário directComposition](directcomposition-glossary.md)<br/>     | Este tópico define os termos do DirectComposition. <br/>                                                                                                        |



 

 

 





