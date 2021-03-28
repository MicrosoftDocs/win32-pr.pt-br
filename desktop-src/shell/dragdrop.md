---
description: Muitos aplicativos permitem que os usuários transfiram dados para outro aplicativo arrastando e soltando os dados com o mouse, ou usando a área de transferência.
title: Transferindo objetos do shell com o recurso de arrastar e soltar e a área de transferência
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b04523d0ae22eac7bef68f37a6d22ac94b21e303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967949"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Transferindo objetos do shell com o recurso de arrastar e soltar e a área de transferência

Muitos aplicativos permitem que os usuários transfiram dados para outro aplicativo arrastando e soltando os dados com o mouse, ou usando a área de transferência. Entre os muitos tipos de dados que podem ser transferidos estão objetos do Shell, como arquivos ou pastas. A transferência de dados do shell pode ocorrer entre dois aplicativos, mas os usuários também podem transferir dados do Shell de ou para o desktop ou o Windows Explorer.

Embora os arquivos sejam o objeto Shell mais transferido, a transferência de dados do shell pode envolver qualquer variedade de objetos encontrados no [namespace do Shell](namespace-intro.md). Por exemplo, seu aplicativo pode precisar transferir um arquivo para uma pasta virtual, como a lixeira, ou aceitar um objeto de uma extensão de namespace que não seja da Microsoft. Se você estiver implementando uma extensão de namespace, ela deverá ser capaz de se comportar corretamente como uma origem e um destino de soltura.

Este documento discute como os aplicativos podem implementar transferências de dados de arrastar e soltar e de área de transferência com objetos do Shell.

-   [O objeto de dados do Shell](dataobject.md)
-   [Formatos de área de transferência do Shell](clipboard.md)
-   [Manipulação de cenários de Transferência de Dados do Shell](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Como o recurso de arrastar e soltar funciona com objetos shell

Geralmente, os aplicativos precisam fornecer aos usuários uma maneira de transferir dados do Shell. Alguns exemplos incluem:

-   Arrastar um arquivo do Windows Explorer ou da área de trabalho e soltá-lo em um aplicativo.
-   Copiar um arquivo para a área de transferência no Windows Explorer e colá-lo em um aplicativo.
-   Arrastando um arquivo de um aplicativo para a lixeira.

Para obter uma discussão detalhada sobre como lidar com esses e outros cenários, consulte [manipulando cenários de transferência de dados do Shell](datascenarios.md). Este documento enfoca os princípios gerais por trás da transferência de dados do Shell.

O Windows fornece duas maneiras padrão para os aplicativos transferirem dados do Shell:

-   Um usuário recorta ou copia dados do Shell, como um ou mais arquivos, para a área de transferência. O outro aplicativo recupera os dados da área de transferência.
-   Um usuário arrasta um ícone que representa os dados do aplicativo de origem e descarta o ícone em uma janela de Propriedade do destino.

Em ambos os casos, os dados transferidos estão contidos em um *objeto de dados*. Os objetos de dados são objetos Component Object Model (COM) que expõem a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Esquemáticomente, há três etapas essenciais que todas as transferências de dados do Shell devem seguir:

1.  A origem cria um objeto de dados que representa os dados a serem transferidos.
2.  O destino recebe um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados.
3.  O destino chama a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) para extrair os dados dela.

A diferença entre transferências de dados de área de transferência e arrastar e soltar depende principalmente de como o ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) é transferido da origem para o destino.

### <a name="clipboard-data-transfers"></a>Transferências de dados da área de transferência

A área de transferência é a maneira mais simples de transferir dados do Shell. O procedimento básico é semelhante a transferências de dados da área de transferência padrão. No entanto, como você está transferindo um ponteiro para um objeto de dados, não os dados em si, deve usar a API da área de transferência OLE em vez da API da área de transferência padrão. O procedimento a seguir descreve como usar a API de área de transferência OLE para transferir dados do shell com a área de transferência:

1.  A fonte de dados cria um objeto de dados para conter os dados.
2.  A fonte de dados chama [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard), que coloca um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados na área de transferência.
3.  O destino chama [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) para recuperar o ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados.
4.  O destino extrai os dados chamando o método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) .
5.  Com algumas transferências de dados do Shell, o destino também pode precisar chamar o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados para fornecer comentários ao objeto de dados no resultado da transferência de dados. Consulte [lidando com operações de movimentação otimizadas](datascenarios.md) para obter um exemplo desse tipo de operação.

### <a name="drag-and-drop-data-transfers"></a>Transferências de dados do tipo "arrastar e soltar"

Embora seja um pouco mais complexo de implementar, a transferência de dados de arrastar e soltar tem algumas vantagens significativas na área de transferência:

-   Transferências de arrastar e soltar podem ser feitas com um simples movimento de mouse, tornando a operação mais flexível e intuitiva para uso do que a área de transferência.
-   O recurso arrastar e soltar fornece ao usuário uma representação visual da operação. O usuário pode seguir o ícone à medida que ele se move da origem para o destino.
-   O recurso de arrastar e soltar notifica o destino quando os dados estão disponíveis.

As operações de arrastar e soltar também usam objetos de dados para transferir dados. No entanto, a origem do descarte deve fornecer funcionalidade além da necessária para transferências da área de transferência:

-   A origem de soltura também deve criar um objeto que expõe uma interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . O sistema usa **IDropSource** para se comunicar com a origem enquanto a operação está em andamento.
-   O objeto de dados do tipo "arrastar e soltar" é responsável por acompanhar o movimento do cursor e exibir um ícone para representar o objeto de dados.

Os destinos de destino também devem fornecer mais funcionalidade do que o necessário para lidar com transferências de área de transferência:

-   O destino de soltura deve expor uma interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Quando o cursor está sobre uma janela de destino, o sistema usa **IDropTarget** para fornecer o destino com informações como a posição do cursor e notificá-lo quando os dados são descartados.
-   O destino de soltura deve se registrar no sistema chamando [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop). Essa função fornece ao sistema o identificador para uma janela de destino e um ponteiro para a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do aplicativo de destino.

> [!Note]  
> Para operações de arrastar e soltar, seu aplicativo deve inicializar com com [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize), não [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

O procedimento a seguir descreve as etapas essenciais que normalmente são usadas para transferir dados do shell com o recurso de arrastar e soltar:

1.  O destino chama [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) para dar ao sistema um ponteiro para sua interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e registrar uma janela como um destino de soltar.
2.  Quando o usuário inicia uma operação de arrastar e soltar, a origem cria um objeto de dados e inicia um *loop de arrastar* chamando [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Quando o cursor está sobre a janela de destino, o sistema notifica o destino chamando um dos métodos [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do destino. O sistema chama [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando o cursor entra na janela de destino e [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) como o cursor passa pela janela de destino. Os dois métodos fornecem o destino de soltura com a posição atual do cursor e o estado das teclas modificadoras de teclado, como CTRL ou ALT. Quando o cursor sai da janela de destino, o sistema notifica o destino chamando [**IDropTarget::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave). Quando qualquer um desses métodos retorna, o sistema chama a interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) para passar o valor de retorno para a origem.
4.  Quando o usuário libera o botão do mouse para descartar os dados, o sistema chama o método [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) do destino. Entre os parâmetros do método está um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados.
5.  O destino chama o método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) do objeto de dados para extrair os dados.
6.  Com algumas transferências de dados do Shell, o destino também pode precisar chamar o método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados para fornecer comentários à fonte no resultado da transferência de dados.
7.  Quando o destino é concluído com o objeto de dados, ele retorna de [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop). O sistema retorna a chamada [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) da origem para notificar a origem de que a transferência de dados foi concluída.
8.  Dependendo do [cenário de transferência de dados](datascenarios.md)específico, a origem pode precisar executar uma ação adicional com base no valor retornado por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) e os valores que são passados para o objeto de dados pelo destino. Por exemplo, quando um arquivo é movido, a origem deve verificar esses valores para determinar se ele deve excluir o arquivo original.
9.  A origem libera o objeto de dados.

Embora os procedimentos descritos acima forneçam um bom modelo geral para transferência de dados do Shell, há muitos tipos diferentes de dados que podem estar contidos em um objeto de dados do Shell. Também há vários cenários de transferência de dados diferentes que seu aplicativo pode precisar manipular. Cada tipo de dados e cenário requer uma abordagem um pouco diferente para três etapas principais no procedimento:

-   Como uma fonte constrói um objeto de dados para conter os dados do Shell.
-   Como um destino extrai dados do shell do objeto de dados.
-   Como a origem conclui a operação de transferência de dados.

O [objeto de dados do Shell](dataobject.md) fornece uma discussão geral de como uma fonte constrói um objeto de dados do Shell e como esse objeto de dados pode ser tratado pelo destino. O [tratamento de cenários de transferência de dados de shell](datascenarios.md) aborda em detalhes como lidar com vários cenários comuns de transferência de dados do Shell.

 

 
