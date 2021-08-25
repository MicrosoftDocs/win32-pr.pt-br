---
title: Usando um editor de método de entrada em um jogo
description: Este artigo explica como você pode implementar um controle de edição IME básico em um aplicativo Microsoft DirectX de tela inteira.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8cb5869579da97aeea465b572082a23a963e9db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471962"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Usando um editor de método de entrada em um jogo

> [!Note]  
> este artigo fornece detalhes sobre como trabalhar com o ime (Editor de método de entrada) do Windows XP. foram feitas alterações no IME para Windows Vista que não são totalmente detalhadas neste artigo. para obter mais informações sobre alterações no ime para Windows Vista, consulte [Input Method editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) no [Windows vista-uma exibição de internacionalização de Ever-Expanding](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) no Portal de desenvolvimento e computação Global da Microsoft.

 

Um IME (editor de método de entrada) é um programa que permite uma entrada de texto fácil usando um teclado padrão para idiomas do leste asiático, como chinês, japonês, coreano e outras linguagens com caracteres complexos. Por exemplo, com IMEs, um usuário pode digitar caracteres complexos em um processador de texto ou um jogador de um jogo online com vários participantes pode bater papo com amigos em caracteres complexos.

Este artigo explica como você pode implementar um controle de edição IME básico em um aplicativo Microsoft DirectX de tela inteira. Os aplicativos que tiram proveito do DXUT automaticamente obtêm a funcionalidade do IME. Para aplicativos que não fazem uso da estrutura, este artigo descreve como adicionar suporte ao IME a um controle de edição.

Conteúdo:

-   [Comportamento padrão do IME](#default-ime-behavior)
-   [Usando IMEs com DXUT](#using-imes-with-dxut)
-   [Substituindo o comportamento padrão do IME](#overriding-the-default-ime-behavior)
-   [Funções](#functions)
-   [Mensagens](#ime-messages)
-   [Exemplos](#examples)
    -   [IME do CHT versão 4,2, 4,3 e 4,4](#cht-ime-version-42-43-and-44)
    -   [IME do CHT versão 5,0](#cht-ime-version-50)
    -   [Chinês do CHT versão 5,1, 5,2 e CHS IME versão 5,3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [O IME CHS versão 4,1](#chs-ime-version-41)
    -   [O IME CHS versão 4,2](#chs-ime-version-42)
-   [Mensagens do IME](#ime-messages)
    -   [INPUTLANGCHANGE do WM \_](#wm_inputlangchange)
    -   [\_STARTCOMPOSITION IME do WM \_](/windows)
    -   [\_composição do IME do WM \_](/windows)
    -   [\_composição de endime do WM \_](/windows)
    -   [\_notificação do IME do WM \_](/windows)
-   [Renderização](#rendering)
    -   [Indicador de localidade de entrada](#input-locale-indicator)
    -   [Janela de composição](#composition-window)
    -   [Leitura e candidatos Windows](#reading-and-candidate-windows)
-   [Limitações](#limitations)
-   [Informações do registro](#registry-information)
-   [Apêndice A: versões do CHT por sistema operacional](#appendix-a-cht-versions-per-operating-system)
-   [Mais informações](#further-information)
-   [Getreadingstring](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Comportamento padrão do IME

Os IMEs mapeiam a entrada de teclado para componentes fonéticos ou outros elementos de linguagem específicos para um idioma selecionado. Em um cenário típico, o usuário digita chaves que representam a pronúncia de um caractere complexo. Se o IME reconhecer a pronúncia como válida, ele apresentará ao usuário uma lista de candidatos a palavras ou frases das quais o usuário pode selecionar uma escolha final. a palavra escolhida é enviada para o aplicativo por meio de uma série de mensagens de caracteres do Microsoft Windows [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) . Como o IME funciona em um nível abaixo do aplicativo interceptando a entrada do teclado, a presença de um IME é transparente para o aplicativo. quase todos os Windows aplicativos podem aproveitar prontamente os IMEs sem estar atento à sua existência e sem a necessidade de codificação especial.

Um IME típico exibe várias janelas para guiar o usuário por meio de entrada de caracteres, conforme mostrado nos exemplos a seguir.

![o IME exibe várias janelas](images/ime-elements.png)

| Tipo de janela                                       | Descrição                                                                                                                                                                                                                                                                                                                 | Saída do IME                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| a. Janela de leitura                                 | Contém pressionamentos de teclas do teclado; Normalmente, muda após cada pressionamento de tecla.                                                                                                                                                                                                                                              | Cadeia de caracteres de leitura                               |
| B. Janela de composição                             | Contém a coleção de caracteres que o usuário criou com o IME. Esses caracteres são desenhados pelo IME na parte superior do aplicativo. Quando o usuário notifica o IME que a cadeia de caracteres de composição é satisfatória, o IME envia a cadeia de caracteres de composição para o aplicativo por meio de uma série de mensagens do WM \_ Char. | Cadeia de caracteres de composição                           |
| C. Janela candidata                               | Quando o usuário insere uma pronúncia válida, o IME exibe uma lista de caracteres candidatos que correspondem à pronúncia determinada. O usuário seleciona o caractere pretendido nessa lista e o IME adiciona esse caractere à janela de composição exibida.                                                    | o próximo caractere na cadeia de caracteres de composição |
| D. Indicador de [localidade de entrada](/windows/desktop/Intl/nls-terminology) | Mostra o idioma que o usuário selecionou para entrada de teclado. esse indicador é inserido na barra de tarefas do Windows. O idioma de entrada pode ser selecionado abrindo o painel de controle opções regionais e de idiomas e clicando em detalhes na guia idiomas.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Usando IMEs com DXUT

No DXUT, a classe CDXUTIMEEditBox implementa a funcionalidade do IME. Essa classe é derivada da classe CDXUTEditBox, o controle de edição básico fornecido pela estrutura. CDXUTIMEEditBox estende esse controle de edição para dar suporte a IMEs, substituindo os métodos CDXUTIMEEditBox. As classes são projetadas dessa forma para ajudar os desenvolvedores a aprender o que precisam tomar da estrutura para implementar o suporte do IME em seus próprios controles de edição. O restante deste tópico explica como a estrutura, e CDXUTIMEEditBox em particular, substitui um controle de edição básico para implementar a funcionalidade do IME.

A maioria das variáveis específicas do IME em CDXUTIMEEditBox são declaradas como estáticas, porque muitos buffers e Estados do IME são específicos para o processo. Por exemplo, um processo tem apenas um buffer para a cadeia de caracteres de composição. Mesmo que o processo tenha dez controles de edição, todos eles estarão compartilhando o mesmo buffer de cadeia de caracteres de composição. O buffer da cadeia de caracteres de composição para CDXUTIMEEditBox é, portanto, estático, impedindo o aplicativo de ocupar espaço de memória desnecessário.

CDXUTIMEEditBox é implementado no seguinte código de DXUT:

(Raiz do SDK) \\ Exemplos do \\ C++ \\ Common \\ DXUTgui. cpp

## <a name="overriding-the-default-ime-behavior"></a>Substituindo o comportamento padrão do IME

normalmente, um IME usa procedimentos de Windows padrão para criar uma janela (consulte [usando Windows](/windows/desktop/winmsg/using-windows)). Em circunstâncias normais, isso produz resultados satisfatórios. No entanto, quando o aplicativo apresenta o modo de tela inteira, como é comum para jogos, as janelas padrão não funcionam mais e podem não ser exibidas na parte superior do aplicativo. para superar esse problema, o aplicativo deve desenhar o próprio windows do IME em vez de depender de Windows para executar essa tarefa.

Quando o comportamento de criação da janela do IME padrão não fornece o que um aplicativo requer, o aplicativo pode substituir a manipulação da janela do IME. Um aplicativo pode conseguir isso processando mensagens relacionadas ao IME e chamando a API do IMM ( [Input Method Manager](/windows/desktop/Intl/input-method-manager) ).

Quando um usuário interage com um IME para inserir caracteres complexos, o IMM envia mensagens ao aplicativo para notificá-lo de eventos importantes, como iniciar uma composição ou mostrar a janela candidata. Um aplicativo normalmente ignora essas mensagens e as passa para o manipulador de mensagens padrão, o que faz com que o IME as manipule. Quando o aplicativo, em vez do manipulador padrão, manipula as mensagens, ele controla exatamente o que acontece em cada um dos eventos do IME. Geralmente, o manipulador de mensagens recupera o conteúdo das várias janelas do IME chamando a API do IMM. Depois que o aplicativo tiver essas informações, ele poderá desenhar corretamente o próprio Windows do IME quando precisar renderizar para a exibição.

## <a name="functions"></a>Funções

Um IME precisa obter a cadeia de caracteres de leitura, ocultar a janela de leitura e obter a orientação da janela de leitura. Esta tabela mostra as funcionalidades por versão do IME:



|                    | Obtendo cadeia de caracteres de leitura                                                | Ocultando janela de leitura                       | Orientação da janela de leitura                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| **Antes da versão 6.0** | a. Ler dados privados do IME de acesso à janela diretamente. Consulte "4 Estrutura" | Intercepte mensagens privadas do IME. Consulte "3 mensagens" | Examine as informações do Registro. Consulte "5 informações do Registro" |
| **Após a versão 6.0**  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>Mensagens

As mensagens a seguir não devem ser processadas para o IME mais novo que implementa [ShowReadingWindow](#showreadingwindow)().

As mensagens a seguir são presas pelo manipulador de mensagens do aplicativo (ou seja, elas não são passadas para DefWindowProc) para impedir que a janela de leitura seja aparecendo.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Exemplos

Os exemplos a seguir ilustram como obter informações de cadeia de caracteres de leitura do IME mais antigo que não tem GetReadingString(). O código gera as seguintes saídas:



| Saída              | Descrição                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | Comprimento da cadeia de caracteres de leitura.                                                          |
| DWORD dwerr  | Índice do caractere de erro.                                                                   |
| LPWSTR wstr  | Ponteiro para a cadeia de caracteres de leitura.                                                         |
| Unicode BOOL | Se true, a cadeia de caracteres de leitura está no formato Unicode. Caso contrário, ele está no formato multibyte. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME versão 4.2, 4.3 e 4.4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME versão 5.0

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>CHT IME versão 5.1, 5.2 e CHS IME versão 5.3

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a>CHS IME versão 4.1

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a>CHS IME versão 4.2

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a>Mensagens do IME

Um aplicativo de tela inteira deve lidar corretamente com as seguintes mensagens relacionadas ao IME:

### <a name="wm_inputlangchange"></a>WM \_ INPUTLANGCHANGE

O IMM envia uma mensagem WM INPUTLANGCHANGE para a janela ativa de um aplicativo depois que a localidade de entrada é alterada pelo usuário com uma combinação de chaves (geralmente ALT+SHIFT) ou com o indicador de localidade de entrada na barra de tarefas ou na barra de \_ idiomas. A barra de idiomas é um controle na tela com o qual o usuário pode configurar um serviço de texto. (Consulte [Como mostrar a barra de idiomas](/windows/desktop/TSF/how-to-set-up-tsf).) A captura de tela a seguir mostra uma lista de seleção de idioma que é exibida quando o usuário clica no indicador de localidade.

![lista de seleção de idioma que é exibida quando o usuário clica no indicador de localidade](images/ime-langselection.png)

Quando o IMM envia uma mensagem WM \_ INPUTLANGCHANGE, CDXUTIMEEditBox deve executar várias tarefas importantes:

1.  O método GetKeyboardLayout é chamado para retornar o ID (identificador de localidade) de entrada para o thread do aplicativo. A classe CDXUTIMEEditBox salva essa ID em sua variável de membro estático s \_ hklCurrent para uso posterior. É importante que o aplicativo conheça a localidade de entrada atual, pois o IME para cada idioma tem seu próprio comportamento distinto. O desenvolvedor pode precisar fornecer código diferente para diferentes localidades de entrada.
2.  CDXUTIMEEditBox inicializa uma cadeia de caracteres a ser exibida no indicador de idioma da caixa de edição. Esse indicador pode exibir o idioma de entrada ativo quando o aplicativo está em execução no modo de tela inteira e nem a barra de tarefas nem a barra de idiomas estão visíveis.
3.  O método ImmGetConversionStatus é chamado para indicar se a localidade de entrada está no modo de conversão nativo ou não nativo. O modo de conversão nativa permite que o usuário insira texto no idioma escolhido. O modo de conversão não nativo faz com que o teclado atue como um teclado padrão em inglês. É importante dar ao usuário uma indicação visual sobre em qual tipo de modo de conversão o IME está, para que o usuário possa saber facilmente quais caracteres esperar ao atingir uma chave. CDXUTIMEEditBox fornece essa indicação visual com uma cor de indicador de idioma. Quando a localidade de entrada usa um IME com o modo de conversão nativo, a classe CDXUTIMEEditBox desenha o texto indicador com a cor definida pelo parâmetro m \_ IndicatorImeColor. Quando o IME está no modo de conversão não nativo ou nenhum IME é usado, a classe desenha o texto do indicador com a cor definida pelo parâmetro m \_ IndicatorEngColor.
4.  CDXUTIMEEditBox verifica a localidade de entrada e define a variável de membro estático bInsertOnType como TRUE para coreano e FALSE para todos \_ os outros idiomas. Esse sinalizador é necessário devido aos diferentes comportamentos dos IMEs coreanos e de todos os outros IMEs. Ao inserir caracteres em idiomas diferentes do coreano, o texto inserido pelo usuário é exibido na janela de composição e o usuário pode alterar livremente o conteúdo da cadeia de caracteres de composição. O usuário pressiona a tecla ENTER quando estiver satisfeito com a cadeia de caracteres de composição e a cadeia de caracteres de composição é enviada ao aplicativo como uma série de mensagens WM \_ CHAR. No entanto, em IMEs coreanos, quando um usuário pressiona uma tecla para inserir texto, um caractere é enviado imediatamente para o aplicativo. Quando o usuário pressiona posteriormente mais teclas para modificar esse caractere inicial, o caractere na caixa de edição muda para refletir a entrada adicional do usuário. Essencialmente, o usuário está compondo caracteres na caixa de edição. Esses dois comportamentos são diferentes o suficiente para que CDXUTIMEEditBox deve codificar para cada um deles especificamente.
5.  O método de membro estático SetupImeApi é chamado para recuperar endereços de duas funções do módulo IME: GetReadingString e ShowReadingWindow. Se essas funções existirem, ShowReadingWindow será chamado para ocultar a janela de leitura padrão para esse IME. Como o aplicativo renderiza a janela de leitura em si, ele notifica o IME para desabilitar o desenho da janela de leitura padrão para que ele não interfira na renderização de tela inteira.

O IMM envia uma mensagem SETCONTEXT do WM IME quando \_ uma janela do aplicativo é \_ ativada. O parâmetro lParam dessa mensagem contém um sinalizador que indica ao IME quais janelas devem ser desenhadas e quais não devem. Como o aplicativo está tratando todo o desenho, ele não precisa do IME para desenhar nenhuma das janelas do IME. Portanto, o manipulador de mensagens do aplicativo simplesmente define lParam como 0 e retorna.

Para que os aplicativos deem suporte ao IME, o processamento especial é necessário para a mensagem relacionada ao IME SETCONTEXT relacionada ao \_ \_ IME. Como Windows normalmente envia essa mensagem para o aplicativo antes de chamar o método PanoramaInitialize(), o Panorama não tem a oportunidade de processar a interface do usuário para mostrar janelas de lista de candidatos.

O snippet de código a seguir especifica Windows aplicativos não exibirão nenhuma interface do usuário associada à janela de lista de candidatos, permitindo que o Panorama manipular especificamente essa interface do usuário.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>WM \_ IME \_ STARTCOMPOSITION

O IMM envia uma mensagem STARTCOMPOSITION do WM IME para o aplicativo quando uma composição do IME está prestes a começar como resultado de trocas de \_ \_ teclas pelo usuário. Se o IME usar a janela de composição, ele exibirá a cadeia de caracteres de composição atual em uma janela de composição. CDXUTIMEEditBox lida com essa mensagem executando duas tarefas:

1.  CDXUTIMEEditBox limpa o buffer de cadeia de caracteres de composição e o buffer de atributo. Esses buffers são membros estáticos de CDXUTIMEEditBox.
2.  CDXUTIMEEditBox define a variável de membro estático \_ bHideCaret como TRUE. Esse membro, definido na classe CDXUTEditBox base, controla se o cursor na caixa de edição deve ser desenhado quando a caixa de edição é renderizada. A janela de composição funciona de forma semelhante a uma caixa de edição com texto e cursor. Para evitar confusão quando a janela de composição estiver visível, a caixa de edição oculta seu cursor para que apenas um cursor seja visível por vez.

### <a name="wm_ime_composition"></a>WM \_ IME \_ COMPOSITION

O IMM envia uma mensagem WM IME COMPOSITION para o aplicativo quando o usuário entra em um teclas para alterar a cadeia \_ \_ de caracteres de composição. O valor de lParam indica que tipo de informações o aplicativo pode recuperar do IMM (Gerenciador de Métodos de Entrada). O aplicativo deve recuperar as informações disponíveis chamando [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) e, em seguida, deve salvar as informações em seu buffer privado para que possa renderizar os elementos IME posteriormente.

CDXUTIMEEditBox verifica e recupera os seguintes dados de cadeia de caracteres de composição:



| [**WM \_ Valor do sinalizador IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam | Dados                           | Descrição                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GCS \_ COMPATTR                                                         | Atributo composition          | Esse atributo contém informações como o status de cada caractere na cadeia de caracteres de composição (por exemplo, convertido ou não convertido). Essas informações são necessárias porque CDXUTIMEEditBox colore os caracteres da cadeia de caracteres de composição de forma diferente com base em seus atributos.                                                                                   |
| GCS \_ COMPCLAUSE                                                       | Informações da cláusula Composition | Essas informações de cláusula são usadas quando o IME japonês está ativo. Quando uma cadeia de caracteres de composição japonesa é convertida, os caracteres podem ser agrupados como uma cláusula que é convertida em uma única entidade. Quando o usuário move o cursor, CDXUTIMEEditBox usa essas informações para realçá-lo, em vez de apenas um único caractere dentro da cláusula . |
| GCS \_ COMPSTR                                                          | Cadeia de caracteres de composição             | Essa cadeia de caracteres é a cadeia de caracteres atualizada que está sendo composta pelo usuário. Essa também é a cadeia de caracteres exibida na janela de composição.                                                                                                                                                                                                                                        |
| GCS \_ CURSORPOS                                                        | Posição do cursor de composição    | A janela de composição implementa um cursor, semelhante ao cursor em uma caixa de edição. O aplicativo pode recuperar a posição do cursor ao processar a mensagem WM \_ IME \_ COMPOSITION para desenhar o cursor corretamente.                                                                                                                                            |
| GCS \_ RESULTSTR                                                        | Cadeia de caracteres de resultado                  | A cadeia de caracteres de resultado está disponível quando o usuário está prestes a concluir o processo de composição. Essa cadeia de caracteres deve ser recuperada e os caracteres devem ser enviados para a caixa de edição.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>WM \_ IME \_ ENDCOMPOSITION

O IMM envia uma mensagem WM IME ENDCOMPOSITION para o aplicativo quando a operação de composição \_ \_ do IME está terminando. Isso pode ocorrer quando o usuário pressiona a tecla ENTER para aprovar a cadeia de caracteres de composição ou a tecla ESC para cancelar a composição. CDXUTIMEEditBox lida com essa mensagem definindo o buffer de cadeia de caracteres de composição como vazio. Em seguida, ele define s bHideCaret como FALSE porque a janela de composição está fechada e o cursor na caixa de edição deve \_ ficar visível novamente.

O manipulador de mensagens CDXUTIMEEditBox também define \_ s bShowReadingWindow como FALSE. Esse sinalizador controla se a classe desenha a janela de leitura quando a caixa de edição se renderiza, portanto, ela deve ser definida como FALSE quando uma composição termina.

### <a name="wm_ime_notify"></a>NOTIFICAÇÃO \_ DO WM IME \_

O IMM envia uma mensagem NOTIFY do WM \_ IME \_ para o aplicativo sempre que uma janela do IME é muda. Um aplicativo que lida com o desenho das janelas do IME deve processar essa mensagem para que ela esteja ciente de qualquer atualização para o conteúdo da janela. O wParam indica o comando ou a alteração que está ocorrendo. CDXUTIMEEditBox lida com os seguintes comandos:




| Comando IME | Descrição | 
|-------------|-------------|
| <a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a> | Esse atributo contém informações como o status de cada caractere na cadeia de caracteres de composição (por exemplo, convertido ou não convertido). Essas informações são necessárias porque CDXUTIMEEditBox colore os caracteres da cadeia de caracteres de composição de forma diferente com base em seus atributos. | 
| <a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a> | Enviado ao aplicativo quando a janela candidata está prestes a ser aberta ou atualizada, respectivamente. A janela candidata é aberta quando um usuário deseja alterar a opção de texto convertido. A janela é atualizada quando um usuário move o indicador de seleção ou altera a página. CDXUTIMEEditBox usa um manipulador de mensagens para ambos os comandos porque as tarefas necessárias são exatamente as mesmas:<br /><ol><li>CDXUTIMEEditBox define o membro bShowWindow da estrutura de lista candidata s_CandList como TRUE para indicar que a janela candidata precisa ser desenhada durante a renderização do quadro.</li><li>CDXUTIMEEditBox recupera a lista de candidatos chamando <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, primeiro para obter o tamanho do buffer necessário e, em seguida, novamente para obter os dados reais.</li><li>A estrutura de lista de candidatos s_CandList é inicializada com os dados candidatos recuperados.</li><li>As cadeias de caracteres candidatas são armazenadas como uma matriz de cadeias de caracteres.</li><li>O índice da entrada selecionada, bem como o índice da página, é salvo.</li><li>CDXUTIMEEditBox verifica se o estilo de janela candidato é vertical ou horizontal. Se o estilo da janela for horizontal, um buffer de cadeia de caracteres adicional, o membro HoriCand do s_CandList, deverá ser inicializado com todas as cadeias de caracteres candidatas, com caracteres de espaço inseridos entre todas as cadeias de caracteres adjacentes. Ao renderizar uma janela candidata vertical, as cadeias de caracteres candidatas individuais são desenhadas uma por vez, com as coordenadas y incrementadas para cada cadeia de caracteres. No entanto, essa cadeia de caracteres HoriCand deve ser usada ao renderizar uma janela candidata horizontal, porque o caractere de espaço é a melhor maneira de separar duas cadeias de caracteres adjacentes na mesma linha.</li></ol> | 
| <a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a> | Enviado ao aplicativo quando uma janela candidata está prestes a ser fechada. Isso acontece quando um usuário faz uma seleção da lista de candidatos. CDXUTIMEEditBox lida com esse comando definindo o sinalizador visível da janela candidata como FALSE e, em seguida, limpando o buffer de cadeia de caracteres candidato. | 
| IMN_PRIVATE | Enviado ao aplicativo quando o IME atualizou sua cadeia de caracteres de leitura como resultado da digitação ou remoção de caracteres pelo usuário. O aplicativo deve recuperar a cadeia de caracteres de leitura e salvá-la para renderização. CDXUTIMEEditBox tem dois métodos para recuperar a cadeia de caracteres de leitura, com base em como as cadeias de caracteres de leitura têm suporte no IME: <br /><ul><li>Se o IME dá suporte à função GetReadingString, GetReadingString é chamado para recuperar a cadeia de caracteres de leitura.</li><li>Se o IME não implementar GetReadingString, CDXUTIMEEditBox recuperará a cadeia de caracteres de leitura do conteúdo de contexto de entrada.</li></ul> | 




 

## <a name="rendering"></a>Renderização

A renderização dos elementos e janelas do IME é simples. CDXUTIMEEditBox permite que a classe base renderiza primeiro porque as janelas IME devem aparecer sobre o controle de edição. Depois que a caixa de edição base é renderizada, CDXUTIMEEditBox verifica o sinalizador de visibilidade de cada janela do IME (indicador, composição, candidato e janela de leitura) e desenha a janela se ela deve estar visível. Consulte Comportamento padrão do IME para ver descrições dos diferentes tipos de janela do IME.

### <a name="input-locale-indicator"></a>Indicador de localidade de entrada

O indicador de localidade de entrada é renderizado antes de qualquer outra janela IME porque é um elemento que sempre é exibido. Portanto, ele deve aparecer abaixo de outras janelas do IME. CDXUTIMEEditBox renderiza o indicador chamando o método RenderIndicator, no qual a cor da fonte do indicador é determinada examinando a variável estática ImeState, que reflete o modo de conversão \_ IME atual. Quando o IME está habilitado e a conversão nativa está ativa, o método usa m \_ IndicatorImeColor como a cor do indicador. Se o IME estiver desabilitado ou estiver no modo de conversão não nativo, m \_ IndicatorImeColor será usado para desenhar o texto do indicador. Por padrão, a própria janela do indicador é desenhada à direita da caixa de edição. Os aplicativos podem alterar esse comportamento substituindo o método RenderIndicator.

A figura a seguir mostra as diferentes aparências de um indicador de localidade de entrada para inglês, japonês no modo de conversão alfanumérico e japonês no modo de conversão nativa:

![diferentes aparências de um indicador de localidade de entrada para inglês e japonês](images/ime-indicator.png)

### <a name="composition-window"></a>Janela composição

O desenho da janela de composição é tratado no método RenderComposition de CDXUTIMEEditBox. A janela de composição flutua acima da caixa de edição. Ele deve ser desenhado na posição do cursor do controle de edição subjacente. CDXUTIMEEditBox lida com a renderização da seguinte forma:

1.  Toda a cadeia de caracteres de composição é desenhada usando as cores da cadeia de caracteres de composição padrão.
2.  Caracteres com determinados atributos especiais devem ser desenhados em cores diferentes, portanto, CDXUTIMEEditBox examina os caracteres da cadeia de caracteres de composição e inspeciona o atributo de cadeia de caracteres. Se o atributo chamar cores diferentes, o caractere será desenhado novamente com as cores apropriadas.
3.  O cursor da janela de composição é desenhado para concluir a renderização.

O cursor deve piscar para IMEs coreanos, mas não para outros IMEs. RenderComposition determina se o cursor deve ser visível com base em valores de temporizador quando o IME coreano é usado.

### <a name="reading-and-candidate-windows"></a>Leitura e candidato Windows

As janelas de leitura e candidata são renderizadas pelo mesmo método CDXUTIMEEditBox, RenderCandidateReadingWindow. Ambas as janelas contêm uma matriz de cadeias de caracteres para layout vertical ou uma única cadeia de caracteres no caso de layout horizontal. A maior parte do código em RenderCandidateReadingWindow é usada para posicionar a janela para que nenhuma parte da janela fique fora da janela do aplicativo e seja recortada.

## <a name="limitations"></a>Limitações

Às vezes, os IMEs contêm recursos avançados para melhorar a facilidade de entrada de texto. Alguns dos recursos encontrados em IMEs mais recentes são mostrados nas figuras a seguir. Esses recursos avançados não estão presentes no DXUT. Implementar o suporte para esses recursos avançados pode ser um desafio porque não há nenhuma interface definida para obter as informações necessárias dos IMEs.

IME chinês tradicional avançado com lista de candidatos expandidos:

![ime chinês tradicional avançado com lista de candidatos expandidos](images/ime-advanced1.png)

IME japonês avançado com algumas entradas candidatas que contêm texto adicional para descrever seus significados:

![ime japonês avançado com algumas entradas candidatas que contêm texto adicional para descrever seus significados](images/ime-advanced2.png)

IME coreano avançado que inclui um sistema de reconhecimento de manuscrito:

![ime coreano avançado que inclui um sistema de reconhecimento de manuscrito](images/ime-advanced3.png)

## <a name="registry-information"></a>Informações do Registro

As informações do Registro a seguir são verificadas para determinar a orientação da janela de leitura, quando o IME atual é mais antigo CHT New Phonetic que não implementa GetReadingString().



| Chave                                                           | Valor            |
|---------------------------------------------------------------|------------------|
| Nome do \\ \\ IME do Microsoft Windows \\ \\ Currentversion \\ do software \_ HKCU | mapeamento de teclado |



 

Em que: \_ o nome do IME será MSTCIPH se a versão do arquivo IME for 5,1 ou posterior; caso contrário, o nome do IME \_ será TINTLGNT.

A orientação da janela de leitura será horizontal se:

-   O IME é a versão 5,0 e o valor de mapeamento de teclado é 0x22 ou 0x23
-   O IME é a versão 5,1 ou a versão 5,2 e o valor de mapeamento de teclado é 0x22, 0x23 ou 0x24.

Se nenhuma das condições for atendida, a janela de leitura será vertical.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Apêndice A: versões do CHT por sistema operacional



| Sistema operacional           | Versão do IME do CHT |
|----------------------------|-----------------|
| Windows 98                 | 4.2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4             |
| Windows Vou                 | 5.0             |
| Office XP                  | 5.1             |
| Windows XP                 | 5.2             |
| Downloadble Web autônomos | 6,0             |



 

## <a name="further-information"></a>Mais informações

Para obter informações adicionais, consulte o seguinte:

-   [Instalar e usar editores de método de entrada](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Exibição de texto internacional](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [O consórcio Unicode](https://www.unicode.org/)
-   Desenvolvendo software internacional. Dr. International. 2º Ed. Redmond, WA: Microsoft Press, 2003.

## <a name="getreadingstring"></a>Getreadingstring

Obtém informações de cadeia de caracteres de leitura.

**Parâmetros**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[no \] contexto de entrada.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[em \] comprimento de lpwReadingBuf, em WCHAR. Se for zero, significa que o tamanho do buffer de leitura da consulta.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[\]cadeia de caracteres de leitura de retorno de saída (não final zero).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[\]índice de retorno de saída de caractere de erro na cadeia de caracteres de leitura, se houver.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[\]se for true, a leitura da interface do usuário será vertical. Caso contrário, horizontal puMaxReadingLen.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[out \] do tamanho da interface do usuário de leitura. O comprimento máximo de leitura não é fixo; Ele depende não apenas do layout do teclado, mas também do modo de entrada (por exemplo, código interno, entrada substituta).

</dd> </dl>

**Valores de retorno**

O comprimento da cadeia de caracteres de leitura.

**Comentários**

Se o valor de retorno for maior que o valor de uReadingBufLen, todos os parâmetros de saída serão indefinidos.

Essa função é implementada no CHT IME 6,0 ou posterior e pode ser adquirida por GetProcAddress em um identificador de módulo IME; o identificador do módulo IME pode ser adquirido por ImmGetIMEFileName e LoadLibrary.

**Requisitos**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Verga**
</dt> <dd>

Declarado em IMM. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importação**
</dt> <dd>

Use o IMM. lib.

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

Mostrar (ou ocultar) a janela de leitura.

**Parâmetros**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[no \] contexto de entrada.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[em \] definido como true para mostrar a janela de leitura (ou false para ocultá-la).

</dd> </dl>

**Valores de retorno**

**Comentários**

Retorna TRUE se for bem-sucedido ou FALSE, caso contrário.

**Requisitos**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Verga**
</dt> <dd>

Declarado em IMM. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importação**
</dt> <dd>

Use o IMM. lib.

</dd> </dl>
