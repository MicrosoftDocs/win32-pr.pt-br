---
description: Muitos aplicativos permitem que os usuários transfiram dados para outro aplicativo arrastando e soltando os dados com o mouse ou usando a Área de Transferência.
title: Transferindo objetos shell com arrastar e soltar e a área de transferência
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c45fc01709c50fd309c285cb486474cab2f1d8ac0b20c56bb7e21578cb8138f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090616"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Transferindo objetos shell com arrastar e soltar e a área de transferência

Muitos aplicativos permitem que os usuários transfiram dados para outro aplicativo arrastando e soltando os dados com o mouse ou usando a Área de Transferência. Entre os muitos tipos de dados que podem ser transferidos estão objetos shell, como arquivos ou pastas. A transferência de dados do Shell pode ocorrer entre dois aplicativos, mas os usuários também podem transferir dados do Shell de ou para a área de trabalho ou Windows Explorer.

Embora os arquivos sejam o objeto Shell mais comumente transferido, a transferência de dados do Shell pode envolver qualquer uma das variedades de objetos encontrados no [namespace shell](namespace-intro.md). Por exemplo, seu aplicativo pode precisar transferir um arquivo para uma pasta virtual, como o Lixeira, ou aceitar um objeto de uma extensão de namespace que não seja da Microsoft. Se você estiver implementando uma extensão de namespace, ela deverá ser capaz de se comportar corretamente como uma origem e um destino de soltar.

Este documento discute como os aplicativos podem implementar transferências de dados do tipo "arrastar e soltar" e da área de transferência com objetos shell.

-   [O objeto de dados do Shell](dataobject.md)
-   [Formatos da área de transferência do Shell](clipboard.md)
-   [Manipulação de cenários de Transferência de Dados do Shell](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Como o "arrastar e soltar" funciona com objetos shell

Os aplicativos geralmente precisam fornecer aos usuários uma maneira de transferir dados do Shell. Alguns exemplos incluem:

-   Arrastando um arquivo do Windows Explorer ou da área de trabalho e soltando-o em um aplicativo.
-   Copiar um arquivo para a Área de Transferência no Windows Explorer e colar em um aplicativo.
-   Arrastar um arquivo de um aplicativo para o Lixeira.

Para ver uma discussão detalhada sobre como lidar com esses e outros cenários, consulte [Tratamento de cenários de transferência de dados do Shell.](datascenarios.md) Este documento se concentra nos princípios gerais por trás da transferência de dados do Shell.

Windows fornece duas maneiras padrão para os aplicativos transferirem dados do Shell:

-   Um usuário corta ou copia dados do Shell, como um ou mais arquivos, para a Área de Transferência. O outro aplicativo recupera os dados da Área de Transferência.
-   Um usuário arrasta um ícone que representa os dados do aplicativo de origem e descarta o ícone em uma janela pertencente ao destino.

Em ambos os casos, os dados transferidos estão contidos em um *objeto de dados*. Objetos de dados são Component Object Model (COM) que expõem a interface [**IDataObject.**](/windows/win32/api/objidl/nn-objidl-idataobject) De forma esquematática, há três etapas essenciais que todas as transferências de dados do Shell devem seguir:

1.  A origem cria um objeto de dados que representa os dados que devem ser transferidos.
2.  O destino recebe um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados.
3.  O destino chama a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) para extrair os dados dela.

A diferença entre a Área de Transferência e as transferências de dados do tipo "arrastar e soltar" está principalmente em como o ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) é transferido da origem para o destino.

### <a name="clipboard-data-transfers"></a>Transferências de dados da área de transferência

A Área de Transferência é a maneira mais simples de transferir dados do Shell. O procedimento básico é semelhante às transferências de dados padrão da Área de Transferência. No entanto, como você está transferindo um ponteiro para um objeto de dados, não para os dados em si, você deve usar a API de área de transferência OLE em vez da API de área de transferência padrão. O procedimento a seguir descreve como usar a API da área de transferência OLE para transferir dados do Shell com a Área de Transferência:

1.  A fonte de dados cria um objeto de dados para conter os dados.
2.  A fonte de dados [**chama OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard), que coloca um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados na Área de Transferência.
3.  O destino chama [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) para recuperar o ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados.
4.  O destino extrai os dados chamando o [**método IDataObject::GetData.**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)
5.  Com algumas transferências de dados do Shell, o destino também pode precisar chamar o método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados para fornecer comentários ao objeto de dados sobre o resultado da transferência de dados. Consulte [Tratamento de operações de movimentação otimizadas](datascenarios.md) para ver um exemplo desse tipo de operação.

### <a name="drag-and-drop-data-transfers"></a>Transferências de dados do arrastar e soltar

Embora seja um pouco mais complexa de implementar, a transferência de dados do tipo "arrastar e soltar" tem algumas vantagens significativas em relação à Área de Transferência:

-   Transferências do tipo "arrastar e soltar" podem ser feitas com um movimento simples do mouse, tornando a operação mais flexível e intuitiva de usar do que a Área de Transferência.
-   O tipo "arrastar e soltar" fornece ao usuário uma representação visual da operação. O usuário pode seguir o ícone conforme ele se move da origem para o destino.
-   O arrastar e soltar notifica o destino quando os dados estão disponíveis.

As operações do tipo "arrastar e soltar" também usam objetos de dados para transferir dados. No entanto, a fonte de soltar deve fornecer funcionalidade além da necessária para transferências da Área de Transferência:

-   A origem de soltar também deve criar um objeto que expõe uma interface [**IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) O sistema usa **IDropSource para** se comunicar com a origem enquanto a operação está em andamento.
-   O objeto de dados do tipo "arrastar e soltar" é responsável por acompanhar a movimentação do cursor e exibir um ícone para representar o objeto de dados.

Os destinos de soltar também devem fornecer mais funcionalidade do que o necessário para lidar com transferências da Área de Transferência:

-   O destino de soltar deve expor uma interface [**IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) Quando o cursor está sobre uma janela de destino, o sistema usa **IDropTarget** para fornecer ao destino informações como a posição do cursor e notificá-lo quando os dados são descartados.
-   O destino de soltar deve registrar-se no sistema chamando [**RegisterDragDrop.**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) Essa função fornece ao sistema o handle para uma janela de destino e um ponteiro para a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) do aplicativo de destino.

> [!Note]  
> Para operações do tipo "arrastar e soltar", seu aplicativo deve inicializar COM com [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize), não [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

O procedimento a seguir descreve as etapas essenciais que normalmente são usadas para transferir dados do Shell com o "arrastar e soltar":

1.  O destino chama [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) para dar ao sistema um ponteiro para sua interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e registrar uma janela como um destino de soltar.
2.  Quando o usuário inicia uma operação do tipo "arrastar e soltar", a origem cria um objeto de dados e inicia um *loop de arrastar* chamando [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Quando o cursor está sobre a janela de destino, o sistema notifica o destino chamando um dos métodos [**IDropTarget do**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) destino. O sistema chama [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando o cursor entra na janela de destino e [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) conforme o cursor passa pela janela de destino. Ambos os métodos fornecem o destino de soltar com a posição atual do cursor e o estado das teclas modificadora de teclado, como CTRL ou ALT. Quando o cursor sai da janela de destino, o sistema notifica o destino chamando [**IDropTarget::D ragLeave.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) Quando qualquer um desses métodos retornar, o sistema chamará a interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) para passar o valor de retorno para a origem.
4.  Quando o usuário libera o botão do mouse para soltar os dados, o sistema chama o método [**IDropTarget::D rop do**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) destino. Entre os parâmetros do método está um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) do objeto de dados.
5.  O destino chama o método [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) do objeto de dados para extrair os dados.
6.  Com algumas transferências de dados do Shell, o destino também pode precisar chamar o método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) do objeto de dados para fornecer comentários à fonte sobre o resultado da transferência de dados.
7.  Quando o destino é concluído com o objeto de dados, ele retorna de [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop). O sistema retorna a chamada [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) da origem para notificar a origem de que a transferência de dados foi concluída.
8.  Dependendo do cenário de transferência de dados [específico,](datascenarios.md)a origem pode precisar tomar medidas adicionais com base no valor retornado por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) e nos valores passados para o objeto de dados pelo destino. Por exemplo, quando um arquivo é movido, a origem deve verificar esses valores para determinar se ele deve excluir o arquivo original.
9.  A origem libera o objeto de dados.

Embora os procedimentos descritos acima forneçam um bom modelo geral para transferência de dados do Shell, há muitos tipos diferentes de dados que podem estar contidos em um objeto de dados do Shell. Também há vários cenários de transferência de dados diferentes que seu aplicativo pode precisar lidar. Cada tipo de dados e cenário exigem uma abordagem um pouco diferente para três etapas principais no procedimento:

-   Como uma origem constrói um objeto de dados para conter os dados do Shell.
-   Como um destino extrai dados do Shell do objeto de dados.
-   Como a origem conclui a operação de transferência de dados.

O [Objeto de Dados do Shell](dataobject.md) fornece uma discussão geral sobre como uma fonte constrói um objeto de dados do Shell e como esse objeto de dados pode ser tratado pelo destino. [Lidar com cenários de transferência de](datascenarios.md) dados do Shell discute detalhadamente como lidar com vários cenários comuns de transferência de dados do Shell.

 

 
