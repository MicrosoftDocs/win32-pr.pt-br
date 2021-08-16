---
title: Caixa de diálogo de fonte
description: A caixa de diálogo Fonte permite que o usuário escolha atributos para uma fonte lógica, como família de fontes e estilo de fonte associado, tamanho do ponto, efeitos (sublinhado, destaque e cor do texto) e um script (ou conjunto de caracteres).
ms.assetid: e8a996aa-4e34-45d0-a325-9c20b1a6ce07
keywords:
- Windows Interface do Usuário, entrada do usuário
- Windows Interface do Usuário, Biblioteca de Caixas de Diálogo Comuns
- entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- capturando entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- Biblioteca de caixas de diálogo comuns
- caixas de diálogo comuns
- caixa de diálogo Fonte
- personalização da caixa de diálogo Fonte
- sinalizadores, caixa de diálogo Fonte
- sinalizadores de inicialização
- caixas de diálogo predefinidos
- caixas de diálogo, Fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8544fcb60e499a360f60d1701863a11138d3f16fb06a770a9a2763800d908e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785873"
---
# <a name="font-dialog-box"></a>Caixa de diálogo de fonte

A  caixa de diálogo Fonte permite que o usuário escolha atributos para uma fonte lógica, como família de fontes e estilo de fonte associado, tamanho do ponto, efeitos (sublinhado, destaque e cor do texto) e um script (ou conjunto de caracteres).

Você cria e exibe uma **caixa de** diálogo Fonte inicializando uma estrutura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e passando a estrutura para a [**função ChooseFont.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)

A captura de tela a seguir mostra uma caixa de **diálogo Fonte** típica.

![captura de tela mostrando a caixa de diálogo de fonte](images/fontdialogboxxp.png)

Se o usuário clicar no **botão OK,** a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornará **TRUE** e define as informações sobre a seleção do usuário na [**estrutura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)

Se o usuário cancelar a **caixa** de diálogo Fonte ou ocorrer um erro, [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornará **FALSE** e o conteúdo da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) não será definido. Você pode determinar a causa de um erro usando a [**função CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

Os tópicos a seguir são discutidos nesta seção.

-   [Sinalizadores de inicialização da caixa de diálogo fonte](#font-dialog-box-initialization-flags)
-   [Personalização da caixa de diálogo Fonte em versões anteriores do Windows](#customizing-the-font-dialog-box-on-earlier-versions-of-windows)
-   [Personalização da caixa de diálogo Fonte no Windows 7](#customizing-the-font-dialog-box-on-windows-7)

## <a name="font-dialog-box-initialization-flags"></a>Sinalizadores de inicialização da caixa de diálogo fonte

Antes de chamar [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), o membro **Flags** da estrutura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) deve especificar **CF \_ SCREENFONTS,** **CF \_ PRINTERFONTS** ou **CF \_ BOTH** para indicar se a caixa de diálogo deve listar fontes de tela, fontes de impressora ou ambas. Se você especificar **CF \_ PRINTERFONTS** ou **CF \_ BOTH**, o membro **hDC** da estrutura **CHOOSEFONT** deverá especificar um handle para um contexto de dispositivo para a impressora.

Se o **sinalizador CF \_ PRINTERFONTS** ou **CF \_ BOTH** estiver definido, o rótulo de descrição do tipo de fonte aparecerá na parte inferior da caixa **de** diálogo Fonte.

A partir do Windows 7, os sinalizadores **CF \_ PRINTERFONTS**, **CF \_ SCREENFONTS,** **CF \_ BOTH** e **CF \_ WYSIWYG** não são mais usados pela função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para enumeração de fonte. Eles estão obsoletos no Windows 7. No entanto, **o sinalizador \_ CF PRINTERFONTS** retém uma função: para exibir o rótulo de descrição do tipo de fonte na parte inferior da caixa **de** diálogo Fonte.

Você pode usar o membro **Flags** para  habilitar ou desabilitar alguns dos controles da caixa de diálogo Fonte e pode usar o membro Flags em conjunto com outros [**membros CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para controlar os valores iniciais de alguns **controles.**

**Para exibir os controles que permitem que o usuário selecione opções de destaque, sublinhado e cor:**

-   De definir o **sinalizador \_ EFEITOS DO CF.** Você pode usar o **membro rgbColors** da estrutura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para especificar uma cor de fonte inicial.

**Para especificar os valores iniciais para os controles da caixa de diálogo Fonte, Estilo da Fonte, Tamanho, Strikeout e Sublinhado:**

1.  Para especificar os valores iniciais para os controles da caixa de diálogo Fonte, Estilo da Fonte, Tamanho, Strikeout e Sublinhado:
2.  De definir o sinalizador **CF \_ INITTOLOGFONTSTRUCT** no membro **Flags,** juntamente com os membros da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que é apontada pelo **lpLogFont**, para especificar os valores iniciais para os atributos de fonte.
3.  Você também pode usar os **sinalizadores CF \_ NOFACESEL**, **CF \_ NOSTYLESEL** e **CF \_ NOSIZESEL** para impedir que a caixa de diálogo Fonte ex ex exibir valores iniciais para os controles correspondentes.  Isso é útil quando você está trabalhando com uma seleção de texto que tem mais de uma face de tipo, estilo ou tamanho de ponto. Esses valores também serão definidos em **Sinalizadores** quando [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornar, se o usuário não tiver selecionado um valor correspondente.

**Para inicializar o controle Estilo da Fonte para um nome de estilo especificado**

-   De definir **o \_ sinalizador CF USESTYLE** e use **o membro lpszStyle** para especificar o nome de estilo.

> [!Note]  
> Para globalizar seu aplicativo, especifique o estilo usando os membros **lfWeight** e **lfItalic** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) apontada por **lpLogFont.** O nome de estilo pode mudar dependendo da linguagem de interface do usuário do sistema.

 

**Para exibir o botão Aplicar**

-   De configurar o **sinalizador \_ CF APPLY** e fornecer um procedimento de gancho para processar mensagens WM [**\_ COMMAND**](/windows/desktop/menurc/wm-command) para o **botão** Aplicar. O procedimento de gancho pode enviar a mensagem [**WM \_ CHOOSEFONT \_ GETLOGFONT**](wm-choosefont-getlogfont.md) para a caixa de diálogo para recuperar o endereço da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém as seleções atuais para a fonte.

**Para exibir o botão Ajuda**

-   De definir **o sinalizador \_ CF SHOWHELP.** O **membro hwndOwner** deve identificar a janela para receber a mensagem [**registrada HELPMSGSTRING**](helpmsgstring.md) quando o usuário clicar no **botão Ajuda.**

**Para restringir as fontes exibidas na caixa de diálogo**

-   Definir qualquer combinação dos sinalizadores **CF \_ TTONLY**, **CF \_ FIXEDPITCHONLY**, **CF \_ NOVECTORFONTS,** **CF \_ NOVERTFONTS**, **CF \_ SCALABLEONLY** e **CF \_ WYSIWYG.** Você também pode restringir os estilos disponíveis que a caixa de diálogo exibe para algumas fontes usando o **valor \_ CF NOSIMULATIONS.**

A partir Windows 7, a lista de fontes exibida na caixa de diálogo é restrita com base nas fontes mostradas pelo usuário. Para remover a restrição, de definido o **sinalizador CF \_ INACTIVEFONTS.**

**Para restringir os nomes de face de tipo, estilos e tamanhos de ponto que o usuário pode especificar**

1.  De definir **o sinalizador CF \_ FORCETEXTEXIST** para restringir o usuário a especificar apenas nomes, estilos e tamanhos de ponto válidos da face de tipo listados na caixa de diálogo.
2.  De definir **o sinalizador \_ CF LIMITSIZE** para restringir o usuário a especificar tamanhos de ponto no intervalo especificado pelos membros **nSizeMin** e **nSizeMax.**

**Para restringir ou desabilitar a caixa de combinação Scripts**

-   De definir **o sinalizador \_ CF NOSCRIPTSEL** para desabilitar a caixa de combinação **Scripts** ou definir o sinalizador **CF \_ SELECTSCRIPT** para restringir seleções na caixa de combinação **Scripts** para um conjunto de caracteres especificado.

## <a name="customizing-the-font-dialog-box-on-earlier-versions-of-windows"></a>Personalização da caixa de diálogo Fonte em versões anteriores do Windows

Você pode fornecer um modelo personalizado para a **caixa** de diálogo Fonte, por exemplo, se quiser incluir controles adicionais exclusivos para seu aplicativo. A [**função ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usa seu modelo personalizado no lugar do modelo padrão.

**Para fornecer um modelo personalizado para a caixa de diálogo Fonte**

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Font.dlg. Os identificadores de controle usados no modelo de caixa de diálogo Fonte padrão são definidos no arquivo Dlgs.h.
2.  Use a [**estrutura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para habilitar o modelo da seguinte forma:
    -   Se o modelo personalizado for um recurso em um aplicativo ou biblioteca de vínculo dinâmico, de definir o **sinalizador CF \_ ENABLETEMPLATE** no **membro Sinalizadores.** Use os **membros hInstance** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso.
    -   Se o modelo personalizado já estiver na memória, de definir o **sinalizador CF \_ ENABLETEMPLATEHANDLE.** Use o **membro hInstance** para identificar o objeto de memória que contém o modelo.

Você pode fornecer um procedimento de gancho [**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) para a **caixa de diálogo** Fonte. O procedimento de gancho pode processar mensagens enviadas para a caixa de diálogo e enviar mensagens para a caixa de diálogo. Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho para processar a entrada para seus controles.

**Para habilitar um procedimento de gancho para a caixa de diálogo Fonte**

1.  De definir **o \_ sinalizador CF ENABLEHOOK** no **membro Flags** da [**estrutura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
2.  Especifique o endereço do procedimento de gancho no **membro lpfnHook.**

Depois de processar a [**mensagem WM \_ INITDIALOG,**](wm-initdialog.md) o procedimento da caixa de diálogo envia uma mensagem **WM \_ INITDIALOG** para o procedimento de gancho. O *parâmetro lParam* dessa mensagem é um ponteiro para a estrutura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) usada para inicializar a caixa de diálogo.

O procedimento de gancho pode enviar as mensagens [**WM \_ CHOOSEFONT \_ GETLOGFONT,**](wm-choosefont-getlogfont.md) [**WM \_ CHOOSEFONT \_ SETLOGFONT**](wm-choosefont-setlogfont.md)e [**WM \_ CHOOSEFONT \_ SETFLAGS**](wm-choosefont-setflags.md) para a caixa de diálogo para obter e definir os valores e sinalizadores atuais da caixa de diálogo.

## <a name="customizing-the-font-dialog-box-on-windows-7"></a>Personalização da caixa de diálogo Fonte no Windows 7

A captura de tela a seguir mostra uma caixa de diálogo **Fonte** típica Windows 7.

![captura de tela mostrando a caixa de diálogo de fonte](images/fontdialogboxwin7.png)

Nas versões Windows anteriores, o arquivo de modelo font.dlg contém um modelo ChooseFont padrão. O arquivo de modelo font.dlg no Windows 7 contém dois modelos padrão: o modelo padrão de versões anteriores do Windows e o novo modelo Windows 7 ChooseFont. Portanto, ao personalizar a caixa **de** diálogo Fonte no Windows 7, você deve considerar os seguintes problemas.

1.  Use o novo modelo ao criar modelos personalizados para aplicativos executados no Windows 7. Esse novo modelo contém um controle de link  que o usuário pode clicar para iniciar a janela Fontes Painel de Controle, conforme mostrado na captura de tela a seguir.

    ![captura de tela mostrando o painel de controle de fonte no Windows 7](images/fontcontrolpanelforwin7.png)

2.  Para usar esse controle de link, seu aplicativo de chamada deve usar o COMCTL32.DLL versão 6 ou posterior. Caso contrário, [**a função ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornará um erro quando tentar criar o controle de link em seu modelo personalizado. Para determinar se esse controle está habilitado, compile seu aplicativo de chamada COMCTL32.DLL versão 6.0. Para obter mais informações, consulte [Habilitando estilos visuais com controles comuns.](/previous-versions//ms649781(v=vs.85))
3.  Se o aplicativo usar COMCTL32.DLL versão 5.0 ou anterior, você deverá fazer o seguinte ao criar um modelo personalizado:

    -   Especifique o controle como **PUSHBUTTON.** O controle usado para iniciar a **fonte Painel de Controle** será exibido como um botão em vez de como um link.
    -   Substitua o seguinte texto no font.dlg:

        `CONTROL         "<A>Show more fonts</A>", IDC_MANAGE_LINK, "SysLink", WS_TABSTOP, 7, 199, 227, 9`

        pelo seguinte texto:

        `PUSHBUTTON      "S&how more fonts", IDC_MANAGE_LINK, 7, 199, 74, 14 , WS_TABSTOP`

    -   para garantir que seu aplicativo use um modelo personalizado, você deve especificar um modelo personalizado com o sinalizador de **\_ habilitação do CF** , criar um modelo personalizado com base no modelo Windows 7 ChooseFont e, opcionalmente, habilitar um procedimento de gancho.

        se você habilitar um procedimento de gancho sem criar um modelo personalizado, o modelo ChooseFont padrão para versões anteriores do Windows será carregado.

> [!Note]  
> Você deve especificar o tipo de **controle de controle ou de** **pressão** no novo modelo, dependendo da versão do COMMCTL.DLL em que seu aplicativo é compilado. observe também que Windows 7 recursos específicos, como exibição WYSIWYG de listas de fontes e famílias estendidas, não estão disponíveis quando seus aplicativos são executados em versões anteriores do sistema operacional Windows.

 

 

 