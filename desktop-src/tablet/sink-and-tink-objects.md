---
description: Para auxiliar o suporte à tinta em aplicativos, há dois objetos, os quais podem ser incorporados e têm suporte de qualquer contêiner OLE.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: Objetos sInk e tInk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef7ed1c06d256fe8eda9fad4bf15afa19fcb833
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754282"
---
# <a name="sink-and-tink-objects"></a>Objetos sInk e tInk

Para auxiliar o suporte à tinta em aplicativos, há dois objetos, os quais podem ser incorporados e têm suporte de qualquer contêiner OLE. Eles são produzidos chamando o método **Ink. ClipboardCopy (Rectangle, InkClipboardFormats, InkClipboardModes)** ou o método **Ink. ClipboardCopy (traços, InkClipboardFormats, InkClipboardModes)** e são:

-   Objeto de tinta de texto (tInk). Este é um objeto OLE que representa a tinta que deve formar palavras. Um objeto tInk permite que a tinta manuscrita seja convertida em texto, seja como o texto retornado por um reconhecedor ou a escolha feita em uma lista de alternativas de reconhecimento. A cor e o tamanho da tinta podem ser definidos programaticamente e podem ser baseados nos atributos do texto em volta do objeto. O objeto tInk deve conter uma única palavra. O objeto tInk é um objeto pequeno e leve que pode executar operações simples como renderização (dado um identificador a um contexto de dispositivo (HDC) e um RECT) e persistindo em si (dado um fluxo). O uso de um objeto tInk permite uma experiência de usuário direta ao trabalhar em um aplicativo que usa a entrada de manuscrito e de texto.
-   Objeto de tinta do esboço (coletor). Este é um objeto OLE que representa a tinta que não é esperada para formar palavras. Um objeto de coletor é interpretado como um desenho. Um objeto sInk também é útil para representar várias palavras.

Esses objetos podem ser usados para interoperabilidade entre aplicativos, seja colocando-os no slot do objeto OLE na área de transferência ou inserindo-os no formato RTF (Rich Text Format).

Você pode usar os objetos tInk e sInk das seguintes maneiras:

-   Os objetos tInk e sInk têm suporte no Microsoft Word 2002. Os usuários podem inserir tinta em um documento do Word usando os painéis de entrada de texto de escrita e desenho fornecidos no Word 2002. Essa tinta é inserida no arquivo do Word como um objeto OLE com o CLSID do objeto sInk ou tInk.
-   O controle [InkEdit](/previous-versions/ms552265(v=vs.100)) do Tablet PC usa o objeto Tink. O controle InkEdit é uma subclasse do controle [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) padrão. A tinta é inserida no fluxo RTF do controle InkEdit como um objeto tInk.
-   Quando um aplicativo move um objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) selecionado para a área de transferência, o slot de área de transferência do objeto OLE contém um objeto OLE TInk ou Sink.

Por exemplo, seu aplicativo pode reconhecer manuscrito e marcar qualquer objeto de [tinta](/previous-versions/aa515768(v=msdn.10)) como um objeto Tink. Em seguida, se você selecionar uma palavra em tinta e copiá-la e colá-la no Word, as alternativas para essa palavra serão mostradas no Word 2002.

> [!Note]  
> O suporte da área de transferência da plataforma do Tablet PC seleciona automaticamente o sinalizador Enhanced Metafile (EMF) para você quando você coloca um objeto sInk ou tInk na área de transferência como um objeto OLE. O próprio objeto é armazenado na área de transferência nos slots de fonte e descritor de objeto embed.

 

Como outro exemplo, usando o objeto sInk, você pode desenhar um esboço de tinta em um aplicativo, copiar e colar o esboço no Word 2002 e, em seguida, editar o desenho usando o painel de entrada do Tablet PC no Word.

Para conter com êxito objetos tInk, um aplicativo deve implementar o suporte a contêiner OLE para objetos inseridos. Em seguida, para tornar o contêiner totalmente compatível com o tInk, você deve instituir:

-   Modificações no código para localizar e substituir. Em vez de ignorar objetos inseridos na pesquisa, esses objetos devem ser interrogados para o tipo. Se eles forem um objeto tInk, eles deverão ser instanciados e consultados para seu texto correspondente.
-   Modificações no comportamento de seleção. A seleção de objetos tInk nunca deve aparecer com identificadores de dimensionamento. Eles devem ser selecionados da mesma maneira que o texto é selecionado no documento. O código de seleção para objetos deve detectar se o tipo é tInk e exibir a seleção adequadamente.
-   Uso de propriedades de ambiente. As propriedades de ambiente, como tamanho da fonte, cor e formatação em negrito, precisam ser transmitidas para o objeto tInk. A aplicação dessas propriedades altera a largura da tinta manuscrita, portanto, uma atualização de tamanho é necessária chamando o método [**GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) ou o método [IOleObject::](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) getestende.
-   Substitua o processamento do método [IOleObject::D overb](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) padrão. Isso permite que a conversão em texto passe um lote de objetos tInk para o reconhecedor, que pode então quebrar as palavras em segmentos de reconhecimento.

Para obter mais informações sobre a quebra de palavras em segmentos de reconhecimento, consulte [segmentos de reconhecimento](recognition-segments.md).

 

 
