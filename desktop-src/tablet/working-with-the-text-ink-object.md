---
description: Para auxiliar o suporte à tinta em aplicativos, há dois objetos, os quais podem ser incorporados e têm suporte de qualquer contêiner OLE, do objeto de tinta de texto (tInk) e do objeto de tinta do esboço (coletor).
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Trabalhando com o objeto de tinta de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082323f7e67e76f7ae39c6b592a86f2be0945a86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763209"
---
# <a name="working-with-the-text-ink-object"></a>Trabalhando com o objeto de tinta de texto

Para auxiliar o suporte à tinta em aplicativos, há dois objetos, os quais podem ser incorporados e têm suporte de qualquer contêiner OLE, do objeto de tinta de texto (tInk) e do objeto de tinta do esboço (coletor).

O objeto de tinta de texto é um objeto OLE que representa a tinta que deve formar palavras. Um objeto de tinta de texto permite que a tinta manuscrita seja convertida em texto, escolhendo em uma lista de alternativas. A cor e o tamanho do objeto de tinta de texto podem ser definidos programaticamente e podem ser baseados nos atributos do texto em volta do objeto. O objeto de tinta de texto deve conter uma única palavra.

O objeto de tinta de texto dá suporte ao conjunto padrão de interfaces OLE necessárias para inserção e suporte à área de transferência. A interface [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) lê e grava em um fluxo no formato serializado da tinta (ISF). O objeto de tinta de texto fornece a interface [**IInkLineInfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) para acessar suas propriedades de exibição e a lista de resultados de reconhecimento.

O objeto de tinta de texto pode ser usado para interoperabilidade entre aplicativos, colocando-o no slot do objeto OLE na área de transferência, inserindo-o em RTF ou mantendo-o em um fluxo ISF.

Um objeto de tinta de texto pode ser gerado das seguintes maneiras.

-   O controle [InkEdit](inkedit-control-reference.md) usa o objeto de tinta de texto. A funcionalidade do controle InkEdit é um superconjunto da funcionalidade de controle RichEdit padrão. A tinta é inserida no fluxo RTF do controle InkEdit como um objeto de tinta de texto.
-   Quando um aplicativo copia um objeto [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ou [InkEdit](inkedit-control-reference.md) na área de transferência e o formato de [**Enumeração InkClipboardFormats**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) é definido, o slot de área de transferência do objeto OLE contém um objeto OLE de tinta de texto.
-   O painel de entrada do Tablet PC pode gerar objetos de tinta de texto.

Por exemplo, seu aplicativo pode reconhecer manuscrito e adicionar o resultado de reconhecimento aos traços. Em seguida, se você copiar e colar os traços no Microsoft Word como um objeto de tinta de texto, as alternativas para essa palavra estarão disponíveis no Word 2003 e em versões posteriores.

Para conter com êxito objetos de tinta de texto, um aplicativo deve implementar o suporte a contêiner OLE para objetos inseridos. Em seguida, para tornar o contêiner totalmente compatível com a tinta de texto, você deve instituir:

-   Modificações no aplicativo para localizar e substituir. Em vez de ignorar objetos inseridos na pesquisa, esses objetos devem ser interrogados para o tipo. Se eles forem um objeto de tinta de texto, eles deverão ser instanciados e consultados para seu texto correspondente.
-   Modificações no comportamento de seleção. A seleção de objetos de tinta de texto nunca deve aparecer com alças de dimensionamento. Eles devem ser selecionados da mesma maneira que o texto é selecionado no documento. O código de seleção para objetos deve detectar se o tipo é tinta de texto e exibir a seleção adequadamente.
-   Uso de propriedades de ambiente. As propriedades de ambiente, como tamanho da fonte, cor e formatação em negrito, precisam ser transmitidas para o objeto de tinta de texto. A aplicação dessas propriedades altera a largura da tinta manuscrita, portanto, uma atualização de tamanho é necessária chamando o método [**IInkLineInfo:: GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) ou [**IOleObject::**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) getestende.

## <a name="in-this-section"></a>Nesta seção

-   [Convertendo um objeto de tinta de texto em tinta](converting-a-text-ink-object-to-ink.md)
-   [APIs de tinta de texto](text-ink-apis.md)
-   [Objetos sInk e tInk](sink-and-tink-objects.md)

 

 
