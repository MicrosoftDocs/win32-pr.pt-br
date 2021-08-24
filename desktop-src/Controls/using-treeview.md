---
title: Usando Tree-View controles
description: Esta seção contém detalhes de implementação e código de exemplo para trabalhar com controles de exibição de árvore.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8beac9ef5163b52582a2ea89820278cc10f9f68ad865354404efd72a61b04993
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318585"
---
# <a name="using-tree-view-controls"></a>Usando Tree-View controles

Esta seção contém detalhes de implementação e código de exemplo para trabalhar com controles de exibição de árvore.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como criar um controle Tree-View dados](create-a-tree-view-control.md)<br/>       | Para criar um controle de exibição de árvore, use a função [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando o [**valor \_ TREEVIEW**](common-control-window-classes.md) do WC para a classe de janela. A classe de janela de exibição de árvore é registrada no espaço de endereço do aplicativo quando a DLL de controle comum é carregada. Para garantir que a DLL seja carregada, use a [**função InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) <br/>                                                                    |
| [Como inicializar a lista de imagens](initialize-the-image-list.md)<br/>         | Cada item em um controle de exibição de árvore pode ter duas imagens associadas a ele. Um item exibe uma imagem quando está selecionada e a outra quando não está. Para incluir imagens com itens de exibição de árvore, primeiro use as funções Listas [de](image-lists.md) Imagens para criar uma lista de imagens e adicionar imagens a ela. Em seguida, associe a lista de imagens ao controle de exibição de árvore usando a mensagem [**\_ TVM SETIMAGELIST.**](tvm-setimagelist.md) <br/>                                                                     |
| [Como adicionar itens Tree-View dados](add-tree-view-items.md)<br/>                     | Adicione um item a um controle de exibição de árvore enviando a mensagem [**TVM \_ INSERTITEM**](tvm-insertitem.md) para o controle. A mensagem inclui o endereço de uma estrutura [**TVINSERTSTRUCT,**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) especificando o item pai, o item após o qual o novo item é inserido e uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define os atributos do item. Os atributos incluem o rótulo do item, suas imagens selecionadas e não selecionadas e um valor definido pelo aplicativo de 32 bits. <br/> |
| [Como arrastar um item Tree-View dados](drag-a-tree-view-item.md)<br/>                 | Este tópico demonstra o código para lidar com arrastar e soltar itens de exibição de árvore. O código de exemplo consiste em três funções. A primeira função inicia a operação de arrastar, a segunda função arrasta a imagem e a terceira função encerra a operação de arrastar. <br/>                                                                                                                                                                                                                                  |
| [Como trabalhar com índices de imagem de estado](work-with-state-image-indexes.md)<br/> | Geralmente, há confusão sobre como definir e recuperar o índice de imagem de estado em um controle de exibição de árvore. Os exemplos a seguir demonstram o método adequado para definir e recuperar o índice de imagem de estado. Os exemplos supõem que há apenas dois índices de imagem de estado no controle de exibição de árvore, desmarcados e verificados. Se o aplicativo contiver mais de duas, essas funções precisarão ser modificadas para lidar com esse caso. <br/>                                                               |
| [Como usar as Tree-View infotips](use-tree-view-infotips.md)<br/>               | Quando você aplica o estilo [**TVS \_ INFOTIP**](tree-view-control-window-styles.md) a um controle de exibição de árvore, ele gera notificações [ \_ GETINFOTIP](tvn-getinfotip.md) de TVN quando o cursor está sobre um item no exibição de árvore. Ao responder a essa notificação, você pode definir o texto que aparece no infotip. <br/>                                                                                                                                                                                    |



 

 

