---
title: Caixa de diálogo Imprimir
description: A caixa de diálogo Imprimir permite que o usuário selecione opções para um trabalho de impressão específico.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Interface do usuário do Windows, entrada do usuário
- Interface do usuário do Windows, biblioteca de caixa de diálogo comum
- entrada do usuário, biblioteca de caixa de diálogo comum
- capturando entrada do usuário, biblioteca de caixa de diálogo comum
- Biblioteca de caixa de diálogo comum
- caixas de diálogo comuns
- caixa de diálogo Imprimir
- Caixa de diálogo Configurar impressão
- Personalizando a caixa de diálogo de impressão
- caixas de diálogo predefinidas
- caixas de diálogo, imprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fae1dd244391ea16478a0cb4f10803cf622dc64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084872"
---
# <a name="print-dialog-box"></a>Caixa de diálogo Imprimir

A caixa de diálogo **Imprimir** permite que o usuário selecione opções para um trabalho de impressão específico. Por exemplo, o usuário pode especificar a impressora a ser usada, o intervalo de páginas a ser impresso e o número de cópias.

Você pode usar a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para exibir uma [folha de propriedades de impressão](print-property-sheet.md), que tem uma página **geral** contendo controles semelhantes à caixa de diálogo **Imprimir** . A folha de propriedades também pode ter páginas de propriedades adicionais específicas do aplicativo e do driver, seguindo a página **geral** .

Você cria e exibe uma caixa de diálogo de **impressão** inicializando uma estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e passando a estrutura para a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .

A ilustração a seguir mostra uma caixa de diálogo de **impressão** típica.

![caixa de diálogo Imprimir](images/printdialogboxxp.png)

Se o usuário clicar no botão **OK** , [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retornará **true** e usará a estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para retornar informações sobre as seleções do usuário. Por exemplo, os membros **hDevMode** e **hDevNames** normalmente retornam identificadores de memória global para estruturas e [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Você pode usar as informações nessas estruturas para criar um contexto de dispositivo ou um contexto de informações para a impressora selecionada.

Se o usuário cancelar a caixa de diálogo de **impressão** ou ocorrer um erro, [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retornará **false**. Você pode determinar a causa de um erro usando a função [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

A caixa de diálogo **Imprimir** inclui um grupo de **intervalos de impressão** de botões de opção que indicam se o usuário deseja imprimir todas as páginas, um intervalo de páginas ou apenas o texto selecionado. Antes de chamar [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)), você pode definir um dos sinalizadores **PD \_**, seleção de **PD \_** ou **PD \_ PAGENUMS** para indicar qual botão está inicialmente selecionado. Quando **PRINTDLG** retorna **true**, a função define um desses sinalizadores para indicar as seleções do usuário. Se **PD \_ PAGENUMS** for definido, os membros **nFromPage** e **nToPage** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) conterão as páginas inicial e final especificadas pelo usuário. Para desabilitar o botão de opção **páginas** e seu associado **de** e **para** editar controles, defina o sinalizador **PD \_ NOPAGENUMS** . Para desabilitar o botão de opção **seleção** , defina o sinalizador **PD \_ noseleções** .

A caixa de diálogo inclui um controle de edição no qual o usuário pode digitar o número de cópias a serem impressas. Se o membro **hDevMode** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) for não **nulo**, o membro **dmCopies** da estrutura especificará o valor inicial para esse controle de edição. Se **hDevMode** for **NULL**, o membro **nCopies** da estrutura **PRINTDLG** especificará o valor inicial. Quando [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retorna, **nCopies** normalmente indica o número de cópias especificado pelo usuário. No entanto, se você definir o sinalizador **PD \_ USEDEVMODECOPIESANDCOLLATE** ao criar a caixa de diálogo, **nCopies** será sempre definido como 1 no retorno e o membro **dmCopies** de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) indicará o número de cópias a serem impressas.

A caixa de seleção **Agrupar** indica se o usuário deseja agrupar as páginas se várias cópias estiverem sendo impressas. O sinalizador de **\_ agrupamento PD** será definido se a caixa de seleção **Agrupar** estiver marcada. Se seu aplicativo não oferecer suporte a várias cópias ou agrupamento simulado, defina o sinalizador **PD \_ USEDEVMODECOPIESANDCOLLATE** no membro **flags** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Isso desabilita a caixa de seleção **Agrupar** e o **número de cópias** Editar controle, a menos que o driver de impressora dê suporte a várias cópias e agrupamento.

A caixa de seleção **Imprimir em arquivo** indica se o usuário deseja enviar a saída para um arquivo em vez de para uma impressora. Você pode definir o sinalizador **PD \_ PRINTTOFILE** para que a caixa de seleção seja selecionada inicialmente. Para ocultar a caixa de seleção, defina o sinalizador **PD \_ HIDEPRINTTOFILE** . Para desabilitá-lo, defina o sinalizador **PD \_ DISABLEPRINTTOFILE** . Se o usuário selecionar a opção **Imprimir em arquivo** , [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) definirá o sinalizador **PD \_ PRINTTOFILE** e retornará "file:" no deslocamento indicado pelo membro **wOutputOffset** da estrutura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Quando você chamar a função para iniciar a operação de impressão, especifique essa cadeia de caracteres "FILE:" no membro **lpszOutput** da estrutura. A especificação dessa cadeia de caracteres faz com que o subsistema de impressão consulte o usuário para obter o nome do arquivo de saída.

Por padrão, a caixa de diálogo **Imprimir** inicialmente exibe informações sobre a impressora padrão atual. Para exibir informações de outra impressora instalada, inicialize a e uma estrutura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e atribua o identificador de memória global à estrutura para os membros **hDevMode** e **hDevNames** . O nome do dispositivo que você especifica no membro **dmDeviceName** da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e no membro **wDriverOffset** da estrutura **DEVNAMES** deve identificar um dispositivo de impressora que também esteja listado na \[ \] seção dispositivos do arquivo Win.ini. Se o dispositivo não estiver listado, [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retornará um erro.

Você pode direcionar o [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para criar um contexto de dispositivo ou um contexto de informações para a impressora, definindo o sinalizador de **\_ retorno** de **PD \_ RETURNDC** ou PD no membro **flags** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . A função retorna um identificador para o contexto do dispositivo ou o contexto de informações no membro **HDC** . Se você usar o sinalizador **PD \_ RETURNDC** , poderá usar o contexto do dispositivo para gerar a saída para a impressora.

Para recuperar informações sobre a impressora padrão sem exibir a caixa de diálogo **Imprimir** , defina o sinalizador **PD \_ RETURNDEFAULT** . Nesse caso, [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retorna imediatamente após a definição dos membros **hDevMode** e **hDevNames** como identificadores para estruturas que contêm as informações.

Por padrão, o [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) exibe caixas de mensagens quando ocorrem erros. Por exemplo, a função exibirá uma mensagem de erro se nenhuma impressora estiver instalada. Para impedir que a função exiba essas mensagens de aviso, defina o sinalizador **PD \_ nowarning** .

Os tópicos a seguir são discutidos nesta seção.

-   [Personalizando a caixa de diálogo Imprimir](#customizing-the-print-dialog-box)
-   [Caixa de diálogo Configurar impressão](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Personalizando a caixa de diálogo Imprimir

Você pode fornecer um modelo personalizado para a caixa de diálogo **Imprimir** , por exemplo, se desejar incluir controles adicionais que sejam exclusivos para seu aplicativo. A função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) usa o modelo personalizado no lugar do modelo padrão.

Para fornecer um modelo personalizado para a caixa de diálogo **Imprimir** :

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Prnsetup. Dlg. Os identificadores de controle usados no modelo de caixa de diálogo de **impressão** padrão são definidos no arquivo Dlgs. h.
2.  Use a estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para habilitar o modelo da seguinte maneira:
    -   Se o modelo personalizado for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina o sinalizador **PD \_ ENABLEPRINTTEMPLATE** no membro **flags** . Use os membros **HINSTANCE** e **lpPrintTemplateName** da estrutura para identificar o módulo e o nome do recurso.

        -Ou-

    -   Se o modelo personalizado já estiver na memória, defina o sinalizador **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Use o membro **hPrintTemplate** para identificar o objeto de memória que contém o modelo.

Você pode fornecer um procedimento de gancho [**PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) para a caixa de diálogo **Imprimir** . O procedimento de gancho pode processar mensagens enviadas para a caixa de diálogo. Ele também pode enviar mensagens para a caixa de diálogo. Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho para processar a entrada para seus controles.

Para habilitar um procedimento de gancho para a caixa de diálogo **Imprimir** :

1.  Defina o sinalizador **PD \_ ENABLEPRINTHOOK** no membro **flags** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Especifique o endereço do procedimento de gancho no membro **lpfnPrintHook** .

Depois de processar sua mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) , o procedimento da caixa de diálogo envia uma mensagem do **WM \_ INITDIALOG** para o procedimento de gancho. O parâmetro *lParam* dessa mensagem é um ponteiro para a estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) usada para inicializar a caixa de diálogo.

## <a name="print-setup-dialog-box"></a>Caixa de diálogo Configurar impressão

Você pode criar e exibir uma caixa de diálogo de **configuração de impressão** definindo o sinalizador de **\_ metaconfiguração de PD** em uma chamada para a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . No entanto, a caixa de diálogo **configuração de impressão** foi substituída pela caixa de diálogo **Configurar página** e não deve ser usada em novos aplicativos.

Os sinalizadores a seguir se aplicam somente à caixa de diálogo **configuração de impressão** :

-   **\_ENABLESETUPHOOK PD**
-   **\_ENABLESETUPTEMPLATE PD**
-   **\_ENABLESETUPTEMPLATEHANDLE PD**

 

 