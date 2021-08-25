---
title: Como personalizar barras de ferramentas
description: A maioria Windows aplicativos baseados em ferramentas usam controles de barra de ferramentas para fornecer aos usuários acesso conveniente à funcionalidade do programa.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f098880676fc0404df2a68694dc80b8601c21926d94ff594029321bafb1528a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929537"
---
# <a name="how-to-customize-toolbars"></a>Como personalizar barras de ferramentas

A maioria Windows aplicativos baseados em ferramentas usam controles de barra de ferramentas para fornecer aos usuários acesso conveniente à funcionalidade do programa. No entanto, as barras de ferramentas estáticas têm algumas deficiências, como muito pouco espaço para exibir efetivamente todas as ferramentas disponíveis. A solução para esse problema é tornar as barras de ferramentas do aplicativo personalizáveis pelo usuário. Em seguida, os usuários podem optar por exibir apenas as ferramentas necessárias e organizá-las de uma maneira que se adapte ao estilo de trabalho pessoal.

> [!Note]  
> As barras de ferramentas nas caixas de diálogo não podem ser personalizadas.

 

Para habilitar a personalização, inclua o sinalizador de estilo de controles comuns [**CCS \_ ADJUSTABLE**](common-control-styles.md) ao criar o controle de barra de ferramentas. Há duas abordagens básicas para personalização:

-   A caixa de diálogo de personalização. Essa caixa de diálogo fornecida pelo sistema é a abordagem mais simples. Ele fornece aos usuários uma interface gráfica do usuário que permite adicionar, excluir ou mover ícones.
-   Arrastando e soltando ferramentas. Implementar a funcionalidade do tipo "arrastar e soltar" permite que os usuários movam ferramentas para outro local na barra de ferramentas ou as excluam arrastando para fora da barra de ferramentas. Ele fornece aos usuários uma maneira rápida e fácil de organizar sua barra de ferramentas, mas não permite que eles adicionem ferramentas.

Você pode implementar uma abordagem ou ambas, dependendo das necessidades do aplicativo. Nenhuma dessas duas abordagens de personalização fornece um mecanismo integrado, como um botão Cancelar ou Desfazer, para retornar a barra de ferramentas para seu estado anterior. Você deve usar explicitamente a API de controle da barra de ferramentas para armazenar o estado de pré-customização da barra de ferramentas. Se necessário, você pode usar essas informações armazenadas posteriormente para restaurar a barra de ferramentas para seu estado original.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="customization-dialog-box"></a>Caixa de diálogo Personalização

A caixa de diálogo personalização é fornecida pelo controle da barra de ferramentas para dar aos usuários uma maneira simples de adicionar, mover ou excluir ferramentas. Os usuários podem inocioná-lo clicando duas vezes na barra de ferramentas. Os aplicativos podem iniciar a caixa de diálogo de personalização programaticamente enviando ao controle da barra de ferramentas uma [**mensagem TB \_ CUSTOMIZE.**](tb-customize.md)

A ilustração a seguir mostra um exemplo da caixa de diálogo de personalização da barra de ferramentas.

![captura de tela de uma janela com uma barra de ferramentas de três itens e uma caixa de diálogo com listas dos botões de barra de ferramentas disponíveis e atuais](images/tb-customdlg.png)

As ferramentas na caixa de listagem à direita são aquelas atualmente na barra de ferramentas. Inicialmente, essa lista conterá as ferramentas que você especificar ao criar a barra de ferramentas. A caixa de listagem à esquerda contém as ferramentas disponíveis para adicionar à barra de ferramentas. Seu aplicativo é responsável por preencher essa lista (diferente do separador, que aparece automaticamente).

O controle da barra de ferramentas notifica seu aplicativo de que ele está iniciando uma caixa de diálogo de personalização enviando à janela pai um código de notificação [TBN \_ BEGINADJUST](tbn-beginadjust.md) seguido por um código de notificação [TBN \_ INITCUSTOMIZE.](tbn-initcustomize.md) Na maioria dos casos, o aplicativo não precisa responder a esses códigos de notificação. No entanto, se você não quiser que a caixa de diálogo Personalizar Barra de Ferramentas exibir um botão Ajuda, manipular TBN \_ INITCUSTOMIZE retornando TBNRF \_ HIDEHELP.

Em seguida, o controle da barra de ferramentas coleta as informações necessárias para inicializar a caixa de diálogo enviando três séries de códigos de notificação, na seguinte ordem:

-   Um [código de \_ notificação TBN QUERYINSERT](tbn-queryinsert.md) para cada botão na barra de ferramentas para determinar onde os botões podem ser inseridos. Retorne **FALSE** para impedir que um botão seja inserido à esquerda do botão especificado na mensagem de notificação. Se você retornar **FALSE para** todos os códigos de notificação TBN \_ QUERYINSERT, a caixa de diálogo não será exibida.
-   Um [código de \_ notificação TBN QUERYDELETE](tbn-querydelete.md) para cada ferramenta que está atualmente na barra de ferramentas. Retornar **TRUE** se uma ferramenta puder ser excluída ou **FALSE** se não.
-   Uma série de [códigos de \_ notificação TBN GETBUTTONINFO](tbn-getbuttoninfo.md) para preencher a lista de botões disponíveis. Para adicionar um botão à lista, preencha a estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) passada com o código de notificação e retorne **TRUE.** Quando você não tiver mais ferramentas para adicionar, retorne **FALSE.** Observe que você pode retornar informações para botões que já estão na barra de ferramentas; esses botões não serão adicionados à lista.

A caixa de diálogo é exibida e o usuário pode começar a personalizar a barra de ferramentas.

Quando a caixa de diálogo estiver aberta, seu aplicativo poderá receber uma variedade de códigos de notificação, dependendo das ações do usuário:

-   [TBN \_ QUERYINSERT.](tbn-queryinsert.md) O usuário alterou o local de uma ferramenta na barra de ferramentas ou adicionou uma ferramenta. Retorne **FALSE** para impedir que a ferramenta seja inserida nesse local.
-   [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md). O usuário está prestes a remover uma ferramenta da barra de ferramentas.
-   [TBN \_ CUSTHELP](tbn-custhelp.md). O usuário clicou no botão Ajuda.
-   [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md). O usuário adicionou, moveu ou excluiu uma ferramenta.
-   [TBN \_ RESET](tbn-reset.md). O usuário clicou no botão Redefinir.

Depois que a caixa de diálogo for destruída, seu aplicativo receberá um código de notificação [ \_ TBN ENDADJUST.](tbn-endadjust.md)

O exemplo de código a seguir mostra uma maneira de implementar a personalização da barra de ferramentas.


```C++
// The buttons are stored in an array of TBBUTTON structures. 
//
// Constants such as STD_FILENEW are identifiers for the 
// built-in bitmaps that have already been assigned as the toolbar's 
// image list.
//
// Constants such as IDM_NEW are application-defined command identifiers.

TBBUTTON allButtons[] = 
    {
        { MAKELONG(STD_FILENEW,  ImageListID), IDM_NEW,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"New" },
        { MAKELONG(STD_FILEOPEN, ImageListID), IDM_OPEN,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Open"},
        { MAKELONG(STD_FILESAVE, ImageListID), IDM_SAVE,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Save"},
        { MAKELONG(STD_CUT,      ImageListID), IDM_CUT,   TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Cut" },
        { MAKELONG(STD_COPY,     ImageListID), IDM_COPY,  TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Copy"},
        { MAKELONG(STD_PASTE,    ImageListID), IDM_PASTE, TBSTATE_ENABLED, 0, {0}, 0, (INT_PTR)L"Paste"}
    };

// The following appears in the window's message handler.

case WM_NOTIFY: 
    {
        switch (((LPNMHDR)lParam)->code) 
        {
        
        case TBN_GETBUTTONINFO:  
            {
                LPTBNOTIFY lpTbNotify = (LPTBNOTIFY)lParam;

                // Pass the next button from the array. There is no need to filter out buttons
                // that are already used—they will be ignored.
                
                int buttonCount = sizeof(allButtons) / sizeof(TBBUTTON);
                
                if (lpTbNotify->iItem < buttonCount)
                {
                    lpTbNotify->tbButton = allButtons[lpTbNotify->iItem];
                    return TRUE;
                }
                
                else
                
                {
                    return FALSE;  // No more buttons.
                }
            }
            
            break;

            case TBN_QUERYINSERT:
            
            case TBN_QUERYDELETE:
                return TRUE; 
        }
    }
```



### <a name="dragging-and-dropping-tools"></a>Arrastando e soltando ferramentas

Os usuários também podem reorganizar os botões em uma barra de ferramentas pressionando a tecla SHIFT e arrastando o botão para outro local. O processo do "arrastar e soltar" é tratado automaticamente pelo controle da barra de ferramentas. Ele exibe uma imagem fantasma do botão enquanto ele é arrastado e reorganiza a barra de ferramentas depois de ser descartado. Os usuários não podem adicionar botões dessa maneira, mas podem excluir um botão soltando-o da barra de ferramentas.

Embora o controle de barra de ferramentas normalmente faça essa operação automaticamente, ele também envia ao aplicativo dois códigos de notificação: [TBN \_ QUERYDELETE](tbn-querydelete.md) e [TBN \_ QUERYINSERT](tbn-queryinsert.md). Para controlar o processo do tipo "arrastar e soltar", processe esses códigos de notificação da seguinte forma:

-   O [código de \_ notificação TBN QUERYDELETE](tbn-querydelete.md) é enviado assim que o usuário tenta mover o botão antes que o botão fantasma seja exibido. Retorne **FALSE** para impedir que o botão seja movido. Se você retornar **TRUE,** o usuário poderá mover a ferramenta ou excluí-la soltando-a da barra de ferramentas. Se uma ferramenta puder ser movida, ela poderá ser excluída. No entanto, se o usuário excluir uma ferramenta, o controle da barra de ferramentas enviará ao seu aplicativo um código de notificação [TBN \_ DELETINGBUTTON,](tbn-deletingbutton.md) momento em que você poderá optar por reinserir o botão em seu local original, cancelando a exclusão.
-   O [código de \_ notificação TBN QUERYINSERT](tbn-queryinsert.md) é enviado quando o usuário tenta soltar o botão na barra de ferramentas. Para impedir que o botão que está sendo movido seja descartado à esquerda do botão especificado na notificação, retorne **FALSE.** Esse código de notificação não será enviado se o usuário tirar a ferramenta da barra de ferramentas.

Se o usuário tentar arrastar um botão sem pressionar também a tecla SHIFT, o controle da barra de ferramentas não manipulará a operação do tipo "arrastar e soltar". No entanto, ele enviará ao seu aplicativo um código de notificação [TBN \_ BEGINDRAG](tbn-begindrag.md) para indicar o início de uma operação de arrastar e um código de notificação [ \_ TBN ENDDRAG](tbn-enddrag.md) para indicar o final. Se você quiser habilitar essa forma de arrastar e soltar, seu aplicativo deverá manipular esses códigos de notificação, fornecer a interface do usuário necessária e modificar a barra de ferramentas para refletir as alterações.

### <a name="saving-and-restoring-toolbars"></a>Salvando e restaurando barras de ferramentas

No processo de personalização de uma barra de ferramentas, seu aplicativo pode precisar salvar informações para que você possa restaurar a barra de ferramentas para seu estado original. Para iniciar o salvar ou restaurar um estado da barra de ferramentas, envie ao controle da barra de ferramentas uma mensagem [**\_ SAVERESTORE de TB**](tb-saverestore.md) com *o lParam definido* como **TRUE.** O *valor lParam* dessa mensagem especifica se você está solicitando uma operação de salvar ou restaurar. Depois que a mensagem é enviada, há duas maneiras de lidar com a operação de salvar/restaurar:

-   Com controles [comuns versão 4.72](common-control-versions.md) e anteriores, você deve implementar um manipulador [ \_ GETBUTTONINFO TBN.](tbn-getbuttoninfo.md) O controle da barra de ferramentas envia esse código de notificação para solicitar informações sobre cada botão conforme ele é restaurado.
-   A versão 5.80 inclui uma opção de salvar/restaurar. No início do processo e conforme cada botão é salvo ou restaurado, seu aplicativo receberá um código de notificação [TBN \_ SAVE](tbn-save.md) ou [TBN \_ RESTORE.](tbn-restore.md) Para usar essa opção, você deve implementar manipuladores de notificação para fornecer o bitmap e as informações de estado necessárias para salvar ou restaurar com êxito o estado da barra de ferramentas.

Os estados da barra de ferramentas são salvos em um fluxo de dados que consiste em blocos de dados definidos pelo Shell alternando com blocos de dados definidos pelo aplicativo. Um bloco de dados de cada tipo é armazenado para cada botão, juntamente com um bloco opcional de dados globais que os aplicativos podem colocar no início do fluxo. Durante o processo de salvar, o manipulador [TBN \_ SAVE](tbn-save.md) adiciona os blocos definidos pelo aplicativo ao fluxo de dados. Durante o processo de restauração, o manipulador [TBN \_ RESTORE](tbn-restore.md) lê cada bloco e fornece ao Shell as informações necessárias para reconstruir a barra de ferramentas.

### <a name="how-to-handle-a-tbn_save-notification"></a>Como lidar com uma notificação TBN \_ SAVE

O primeiro [código de notificação \_ TBN SAVE](tbn-save.md) é enviado no início do processo de salvar. Antes que todos os botões sejam salvos, os membros da estrutura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) são definidos conforme mostrado na tabela a seguir.



| Membro       | Configuração                                                                                                                                                                                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**    | – 1                                                                                                                                                                                                                                                                                                                                                 |
| **cbData**   | A quantidade de memória necessária para dados definidos por shell.                                                                                                                                                                                                                                                                                                |
| **cButtons** | O número de botões.                                                                                                                                                                                                                                                                                                                             |
| **pData**    | A quantidade calculada de memória necessária para dados definidos pelo aplicativo. Normalmente, você inclui alguns dados globais, além de dados para cada botão. Adicione esse valor a **cbData** e aloque memória suficiente para o **pData** para manter tudo.                                                                                                                      |
| **pCurrent** | O primeiro byte não utilizado no fluxo de dados. Se você não precisar de informações da barra de ferramentas global, defina **pCurrent**  =  **pData** para que ele aponte para o início do fluxo de dados. Se você precisar de informações da barra de ferramentas global, armazene-as em **pData** e, em seguida, defina **pCurrent** para o início da parte não usada do fluxo de dados antes de retornar. |



 

Se você quiser adicionar algumas informações globais da barra de ferramentas, coloque-as no início do fluxo de dados. Avance **pCurrent** até o final dos dados globais para que ele aponte para o início da parte não utilizada do fluxo de dados e retorne.

Depois de retornar, o Shell começa a salvar as informações do botão. Ele adiciona os dados definidos por Shell para o primeiro botão em **pCurrent** e, em seguida, avança **pCurrent** para o início da parte não utilizada.

Depois que cada botão é salvo, um código de notificação [tbn \_ Save](tbn-save.md) é enviado e [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) é retornado com esses membros definidos da seguinte maneira.



| Membro                       | Configuração                                                                                                                                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **iItem**                    | O índice de base zero do número do botão.                                                                                                                                                                                                                           |
| **pCurrent**                 | Um ponteiro para o primeiro byte não utilizado no fluxo de dados. Se você quiser armazenar informações adicionais sobre o botão, armazene-o no local apontado por **pCurrent** e atualize **pCurrent** para apontar para a primeira parte não utilizada do fluxo de dados depois disso. |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) | Uma estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que descreve o botão que está sendo salvo.                                                                                                                                                                              |



 

Ao receber o código de notificação, você deve extrair as informações específicas de cada botão de que precisa do [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton). Lembre-se de que, ao adicionar um botão, você pode usar o membro **dwData** de **TBBUTTON** para armazenar dados específicos do aplicativo. Carregue seus dados no fluxo de dados em **pCurrent**. Avance **pCurrent** até o final de seus dados, apontando novamente para o início da parte não utilizada do fluxo e retorne.

Em seguida, o Shell vai para o botão Avançar, adiciona suas informações a **pData**, avança **PCurrent**, carrega [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e envia outro código de notificação de [tbn \_ salvar](tbn-save.md) . Esse processo continua até que todos os botões sejam salvos.

### <a name="restoring-saved-toolbars"></a>Restaurando barras de ferramentas salvas

O processo de restauração basicamente reverte o processo de salvamento. No início, seu aplicativo receberá um código de notificação [tbn \_ Restore](tbn-restore.md) com o membro **iItem** da estrutura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) definida como – 1. O membro **cbData** é definido como o tamanho de **pData** e **cButtons** é definido como o número de botões.

Seu manipulador de notificação deve extrair as informações globais que foram colocadas no início de **pData** durante a gravação e avançar **pCurrent** até o início do primeiro bloco de dados definidos por shell. Defina **cBytesPerRecord** como o tamanho dos blocos de dados usados para salvar os dados do botão. Defina **cButtons** como o número de botões e retorne.

O próximo [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) é para o primeiro botão. O membro **pCurrent** aponta para o início do primeiro bloco de dados de botão e **iItem** é definido como o índice de botão. Extraia esses dados e **pCurrent** avançados. Carregue os dados em [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)e retorne. Para omitir um botão da barra de ferramentas restaurada, defina o membro **idCommand** de **TBBUTTON** como zero. O Shell repetirá o processo para os botões restantes. Além das mensagens [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) e **NMTBRESTORE** , você também pode usar mensagens como [tbn \_ Reset](tbn-reset.md) para salvar e restaurar uma barra de ferramentas.

O exemplo de código a seguir salva uma barra de ferramentas antes de ser personalizada e a restaura se o aplicativo receber uma mensagem de [ \_ redefinição de tbn](tbn-reset.md) .


```C++
int               i;
LPNMHDR           lpnmhdr;
static int        nResetCount;
static LPTBBUTTON lpSaveButtons;
LPARAM            lParam;

switch( lpnmhdr->code)
{
    case TBN_BEGINADJUST: // Begin customizing the toolbar.
    {
        LPTBNOTIFY  lpTB = (LPTBNOTIFY)lparam;
       
        // Allocate memory for the button information.
        
        nResetCount   = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        lpSaveButtons = (LPTBBUTTON)GlobalAlloc(GPTR, sizeof(TBBUTTON) * nResetCount);
      
        // In case the user presses reset, save the current configuration 
        // so the original toolbar can be restored.
        
        for(i = 0; i < nResetCount; i++)
        {
            SendMessage(lpTB->hdr.hwndFrom, 
                        TB_GETBUTTON, i, 
                        (LPARAM)(lpSaveButtons + i));
        }
    }
    
    return TRUE;
   
    case TBN_RESET:
    {
        LPTBNOTIFY lpTB = (LPTBNOTIFY)lparam;
        
        int nCount, i;
    
        // Remove all of the existing buttons, starting with the last one.
        
        nCount = SendMessage(lpTB->hdr.hwndFrom, TB_BUTTONCOUNT, 0, 0);
        
        for(i = nCount - 1; i >= 0; i--)
        {
            SendMessage(lpTB->hdr.hwndFrom, TB_DELETEBUTTON, i, 0);
        }
      
        SendMessage(lpTB->hdr.hwndFrom,      // Restore the saved buttons.
                    TB_ADDBUTTONS, 
                    (WPARAM)nResetCount, 
                    (LPARAM)lpSaveButtons);
    }
    
    return TRUE;
   
    case TBN_ENDADJUST:                // Free up the memory you allocated.
        GlobalFree((HGLOBAL)lpSaveButtons);
        
        return TRUE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles da barra de ferramentas](using-toolbar-controls.md)
</dt> <dt>

[**Valores de índice da imagem do botão padrão da barra de ferramentas**](toolbar-standard-button-image-index-values.md)
</dt> <dt>

[Windows de demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




