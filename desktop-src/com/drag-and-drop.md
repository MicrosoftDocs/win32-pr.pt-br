---
title: Arrastar e soltar
description: Arrastar e soltar refere-se a transferências de dados nas quais um mouse ou outro dispositivo apontador é usado para especificar a fonte de dados e seu destino.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b388fc6c051fa73c72720d1f349cd50a4fa6902b8f880fbf5ccfb4cf263a4227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993156"
---
# <a name="drag-and-drop"></a>Arrastar e soltar

*Arrastar e soltar* refere-se a transferências de dados nas quais um mouse ou outro dispositivo apontador é usado para especificar a fonte de dados e seu destino. Em uma operação típica de arrastar e soltar, um usuário seleciona o objeto a ser transferido movendo o ponteiro do mouse para ele e mantendo o botão esquerdo ou algum outro botão designado para essa finalidade. Enquanto continua mantendo o botão, o usuário inicia a transferência arrastando o objeto para seu destino, que pode ser qualquer contêiner OLE. O recurso arrastar e soltar fornece exatamente a mesma funcionalidade da cópia e colagem da área de transferência OLE, mas adiciona comentários visuais e elimina a necessidade de menus. Na verdade, se um aplicativo der suporte para copiar e colar da área de transferência, será necessário um pouco mais de suporte para arrastar e soltar.

Durante uma operação de arrastar e soltar OLE, são usadas as três partes separadas de código a seguir.



| Fonte de código do tipo "arrastar e soltar"                               | Implementação e uso                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interface [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> | Implementado pelo objeto que contém os dados arrastados, chamados de *fonte de arrastar*.<br/>                                                                                         |
| Interface [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> | Implementado pelo objeto que se destina a aceitar o drop, chamado de *destino de soltura*.<br/>                                                                                 |
| Função [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)<br/>    | Implementado pelo OLE e usado para iniciar uma operação de arrastar e soltar. Depois que a operação estiver em andamento, ela facilitará a comunicação entre a origem de arrastar e o destino de soltar.<br/> |



 

As interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) podem ser implementadas em um contêiner ou em um aplicativo de objeto. A função de arrastar origem ou soltar destino não está limitada a nenhum tipo de aplicativo OLE.

A função OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementa um loop que controla o movimento do mouse e do teclado até o momento em que a operação de arrastar é cancelada ou uma queda ocorre. **DoDragDrop** é a função fundamental no processo de arrastar e soltar, facilitando a comunicação entre a origem de arrastar e o destino de soltar.

Durante uma operação de arrastar e soltar, três tipos de comentários podem ser exibidos para o usuário.



| Tipo de comentário            | Descrição                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comentários de origem<br/>  | Fornecido pela fonte de arrastar, os comentários de origem indicam que os dados estão sendo arrastados e não são alterados durante a operação de arrastar. Normalmente, os dados são realçados para sinalizar que ele foi selecionado.<br/>                                                                                                                                            |
| Comentários do ponteiro<br/> | Fornecido pela fonte de arrastar, o feedback do ponteiro indica o que acontece se o mouse for liberado em um determinado momento. Os comentários do ponteiro são alterados continuamente conforme o usuário move o mouse e/ou pressiona uma tecla modificadora. Por exemplo, se o ponteiro for movido para uma janela que não aceita um drop, o ponteiro muda para o símbolo "não permitido".<br/> |
| Comentários de destino<br/>  | Fornecido pelo destino de soltar, os comentários de destino indicam onde a queda deve ocorrer.<br/>                                                                                                                                                                                                                                                                    |



 

Para obter mais informações, consulte [arrastar responsabilidades de origem](drag-source-responsibilities.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de dados](data-transfer.md)
</dt> </dl>

 

 





