---
title: Caixa de diálogo Imprimir
description: A caixa de diálogo Imprimir permite que o usuário selecione opções para um trabalho de impressão específico.
ms.assetid: 34f69b25-8a89-4322-af4c-a80b85a4a973
keywords:
- Windows Interface do Usuário, entrada do usuário
- Windows Interface do Usuário, Biblioteca de Caixas de Diálogo Comuns
- entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- capturando entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- Biblioteca de caixas de diálogo comuns
- caixas de diálogo comuns
- caixa de diálogo Imprimir
- Caixa de diálogo Configuração de Impressão
- personalização da caixa de diálogo Imprimir
- caixas de diálogo predefinidos
- caixas de diálogo, Imprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afd8cfa31a83f664e859cd93acc9d28543b7ab00dcb8f130fdbac329cd1429e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720909"
---
# <a name="print-dialog-box"></a>Caixa de diálogo Imprimir

A **caixa de** diálogo Imprimir permite que o usuário selecione opções para um trabalho de impressão específico. Por exemplo, o usuário pode especificar a impressora a ser usada, o intervalo de páginas a imprimir e o número de cópias.

Você pode usar [a](print-property-sheet.md) [**função PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para exibir  uma Folha de Propriedades de Impressão , que tem uma página Geral que contém controles semelhantes à **caixa** de diálogo Imprimir. A folha de propriedades também pode ter páginas de propriedades adicionais específicas do aplicativo e específicas do driver seguindo a **página** Geral.

Você cria e exibe uma **caixa de** diálogo Imprimir inicializando uma estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e passando a estrutura para a [**função PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))

A ilustração a seguir mostra uma caixa **de diálogo Imprimir** típica.

![caixa de diálogo imprimir](images/printdialogboxxp.png)

Se o usuário clicar no **botão OK,** [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retornará **TRUE** e usará a estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para retornar informações sobre as seleções do usuário. Por exemplo, os **membros hDevMode** e **hDevNames** normalmente retornam alças de memória global para estruturas [**e DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Você pode usar as informações nessas estruturas para criar um contexto de dispositivo ou um contexto de informações para a impressora selecionada.

Se o usuário cancelar a caixa **de diálogo** Imprimir ou ocorrer um erro, [**PrintDlg retornará**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) **FALSE.** Você pode determinar a causa de um erro usando a [**função CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

A **caixa de** diálogo  Imprimir inclui um grupo intervalo de impressão de botões de opção que indicam se o usuário deseja imprimir todas as páginas, um intervalo de páginas ou apenas o texto selecionado. Antes de [**chamar PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)), você pode definir um dos sinalizadores **PD \_ ALLPAGES,** **PD \_ SELECTION** ou **PD \_ PAGENUMS** para indicar qual botão está selecionado inicialmente. Quando **PrintDlg** retorna **TRUE**, a função define um desses sinalizadores para indicar as seleções do usuário. Se **PD \_ PAGENUMS** for definido, os membros **nFromPage** e **nToPage** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) conterão as páginas inicial e final especificadas pelo usuário. Para desabilitar **o botão** de rádio Páginas e seus controles de edição **de** e **para** associados, de definir o sinalizador **PD \_ NOPAGENUMS.** Para desabilitar **o botão** de rádio Seleção, demarque o **sinalizador PD \_ NOSELECTION.**

A caixa de diálogo inclui um controle de edição no qual o usuário pode digitar o número de cópias a serem impressas. Se o **membro hDevMode** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) for não **NULL,** o membro **dmCopies** da estrutura especificará o valor inicial para esse controle de edição. Se **hDevMode** for **NULL,** o **membro nCopies** da estrutura **PRINTDLG** especificará o valor inicial. Quando [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retorna, **o nCopies** normalmente indica o número de cópias especificadas pelo usuário. No entanto, se você definir o sinalizador **PD \_ USEDEVMODECOPIESANDCOLLATE** ao criar a caixa de diálogo, **nCopies** será sempre definido como 1 no retorno e o membro **dmCopies** [**de DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) indicará o número de cópias a serem impressas.

A **caixa de seleção Collate** indica se o usuário deseja collar as páginas se várias cópias estão sendo impressas. O **sinalizador \_ COLLATE de PD** será definido se a caixa de seleção **Collate** estiver marcada. Se seu aplicativo não dá suporte a várias cópias ou a uma colagem simulada, defina o sinalizador **PD \_ USEDEVMODECOPIESANDCOLLATE** no membro **Flags** da estrutura [**PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Isso desabilita a caixa de  **seleção Collate** e o controle de edição Número de Cópias, a menos que o driver de impressora seja compatível com várias cópias e uma colagem.

A **caixa de seleção** Imprimir em Arquivo indica se o usuário deseja enviar a saída para um arquivo em vez de para uma impressora. Você pode definir o **sinalizador PD \_ PRINTTOFILE** para que a caixa de seleção seja selecionada inicialmente. Para ocultar a caixa de seleção, de definido o **sinalizador \_ PD HIDEPRINTTOFILE.** Para desabilitá-lo, de definido **o sinalizador PD \_ DISABLEPRINTTOFILE.** Se o usuário  selecionar a opção Imprimir no Arquivo, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) define o sinalizador **PD \_ PRINTTOFILE** e retorna "FILE:" no deslocamento indicado pelo **membro wOutputOffset** da estrutura [**DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Ao chamar a função para iniciar a operação de impressão, especifique essa cadeia de caracteres "FILE:" no membro **lpszOutput** da estrutura. Especificar essa cadeia de caracteres faz com que o subsistema de impressão consulte o usuário quanto ao nome do arquivo de saída.

Por padrão, a **caixa de** diálogo Imprimir exibe inicialmente informações sobre a impressora padrão atual. Para exibir informações de outra impressora instalada, inicialize um e uma estrutura [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e atribua o alça de memória global à estrutura aos membros **hDevMode** e **hDevNames.** O nome do dispositivo especificado no membro **dmDeviceName** da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e no **membro wDriverOffset** da estrutura **DEVNAMES** deve identificar um dispositivo de impressora que também está listado na seção Dispositivos do arquivo \[ \] Win.ini. Se o dispositivo não estiver listado, [**PrintDlg retornará**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) um erro.

Você pode direcionar [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para criar um contexto de dispositivo ou contexto de informações para a impressora definindo o **sinalizador \_ RETURNDC** pd ou **PD \_ RETURNIC** no membro **Flags** da estrutura [**PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) A função retorna um handle para o contexto do dispositivo ou contexto de informações no **membro hDC.** Se você usar o **sinalizador PD \_ RETURNDC,** poderá usar o contexto do dispositivo para gerar a saída para a impressora.

Para recuperar informações sobre a impressora padrão sem exibir a **caixa** de diálogo Imprimir, de definido o sinalizador **PD \_ RETURNDEFAULT.** Nesse caso, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retorna imediatamente depois de definir os membros **hDevMode** e **hDevNames** para lidar com estruturas que contêm as informações.

Por padrão, [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) exibe caixas de mensagem quando ocorrem erros. Por exemplo, a função exibirá uma mensagem de erro se nenhuma impressora estiver instalada. Para impedir que a função exibe essas mensagens de aviso, de definir o **sinalizador PD \_ NOWARNING.**

Os tópicos a seguir são discutidos nesta seção.

-   [Personalização da caixa de diálogo Imprimir](#customizing-the-print-dialog-box)
-   [Caixa de diálogo Configuração de Impressão](#print-setup-dialog-box)

## <a name="customizing-the-print-dialog-box"></a>Personalização da caixa de diálogo Imprimir

Você pode fornecer um modelo personalizado para a **caixa** de diálogo Imprimir, por exemplo, se quiser incluir controles adicionais exclusivos para seu aplicativo. A [**função PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) usa seu modelo personalizado no lugar do modelo padrão.

Para fornecer um modelo personalizado para a **caixa de diálogo** Imprimir:

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Prnsetup.dlg. Os identificadores de controle usados no **modelo** de caixa de diálogo Imprimir padrão são definidos no arquivo Dlgs.h.
2.  Use a [**estrutura PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para habilitar o modelo da seguinte forma:
    -   Se o modelo personalizado for um recurso em um aplicativo ou biblioteca de vínculo dinâmico, de definir o sinalizador **PD \_ ENABLEPRINTTEMPLATE** no **membro Sinalizadores.** Use os **membros hInstance** e **lpPrintTemplateName** da estrutura para identificar o módulo e o nome do recurso.

        -Ou-

    -   Se o modelo personalizado já estiver na memória, de definir o **sinalizador PD \_ ENABLEPRINTTEMPLATEHANDLE.** Use o **membro hPrintTemplate** para identificar o objeto de memória que contém o modelo.

Você pode fornecer um procedimento de gancho [**PrintHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc) para a **caixa de diálogo** Imprimir. O procedimento de gancho pode processar mensagens enviadas para a caixa de diálogo. Ele também pode enviar mensagens para a caixa de diálogo. Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho para processar a entrada para seus controles.

Para habilitar um procedimento de gancho para a **caixa de diálogo** Imprimir:

1.  Defina **o sinalizador PD \_ ENABLEPRINTHOOK** no **membro Flags** da [**estrutura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
2.  Especifique o endereço do procedimento de gancho no **membro lpfnPrintHook.**

Depois de processar sua [**mensagem WM \_ INITDIALOG,**](wm-initdialog.md) o procedimento da caixa de diálogo envia uma mensagem **WM \_ INITDIALOG** para o procedimento de gancho. O *parâmetro lParam* dessa mensagem é um ponteiro para a estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) usada para inicializar a caixa de diálogo.

## <a name="print-setup-dialog-box"></a>Caixa de diálogo Configuração de Impressão

Você pode criar e exibir **uma** caixa de diálogo Instalação de Impressão definindo o sinalizador **PD \_ PRINTSETUP** em uma chamada para a [**função PrintDlg.**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) No entanto, **a caixa de** diálogo Instalação de Impressão foi superada pela caixa de diálogo **Configuração** de Página e não deve ser usada em novos aplicativos.

Os seguintes sinalizadores se aplicam somente à caixa **de diálogo Instalação** de Impressão:

-   **PD \_ ENABLESETUPHOOK**
-   **PD \_ ENABLESETUPTEMPLATE**
-   **PD \_ ENABLESETUPTEMPLATEHANDLE**

 

 