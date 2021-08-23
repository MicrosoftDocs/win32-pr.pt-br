---
description: Para auxiliar o suporte de tinta em aplicativos, há dois objetos, que podem ser inseridos e têm suporte de qualquer contêiner OLE.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: Objetos sInk e tInk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e25e1f258ac789382475666878c986f5053323a1b19bf8f4b6110c096f2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091286"
---
# <a name="sink-and-tink-objects"></a>Objetos sInk e tInk

Para auxiliar o suporte de tinta em aplicativos, há dois objetos, que podem ser inseridos e têm suporte de qualquer contêiner OLE. Eles são produzidos chamando o método **Ink.ClipboardCopy (Rectangle, InkClipboardFormats, InkClipboardModes)** ou o método **Ink.ClipboardCopy (Strokes, InkClipboardFormats, InkClipboardModes)** e são:

-   Objeto de tinta de texto (tInk). Esse é um objeto OLE que representa tinta que deve formar palavras. Um objeto tInk permite que a tinta manuscrita seja convertida em texto, seja como o texto retornado por um reconhecedor ou a escolha tomada de uma lista de alternativas de reconhecimento. A cor e o tamanho da tinta podem ser definidos programaticamente e podem ser baseados nos atributos do texto em torno do objeto. O objeto tInk destina-se a conter uma única palavra. O objeto tInk é um objeto pequeno e leve que pode executar operações simples, como renderização (dado um identificador para um HDC (contexto de dispositivo) e um RECT) e persistir a si mesmo (dado um fluxo). O uso de um objeto tInk permite uma experiência perfeita do usuário ao trabalhar em um aplicativo que usa a entrada de manuscrito e texto.
-   Objeto de tinta de esboço (sInk). Esse é um objeto OLE que representa tinta que não deve formar palavras. Um objeto sInk é interpretado como um desenho. Um objeto sInk também é útil para representar várias palavras.

Esses objetos podem ser usados para interoperabilidade entre aplicativos, colocando-os no slot de objeto OLE na Área de Transferência ou incorporando-os no RTF (Rich Text Format).

Você pode usar objetos tInk e sInk das seguintes maneiras:

-   Os objetos tInk e sInk têm suporte no Microsoft Word 2002. Os usuários podem inserir tinta em um documento do Word usando os painéis de entrada de texto de escrita e desenho fornecidos no Word 2002. Essa tinta é inserida no arquivo do Word como um objeto OLE com o CLSID do objeto sInk ou tInk.
-   O controle [InkEdit](/previous-versions/ms552265(v=vs.100)) do tablet faz uso do objeto tInk. O controle InkEdit é uma subclasse do controle [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) padrão. A tinta é inserida no fluxo RTF do controle InkEdit como um objeto tInk.
-   Quando um aplicativo move um objeto [Ink](/previous-versions/aa515768(v=msdn.10)) selecionado para a Área de Transferência, o slot da Área de Transferência do objeto OLE contém um objeto OLE tInk ou sInk.

Por exemplo, seu aplicativo pode reconhecer manuscrito e marcar qualquer [objeto Ink](/previous-versions/aa515768(v=msdn.10)) como um objeto tInk. Em seguida, se você selecionar uma palavra em tinta e copiar e colar no Word, as alternativas para essa palavra serão mostradas no Word 2002.

> [!Note]  
> O suporte à Área de Transferência da Plataforma de Tablet PC seleciona automaticamente o sinalizador EMF (Metadado Avançado) para você quando você coloca um objeto sInk ou tInk na Área de Transferência como um objeto OLE. O próprio objeto é armazenado na Área de Transferência nos slots de descritor de origem e objeto de inserir.

 

Como outro exemplo, usando o objeto sInk, você pode desenhar um esboço de tinta em um aplicativo, copiar e colar o esboço no Word 2002 e editar o desenho usando o Painel de Entrada do Tablet PC no Word.

Para conter com êxito objetos tInk, um aplicativo deve implementar o suporte de contêiner OLE para objetos inseridos. Em seguida, para fazer com que o contêiner tenha suporte total para tInk, você deve institur:

-   Modificações no código para Encontrar e Substituir. Em vez de ignorar objetos inseridos na pesquisa, esses objetos devem ser interrogados quanto ao tipo. Se eles são um objeto tInk, eles devem ser instautados e consultados quanto ao texto correspondente.
-   Modificações no comportamento de seleção. A seleção de objetos tInk nunca deve aparecer com alças de escala. Eles devem ser selecionados da mesma maneira que o texto é selecionado no documento. O código de seleção para objetos deve detectar se o tipo é tInk e exibir a seleção adequadamente.
-   Uso de propriedades de ambiente. Propriedades de ambiente, como tamanho da fonte, cor e formatação em negrito, precisam ser transmitidas para o objeto tInk. A aplicação dessas propriedades altera a largura da tinta manuscrita, portanto, uma atualização de tamanho é necessária chamando o método [**GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) ou [o método IOleObject::GetExtent.](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent)
-   Substitua o processamento [do método IOleObject::D oVerb](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) padrão. Isso permite que a conversão em texto passe um lote de objetos tInk para o reconhecedor, o que pode, em seguida, quebrar as palavras em segmentos de reconhecimento.

Para obter mais informações sobre como quebrar palavras em segmentos de reconhecimento, consulte [Segmentos de reconhecimento](recognition-segments.md).

 

 
