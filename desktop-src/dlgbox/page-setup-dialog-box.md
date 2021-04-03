---
title: Caixa de diálogo Configurar Página
description: Exibe uma caixa de diálogo modal que permite ao usuário escolher as configurações que incluem o tipo de papel, a origem do papel, a orientação da página e a largura das margens da página.
ms.assetid: debde0a0-07d4-46ed-a936-e517eab1852d
keywords:
- Interface do usuário do Windows, entrada do usuário
- Interface do usuário do Windows, biblioteca de caixa de diálogo comum
- entrada do usuário, biblioteca de caixa de diálogo comum
- capturando entrada do usuário, biblioteca de caixa de diálogo comum
- Biblioteca de caixa de diálogo comum
- caixas de diálogo comuns
- caixa de diálogo Configurar Página
- Personalizando a caixa de diálogo configuração de página
- ganchos, caixa de diálogo configuração de página
- caixas de diálogo predefinidas
- caixas de diálogo, configuração de página
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b9a8f7f30a8313017dc3a124cdccb7d00c872b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084873"
---
# <a name="page-setup-dialog-box"></a>Caixa de diálogo Configurar Página

Exibe uma caixa de diálogo modal que permite ao usuário definir os seguintes atributos da página impressa:

-   O tipo de papel (envelope, ofício, carta e assim por diante)
-   A fonte de papel (alimentação manual, feed de tratores, alimentador de planilha e assim por diante)
-   A orientação da página (retrato ou paisagem)
-   A largura das margens da página

Você cria e exibe uma caixa de diálogo de **configuração de página** inicializando uma estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) e passando a estrutura para a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) . No entanto, os atributos apresentados na caixa de diálogo variam de acordo com os recursos da impressora. A ilustração a seguir mostra uma caixa de diálogo de **configuração de página** típica.

![caixa de diálogo Configurar página](images/pagesetupdialogboxxp.png)

Se o usuário clicar no botão **OK** , [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) retornará **true** depois de definir vários membros na estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para especificar as seleções do usuário. Os membros **ptPaperSize** e **rtMargin** contêm os valores especificados pelo usuário. Os membros **hDevMode** e **hDevNames** contêm identificadores de memória global para as estruturas [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) e [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) . Essas estruturas contêm informações de página adicionais, bem como informações sobre a impressora. Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.

Se o usuário cancelar a caixa de diálogo de **configuração de página** ou ocorrer um erro, [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) retornará **false**. Para determinar a causa do erro, chame a função [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

Esta seção aborda os tópicos a seguir.

-   [Inicializando a caixa de diálogo Configurar página](#initializing-the-page-setup-dialog-box)
-   [Personalizando a caixa de diálogo Configurar página](#customizing-the-page-setup-dialog-box)
-   [Personalizando a página de exemplo](#customizing-the-sample-page)

## <a name="initializing-the-page-setup-dialog-box"></a>Inicializando a caixa de diálogo Configurar página

Por padrão, a caixa de diálogo **Configurar página** exibe informações sobre a impressora padrão atual. Para direcionar a caixa de diálogo para exibir informações sobre uma impressora específica, defina os membros de uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ou [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) e atribua os identificadores de memória global dessas estruturas ao membro correspondente no [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga). Se você especificar o nome de uma impressora que não está instalada atualmente, a caixa de diálogo exibirá uma mensagem de erro. Para impedir que a caixa de diálogo exiba mensagens de erro, use o valor de **\_ nowarning do PSD** . Para recuperar informações sobre a impressora padrão sem exibir a caixa de diálogo **Configurar página** , use o valor **\_ RETURNDEFAULT do PSD** .

Se o sistema de medidas padrão for polegadas, a caixa de diálogo usará milésimos de polegadas como a unidade de medida padrão. Se o sistema de medidas padrão for a métrica, a caixa de diálogo usará centésimos de milímetros como a unidade de medida padrão. Para substituir a unidade de medida padrão, defina o **sinalizador \_ PSD INHUNDREDTHSOFMILLIMETERS** ou **\_ INTHOUSANDTHSOFINCHES PSD** no membro **flags** da estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

Por padrão, os valores iniciais das margens são uma polegada. Se você definir o sinalizador de **\_ margens do PSD** , a caixa de diálogo exibirá os valores de margem inicial especificados no membro **rtMargin** . Os valores mínimos padrão que o usuário pode especificar para as margens são as margens mínimas permitidas pela impressora. Se você definir o **sinalizador \_ MINMARGINS do PSD** , a caixa de diálogo aplicará as margens mínimas especificadas no membro **rtMinMargin** .

Para impedir que os usuários selecionem determinadas opções, defina qualquer combinação dos sinalizadores a seguir para desabilitar os controles correspondentes.



| Sinalizador                        | Significado                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **\_DISABLEMARGINS PSD**     | Desabilita os controles de edição nos quais o usuário insere as configurações de margem. |
| **\_DISABLEORIENTATION PSD** | Desabilita os botões de opção **retrato** e **paisagem** .               |
| **\_DISABLEPAPER PSD**       | Desabilita os controles para selecionar o tamanho do papel e a origem do papel.     |
| **\_DISABLEPRINTER PSD**     | Desabilita o botão da **impressora** .                                         |



 

## <a name="customizing-the-page-setup-dialog-box"></a>Personalizando a caixa de diálogo Configurar página

Você pode fornecer um modelo personalizado para a caixa de diálogo **Configurar página** , por exemplo, se você quiser incluir controles adicionais que são exclusivos do seu aplicativo. A função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) usa o modelo personalizado no lugar do modelo padrão.

**Para fornecer um modelo personalizado para a caixa de diálogo Configurar página**

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Prnsetup. Dlg. Os identificadores de controle usados no modelo de caixa de diálogo de **configuração de página** padrão são definidos no arquivo Dlgs. h.
2.  Use a estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) para habilitar o modelo da seguinte maneira:
    -   -   Se o modelo personalizado for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina o sinalizador **\_ ENABLEPAGESETUPTEMPLATE do PSD** no membro **flags** . Use os membros **HINSTANCE** e **lpPageSetupTemplateName** da estrutura para identificar o módulo e o nome do recurso.

            -Ou-

        -   Se o modelo personalizado já estiver na memória, defina o **sinalizador \_ ENABLEPAGESETUPTEMPLATEHANDLE do PSD** . Use o membro **hPageSetupTemplate** para identificar o objeto de memória que contém o modelo.

Para filtrar as mensagens enviadas para o procedimento da caixa de diálogo, você pode fornecer um procedimento de gancho [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho **PageSetupHook** para processar a entrada para seus controles. Além disso, você pode fornecer um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar o conteúdo da página de exemplo exibida pela caixa de diálogo **Configurar página** . Para obter mais informações sobre o procedimento de gancho **PagePaintHook** , consulte [Personalizando a página de exemplo](#customizing-the-sample-page).

**Para habilitar um procedimento de gancho PageSetupHook**

1.  Defina o **sinalizador \_ ENABLEPAGESETUPHOOK do PSD** no membro **flags** da estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Especifique o endereço do procedimento de gancho no membro **lpfnPageSetupHook** .

Depois de processar sua mensagem [**\_ INITDIALOG do WM**](wm-initdialog.md) , o procedimento da caixa de diálogo envia uma mensagem do **WM \_ INITDIALOG** para o procedimento de gancho [**PageSetupHook**](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook) . O parâmetro *lParam* dessa mensagem é um ponteiro para a estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) usada para inicializar a caixa de diálogo.

## <a name="customizing-the-sample-page"></a>Personalizando a página de exemplo

A caixa de diálogo **Configurar página** inclui uma imagem de uma página de exemplo que mostra como as seleções do usuário afetam a aparência da saída impressa. A imagem consiste em um retângulo que representa o papel selecionado ou o tipo de envelope, com um retângulo de linha pontilhada representando as margens atuais e caracteres parciais (texto grego) para mostrar a aparência do texto na página impressa.

Ao chamar a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) , você pode fornecer um procedimento de gancho de [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar a aparência da página de exemplo.

**Para habilitar um procedimento de gancho PagePaintHook**

1.  Defina o **sinalizador \_ ENABLEPAGEPAINTHOOK do PSD** no membro **flags** da estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .
2.  Especifique o endereço do procedimento de gancho no membro **lpfnPagePaintHook** .

Sempre que a caixa de diálogo estiver prestes a desenhar o conteúdo da página de exemplo, o procedimento de gancho receberá as seguintes mensagens na ordem em que elas estão listadas.



| Mensagem                                                  | Significado                                                                                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_PAGESETUPDLG de PSD do WM \_**](wm-psd-pagesetupdlg.md)     | A caixa de diálogo está prestes a desenhar a página de exemplo. O procedimento de gancho pode usar essa mensagem para se preparar para desenhar o conteúdo da página de exemplo.     |
| [**\_FULLPAGERECT de PSD do WM \_**](wm-psd-fullpagerect.md)     | A caixa de diálogo está prestes a desenhar a página de exemplo. Esta mensagem Especifica o retângulo delimitador da página de exemplo.                               |
| [**\_MINMARGINRECT de PSD do WM \_**](wm-psd-minmarginrect.md)   | A caixa de diálogo está prestes a desenhar a página de exemplo. Esta mensagem Especifica o retângulo da margem.                                                    |
| [**\_MARGINRECT de PSD do WM \_**](wm-psd-marginrect.md)         | A caixa de diálogo está prestes a desenhar o retângulo de margem.                                                                                            |
| [**\_GREEKTEXTRECT de PSD do WM \_**](wm-psd-greektextrect.md)   | A caixa de diálogo está prestes a desenhar o texto grego dentro do retângulo de margem.                                                                      |
| [**\_ENVSTAMPRECT de PSD do WM \_**](wm-psd-envstamprect.md)     | A caixa de diálogo está prestes a desenhar no retângulo do carimbo de envelope de uma página de exemplo de envelope. Esta mensagem é enviada somente para envelopes.             |
| [**\_YAFULLPAGERECT de PSD do WM \_**](wm-psd-yafullpagerect.md) | A caixa de diálogo está prestes a desenhar a parte de endereço de retorno de uma página de exemplo de envelope. Essa mensagem é enviada para envelopes e outros tamanhos de papel. |



 

Se o procedimento de gancho retornar **true** para qualquer uma das três primeiras mensagens de uma sequência de desenho ([**WM \_ PSD \_ PAGESETUPDLG**](wm-psd-pagesetupdlg.md), [**WM \_ PSD \_ FULLPAGERECT**](wm-psd-fullpagerect.md)ou [**WM \_ PSD \_ MINMARGINRECT**](wm-psd-minmarginrect.md)), a caixa de diálogo não enviará mais mensagens e não desenhará na página de exemplo até a próxima vez que o sistema precisar redesenhar a página de exemplo. Se o procedimento de gancho retornar **false** para todas as três mensagens, a caixa de diálogo enviará as mensagens restantes da sequência de desenho.

Se o procedimento de gancho retornar **true** para qualquer uma das mensagens restantes em uma sequência de desenho, a caixa de diálogo não desenhará a parte correspondente da página de exemplo. Se o procedimento de gancho retornar **false** para qualquer uma dessas mensagens, a caixa de diálogo desenhará essa parte da página de exemplo.

Para impedir que a caixa de diálogo desenhasse o conteúdo da página de exemplo, você pode definir o sinalizador **\_ DISABLEPAGEPAINTING do PSD** . Esse sinalizador não afeta o procedimento de gancho do [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) , que ainda recebe todas as mensagens do **WM \_ PSD \_ \*** e pode desenhar o conteúdo da página de exemplo.

 

 