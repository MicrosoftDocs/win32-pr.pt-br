---
title: Caixa de diálogo de fonte
description: A caixa de diálogo fonte permite que o usuário escolha atributos para uma fonte lógica, como família de fontes e estilo de fonte associado, tamanho do ponto, efeitos (sublinhado, riscado e cor do texto) e um script (ou conjunto de caracteres).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Interface do usuário do Windows, entrada do usuário
- Interface do usuário do Windows, biblioteca de caixa de diálogo comum
- entrada do usuário, biblioteca de caixa de diálogo comum
- capturando entrada do usuário, biblioteca de caixa de diálogo comum
- Biblioteca de caixa de diálogo comum
- caixas de diálogo comuns
- caixa de diálogo Fonte
- caixa de diálogo Personalizando fonte
- sinalizadores, caixa de diálogo fonte
- sinalizadores de inicialização
- caixas de diálogo predefinidas
- caixas de diálogo, fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a752ce53ecf496c58efb0c346a8c3d67c4f1b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008301"
---
# <a name="font-dialog-box"></a>Caixa de diálogo de fonte

A caixa de diálogo **fonte** permite que o usuário escolha atributos para uma fonte lógica, como família de fontes e estilo de fonte associado, tamanho do ponto, efeitos (sublinhado, riscado e cor do texto) e um script (ou conjunto de caracteres).

Você cria e exibe uma caixa de diálogo de **fonte** inicializando uma estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e passando a estrutura para a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

A captura de tela a seguir mostra uma caixa de diálogo de **fonte** típica.

![captura de tela mostrando a caixa de diálogo fonte](images/fontdialogboxxp.png)

Se o usuário clicar no botão **OK** , a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornará **true** e definirá as informações sobre a seleção do usuário na estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .

Se o usuário cancelar a caixa de diálogo **fonte** ou ocorrer um erro, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornará **false** e o conteúdo da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) não será definido. Você pode determinar a causa de um erro usando a função [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

Os tópicos a seguir são discutidos nesta seção.

-   [Sinalizadores de inicialização da caixa de diálogo de fonte](#font-dialog-box-initialization-flags)
-   [Personalizando a caixa de diálogo fonte em versões anteriores do Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Personalizando a caixa de diálogo fonte no Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Sinalizadores de inicialização da caixa de diálogo de fonte

Antes de [**chamar ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), o membro **flags** da [**estrutura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) deve especificar o **CF \_ SCREENFONTS**, o **CF \_ PRINTERFONTS** ou **\_ o CF ambos**, para indicar se a caixa de diálogo deve listar as fontes da tela, as fontes da impressora ou ambos. Se você especificar **o CF \_ PRINTERFONTS** ou o CF, o membro **HDC** da estrutura **ChooseFont** deverá especificar um identificador para um contexto de dispositivo para a impressora. **\_**

Se o sinalizador **CF \_ PRINTERFONTS** ou **CF \_ both** for definido, o rótulo de descrição do tipo de fonte aparecerá na parte inferior da caixa de diálogo **fonte** .

A partir do Windows 7, os sinalizadores do **CF \_ PRINTERFONTS**, do **CF \_ SCREENFONTS**, do **CF \_ ambos** e do **CF \_ WYSIWYG** não são mais usados pela função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para a enumeração de fontes. Eles são obsoletos no Windows 7. No entanto, o sinalizador **\_ PRINTERFONTS do CF** retém uma função: para exibir o rótulo de descrição do tipo de fonte na parte inferior da caixa de diálogo **fonte** .

Você pode usar o membro **flags** para habilitar ou desabilitar alguns dos controles da caixa de diálogo **fonte** , e pode usar o membro **flags** em conjunto com outros membros [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para controlar os valores iniciais de alguns controles.

**Para exibir os controles que permitem ao usuário selecionar as opções de riscar, sublinhado e cor:**

-   Defina o sinalizador de **\_ efeitos do CF** . Você pode usar o membro **rgbColors** da estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar uma cor de fonte inicial.

**Para especificar os valores iniciais dos controles de caixa de diálogo fonte, estilo da fonte, tamanho, riscado e sublinhado:**

1.  Para especificar os valores iniciais dos controles de caixa de diálogo fonte, estilo da fonte, tamanho, riscado e sublinhado:
2.  Defina o **sinalizador \_ INITTOLOGFONTSTRUCT do CF** no **membro flags** , juntamente com os membros da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) apontada pelo **lpLogFont**, para especificar os valores iniciais para os atributos de fonte.
3.  Você também pode usar os **sinalizadores \_ NOFACESEL CF**, **CF \_ NOSTYLESEL** e **CF \_ NOSIZESEL** para impedir que a caixa de diálogo **fonte** exiba valores iniciais para os controles correspondentes. Isso é útil quando você está trabalhando com uma seleção de texto que tem mais de uma face de tipos, estilo ou tamanho de ponto. Esses valores também serão definidos em **sinalizadores** quando [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornar, se o usuário não tiver selecionado um valor correspondente.

**Para inicializar o controle de estilo da fonte para um nome de estilo especificado**

-   Defina o **sinalizador \_ USESTYLE do CF** e use o membro **lpszStyle** para especificar o nome do estilo.

> [!Note]  
> Para globalizar seu aplicativo, especifique o estilo usando os membros **lfWeight** e **LfItalic** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) apontada por **lpLogFont**. O nome do estilo pode ser alterado dependendo do idioma da interface do usuário do sistema.

 

**Para exibir o botão aplicar**

-   Defina o sinalizador de **\_ aplicação do CF** e forneça um procedimento de gancho para processar mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para o botão **aplicar** . O procedimento de gancho pode enviar a mensagem [**\_ \_ GETLOGFONT do WM ChooseFont**](wm-choosefont-getlogfont.md) para a caixa de diálogo para recuperar o endereço da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém as seleções atuais da fonte.

**Para exibir o botão ajuda**

-   Defina o **sinalizador \_ SHOWHELP de CF** . O membro **hwndOwner** deve identificar a janela para receber a mensagem registrada [**HELPMSGSTRING**](helpmsgstring.md) quando o usuário clica no botão **ajuda** .

**Para restringir as fontes exibidas na caixa de diálogo**

-   Defina qualquer combinação dos sinalizadores **CF \_ TTONLY**, **CF \_ FIXEDPITCHONLY**, **CF \_ NOVECTORFONTS**, **CF \_ NOVERTFONTS**, **CF \_ SCALABLEONLY** e **CF \_ WYSIWYG** . Você também pode restringir os estilos disponíveis que a caixa de diálogo exibe para algumas fontes usando o valor do **CF \_ nosimulations** .

A partir do Windows 7, a lista de fontes exibida na caixa de diálogo é restrita com base nas fontes mostradas pelo usuário. Para remover a restrição, defina o **sinalizador \_ INACTIVEFONTS do CF** .

**Para restringir os nomes de tipos, estilos e tamanhos de pontos que o usuário pode especificar**

1.  Defina o **sinalizador \_ FORCEFONTEXIST do CF** para restringir o usuário a especificar somente nomes de tipos, estilos e tamanhos de pontos válidos listados na caixa de diálogo.
2.  Defina o sinalizador de **\_ limite de CF** para restringir o usuário a especificar os tamanhos de ponto no intervalo especificado pelos membros **nSizeMin** e **nSizeMax** .

**Para restringir ou desabilitar a caixa de combinação de scripts**

-   Defina o **sinalizador \_ NOSCRIPTSEL do CF** para desabilitar a caixa de combinação **scripts** ou defina o sinalizador **\_ SELECTSCRIPT do CF** para restringir as seleções na caixa de combinação **scripts** a um conjunto de caracteres especificado.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Personalizando a caixa de diálogo fonte em versões anteriores do Windows

Você pode fornecer um modelo personalizado para a caixa de diálogo **fonte** , por exemplo, se desejar incluir controles adicionais que são exclusivos para seu aplicativo. A função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usa o modelo personalizado no lugar do modelo padrão.

**Para fornecer um modelo personalizado para a caixa de diálogo fonte**

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Font. Dlg. Os identificadores de controle usados no modelo de caixa de diálogo fonte padrão são definidos no arquivo Dlgs. h.
2.  Use a estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para habilitar o modelo da seguinte maneira:
    -   Se o modelo personalizado for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina o sinalizador de **\_ habilitação do CF** no membro **flags** . Use os membros **HINSTANCE** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso.
    -   Se o modelo personalizado já estiver na memória, defina o **sinalizador \_ ENABLETEMPLATEHANDLE do CF** . Use o membro **HINSTANCE** para identificar o objeto de memória que contém o modelo.

Você pode fornecer um procedimento de gancho [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para a caixa de diálogo **fonte** . O procedimento de gancho pode processar mensagens enviadas para a caixa de diálogo e enviar mensagens para a caixa de diálogo. Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho para processar a entrada para seus controles.

**Para habilitar um procedimento de gancho para a caixa de diálogo fonte**

1.  Defina o **sinalizador \_ ENABLEHOOK do CF** no membro **flags** da estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) .
2.  Especifique o endereço do procedimento de gancho no membro **lpfnHook** .

Depois de processar a mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) , o procedimento da caixa de diálogo envia uma mensagem do **WM \_ INITDIALOG** para o procedimento de gancho. O parâmetro *lParam* dessa mensagem é um ponteiro para a estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) que é usada para inicializar a caixa de diálogo.

O procedimento de gancho pode enviar o [**WM \_ ChooseFont \_ GETLOGFONT**](wm-choosefont-getlogfont.md), o [**WM \_ ChooseFont \_ SETLOGFONT**](wm-choosefont-setlogfont.md)e o [**WM \_ ChooseFont \_ setsinaliza**](wm-choosefont-setflags.md) as mensagens para a caixa de diálogo para obter e definir os valores e sinalizadores atuais da caixa de diálogo.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Personalizando a caixa de diálogo fonte no Windows 7

A captura de tela a seguir mostra uma caixa de diálogo de **fonte** típica no Windows 7.

![captura de tela mostrando a caixa de dialob da fonte](images/fontdialogboxwin7.png)

Nas versões anteriores do Windows, o arquivo de modelo Font. DLG contém um modelo ChooseFont padrão. O arquivo de modelo Font. DLG no Windows 7 contém dois modelos padrão: o modelo padrão de versões anteriores do Windows e o novo modelo do Windows 7 ChooseFont. Portanto, ao personalizar a caixa de diálogo **fonte** no Windows 7, você deve considerar os seguintes problemas.

1.  Use o novo modelo ao criar modelos personalizados para aplicativos executados no Windows 7. Esse novo modelo contém um controle de link no qual o usuário pode clicar para iniciar a janela **painel de controle de fontes** , conforme mostrado na captura de tela a seguir.

    ![captura de tela mostrando o painel de controle fonte no Windows 7](images/fontcontrolpanelforwin7.png)

2.  Para usar esse controle de link, seu aplicativo de chamada deve usar o COMCTL32.DLL versão 6 ou posterior. Caso contrário, a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornará um erro ao tentar criar o controle de link em seu modelo personalizado. Para determinar se esse controle está habilitado, compile seu aplicativo de chamada em relação ao COMCTL32.DLL versão 6,0. Para obter mais informações, consulte [habilitando estilos visuais com controles comuns](/previous-versions//ms649781(v=vs.85)).
3.  Se seu aplicativo usar COMCTL32.DLL versão 5,0 ou anterior, você deverá fazer o seguinte ao criar um modelo personalizado:

    -   Especifique o controle como um botão de **pressão**. O controle usado para iniciar o **painel de controle de fontes** aparecerá como um botão, e não como um link.
    -   Substitua o seguinte texto na Font. DLG:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        pelo seguinte texto:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   Para garantir que seu aplicativo use um modelo personalizado, você deve especificar um modelo personalizado com o sinalizador de **\_ habilitação do CF** , criar um modelo personalizado com base no modelo ChooseFont do Windows 7 e, opcionalmente, habilitar um procedimento de gancho.

        Se você habilitar um procedimento de gancho sem criar um modelo personalizado, o modelo de ChooseFont padrão para versões anteriores do Windows será carregado.

> [!Note]  
> Você deve especificar o tipo de **controle de controle ou de** **pressão** no novo modelo, dependendo da versão do COMMCTL.DLL em que seu aplicativo é compilado. Observe também que os recursos específicos do Windows 7, como exibição WYSIWYG de listas de fontes e famílias estendidas, não estão disponíveis quando seus aplicativos são executados em versões anteriores do sistema operacional Windows.

 

 

 