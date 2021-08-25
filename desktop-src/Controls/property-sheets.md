---
title: Sobre as folhas de propriedades
description: Uma folha de propriedades é uma janela que permite ao usuário exibir e editar as propriedades de um item.
ms.assetid: 93676a64-7980-48cd-8615-23b14a118e1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d5ed4299a0771d9f2b4df6f17929474c7f4868edf7bcaf1ade5baa7e572b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914688"
---
# <a name="about-property-sheets"></a>Sobre as folhas de propriedades

Uma *folha de propriedades* é uma janela que permite ao usuário exibir e editar as propriedades de um item. Por exemplo, um aplicativo de planilha pode usar uma folha de propriedades para permitir que o usuário defina as propriedades de fonte e borda de uma célula ou exiba e defina as propriedades de um dispositivo, como uma unidade de disco, impressora ou mouse.

Esta seção aborda os tópicos a seguir.

-   [Noções básicas da folha de propriedades](#property-sheet-basics)
-   [Caixas de diálogo da folha de propriedades](#property-sheet-dialog-boxes)
-   [Páginas](#pages)
-   [Criação da folha de propriedades](#property-sheet-creation)
-   [Adicionando e removendo páginas](#adding-and-removing-pages)
-   [Título da folha de propriedades e rótulos de página](#property-sheet-title-and-page-labels)
-   [Ativação de página](#page-activation)
-   [Botão ajuda](#help-button)
    -   [Removendo o botão de ajuda da barra de legenda](#removing-the-caption-bar-help-button)
-   [Botões OK, cancelar e aplicar](#ok-cancel-and-apply-buttons)
-   [Assistentes](#wizards)

## <a name="property-sheet-basics"></a>Noções básicas da folha de propriedades

Para implementar folhas de propriedades em seu aplicativo, inclua o arquivo de cabeçalho Prsht. h em seu projeto. Prsht. h contém todos os identificadores usados com folhas de propriedades.

Uma folha de propriedades contém uma ou mais janelas filho sobrepostas chamadas páginas, cada uma contendo janelas de controle para definir um grupo de propriedades relacionadas. Por exemplo, uma página pode conter os controles para definir as propriedades de fonte de um item, incluindo o estilo de tipo, o tamanho do ponto, a cor e assim por diante. Cada página tem uma guia que o usuário pode selecionar para trazer a página para o primeiro plano da folha de propriedades. Por exemplo, o aplicativo do painel de controle Date-Time exibe a folha de propriedades a seguir.

![captura de tela de uma folha de propriedades com duas guias, uma das quais mostra um relógio e um controle de calendário mensal](images/propsheet1.png)

Uma folha de propriedades padrão com várias páginas com guias permite que o usuário tenha acesso aleatório a todas as propriedades. Se for mais apropriado ter propriedades definidas em sequência, você poderá usar um [Assistente](#wizards).

## <a name="property-sheet-dialog-boxes"></a>Caixas de diálogo da folha de propriedades

Uma folha de propriedades e as páginas contidas nela são caixas de diálogo na verdade. A folha de propriedades é uma caixa de diálogo definida pelo sistema que gerencia as páginas e fornece um contêiner comum para elas. Uma caixa de diálogo de folha de propriedades pode ser modal ou sem janela restrita. Ele inclui um quadro, uma barra de título e quatro botões: **OK**, **Cancelar**, **aplicar** e (opcionalmente) **ajuda**. Os procedimentos da caixa de diálogo para as páginas recebem códigos de notificação na forma de [**\_ notificar**](wm-notify.md) mensagens do WM quando o usuário clica nos botões.

> [!NOTE]  
> Nem todas as informações nesta seção se aplicam a assistentes, que têm uma aparência e um comportamento um pouco diferentes. Por exemplo, os assistentes têm um conjunto diferente de botões e nenhuma guia. Para obter mais informações, consulte [Criando assistentes](wizards.md).

Cada página em uma folha de propriedades é uma caixa de diálogo sem janela restrita de aplicativo que gerencia as janelas de controle usadas para exibir e editar as propriedades de um item. Você fornece o modelo de caixa de diálogo usado para criar cada página, bem como o procedimento de caixa de diálogo que gerencia os controles e define as propriedades do item correspondente.

Uma folha de propriedades envia códigos de notificação para o procedimento da caixa de diálogo para uma página quando a página está ganhando ou perdendo a ativação e quando o usuário clica no botão **OK**, **Cancelar**, **aplicar** ou **ajuda** . As notificações são enviadas na forma de mensagens [**de \_ notificação do WM**](wm-notify.md) . O parâmetro *lParam* é o endereço de uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que inclui o identificador de janela para a caixa de diálogo folha de propriedades.

Alguns códigos de notificação exigem uma página para retornar **true** ou **false** em resposta à mensagem [**de \_ notificação do WM**](wm-notify.md) . Para fazer isso, a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir o valor **DWL \_ MSGRESULT** para a caixa de diálogo Page como **true** ou **false**.

## <a name="pages"></a>Pages (Páginas)

uma folha de propriedades deve conter pelo menos uma página, mas não pode conter mais do que o valor de **MAXPROPPAGES** , conforme definido nos arquivos de cabeçalho de Windows. Cada página tem um índice de base zero que a folha de propriedades atribui de acordo com a ordem na qual a página é adicionada à folha de propriedades. Os índices são usados em mensagens que você envia para a folha de propriedades.

Uma página de propriedades pode conter uma caixa de diálogo aninhada. Se tiver, você deverá incluir o estilo [**WS \_ ex \_ CONTROLPARENT**](/windows/desktop/winmsg/extended-window-styles) para a caixa de diálogo de nível superior e chamar a função [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) com o identificador para a caixa de diálogo pai. Isso garante que o usuário possa usar mnemônicos e as teclas de navegação da caixa de diálogo para mover o foco para controles na caixa de diálogo aninhada.

Cada página tem um ícone e rótulo correspondente. A folha de Propriedades cria uma guia para cada página e exibe o ícone e o rótulo na guia. Espera-se que todas as páginas da folha de propriedades usem uma fonte que não seja negrito. Para garantir que a fonte não esteja em negrito, especifique o estilo **DS \_ 3DLOOK** no modelo da caixa de diálogo.

O procedimento da caixa de diálogo para uma página não deve chamar a função [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) . Isso irá destruir toda a folha de propriedades, não apenas a página.

O tamanho mínimo de uma página de folha de propriedades é de 212 unidades de caixa de diálogo horizontais e 114 de caixas de diálogo verticalmente. Se uma caixa de diálogo de página for menor do que isso, a página será ampliada até atender ao tamanho mínimo. O arquivo de cabeçalho Prsht. h contém três conjuntos de tamanhos recomendados para páginas de folha de propriedades, conforme mostrado na tabela a seguir.

|  Tamanho                |   Descrição                                                   |
|----------------------|-----------------------------------------------------------------|
| **PROP \_ SM \_ CXDLG**  | Largura, em unidades de diálogo, de uma página de folha de propriedades pequena.         |
| **PROP \_ SM \_ CYDLG**  | Altura, em unidades de diálogo, de uma página de folha de propriedades pequena.        |
| **\_CXDLG do MED de prop \_** | Largura, em unidades de diálogo, de uma página de folha de propriedades de tamanho médio.  |
| **\_CYDLG do MED de prop \_** | Altura, em unidades de diálogo, de uma página de folha de propriedades de tamanho médio. |
| **PROP \_ LG \_ CXDLG**  | Largura, em unidades de diálogo, de uma página de folha de propriedades grande.         |
| **PROP \_ LG \_ CYDLG**  | Altura, em unidades de diálogo, de uma página de folha de propriedades grande.        |

usar esses tamanhos recomendados ajudará a garantir a consistência visual entre seu aplicativo e outros aplicativos Windows da Microsoft.

no editor de recursos Microsoft Visual Studio, você pode criar uma página do tamanho apropriado na caixa de diálogo **adicionar recurso** . Expanda o nó da caixa de diálogo e selecione **IDD \_ PROPPAGE \_ grande**, **IDD \_ PROPPAGE \_ médio** ou **IDD \_ PROPPAGE \_ Small**.

A folha de propriedades é dimensionada automaticamente para acomodar a maior página.

## <a name="property-sheet-creation"></a>Criação da folha de propriedades

Antes de criar uma folha de propriedades, você deve definir uma ou mais páginas. Isso envolve preencher uma estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) com informações sobre a página – seu ícone, rótulo, modelo de caixa de diálogo, procedimento de caixa de diálogo e assim por diante — e, em seguida, especificar o endereço da estrutura em uma chamada para a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) . A função retorna um identificador para o tipo HPROPSHEETPAGE que identifica exclusivamente a página.

Para criar uma folha de propriedades, você especifica o endereço de uma estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) em uma chamada para a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) . A estrutura define o ícone e o título da folha de propriedades e também inclui o endereço de uma matriz de identificadores HPROPSHEETPAGE que você obtém usando [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea). Quando o **folha** cria a folha de propriedades, ele inclui as páginas identificadas na matriz. As páginas aparecem na folha de propriedades na mesma ordem em que estão contidas na matriz.

Outra maneira de atribuir páginas a uma folha de propriedades é especificar uma matriz de estruturas [**PROPSHEETPAGE**](pss-propsheetpage.md) em vez de uma matriz de identificadores **HPROPSHEETPAGE** . Nesse caso, o [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) cria identificadores para as páginas antes de adicioná-las à folha de propriedades.

Quando uma página é criada, seu procedimento de caixa de diálogo recebe uma mensagem do [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . O parâmetro *lParam* da mensagem é um ponteiro para uma cópia da estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) que é definida quando a página é criada. Em particular, quando uma página é criada, o membro **lParam** da estrutura pode ser usado para passar informações definidas pelo aplicativo para o procedimento da caixa de diálogo. Com exceção do membro **lParam** , essa estrutura deve ser tratada como somente leitura. Modificar algo diferente de **lParam** terá consequências imprevisíveis.

Quando o sistema passa subsequentemente uma cópia da estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) da página para seu aplicativo, ele usa o mesmo ponteiro. Todas as alterações na estrutura serão passadas. Como o membro **lParam** é ignorado pelo sistema, ele pode ser modificado para enviar informações para outras partes do seu aplicativo. Você pode, por exemplo, usar **lParam** para passar informações para a função de retorno de chamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) da página.

[**Folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) define automaticamente o tamanho e a posição inicial de uma folha de propriedades. A posição é baseada na posição da janela do proprietário e o tamanho é baseado na maior página especificada na matriz de páginas quando a folha de propriedades foi criada. Se você quiser que as páginas correspondam à largura dos quatro botões na parte inferior da folha de propriedades, defina a largura da página mais larga para as unidades de diálogo 190.

O tamanho de uma folha de propriedades é computado das propriedades *Width* e *Height* do modelo de caixa de diálogo no arquivo de recursos. Consulte [**recurso de caixa de diálogo**](/windows/desktop/menurc/dialog-resource) ou [**recurso DIALOGEX**](/windows/desktop/menurc/dialogex-resource) para obter mais detalhes. No entanto, observe que, por motivos de compatibilidade, as dimensões são computadas em relação à fonte MS Shell Dlg, em vez da fonte usada pela página. Se você criar uma página que usa outra fonte, uma das sugestões a seguir poderá ser usada.

-   Ajuste as dimensões do modelo de caixa de diálogo para compensar a diferença de tamanho entre a fonte MS Shell Dlg e a fonte que a página realmente usa. Por exemplo, se você escolher uma fonte que seja duas vezes maior que o MS Shell Dlg, defina a propriedade Width do modelo de caixa de diálogo como duas vezes o uso normal.
-   Use um modelo [**DIALOGEX**](/windows/desktop/menurc/dialogex-resource) e defina o estilo de caixa de diálogo **\_ SHELLFONT do DS** . Nesse caso, o Gerenciador de folhas de propriedades interpreta as dimensões do modelo de caixa de diálogo em relação à fonte usada pelo modelo de caixa de diálogo.

## <a name="adding-and-removing-pages"></a>Adicionando e removendo páginas

Depois de criar uma folha de propriedades, um aplicativo pode adicionar uma página ao final do conjunto de páginas existente enviando uma mensagem de [**PSM \_ ADDPAGE**](psm-addpage.md) . Para inserir uma página entre páginas existentes, envie uma mensagem [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) . Observe que o tamanho da folha de propriedades não pode ser alterado após ter sido criado. As páginas adicionadas ou inseridas não devem ser maiores do que a maior página atualmente na folha de propriedades. Para remover uma página, envie uma mensagem de [**PSM \_ REMOVEPAGE**](psm-removepage.md) .

Ao definir uma página, você pode especificar o endereço de uma função de retorno de chamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) que a folha de propriedades chama quando está criando ou removendo a página. Usar o *PropSheetPageProc* oferece a oportunidade de executar operações de inicialização e limpeza para páginas individuais.

> [!NOTE]  
> Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas. Enquanto essa ação está ocorrendo, a tentativa de modificar a lista de páginas terá resultados imprevisíveis. não adicione, insira ou remova páginas em sua implementação do [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka), ou ao manipular as notificações e Windows mensagens a seguir.
>
> -   [PSN \_ aplicar](psn-apply.md)
> -   [PSN \_ KILLACTIVE](psn-killactive.md)
> -   [redefinição de PSN \_](psn-reset.md)
> -   [PSN \_ SETactive](psn-setactive.md)
> -   [PSN \_ WIZBACK](psn-wizback.md)
> -   [PSN \_ WIZNEXT](psn-wiznext.md)
> -   [**INITDIALOG do WM \_**](/windows/desktop/dlgbox/wm-initdialog)
> -   [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)

se houver necessidade de modificar uma página de folha de propriedades enquanto você estiver manipulando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem de Windows privada. Seu aplicativo não receberá essa mensagem até que o Gerenciador de folhas de propriedades tenha concluído suas tarefas. nesse ponto, será seguro modificar a lista de páginas.

Quando uma folha de propriedades é destruída, ela destrói automaticamente todas as páginas que foram adicionadas a ela. As páginas são destruídas na ordem inversa da especificada na matriz usada para criar as páginas. Para destruir uma página que foi criada pela função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) , mas não foi adicionada à folha de propriedades, use a função [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) .

## <a name="property-sheet-title-and-page-labels"></a>Título da folha de propriedades e rótulos de página

Você especifica o título de uma folha de propriedades na estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) usada para criar a folha de propriedades. Se o membro **dwFlags** incluir o valor **PSH \_ PROPTITLE** , a folha de propriedades adicionará o sufixo "Properties" ou o prefixo "Properties for", dependendo da versão. Você pode alterar o título depois que uma folha de propriedades é criada usando a mensagem de [**PSM \_ SetTitle**](psm-settitle.md) . Em um assistente Aero, essa mensagem pode ser usada para alterar o título de uma página interior dinamicamente.

Por padrão, uma folha de propriedades usa a cadeia de caracteres de nome especificada no modelo da caixa de diálogo como o rótulo de uma página. Você pode substituir a cadeia de caracteres de nome, incluindo o valor de **PSP \_ USETITLE** no membro **dwFlags** da estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) que define a página. Quando **PSP \_ USETITLE** é especificado, o membro **pszTitle** deve conter o endereço da cadeia de caracteres do rótulo para a página.

## <a name="page-activation"></a>Ativação de página

Uma folha de propriedades pode ter apenas uma página ativa por vez. A página que tem a ativação está no primeiro plano da pilha sobreposta de páginas. O usuário ativa uma página selecionando sua guia; um aplicativo ativa uma página usando a mensagem de [**PSM \_ setcurse**](psm-setcursel.md) .

A folha de propriedades envia o código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) para a página que está prestes a perder a ativação. Em resposta, a página deve validar as alterações que o usuário fez na página. Se a página exigir entrada de usuário adicional antes de perder a ativação, use a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir o valor de **\_ MSGRESULT de DWL** da página como **true**. Além disso, a página deve exibir uma caixa de mensagem que descreve o problema e fornece a ação recomendada. Defina **DWL \_ MSGRESULT** como **false** quando houver problema para perder a ativação.

Antes que a página que está recebendo a ativação esteja visível, a folha de propriedades envia o código de notificação [PSN \_ SetActive](psn-setactive.md) para a página. A página deve responder inicializando suas janelas de controle.

## <a name="help-button"></a>Botão ajuda

As folhas de propriedades podem exibir dois botões de ajuda: um botão de ajuda da folha de propriedades que é exibido na parte inferior do quadro, ao lado do botão **OK** / **Cancelar** / **aplicar** botões e de barra de legenda padrão que fornece ajuda contextual.

O botão de ajuda da folha de propriedades é opcional e pode ser habilitado em uma página por página. Para exibir o botão de ajuda da folha de propriedades de uma ou mais páginas:

-   Defina o sinalizador **PSH \_ HasHelp** no membro **dwFlags** da estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) da folha de propriedades.
-   Para cada página que exibirá um botão ajuda, defina o sinalizador **PSP \_ HasHelp** no membro **dwFlags** da estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) da página.

Quando o usuário clica no botão ajuda, a página ativa recebe um código de notificação de [ \_ ajuda PSN](psn-help.md) . A página deve responder exibindo informações de ajuda, normalmente chamando a função [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) .

### <a name="removing-the-caption-bar-help-button"></a>Removendo o botão de ajuda da barra de legenda

O botão de ajuda da barra de legenda é exibido por padrão, de forma que a ajuda contextual sempre esteja disponível para os botões OK/cancelar/aplicar. No entanto, esse botão pode ser removido, se necessário. Para remover o botão de ajuda da barra de legenda de uma folha de propriedades:

-   Para versões dos controles comuns anteriores à [versão 5,80](common-control-versions.md), você deve implementar uma [**função de retorno de chamada de folha de propriedades**](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback).
-   Para a [versão 5,80](common-control-versions.md) e posterior dos controles comuns, você pode simplesmente definir o \_ sinalizador PSH NOCONTEXTHELP no membro **dwFlags** da estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) da folha de propriedades. No entanto, se precisar de compatibilidade com versões anteriores de controle comum, você deve implementar a função de retorno de chamada.

Para implementar uma função de retorno de chamada de folha de propriedades que remove o botão de ajuda da barra de legenda:

-   Defina o sinalizador **PSH \_ USECALLBACK** no membro **dwFlags** da estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) da folha de propriedades.
-   Defina o membro **pfnCallBack** da estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) para apontar para a função de retorno de chamada.
-   Implemente a função de retorno de chamada. Quando essa função recebe a mensagem de **\_ precreate do PSCB** , ela também receberá um ponteiro para o modelo da caixa de diálogo da folha de propriedades. Remova o estilo **DS \_ CONTEXTHELP** deste modelo.

O exemplo a seguir ilustra como implementar essa função de retorno de chamada:

```cpp
int CALLBACK RemoveContextHelpProc(HWND hwnd, UINT message, LPARAM lParam)
{
    switch (message) 
    {
    case PSCB_PRECREATE:
        // Remove the DS_CONTEXTHELP style from the
        // dialog box template
        if (((LPDLGTEMPLATEEX)lParam)->signature ==    
           0xFFFF)
           {
            ((LPDLGTEMPLATEEX)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        else {
            ((LPDLGTEMPLATE)lParam)->style 
            &= ~DS_CONTEXTHELP;
        }
        return TRUE;
    }
    return TRUE;
}
```

Se a estrutura [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) não estiver definida, inclua a seguinte declaração:

```cpp
#include <pshpack1.h>

typedef struct DLGTEMPLATEEX
{
    WORD dlgVer;
    WORD signature;
    DWORD helpID;
    DWORD exStyle;
    DWORD style;
    WORD cDlgItems;
    short x;
    short y;
    short cx;
    short cy;
} DLGTEMPLATEEX, *LPDLGTEMPLATEEX;

#include <poppack.h>
```

## <a name="ok-cancel-and-apply-buttons"></a>Botões OK, cancelar e aplicar

Os botões **OK** e **aplicar** são semelhantes; ambas direcionam as páginas de uma folha de propriedades para validar e aplicar as alterações de propriedade feitas pelo usuário. A única diferença é que clicar no botão **OK** faz com que a folha de propriedades seja destruída após a aplicação das alterações.

Quando o usuário clica no botão **OK** ou **aplicar** , a folha de propriedades envia uma notificação [PSN \_ KILLACTIVE](psn-killactive.md) para a página ativa, dando a ela uma oportunidade de validar as alterações do usuário. Se as alterações forem válidas, a página deverá chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o valor **DWL \_ MSGRESULT** definido como **false**. Se as alterações do usuário não forem válidas, a página deverá definir **DWL \_ MSGRESULT** como **true** e exibir uma caixa de diálogo informando o usuário do problema. A página permanece ativa até que ela defina **DWL \_ MSGRESULT** como **false** em resposta a uma \_ mensagem PSN KILLACTIVE.

Depois que uma página responde a uma notificação [PSN \_ KILLACTIVE](psn-killactive.md) definindo **DWL \_ MSGRESULT** como **false**, a folha de propriedades enviará uma notificação de [PSN \_](psn-apply.md) para cada página. Quando uma página recebe essa notificação, ela deve aplicar as novas propriedades ao item correspondente. Para indicar à folha de propriedades que as alterações são válidas para a página, chame [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com **DWL \_ MSGRESULT** definido como **PSNRET \_ NOERROR**. Se as alterações forem inválidas para a página, retorne um erro. Isso impede que a folha de propriedades seja destruída e retorne o foco para a página que recebeu a \_ notificação de aplicação de PSN ou a página que tinha o foco quando o botão **aplicar** foi pressionado. Para retornar um erro e indicar qual página receberá o foco, defina **DWL \_ MSGRESULT** como um dos valores a seguir.

-   **PSNRET \_ INVÁLIDO**. A folha de propriedades não será destruída e o foco será retornado para esta página.
-   **PSNRET \_ \_NOCHANGEPAGE inválido**. A folha de propriedades não será destruída e o foco será retornado para a página que tinha o foco quando o botão foi pressionado.

Um aplicativo pode usar a mensagem de [**\_ aplicação de PSM**](psm-apply.md) para simular a seleção do botão **aplicar** .

O botão **aplicar** inicialmente é desabilitado quando uma página se torna ativa, indicando que ainda não há nenhuma alteração de propriedade a ser aplicada. Quando a página recebe a entrada por meio de um de seus controles, indicando que o usuário editou uma propriedade, a página deve enviar a mensagem [**\_ alteração de PSM**](psm-changed.md) para a folha de propriedades. A mensagem faz com que a folha de propriedades habilite o botão **aplicar** . Se o usuário clicar em seguida no botão **aplicar** ou **Cancelar** , a página deverá reinicializar seus controles e, em seguida, enviar a mensagem de [**PSM \_ inalterada**](psm-unchanged.md) para desabilitar novamente o botão **aplicar** .

Às vezes, o botão **aplicar** faz com que uma página faça uma alteração em uma folha de propriedades, e a alteração não pode ser desfeita. Quando isso acontece, a página deve enviar a mensagem de [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) para a folha de propriedades. A mensagem faz com que a folha de propriedades altere o texto do botão **OK** para "fechar", indicando que as alterações aplicadas não podem ser canceladas.

às vezes, uma página faz uma alteração na configuração do sistema que requer que Windows seja reiniciada ou o sistema seja reinicializado antes que a alteração entre em vigor. Depois de fazer essa alteração, uma página deve enviar a mensagem [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) ou [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) para a folha de propriedades. Essas mensagens fazem com que a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorne o valor da **ID \_ PSRESTARTWINDOWS** ou **ID \_ PSREBOOTSYSTEM** após a destruição da folha de propriedades.

Quando um usuário clica no botão **Cancelar** , a folha de propriedades envia o código de notificação de [ \_ redefinição de PSN](psn-reset.md) para todas as páginas, indicando que a folha de propriedades está prestes a ser destruída. Uma página deve usar a notificação para executar operações de limpeza.

## <a name="wizards"></a>Assistentes

Um assistente é um tipo especial de folha de propriedades. Os assistentes são projetados para apresentar as páginas uma de cada vez em uma sequência que é controlada pelo aplicativo. Em vez de selecionar um grupo de páginas clicando em uma guia, os usuários navegam para frente e para trás na sequência, uma página por vez clicando em botões. Por exemplo, a captura de tela a seguir mostra a página de boas-vindas do assistente para adicionar hardware:

![captura de tela da página inicial de um assistente](images/wizard97.png)

a captura de tela a seguir mostra a primeira página de um assistente Aero, o novo estilo introduzido no Windows Vista.

![captura de tela da primeira página de um assistente Aero](images/wizardaero.png)

Consulte [Criando assistentes](wizards.md) para uma discussão completa dos assistentes.
