---
title: Como personalizar barras de ferramentas
description: A maioria dos aplicativos baseados no Windows usa controles da barra de ferramentas para fornecer aos usuários acesso conveniente à funcionalidade do programa.
ms.assetid: 0CE2988E-D887-433B-BFB2-5F3442E8E1B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091451a139cf846b1106916f28c165d6640699eb
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104007264"
---
# <a name="how-to-customize-toolbars"></a>Como personalizar barras de ferramentas

A maioria dos aplicativos baseados no Windows usa controles da barra de ferramentas para fornecer aos usuários acesso conveniente à funcionalidade do programa. No entanto, as barras de ferramentas estáticas têm algumas deficiências — por exemplo, pouco espaço para exibir efetivamente todas as ferramentas disponíveis. A solução para esse problema é tornar as barras de ferramentas do aplicativo personalizáveis pelo usuário. Em seguida, os usuários podem optar por exibir apenas as ferramentas de que precisam e podem organizá-los de uma forma que se adaptem ao seu organizador de trabalho pessoal.

> [!Note]  
> As barras de ferramentas nas caixas de diálogo não podem ser personalizadas.

 

Para habilitar a personalização, inclua o sinalizador estilo de controles comuns de [**ccs \_ ajustável**](common-control-styles.md) ao criar o controle da barra de ferramentas. Há duas abordagens básicas para a personalização:

-   A caixa de diálogo personalização. Essa caixa de diálogo fornecida pelo sistema é a abordagem mais simples. Ele fornece aos usuários uma interface gráfica do usuário que permite adicionar, excluir ou mover ícones.
-   Ferramentas de arrastar e soltar. A implementação da funcionalidade de arrastar e soltar permite aos usuários mover ferramentas para outro local na barra de ferramentas ou excluí-las arrastando-as para fora da barra de ferramentas. Ele fornece aos usuários uma maneira rápida e fácil de organizar sua barra de ferramentas, mas não permite que elas adicionem ferramentas.

Você pode implementar uma das abordagens ou ambas, dependendo das necessidades do aplicativo. Nenhuma dessas duas abordagens à personalização fornece um mecanismo interno, como um botão cancelar ou desfazer, para retornar a barra de ferramentas ao estado anterior. Você deve usar explicitamente a API de controle da barra de ferramentas para armazenar o estado de prepersonalização da barra de ferramentas. Se necessário, você pode usar essas informações armazenadas posteriormente para restaurar a barra de ferramentas ao seu estado original.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="customization-dialog-box"></a>Caixa de diálogo personalização

A caixa de diálogo personalização é fornecida pelo controle barra de ferramentas para fornecer aos usuários uma maneira simples de adicionar, mover ou excluir ferramentas. Os usuários podem iniciá-lo clicando duas vezes na barra de ferramentas. Os aplicativos podem iniciar a caixa de diálogo de personalização programaticamente enviando o controle Toolbar a uma mensagem de [**\_ personalização de TB**](tb-customize.md) .

A ilustração a seguir mostra um exemplo da caixa de diálogo personalização da barra de ferramentas.

![captura de tela de uma janela com uma barra de ferramentas de três itens e uma caixa de diálogo com listas dos botões da barra de ferramentas disponível e atual](images/tb-customdlg.png)

As ferramentas na caixa de listagem à direita são aquelas atualmente na barra de ferramentas. Inicialmente, essa lista conterá as ferramentas que você especificar ao criar a barra de ferramentas. A caixa de listagem à esquerda contém as ferramentas que estão disponíveis para adicionar à barra de ferramentas. Seu aplicativo é responsável por preencher essa lista (diferente de com o separador, que aparece automaticamente).

O controle Toolbar notifica seu aplicativo de que ele está iniciando uma caixa de diálogo de personalização enviando a janela pai um código de notificação [tbn \_ BEGINADJUST](tbn-beginadjust.md) seguido por um código de notificação [tbn \_ INITCUSTOMIZE](tbn-initcustomize.md) . Na maioria dos casos, o aplicativo não precisa responder a esses códigos de notificação. No entanto, se você não quiser que a caixa de diálogo Personalizar barra de ferramentas exiba um botão ajuda, manipule TBN \_ INITCUSTOMIZE retornando TBNRF \_ HIDEHELP.

O controle ToolBar, em seguida, coleta as informações necessárias para inicializar a caixa de diálogo enviando três séries de códigos de notificação, na seguinte ordem:

-   Um código de notificação [tbn \_ QUERYINSERT](tbn-queryinsert.md) para cada botão na barra de ferramentas para determinar onde os botões podem ser inseridos. Retorne **false** para impedir que um botão seja inserido à esquerda do botão especificado na mensagem de notificação. Se você retornar **false** para todos os \_ códigos de notificação tbn QUERYINSERT, a caixa de diálogo não será exibida.
-   Um código de notificação [tbn \_ QUERYDELETE](tbn-querydelete.md) para cada ferramenta que está atualmente na barra de ferramentas. Retorna **true** se uma ferramenta puder ser excluída ou **false** se não.
-   Uma série de códigos de notificação [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md) para popular a lista de botões disponíveis. Para adicionar um botão à lista, preencha a estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que é passada com o código de notificação e retorna **true**. Quando você não tiver mais ferramentas para adicionar, retorne **false**. Observe que você pode retornar informações para botões que já estão na barra de ferramentas; esses botões não serão adicionados à lista.

A caixa de diálogo é exibida e o usuário pode começar a personalizar a barra de ferramentas.

Quando a caixa de diálogo estiver aberta, seu aplicativo poderá receber uma variedade de códigos de notificação, dependendo das ações do usuário:

-   [Tbn \_ QUERYINSERT](tbn-queryinsert.md). O usuário alterou o local de uma ferramenta na barra de ferramentas ou adicionou uma ferramenta. Retorne **false** para impedir que a ferramenta seja inserida nesse local.
-   [Tbn \_ DELETINGBUTTON](tbn-deletingbutton.md). O usuário está prestes a remover uma ferramenta da barra de ferramentas.
-   [Tbn \_ CUSTHELP](tbn-custhelp.md). O usuário clicou no botão ajuda.
-   [Tbn \_ TOOLBARCHANGE](tbn-toolbarchange.md). O usuário adicionou, moveu ou excluiu uma ferramenta.
-   [Tbn \_ REDEFINIR](tbn-reset.md). O usuário clicou no botão redefinir.

Depois que a caixa de diálogo for destruída, seu aplicativo receberá um código de notificação [tbn \_ endadjust](tbn-endadjust.md) .

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



### <a name="dragging-and-dropping-tools"></a>Ferramentas de arrastar e soltar

Os usuários também podem reorganizar os botões em uma barra de ferramentas pressionando a tecla SHIFT e arrastando o botão para outro local. O processo de arrastar e soltar é manipulado automaticamente pelo controle da barra de ferramentas. Ele exibe uma imagem fantasma do botão conforme ele é arrastado e reorganiza a barra de ferramentas depois que ela é descartada. Os usuários não podem adicionar botões dessa maneira, mas eles podem excluir um botão, removendo-o da barra de ferramentas.

Embora o controle Toolbar normalmente faça essa operação automaticamente, ele também envia os dois códigos de notificação do seu aplicativo: [tbn \_ QUERYDELETE](tbn-querydelete.md) e [tbn \_ QUERYINSERT](tbn-queryinsert.md). Para controlar o processo de arrastar e soltar, manipule esses códigos de notificação da seguinte maneira:

-   O código de notificação [tbn \_ QUERYDELETE](tbn-querydelete.md) é enviado assim que o usuário tenta mover o botão, antes que o botão fantasma seja exibido. Retorne **false** para impedir que o botão seja movido. Se você retornar **true**, o usuário poderá mover a ferramenta ou excluí-la removendo-a da barra de ferramentas. Se uma ferramenta puder ser movida, ela poderá ser excluída. No entanto, se o usuário excluir uma ferramenta, o controle Toolbar enviará ao seu aplicativo um código de notificação [tbn \_ DELETINGBUTTON](tbn-deletingbutton.md) , no ponto em que você pode optar por reinserir o botão em seu local original, cancelando assim a exclusão.
-   O código de notificação [tbn \_ QUERYINSERT](tbn-queryinsert.md) é enviado quando o usuário tenta soltar o botão na barra de ferramentas. Para impedir que o botão que está sendo movido seja Descartado à esquerda do botão especificado na notificação, retorne **false**. Esse código de notificação não será enviado se o usuário descartar a ferramenta para fora da barra de ferramentas.

Se o usuário tentar arrastar um botão sem também pressionar a tecla SHIFT, o controle Toolbar não tratará a operação de arrastar e soltar. No entanto, ele enviará ao seu aplicativo um código de notificação [tbn \_ BEGINDRAG](tbn-begindrag.md) para indicar o início de uma operação de arrastar e um código de notificação do [tbn \_ endarraste](tbn-enddrag.md) para indicar o final. Se você quiser habilitar essa forma de arrastar e soltar, seu aplicativo deverá lidar com esses códigos de notificação, fornecer a interface do usuário necessária e modificar a barra de ferramentas para refletir as alterações.

### <a name="saving-and-restoring-toolbars"></a>Salvando e restaurando barras de ferramentas

No processo de personalização de uma barra de ferramentas, seu aplicativo pode precisar salvar informações para que você possa restaurar a barra de ferramentas para seu estado original. Para iniciar o salvamento ou a restauração de um estado de barra de ferramentas, envie a barra de ferramentas para uma mensagem [**\_ SAVERESTORE TB**](tb-saverestore.md) com o *lParam* definido como **true**. O valor de *lParam* dessa mensagem Especifica se você está solicitando uma operação de salvamento ou de restauração. Depois que a mensagem é enviada, há duas maneiras de lidar com a operação de salvar/restaurar:

-   Com os controles comuns [versão 4,72](common-control-versions.md) e anteriores, você deve implementar um manipulador [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md) . O controle Toolbar envia esse código de notificação para solicitar informações sobre cada botão à medida que ele é restaurado.
-   A versão 5,80 inclui uma opção salvar/restaurar. No início do processo e, como cada botão é salvo ou restaurado, seu aplicativo receberá um código de notificação [tbn \_ Save](tbn-save.md) ou [tbn \_ Restore](tbn-restore.md) . Para usar essa opção, você deve implementar manipuladores de notificação para fornecer as informações de bitmap e estado necessárias para salvar ou restaurar com êxito o estado da barra de ferramentas.

Os Estados da barra de ferramentas são salvos em um fluxo de dados que consiste em blocos de dados definidos por shell alternando com blocos de dados definidos pelo aplicativo. Um bloco de dados de cada tipo é armazenado para cada botão, juntamente com um bloco opcional de dados globais que os aplicativos podem posicionar no início do fluxo. Durante o processo de salvamento, o manipulador de [ \_ salvamento do tbn](tbn-save.md) adiciona os blocos definidos pelo aplicativo ao fluxo de dados. Durante o processo de restauração, o manipulador de [ \_ restauração tbn](tbn-restore.md) lê cada bloco e fornece ao shell as informações necessárias para reconstruir a barra de ferramentas.

### <a name="how-to-handle-a-tbn_save-notification"></a>Como lidar com uma notificação de salvamento de TBN \_

O primeiro código de notificação [tbn \_ Save](tbn-save.md) é enviado no início do processo de salvamento. Antes que todos os botões sejam salvos, os membros da estrutura [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) são definidos conforme mostrado na tabela a seguir.



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

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




