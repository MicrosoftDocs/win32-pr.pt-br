---
title: Tipo de controle de imagem
description: Este tópico fornece informações sobre o suporte à automação da interface do usuário da Microsoft para o tipo de controle imagem.
ms.assetid: 439c708c-4fb4-481b-a2ff-3816d649f3ff
keywords:
- Automação da interface do usuário, suporte para tipo de controle de imagem
- Automação da interface do usuário, tipo de controle de imagem
- Automação da interface do usuário, estrutura de árvore para tipo de controle de imagem
- Automação da interface do usuário, propriedades para tipo de controle de imagem
- Automação da interface do usuário, padrões de controle para tipo de controle de imagem
- Automação da interface do usuário, eventos para tipo de controle de imagem
- estruturas de árvore, tipo de controle de imagem
- Propriedades, tipo de controle de imagem
- padrões de controle, tipo de controle de imagem
- eventos, tipo de controle de imagem
- suporte para tipo de controle de imagem
- tipo de controle Imagem
- tipos de controle, estrutura de árvore para tipo de controle de imagem
- tipos de controle, padrões de controle para tipo de controle de imagem
- tipos de controle, suporte para imagem
- tipos de controle, imagem
ms.topic: article
ms.date: 10/08/2019
ms.openlocfilehash: b91d55bf8e21813e180476146625172e3eab1a6d
ms.sourcegitcommit: da8cc3fb3c9f14cb768855502a2b6815ddee13b6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/10/2019
ms.locfileid: "105759280"
---
# <a name="image-control-type"></a>Tipo de controle de imagem

Este tópico fornece informações sobre o suporte à automação da interface do usuário da Microsoft para o tipo de controle **imagem** .

Os controles de imagem usados como ícones, gráficos informativos e gráficos terão suporte para o tipo de controle de **imagem** . Os controles usados como imagens de plano de fundo ou marca d' água não oferecerão suporte ao tipo de controle **Image** .

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Image** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de imagem em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

- [Estrutura de árvore típica](#typical-tree-structure)
- [Propriedades relevantes](#relevant-properties)
- [Padrões de controle necessários](#required-control-patterns)
- [Eventos necessários](#required-events)
- [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de imagem e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).

| Exibição de controle | Exibição de conteúdo |
| ------------ | ------------ |
| Imagem | Imagem (depende se a imagem contém informações, com base no valor da propriedade [identificadores de Propriedade do elemento Automation](uiauto-automation-element-propids.md) ) |

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de imagem. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).

| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | O ponto clicável do controle de imagem deve ser um ponto dentro do retângulo delimitador do controle de imagem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Imagem**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | A propriedade **HelpText** expõe uma cadeia de caracteres localizada que descreve a aparência visual real do controle ou outras informações de dica de ferramenta associadas à imagem. Essa propriedade deve ter suporte quando uma descrição longa for necessária para transmitir mais informações sobre o controle de imagem (por exemplo, se a imagem for um gráfico complicado ou diagrama). Essa propriedade é mapeada para a marca HTML **longdesc** e a marca **desc** (SVG) de gráficos escalonáveis. Os desenvolvedores que trabalham com controles de imagem devem dar suporte a uma propriedade para permitir que a descrição visual seja definida no controle. Essa propriedade deve ser mapeada para a propriedade **VisualDescription** de automação da interface do usuário. |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Consulte observações. | O controle de imagem deve ser incluído na exibição de conteúdo da árvore de automação da interface do usuário quando ela contiver informações significativas ainda não expostas ao usuário final.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de imagem é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Consulte observações. | Se o controle de imagem representar informações de estado sobre um item específico na tela, o controle deverá estar contido no item. Quando a imagem está contida em um item, o item deve dar suporte à propriedade Status e gerar notificações apropriadas quando o status for alterado. Se uma imagem for um controle autônomo e estiver transmitindo o status, essa propriedade deverá ter suporte.                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **imagem** . O valor padrão é "Image" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | A propriedade **Name** deve ser exposta para todos os controles de imagem que contêm informações. O acesso programático a essas informações requer que um equivalente textual para o gráfico seja fornecido. Se o controle de imagem for puramente decorativo, ele só deverá aparecer na exibição de controle da árvore de automação da interface do usuário e não precisará ter um nome (consulte [comentários](#remarks)). As estruturas de interface do usuário devem oferecer suporte a uma propriedade ALT ou de texto alternativo em imagens que podem ser definidas de dentro de sua estrutura. Essa propriedade será mapeada para a propriedade de nome de automação da interface do usuário.                                                                                                                                                     |

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte para controles de imagem. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).

| Padrão de controle                                                 | Suporte | Observações                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)           | Depende | O controle de imagem dá suporte ao padrão de controle [GridItem](uiauto-implementinggriditem.md) se o controle estiver dentro de um contêiner de grade.                                                                                                                                                                                                                                                                                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nunca   | Se o controle de imagem for um objeto clicável, o controle deverá dar suporte a um tipo de controle que dá suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , como o tipo de controle [Button](uiauto-supportbuttoncontroltype.md) . Para um objeto Image que contém vários objetos clicáveis, o elemento (tipo de controle Image) pode hospedar links filho (tipo de controle[Hyperlink](uiauto-supporthyperlinkcontroltype.md) ) na árvore de automação da interface do usuário. |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Nunca   | Os controles de imagem não devem dar suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) . Se as imagens fizerem parte de um contêiner que é selecionável, como um botão que tem um ícone de imagem como conteúdo, esse contêiner dará suporte ao padrão, não à imagem no.                                                                                                                                                                           |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)         | Depende | O controle de imagem dá suporte ao padrão de controle [TableItem](uiauto-implementingtableitem.md) se o controle estiver dentro de um contêiner que tem controles de cabeçalho.                                                                                                                                                                                                                                                                                                |

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de imagem são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).

| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade ItemStatusPropertyId.               | Se o controle der suporte [**à propriedade ItemProperty**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |

## <a name="remarks"></a>Comentários

O World Wide Web Consortium (W3C) define uma imagem decorativa como uma que não adiciona informações ao conteúdo de uma página. Para obter mais detalhes, consulte o tópico W3C sobre [imagens decorativas](https://www.w3.org/WAI/tutorials/images/decorative/).

Em relação à automação da interface do usuário:

- Se uma imagem é puramente decorativa, não é interativa e não transmite nenhuma informação, a imagem:
  - Pode ou não estar na árvore UIA
  - Pode ou não estar na exibição bruta UIA
  - Não deve estar no modo de exibição de controle UIA
  - Não deve estar no modo de exibição de conteúdo
  - Pode ou não ter um nome
- Se uma imagem transmite informações, mas há um texto claramente associado que fornece as mesmas informações (como um botão de reprodução que contém um gráfico de triângulo apontando para a esquerda, juntamente com o texto "Play"), a imagem é considerada decorativa e a imagem:
  - Deve estar na exibição bruta
  - Deve estar no modo de exibição de controle
  - Não deve estar no modo de exibição de conteúdo
  - Pode ou não ter um valor na propriedade Name
  - O texto que também transmite o significado da imagem deve estar na exibição de conteúdo
- Se uma imagem é informativa e transmite detalhes que não são fornecidos por nenhum texto associado, a imagem:
  - Deve estar na exibição bruta
  - Deve estar no modo de exibição de controle
  - Deve estar na exibição de conteúdo
  - Deve ter um valor de nome que descreva a imagem e seu significado

## <a name="related-topics"></a>Tópicos relacionados

### <a name="conceptual"></a>Conceitual

- [Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
- [Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
