---
title: Usando controles de Tree-View
description: Esta seção contém detalhes de implementação e código de exemplo para trabalhar com controles de exibição de árvore.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9ed8d1040a635964e772b8399a5c476e67f9aba
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105755823"
---
# <a name="using-tree-view-controls"></a>Usando controles de Tree-View

Esta seção contém detalhes de implementação e código de exemplo para trabalhar com controles de exibição de árvore.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como criar um controle de Tree-View](create-a-tree-view-control.md)<br/>       | Para criar um controle de exibição de árvore, use a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando o valor de [**\_ TreeView WC**](common-control-window-classes.md) para a classe Window. A classe de janela de exibição de árvore é registrada no espaço de endereço do aplicativo quando a DLL de controle comum é carregada. Para garantir que a DLL seja carregada, use a função [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) . <br/>                                                                    |
| [Como inicializar a lista de imagens](initialize-the-image-list.md)<br/>         | Cada item em um controle de exibição de árvore pode ter duas imagens associadas a ele. Um item exibe uma imagem quando ela é selecionada e a outra quando não está. Para incluir imagens com itens de exibição em árvore, primeiro use as funções de [lista de imagens](image-lists.md) para criar uma lista de imagens e adicionar imagens a ela. Em seguida, associe a lista de imagens ao controle de exibição em árvore usando a mensagem [**TVM \_ SetImageList**](tvm-setimagelist.md) . <br/>                                                                     |
| [Como adicionar itens de Tree-View](add-tree-view-items.md)<br/>                     | Você adiciona um item a um controle de exibição de árvore enviando a mensagem [**TVM \_ INSERTITEM**](tvm-insertitem.md) para o controle. A mensagem inclui o endereço de uma estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , especificando o item pai, o item após o qual o novo item é inserido e uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define os atributos do item. Os atributos incluem o rótulo do item, suas imagens selecionadas e não selecionadas, e um valor definido pelo aplicativo de 32 bits. <br/> |
| [Como arrastar um item de Tree-View](drag-a-tree-view-item.md)<br/>                 | Este tópico demonstra o código para a manipulação de arrastar e soltar de itens de exibição em árvore. O código de exemplo consiste em três funções. A primeira função inicia a operação de arrastar, a segunda função arrasta a imagem e a terceira função encerra a operação de arrastar. <br/>                                                                                                                                                                                                                                  |
| [Como trabalhar com índices de imagem de estado](work-with-state-image-indexes.md)<br/> | Geralmente, há confusão sobre como definir e recuperar o índice de imagem de estado em um controle de exibição de árvore. Os exemplos a seguir demonstram o método apropriado para configurar e recuperar o índice de imagem de estado. Os exemplos supõem que haja apenas dois índices de imagem de estado no controle de exibição de árvore, desmarcado e marcado. Se seu aplicativo contiver mais de duas, será necessário modificar essas funções para lidar com esse caso. <br/>                                                               |
| [Como usar Tree-View Infotips](use-tree-view-infotips.md)<br/>               | Quando você aplica o [**estilo \_ INFOTIP de TVs**](tree-view-control-window-styles.md) a um controle de exibição de árvore, ele gera notificações [TVN \_ GETINFOTIP](tvn-getinfotip.md) quando o cursor está sobre um item no modo de exibição de árvore. Ao responder a essa notificação, você pode definir o texto que aparece na InfoTip. <br/>                                                                                                                                                                                    |



 

 

