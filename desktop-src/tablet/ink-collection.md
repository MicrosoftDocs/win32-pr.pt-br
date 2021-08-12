---
description: A coleção de tintas começa com o digitalizador.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Coleção de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45988ea93aac5016391e22c352b9d0123a5e122f4a79c55e41e06834ed040e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452060"
---
# <a name="ink-collection"></a>Coleção de tinta

A coleção de tintas começa com o digitalizador. Um usuário coloca uma caneta no digitalizador e começa a gravar. Você pode usar os recursos de coleção de tinta da API para gerenciar a coleção de dados de tinta que "flui" da caneta. Você tem acesso às informações sobre o hardware disponível no Tablet PC por meio da coleção [**Tablets**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) e do [**objeto Tablet.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) Em seguida, use [**o objeto InkCollector**](inkcollector-class.md) para obter os dados que vêm do digitalizador.

## <a name="tablets-and-the-tablet-object"></a>Tablets e o objeto Tablet

Um [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) representa um dispositivo digitalizador do Tablet PC. Um tablet pc pode ter mais de um digitalizador. Usando o **objeto Tablet,** você pode consultar os dispositivos de digitalizador disponíveis que estão anexados ao Tablet PC e suas respectivas funcionalidades de hardware. Por exemplo, você pode determinar se o **Tablet com** o qual você está trabalhando está integrado à exibição ou se é um dispositivo externo separado.

## <a name="inkcollector-object"></a>Objeto InkCollector

O [**objeto InkCollector**](inkcollector-class.md) captura a entrada de tinta de dispositivos [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) disponíveis. O **objeto InkCollector** coleta apenas tinta e gestos que são entrada em uma janela específica. Um sink de evento muito eficiente renderiza essa entrada em tempo real. O **objeto InkCollector** captura a entrada e a direciona para um [**objeto Ink.**](inkdisp-class.md)

> [!Note]  
> A colocação simultânea de tinta com várias canetas pode ou não funcionar, dependendo das funcionalidades de hardware do dispositivo digitalizador.

 

### <a name="how-the-ink-collector-works"></a>Como funciona o coletor de tinta

O [**objeto InkCollector**](inkcollector-class.md) se anexa a uma janela de aplicativo conhecida. Em seguida, ele permite que os usuários empresem qualquer dispositivo tablet disponível (incluindo o mouse) para colocar tinta em tempo real nessa janela. Os traços de tinta que ele coleta são armazenados em um objeto [**Ink**](inkdisp-class.md) associado. Esses traços podem ser manipulados ou enviados a um reconhecedor para reconhecimento. O **objeto InkCollector** também notifica o aplicativo quando um cursor entra no intervalo de qualquer um dos dispositivos tablet pc que estão sendo usados.

Para o [**objeto InkCollector**](inkcollector-class.md) definir com precisão o cursor do mouse em uma janela habilitada para tinta, essa janela deve ser capaz de receber a mensagem **WM \_ SETCURSOR.** Isso é bem-sucedido para todas as janelas regulares, mas, para um controle dentro de uma caixa de diálogo, o pai da caixa de diálogo do controle filtra essa mensagem. Para que o controle receba a mensagem, de definido o **estilo \_ NOTIFICAÇÃO do SS.**

## <a name="inkoverlay-object"></a>Objeto InkOverlay

O [**objeto InkCollector,**](inkcollector-class.md) discutido anteriormente, é útil para que os aplicativos forneçam seu próprio modelo para selecionar, apagar e outras interações do usuário. O [**objeto InkOverlay**](inkoverlay-class.md) é um superconjunto do **objeto InkCollector** que dá suporte à edição. Isso é útil para que os aplicativos integrem o desenho à tinta e a edição em suas próprias telas de documento usando um conjunto de modelos de seleção de tinta padrão que o objeto fornece.

O objeto [**InkCollector**](inkcollector-class.md) e o objeto [**InkOverlay**](inkoverlay-class.md) (bem como o controle [InkPicture)](inkpicture-control.md) usam constructos comuns, como o objeto [**Ink**](inkdisp-class.md) e a coleção [**DrawingAttributes,**](inkdrawingattributes-class.md) para que a maneira básica de alterar a cor da tinta seja a mesma em todos os lugares. Isso permite que você reutilizar o código e ter acesso programático comum, o que pode ser particularmente importante se você oferecer suporte a scripts em seu aplicativo.

[**InkOverlay**](inkoverlay-class.md) é um objeto COM que é útil para cenários de anotação em que os usuários não estão preocupados com a execução de reconhecimento na tinta, mas, em vez disso, estão interessados no tamanho, forma, cor e posição da tinta. Ele é adequado para fazer anotações e rabiscos básicos. A interface do usuário padrão é um retângulo transparente com tinta opaca.

[**InkOverlay**](inkoverlay-class.md) estende a [**classe InkCollector**](inkcollector-class.md) de três maneiras:

-   Ele gera eventos para alterações de atributo begin-stroke, end-stroke e ink.
-   Ele permite que os usuários selecionem, apaguem e reizem tinta.
-   Ele dá suporte aos comandos Recortar, Copiar e Colar.

Um cenário típico no qual [**InkOverlay**](inkoverlay-class.md) é útil é marcar um slide ou uma imagem de apresentação. O **objeto InkOverlay** permite a implementação fácil das funcionalidades de tinta e layout que esse cenário requer.

Para trabalhar com [**o InkOverlay,**](inkoverlay-class.md)você:

1.  Insinue um [**objeto InkOverlay.**](inkoverlay-class.md)
2.  Anexe o hWnd (identificador, no código gerenciado) de uma janela à propriedade [**hWnd**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) do objeto [**InkOverlay**](inkoverlay-class.md) ( propriedade [Handle,](/previous-versions/ms582171(v=vs.100)) em código gerenciado).
3.  De definir a propriedade [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) do objeto [**InkOverlay**](inkoverlay-class.md) como **TRUE.**

O [**objeto InkOverlay inclui**](inkoverlay-class.md) suporte básico à impressão, mas você deve implementar a visualização de impressão ou outros recursos avançados de impressão.

[**InkOverlay**](inkoverlay-class.md) persiste tinta em formato serializado de tinta (ISF).

> [!Note]  
> Se  o [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) do objeto [**InkOverlay**](inkoverlay-class.md) estiver definido como Excluir ou Selecionar **,** outros eventos (como [**InkAdded,**](inkdisp-inkadded.md) [**InkDeleted**](inkdisp-inkdeleted.md)e [**Stroke)**](inkoverlay-stroke.md)serão disparados. Esses eventos serão úteis se você quiser implementar seus próprios modos de exclusão ou seleção.

 

### <a name="selecting-ink"></a>Selecionando Tinta

O [**objeto InkOverlay**](inkoverlay-class.md) permite que os usuários usem uma ferramenta de laço para selecionar objetos de tinta contidos em uma região rastreada. Os usuários também podem selecionar tinta tocando em qualquer [**objeto Ink.**](inkdisp-class.md)

Use a [**propriedade Seleção**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) para retornar uma coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que você pode usar para manipular a seleção de um usuário.

Quando um [**objeto Ink**](inkdisp-class.md) ou um conjunto de objetos **Ink** é selecionado, as alças de redução aparecem nos quatro cantos da caixa delimitada da tinta e em todos os pontos médios entre cantos adjacentes. Se o usuário arrastar em qualquer lugar dentro da região selecionada, a tinta se tornará móvel dentro do controle .

### <a name="default-behavior"></a>Comportamento padrão

O [**objeto InkOverlay**](inkoverlay-class.md) é definido para coletar tinta por padrão. A tinta tem 53 unidades de espaço em tinta (em que 1 unidade de espaço em tinta = 1 HIMETRIC). A tinta será preta se o usuário não estiver em execução no modo de alto contraste. Caso contrário, ink será definido como o **valor COLOR \_ WINDOWTEXT** (**WindowText** no código gerenciado). [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) é **FALSE.**

### <a name="cursor-and-button-objects"></a>Objetos de cursor e botão

Um cursor corresponde à dica da caneta usada no Tablet PC. Por exemplo, um lápis tem duas extremidades. Normalmente, uma extremidade é usada para escrita e a outra é usada para apagar. Essas duas extremidades correspondem a dois cursores. A [**classe Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) não é confundido com [**System.Windows. Forms.Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

No Tablet PC, um cursor geralmente é definido para ser usado para escrever ou apagar. Um cursor pode potencialmente alterar funções se o aplicativo habilitar essa funcionalidade. Alguns dispositivos Tablet PC permitem várias canetas. Cada cursor tem uma ID de cursor associada que é exclusiva no sistema. Um cursor pode ter zero ou mais botões associados. Esses botões são fornecidos ao aplicativo como objetos CursorButton. O aplicativo pode fornecer um objeto [**DrawingAttributes**](inkdrawingattributes-class.md) específico para qualquer cursor específico.

### <a name="drawing-attributes-object"></a>Objeto Drawing Attributes

Um [**objeto DrawingAttributes**](inkdrawingattributes-class.md) descreve como qualquer conjunto conhecido de tinta deve ser desenhado. Um **objeto DrawingAttributes** inclui propriedades básicas, como [**Color,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color) [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)e [**PenTip.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip) Ele também pode abranger parâmetros avançados, como transparência variável e suavização de Bezier, que podem fornecer efeitos interessantes ou melhorar a facilitar a leitura da tinta.

### <a name="peninputpanel-object"></a>Objeto PenInputPanel

> [!Note]  
> A [**classe PenInputPanel**](peninputpanel-class.md) foi preterida. A **classe PenInputPanel** foi substituída pela [**classe TextInputPanel.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)

 

O [**objeto PenInputPanel**](peninputpanel-class.md) permite que você adicione facilmente entrada de caneta in-loque aos seus aplicativos. O **PenInputPanel** está disponível como um objeto anexável que permite adicionar a funcionalidade do Painel de Entrada do Tablet PC aos controles existentes. A interface do usuário é amplamente ordenada pela linguagem de entrada atual. Você tem a opção de escolher o método de entrada padrão **para o PenInputPanel**, manuscrito ou teclado. O usuário final pode alternar entre métodos de entrada usando botões na interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe InkCollector (C++)**](inkcollector-class.md)
</dt> <dt>

[**Classe InkOverlay (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Microsoft.Ink Namespace**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
