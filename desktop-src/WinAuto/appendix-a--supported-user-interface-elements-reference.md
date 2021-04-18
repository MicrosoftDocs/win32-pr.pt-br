---
title: Apêndice A referência de elementos da interface do usuário com suporte
description: Este apêndice contém informações sobre os elementos de interface do usuário fornecidos pelo sistema expostos pela Microsoft Acessibilidade Ativa no Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP e Windows 2000 Server.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f75cd4251ed7d75d9aa6a2d83387a51a8b157e9
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "105764379"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Apêndice A: referência de elementos da interface do usuário com suporte

Este apêndice contém informações sobre os elementos de interface do usuário fornecidos pelo sistema expostos pela Microsoft Acessibilidade Ativa no Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP e Windows 2000 Server. Esse suporte permite que os utilitários de cliente obtenham informações sobre elementos de interface do usuário fornecidos pelo sistema em aplicativos que não implementam o Microsoft Acessibilidade Ativa.

O Oleacc.dll dá suporte a controles que são definidos em elementos de interface do usuário User32.dll, Comctl32.dll e Windows. Especificamente, ele dá suporte aos seguintes tipos de elementos da interface do usuário (listados pelo nome da classe do Windows).



| Nome da classe do Windows                   | Tipo de elemento de interface do usuário                                         | Atualizações do Windows Vista                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Caixas de listagem                                              | Nenhum                                                                                                                                                                                                                 |
| Botão                               | Botões de push, botões de opção, botões de seleção, caixas de grupo | Os botões de divisão podem ter zero ou mais filhos.                                                                                                                                                                        |
| Estático                               | Rótulos                                                  | Nenhum                                                                                                                                                                                                                 |
| Editar                                 | Caixas de texto                                              | Nenhum                                                                                                                                                                                                                 |
| ComboBox                             | Caixas de combinação, listas suspensas                            | Nenhum                                                                                                                                                                                                                 |
| ScrollBar                            | Barras de rolagem                                             | [**Evento \_ de O objeto \_ CONTENTSCROLLED**](event-constants.md) é um novo evento para controle que tem funcionalidade de rolagem, mas não inclui uma barra de rolagem padrão como parte do controle. |
| \#32768                              | Menus do usuário                                              | Nenhum                                                                                                                                                                                                                 |
| \#32770                              | Caixas de diálogo de usuário                                       | Nenhum                                                                                                                                                                                                                 |
| \#32771                              | Alt-janela da guia                                          | Disponível somente no modo clássico.                                                                                                                                                                                      |
| msctls \_ statusbar32                  | Barras de status                                             | Nenhum                                                                                                                                                                                                                 |
| msctls \_ progress32                   | Barras de progresso                                           | As novas opções de cor das barras de progresso não são expostas pelo Microsoft Acessibilidade Ativa ou propriedades de automação da interface do usuário da Microsoft.                                                                                         |
| msctls \_ hotkey32                     | Controles de tecla quente                                        | Nenhum                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Trackbars, controles deslizantes                                      | Nenhum                                                                                                                                                                                                                 |
| msctls \_ updown32                     | Controles de cima para baixo ou de rotação                                | Nenhum                                                                                                                                                                                                                 |
| SysAnimate32                         | Controle de animação                                       | Nenhum                                                                                                                                                                                                                 |
| SysTabControl32                      | Controle guia                                             | Nenhum                                                                                                                                                                                                                 |
| SysHeader32                          | Cabeçalhos de exibição de lista                                       | Nenhum                                                                                                                                                                                                                 |
| SysListView32                        | Controles de exibição de lista                                      | Nenhum                                                                                                                                                                                                                 |
| SysTreeView32                        | Controles de exibição de árvore                                      | Nenhum                                                                                                                                                                                                                 |
| SysDateTimePick32 (versões 5 e 6) | Seletor de data e/ou hora                                 | A versão 6 deste controle no Windows Vista tem uma implementação de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa.                                                                                                           |
| SysIPAddress32                       | Controles de endereço IP                                     | Nenhum                                                                                                                                                                                                                 |
| Dicas de ferramenta \_ class32                    | Dicas                                                | Nenhum                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Barras de ferramentas                                                | Nenhum                                                                                                                                                                                                                 |
| RICHEDIT, RichEdit20A, RichEdit20W   | Campos de texto                                             | Nenhum                                                                                                                                                                                                                 |
| SysMonthCal32 (versões 5 e 6)     | Calendário mensal                                          | A versão 6 deste controle no Windows Vista tem uma implementação de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa.                                                                                                           |



 

Embora algum suporte para elementos de interface do usuário fornecidos pelo sistema seja fornecido pelo Microsoft Acessibilidade Ativa no Microsoft Windows NT 4,0 com o service pack 4, esse suporte é limitado.

Este apêndice lista as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e os métodos aos quais o Microsoft acessibilidade ativa dá suporte para cada elemento de interface do usuário. Quando aplicável, a documentação também lista o [WinEvents](winevents-infrastructure.md) que o elemento de interface do usuário dispara e inclui informações adicionais sobre as propriedades e os métodos com suporte. Ele também inclui informações sobre as funções de objeto e seus métodos e propriedades **IAccessible** com suporte.

Esses detalhes podem ajudar os desenvolvedores clientes a evitar fazer chamadas desnecessárias para métodos e propriedades sem suporte. Essas informações também permitem que os desenvolvedores de servidor saibam quais propriedades e métodos seus controles personalizados devem dar suporte e quais WinEvents seus controles devem disparar.

Use as informações neste apêndice como um guia. É altamente recomendável que você use as ferramentas de Acessibilidade Ativa da Microsoft para verificar o comportamento esperado para elementos de interface do usuário ou funções de objeto.

Para mais informações, consulte os seguintes tópicos:

-   [Como Acessibilidade Ativa expõe elementos da interface do usuário](how-active-accessibility-exposes-user-interface-elements.md)
-   [Referência de elemento de interface do usuário](user-interface-element-reference.md)

 

 




