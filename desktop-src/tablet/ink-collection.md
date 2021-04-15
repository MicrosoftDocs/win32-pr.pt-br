---
description: A coleta de tinta começa com o digitalizador.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Coleta de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fcd5bf0d73f48e63366843c85c9d6dd7cd388f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501407"
---
# <a name="ink-collection"></a>Coleta de tinta

A coleta de tinta começa com o digitalizador. Um usuário coloca uma caneta no digitalizador e começa a escrever. Você pode usar os recursos da coleção de tinta da API para gerenciar a coleta de dados de tinta que "flui" da caneta. Você tem acesso a informações sobre o hardware disponível no Tablet PC por meio da coleção [**tablets**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) e do objeto [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Em seguida, você usa o objeto [**InkCollector**](inkcollector-class.md) para obter os dados provenientes do digitalizador.

## <a name="tablets-and-the-tablet-object"></a>Tablets e o objeto do Tablet

Um [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) representa um dispositivo digitalizador do Tablet PC. Um Tablet PC pode ter mais de um digitalizador. Usando o objeto **Tablet** , você pode consultar os dispositivos digitalizadores disponíveis que estão conectados ao Tablet PC e seus respectivos recursos de hardware. Por exemplo, você pode determinar se o **Tablet** com o qual você está trabalhando está integrado à exibição ou é um dispositivo externo separado.

## <a name="inkcollector-object"></a>Objeto InkCollector

O objeto [**InkCollector**](inkcollector-class.md) captura a entrada de tinta de dispositivos [**tablets**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) disponíveis. O objeto **InkCollector** só coleta tinta e gestos que são inseridos em uma janela específica. Um coletor de eventos muito eficiente renderiza essa entrada em tempo real. O objeto **InkCollector** captura a entrada e a direciona para um objeto [**Ink**](inkdisp-class.md) .

> [!Note]  
> O layout simultâneo da tinta com várias canetas pode ou não funcionar, dependendo dos recursos de hardware do dispositivo digitalizador.

 

### <a name="how-the-ink-collector-works"></a>Como funciona o coletor de tinta

O objeto [**InkCollector**](inkcollector-class.md) se anexa a uma janela de aplicativo conhecida. Em seguida, ele permite que os usuários empreguem qualquer dispositivo de Tablet PC disponível (incluindo o mouse) para dispor a tinta em tempo real nessa janela. Os traços de tinta coletados são armazenados em um objeto de [**tinta**](inkdisp-class.md) associado. Esses traços podem ser manipulados ou enviados a um reconhecedor para reconhecimento. O objeto **InkCollector** também notifica o aplicativo quando um cursor chega ao intervalo de qualquer um dos dispositivos do Tablet PC que estão sendo usados.

Para que o objeto [**InkCollector**](inkcollector-class.md) defina com precisão o cursor do mouse em uma janela habilitada para tinta, essa janela deve ser capaz de receber a mensagem **\_ SetCursor do WM** . Isso é bem-sucedido para todas as janelas regulares, mas, para um controle dentro de uma caixa de diálogo, o pai de diálogo do controle filtra essa mensagem. Para que o controle receba a mensagem, defina o estilo de **\_ notificação SS** .

## <a name="inkoverlay-object"></a>Objeto InkOverlay

O objeto [**InkCollector**](inkcollector-class.md) , discutido anteriormente, é útil para que os aplicativos forneçam seu próprio modelo para seleção, apagamento e outra interação do usuário. O objeto [**InkOverlay**](inkoverlay-class.md) é um superconjunto do objeto **InkCollector** que fornece suporte à edição. Isso é útil para que os aplicativos integrem o desenho e a edição de tinta em sua própria tela do documento usando um conjunto de modelos de seleção de tinta padrão que o objeto fornece.

O objeto [**InkCollector**](inkcollector-class.md) e o objeto [**InkOverlay**](inkoverlay-class.md) (bem como o controle [InkPicture](inkpicture-control.md) ) usam construções comuns, como o objeto [**Ink**](inkdisp-class.md) e a coleção [**DrawingAttributes**](inkdrawingattributes-class.md) , para que a maneira básica de alterar a cor da tinta seja a mesma em todos os lugares. Isso permite que você reutilize o código e tenha acesso programático comum, o que pode ser particularmente importante se você oferecer suporte a scripts em seu aplicativo.

[**InkOverlay**](inkoverlay-class.md) é um objeto com que é útil para cenários de anotação nos quais os usuários não se preocupam com a execução de reconhecimento na tinta, mas, em vez disso, estão interessados no tamanho, na forma, na cor e na posição da tinta. Ele é adequado para fazer anotações e scribbling básicos. A interface do usuário padrão é um retângulo transparente com tinta opaca.

[**InkOverlay**](inkoverlay-class.md) estende a classe [**InkCollector**](inkcollector-class.md) de três maneiras:

-   Ele gera eventos para alterações de atributo de tinta e de traço inicial.
-   Ele permite que os usuários selecionem, apaguem e redimensionem tinta.
-   Ele dá suporte a comandos Recortar, copiar e colar.

Um cenário típico no qual [**InkOverlay**](inkoverlay-class.md) é útil é marcar um slide ou imagem de apresentação. O objeto **InkOverlay** permite uma implementação fácil dos recursos de tinta e de layout que esse cenário requer.

Para trabalhar com [**InkOverlay**](inkoverlay-class.md), você:

1.  Crie uma instância de um objeto [**InkOverlay**](inkoverlay-class.md) .
2.  Anexe o hWnd (identificador, no código gerenciado) de uma janela à propriedade [**HWND**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) do objeto [**InkOverlay**](inkoverlay-class.md) (propriedade [Handle](/previous-versions/ms582171(v=vs.100)) , no código gerenciado).
3.  Defina a propriedade [**habilitada**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) do objeto [**InkOverlay**](inkoverlay-class.md) como **true**.

O objeto [**InkOverlay**](inkoverlay-class.md) inclui suporte de impressão básica, mas você deve implementar a visualização de impressão ou outros recursos de impressão avançados.

[**InkOverlay**](inkoverlay-class.md) mantém a tinta no formato serializado da tinta (ISF).

> [!Note]  
> Se o [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) do objeto [**InkOverlay**](inkoverlay-class.md) for definido como **delete** ou **Select**, outros eventos (como [**InkAdded**](inkdisp-inkadded.md), [**InkDeleted**](inkdisp-inkdeleted.md)e [**Stroke**](inkoverlay-stroke.md)) serão disparados. Esses eventos serão úteis se você quiser implementar seus próprios modos de exclusão ou de seleção.

 

### <a name="selecting-ink"></a>Selecionando tinta

O objeto [**InkOverlay**](inkoverlay-class.md) permite que os usuários usem uma ferramenta de laço para selecionar objetos de tinta que estão contidos em uma região rastreada. Os usuários também podem selecionar tinta tocando em qualquer objeto de [**tinta**](inkdisp-class.md) .

Use a propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) para retornar uma coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que você pode usar para manipular a seleção de um usuário.

Quando um objeto de [**tinta**](inkdisp-class.md) ou um conjunto de objetos de **tinta** é selecionado, os identificadores de dimensionamento aparecem nos quatro cantos da caixa delimitadora da tinta e em todos os pontos médios entre os cantos adjacentes. Se o usuário arrastar qualquer lugar dentro da região selecionada, a tinta se tornará móvel dentro do controle.

### <a name="default-behavior"></a>Comportamento padrão

O objeto [**InkOverlay**](inkoverlay-class.md) é definido para coletar tinta por padrão. A tinta é de 53 unidades de espaço de tinta de largura (em que 1 unidade de espaço de tinta = 1 HIMETRIC). A tinta ficará preta se o usuário não estiver sendo executado no modo de alto contraste. Caso contrário, Ink será definido como o valor de **\_ WINDOWTEXT de cor** (**WINDOWTEXT** no código gerenciado). [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) é **false**.

### <a name="cursor-and-button-objects"></a>Objetos cursor e Button

Um cursor corresponde à ponta da caneta usada no Tablet PC. Por exemplo, um lápis tem duas extremidades. Normalmente, uma extremidade é usada para gravação e a outra é usada para apagar. Essas duas extremidades correspondem a dois cursores. A classe de [**cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) não é confundida com [**System. Windows. Forms. cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

No Tablet PC, um cursor geralmente é definido para ser usado para gravação ou apagamento. Um cursor pode potencialmente alterar funções se o aplicativo habilitar essa funcionalidade. Alguns dispositivos do Tablet PC permitem várias canetas. Cada cursor tem uma ID de cursor associada que é exclusiva no sistema. Um cursor pode ter zero ou mais botões associados. Esses botões são fornecidos ao aplicativo como objetos CursorButton. O aplicativo pode fornecer um objeto [**DrawingAttributes**](inkdrawingattributes-class.md) específico para qualquer cursor em questão.

### <a name="drawing-attributes-object"></a>Objeto de atributos de desenho

Um objeto [**DrawingAttributes**](inkdrawingattributes-class.md) descreve como qualquer conjunto conhecido de tinta deve ser desenhado. Um objeto **DrawingAttributes** inclui propriedades básicas, como [**Color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color), [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)e [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip). Ele também pode abranger parâmetros avançados, como transparência variável e suavização de Bézier, que pode fornecer efeitos interessantes ou melhorar a legibilidade da tinta.

### <a name="peninputpanel-object"></a>Objeto PenInputPanel

> [!Note]  
> A classe [**PenInputPanel**](peninputpanel-class.md) foi preterida. A classe **PenInputPanel** foi substituída pela classe [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .

 

O objeto [**PenInputPanel**](peninputpanel-class.md) permite que você adicione facilmente entrada de caneta in-loco aos seus aplicativos. O **PenInputPanel** está disponível como um objeto anexável que permite adicionar funcionalidade do painel de entrada do Tablet PC a controles existentes. A interface do usuário é amplamente exigida pelo idioma de entrada atual. Você tem a opção de escolher o método de entrada padrão para o **PenInputPanel**, manuscrito ou teclado. O usuário final pode alternar entre os métodos de entrada usando os botões na interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe InkCollector (C++)**](inkcollector-class.md)
</dt> <dt>

[**Classe InkOverlay (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Namespace Microsoft. Ink**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
