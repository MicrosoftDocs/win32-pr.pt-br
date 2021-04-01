---
description: O exemplo de reconhecimento avançado demonstra os recursos avançados da API (interface de programação de aplicativo) do Microsoft Tablet PC Automation usada para o reconhecimento de manuscrito.
ms.assetid: 4c9b9f31-c317-43fd-8404-35295b41d093
title: Exemplo de reconhecimento avançado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e23a078ded9c6967f8e45780f8cb3a739b246f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646554"
---
# <a name="advanced-recognition-sample"></a>Exemplo de reconhecimento avançado

O exemplo de reconhecimento avançado demonstra os recursos avançados da API (interface de programação de aplicativo) do Microsoft Tablet PC Automation usada para o reconhecimento de manuscrito.

Ele contém os seguintes recursos:

-   Enumerando o reconhecedor instalado
-   Criando um contexto de reconhecedor com um idioma específico
-   Usando o objeto Recognizer
-   Definindo o facto de reconhecimento e as listas de palavras
-   Usando guias para melhorar a qualidade do reconhecimento
-   Reconhecimento dinâmico em segundo plano
-   Reconhecimento de gesto

As interfaces usadas são: [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer), **IInkRecoContext**, [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult), **IInkRecognitionGuide**, **IInkWordList**, [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture), **IInkCollector**, **IInkDisp**, **IInkRenderer**, **IInkDrawingAttributes**, **IInkStrokes** e **IInkStroke**.

## <a name="ink-and-project-headers"></a>Cabeçalhos de tinta e de projeto

Primeiro, inclua os cabeçalhos para interfaces de automação do Tablet PC. Eles são instalados com o SDK da plataforma Tablet PC. O arquivo TpcError. h contém as definições de código de erro da API do Tablet PC.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
#include <TpcError.h>
```



O arquivo EventSinks. h define as interfaces **IInkEventsImpl** e **IInkRecognitionEventsImpl** e configura os eventos [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md), [**Stroke**](inkcollector-stroke.md)e [**Gesture**](inkcollector-gesture.md) .


```C++
#include "EventSinks.h"
```



O arquivo ChildWnds. h contém as definições das classes **CInkInputWnd** e **CRecoOutputWnd**, que são derivadas do CWindowImpl da ATL e usadas para criar as janelas filho da amostra.


```C++
#include "ChildWnds.h"
```



O arquivo AdvReco. h declara a classe **CAdvRecoApp** , que é a classe de janela do aplicativo para este exemplo.


```C++
#include "AdvReco.h"
```



## <a name="initializing-the-application-window"></a>Inicializando a janela do aplicativo

O método da janela `Run` configura o objeto **CAdvRecoApp** , carrega o menu e o ícone da janela, cria um objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para o reconhecedor padrão e inicia o loop de mensagem da janela.

O método **OnCreate** da janela manipula o evento de **\_ criação do WM** e cria as janelas filhas. Um objeto [**InkCollector**](inkcollector-class.md) conecta-se à fonte do evento do coletor de tinta e habilita a entrada à tinta na janela de entrada. Em seguida, ele cria um objeto [**InkRecognizerGuide**](inkrecognizerguide-class.md) e usa a propriedade [**Renderer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer) do coletor de tinta para converter os retângulos da caixa do guia de reconhecimento em espaço de tinta. Por fim, o método **OnCreate** cria um objeto [**InkWordList**](inkwordlist-class.md) .

## <a name="handling-ink-collector-events"></a>Manipulando eventos do coletor de tinta

O método **onstroke** da janela manipula o evento de [**traço**](inkcollector-stroke.md) do coletor de tinta. O novo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) é adicionado à [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) do coletor de tinta.

O método **ongesto** da janela manipula o evento de [**gesto**](inkcollector-gesture.md) do coletor de tinta. O método **ongesto** identifica o gesto, usando o gesto de confiança mais alto primeiro e verifica se a janela dá suporte a esse gesto específico. Se houver suporte para o gesto, a caixa delimitadora do gesto será invalidada, pois o gesto será removido da coleção de traços. Se não houver suporte para o gesto, o evento de **gesto** será cancelado, o que faz com que o coletor de tinta gere um evento de [**traço**](inkcollector-stroke.md) . Por fim, a janela de resultados é atualizada.

## <a name="handling-recognizer-context-events"></a>Lidando com eventos de contexto do reconhecedor

O método **OnRecognitionWithAlternates** da janela manipula o evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) do contexto do reconhecedor. O método **OnRecognitionWithAlternates** exibe os resultados de reconhecimento na janela resultados.

## <a name="handling-menu-commands"></a>Manipulando comandos de menu

O método **Recognizer** da janela manipula os comandos no menu Recognizer. Se o comando **padrão** foi selecionado, o método [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) do [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) será usado para recuperar o reconhecedor padrão; caso contrário, o reconhecedor selecionado será recuperado. Em seguida, um contexto de reconhecedor é criado e usado, e a barra de menus e de status é atualizada.

O método **OnFactoidWordlist** da janela manipula o comando usar a barra de **palavras** no menu do **factor** . A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do contexto do reconhecedor é definida como **nula** para redefinir o contexto do reconhecedor. Se a opção **usar palavras** -opções estiver desativada, a propriedade de [**listas de palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do contexto do Recognizer será definida como **NULL**; caso contrário, a propriedade de **listas de palavras** do contexto do Recognizer é definida como o [**InkWordList**](inkwordlist-class.md) que foi criado no método **OnCreate** . Por fim, o [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) do coletor de tinta é reanexado ao contexto do reconhecedor, o método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) do contexto do Recognizer é chamado e o menu é atualizado.

O método **Onfactoid** da janela manipula os comandos de facto no menu do **factor** . Ele primeiro define a propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do contexto do Recognizer como **NULL**, define a propriedade [**factoname**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) do contexto do Recognizer para o factor selecionado e reatribui o [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) do coletor de tinta ao contexto do reconhecedor. Se o objeto [factor](factoid-constants.md) for suportado pelo contexto do reconhecedor, o método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) do contexto do Recognizer será chamado; caso contrário, uma mensagem de erro será exibida. Por fim, o menu e a barra de status são atualizados.

O método **OnGuide** da janela manipula os comandos no menu **guia** . Se o contexto do reconhecedor oferecer suporte às opções de guia, o método **OnGuide** definirá a propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do contexto do reconhecedor como **NULL**, definirá a propriedade [**guia**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) do contexto do reconhecedor como a configuração do guia selecionado, reatribuirá o [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) do coletor de tinta ao contexto do reconhecedor e chamará o método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) do contexto do Recognizer. Caso contrário, uma mensagem de erro será exibida. Por fim, a janela de entrada, o menu e a barra de status são atualizados.

O método **onmode** da janela manipula os comandos no menu **modo** . Ele desabilita o coletor de tinta, atualiza a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) do coletor de tinta, atualiza o menu e mostra ou oculta as listas de gestos. Por fim, o coletor de tinta está habilitado.

O método **Recognize** da janela manipula o comando **Recognize** no menu Ink. Ele chama o método [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) do contexto do reconhecedor para impedir que a tinta seja adicionada ao contexto do reconhecedor. Às vezes, isso é necessário, pois nem todos os reconhecedores dão suporte ao reconhecimento parcial. Em seguida, ele chama o método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) do contexto do Recognizer e passa os resultados para o método **OnRecognitionWithAlternates** da janela. Por fim, o [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) do coletor de tinta é reatribuído ao contexto do reconhecedor.

O método **OnClear** da janela manipula o comando **Clear** no menu **Ink** . Ele exclui os traços da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) do coletor de tinta, libera a coleção de traços antigos e cria um novo para a propriedade **Ink** do coletor de tinta e anexa a nova coleção Strokes ao contexto do reconhecedor.

O método **onexit** da janela manipula o comando **Exit** no menu **Ink** e gera o \_ evento WM Close.

## <a name="helper-methods"></a>Métodos auxiliares

O método **LoadMenu** da janela é chamado a partir do método **Run** da janela e adiciona a lista de reconhecedores com suporte e a lista de factores com suporte no menu. Primeiro, ele recupera o [InkRecognizers](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)). Em seguida, ele faz a iteração pelos reconhecedores disponíveis e seleciona apenas aqueles que têm uma lista de idiomas na propriedade **Languages** , que ele adiciona ao menu **Recognizer** . Por fim, ele preenche o menu do **factor** com a lista de factos definida como uma constante global.

O método **UseRecognizer** da janela é chamado a partir do método **Recognizer** da janela quando o usuário seleciona um novo reconhecedor. Ele cria um contexto de reconhecedor, desanexa o contexto antigo do coletor de eventos do reconhecedor, limpa e libera o contexto antigo e anexa o novo contexto ao coletor de eventos do reconhecedor.

Em seguida, o método **UseRecognizer** verifica a propriedade [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) do reconhecedor, que retorna um valor [**InkRecognizerCapabilities**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities) . Se o reconhecedor der suporte à entrada em linha, o comando **linhas** no menu **guia** será habilitado. Se o reconhecedor der suporte à entrada em caixa, o comando **caixas** será habilitado. Se o reconhecedor não oferecer suporte à entrada gratuita, o comando **None** será desabilitado. Se a seleção atual do guia não for suportada, a propriedade [**guia**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide) do contexto do reconhecedor e o menu serão atualizados.

Em seguida, o método **UseRecognizer** tenta definir as propriedades da propriedade de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) e do [**factor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) do contexto do reconhecedor. Se uma das configurações não for suportada pelo reconhecedor, o valor padrão será usado e o menu será atualizado.

Por fim, o método **UseRecognizer** anexa a propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do objeto [**InkDisp**](inkdisp-class.md) do coletor de tinta ao contexto do reconhecedor, altera a fonte da janela de saída para uma com suporte na linguagem do reconhecedor, redefine a janela de saída e atualiza os resultados de reconhecimento chamando o método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) do contexto do reconhecedor.

O método **Getgestoname** da janela é chamado a partir do método **ongesto** da janela. Ele procura o gesto e retorna um índice para o nome do gesto, que é armazenado em uma tabela de cadeia de caracteres no arquivo AdvReco. rc.

 

 
