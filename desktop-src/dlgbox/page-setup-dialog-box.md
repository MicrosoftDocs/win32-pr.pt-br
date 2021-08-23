---
title: Caixa de diálogo Configurar Página
description: Exibe uma caixa de diálogo modal que permite que o usuário escolha configurações que incluem o tipo de papel, a origem do papel, a orientação da página e a largura das margens da página.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Windows Interface do Usuário, entrada do usuário
- Windows Interface do Usuário, Biblioteca de Caixas de Diálogo Comuns
- entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- capturando entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- Biblioteca de caixas de diálogo comuns
- caixas de diálogo comuns
- caixa de diálogo Configurar Página
- personalização da caixa de diálogo Configuração de Página
- ganchos, caixa de diálogo Configuração de Página
- caixas de diálogo predefinidos
- caixas de diálogo,Configuração de Página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af64357be8bd39217c6527dc81f7ac426f5e06e183de92b3bb479f4633c75d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741646"
---
# <a name="page-setup-dialog-box"></a>Caixa de diálogo Configurar Página

Exibe uma caixa de diálogo modal que permite que o usuário defina os seguintes atributos da página impressa:

-   O tipo de papel (envelope, legal, letra e assim por diante)
-   A fonte de papel (feed manual, feed de trator, alimentador de planilhas e assim por diante)
-   A orientação da página (retrato ou paisagem)
-   A largura das margens da página

Você cria e exibe **uma** caixa de diálogo Configuração de Página inicializando uma estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) e passando a estrutura para a [**função PageSetupDlg.**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) No entanto, os atributos apresentados na caixa de diálogo variam, dependendo dos recursos da impressora. A ilustração a seguir mostra uma caixa de **diálogo Típica de Configuração** de Página.

![caixa de diálogo de configuração de página](images/pagesetupdialogboxxp.png)

Se o usuário clicar no **botão OK,** [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) retornará **TRUE** depois de definir vários membros na estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para especificar as seleções do usuário. Os **membros ptPaperSize** e **rtMargin** contêm os valores especificados pelo usuário. Os **membros hDevMode** e **hDevNames** contêm alças de memória global para as estruturas [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e [**DEVNAMES.**](/windows/win32/api/commdlg/ns-commdlg-devnames) Essas estruturas contêm informações de página adicionais, bem como informações sobre a impressora. Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.

Se o usuário cancelar a caixa de **diálogo Configuração** de Página ou ocorrer um erro, [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) retornará **FALSE.** Para determinar a causa do erro, chame a [**função CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

Esta seção discute os tópicos a seguir.

-   [Inicializando a caixa de diálogo Configuração da Página](#initializing-the-page-setup-dialog-box)
-   [Personalização da caixa de diálogo Configuração da Página](#customizing-the-page-setup-dialog-box)
-   [Personalização da página de exemplo](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Inicializando a caixa de diálogo Configuração da Página

Por padrão, a **caixa de diálogo Configuração** de Página exibe informações sobre a impressora padrão atual. Para direcionar a caixa de diálogo para exibir informações sobre uma impressora específica, defina os membros de uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ou [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e atribua os alças de memória global dessas estruturas ao membro correspondente em [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga). Se você especificar o nome de uma impressora que não está instalada no momento, a caixa de diálogo exibirá uma mensagem de erro. Para impedir que a caixa de diálogo exibe mensagens de erro, use o **valor \_ PSD NOWARNING.** Para recuperar informações sobre a impressora padrão sem exibir a caixa de diálogo Configuração **de** Página, use o **valor \_ RETURNDEFAULT do PSD.**

Se o sistema de medição padrão for de polegadas, a caixa de diálogo usará milésimos de polegadas como a unidade padrão de medida. Se o sistema de medição padrão for métrica, a caixa de diálogo usará centésimos de milímetros como a unidade padrão de medida. Para substituir a unidade de medida padrão, defina o sinalizador **\_ PSD IN LTDOMELLIMETERS** ou **\_ PSD INTHOUSANDTHSOFINCHES** no membro **Flags** da estrutura [**PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)

Os valores iniciais para as margens são de uma polegada, por padrão. Se você definir o **sinalizador PSD \_ MARGINS,** a caixa de diálogo exibirá os valores de margem iniciais especificados no **membro rtMargin.** Os valores mínimos padrão que o usuário pode especificar para as margens são as margens mínimas permitidas pela impressora. Se você definir o **sinalizador PSD \_ MINMARGINS,** a caixa de diálogo imporá as margens mínimas especificadas no **membro rtMinMargin.**

Para impedir que os usuários selecionem determinadas opções, de definir qualquer combinação dos sinalizadores a seguir para desabilitar os controles correspondentes.



| Sinalizador                        | Significado                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **PSD \_ DISABLEMARGINS**     | Desabilita os controles de edição nos quais o usuário insibilitar as configurações de margem. |
| **PSD \_ DISABLEORIENTATION** | Desabilita os **botões de** rádio **Retrato** e Paisagem.               |
| **PSD \_ DISABLEPAPER**       | Desabilita os controles para selecionar o tamanho do papel e a fonte de papel.     |
| **PSD \_ DISABLEPRINTER**     | Desabilita o **botão Impressora.**                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Personalização da caixa de diálogo Configuração da Página

Você pode fornecer um modelo personalizado para a **caixa** de diálogo Configuração de Página, por exemplo, se quiser incluir controles adicionais exclusivos para seu aplicativo. A [**função PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) usa seu modelo personalizado no lugar do modelo padrão.

**Para fornecer um modelo personalizado para a caixa de diálogo Configuração de Página**

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Prnsetup.dlg. Os identificadores de controle usados no modelo de caixa de **diálogo** configuração de página padrão são definidos no arquivo Dlgs.h.
2.  Use a [**estrutura PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para habilitar o modelo da seguinte forma:
    -   -   Se o modelo personalizado for um recurso em um aplicativo ou biblioteca de vínculo dinâmico, de definir o sinalizador **PSD \_ ENABLEPAGESETUPTEMPLATE** no **membro Sinalizadores.** Use os **membros hInstance e** **lpPageSetupTemplateName** da estrutura para identificar o módulo e o nome do recurso.

            -Ou-

        -   Se o modelo personalizado já estiver na memória, de definir o **sinalizador PSD \_ ENABLEPAGESETUPTEMPLATEHANDLE.** Use o **membro hPageSetupTemplate** para identificar o objeto de memória que contém o modelo.

Para filtrar as mensagens enviadas ao procedimento da caixa de diálogo, você pode fornecer um procedimento de gancho [**PageSetupHook.**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho **PageSetupHook** para processar a entrada para seus controles. Além disso, você pode fornecer um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar o conteúdo da página de exemplo exibida pela caixa **de diálogo Configuração** de Página. Para obter mais informações sobre o procedimento de gancho **PagePaintHook,** consulte [Personalização da página de exemplo](#customizing-the-sample-page).

**Para habilitar um procedimento de gancho PageSetupHook**

1.  Defina **o sinalizador \_ PSD ENABLEPAGESETUPHOOK** no membro **Flags** da estrutura [**PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
2.  Especifique o endereço do procedimento de gancho no **membro lpfnPageSetupHook.**

Depois de processar sua mensagem [**WM \_ INITDIALOG,**](wm-initdialog.md) o procedimento da caixa de diálogo envia uma mensagem **WM \_ INITDIALOG** para o procedimento de gancho [**PageSetupHook.**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) O *parâmetro lParam* dessa mensagem é um ponteiro para a estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) usada para inicializar a caixa de diálogo.

## <a name="customizing-the-sample-page"></a>Personalização da página de exemplo

A **caixa de diálogo** Configuração de Página inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa. A imagem consiste em um retângulo que representa o tipo de papel ou envelope selecionado, com um retângulo de linha pontilhada que representa as margens atuais e caracteres parciais (texto grego) para mostrar a aparência do texto na página impressa.

Ao chamar a [**função PageSetupDlg,**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) você pode fornecer um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo.

**Para habilitar um procedimento de gancho PagePaintHook**

1.  Defina **o sinalizador \_ PSD ENABLEPAGEPAINTHOOK** no membro **Flags** da estrutura [**PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
2.  Especifique o endereço do procedimento de gancho no **membro lpfnPagePaintHook.**

Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, o procedimento de gancho receberá as seguintes mensagens na ordem em que elas estão listadas.



| Mensagem                                                  | Significado                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md)     | A caixa de diálogo está prestes a desenhar a página de exemplo. O procedimento de gancho pode usar essa mensagem para se preparar para desenhar o conteúdo da página de exemplo.     |
| [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)     | A caixa de diálogo está prestes a desenhar a página de exemplo. Essa mensagem especifica o retângulo delimitado da página de exemplo.                               |
| [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)   | A caixa de diálogo está prestes a desenhar a página de exemplo. Essa mensagem especifica o retângulo de margem.                                                    |
| [**WM \_ PSD \_ MARGINRECT**](wm-psd-marginrect.md)         | A caixa de diálogo está prestes a desenhar o retângulo de margem.                                                                                            |
| [**\_GREEKTEXTRECT de PSD do WM \_**](wm-psd-greektextrect.md)   | A caixa de diálogo está prestes a desenhar o texto grego dentro do retângulo de margem.                                                                      |
| [**\_ENVSTAMPRECT de PSD do WM \_**](wm-psd-envstamprect.md)     | A caixa de diálogo está prestes a desenhar no retângulo do carimbo de envelope de uma página de exemplo de envelope. Esta mensagem é enviada somente para envelopes.             |
| [**\_YAFULLPAGERECT de PSD do WM \_**](wm-psd-yafullpagerect.md) | A caixa de diálogo está prestes a desenhar a parte de endereço de retorno de uma página de exemplo de envelope. Essa mensagem é enviada para envelopes e outros tamanhos de papel. |



 

Se o procedimento de gancho retornar **true** para qualquer uma das três primeiras mensagens de uma sequência de desenho ([**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md), [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)ou [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)), a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo. Se o procedimento de gancho retornar **false** para todas as três mensagens, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.

Se o procedimento de gancho retornar **true** para qualquer uma das mensagens restantes em uma sequência de desenho, a caixa de diálogo não desenhará a parte correspondente da página de exemplo. Se o procedimento de gancho retornar **false** para qualquer uma dessas mensagens, a caixa de diálogo desenhará essa parte da página de exemplo.

Para impedir que a caixa de diálogo desenhasse o conteúdo da página de exemplo, você pode definir o sinalizador **\_ DISABLEPAGEPAINTING do PSD** . Esse sinalizador não afeta o procedimento de gancho do [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) , que ainda recebe todas as mensagens do **WM \_ PSD \_ \*** e pode desenhar o conteúdo da página de exemplo.

 

 