---
title: Caixas de diálogo Encontrar e Substituir
description: Exibe uma caixa de diálogo sem modo que permite que o usuário especifique uma cadeia de caracteres a ser pesquisada, bem como opções a serem usadas ao pesquisar texto em um documento.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Windows Interface do Usuário, entrada do usuário
- Windows Interface do Usuário, Biblioteca de Caixas de Diálogo Comuns
- entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- capturando entrada do usuário, Biblioteca de Caixas de Diálogo Comuns
- Biblioteca de caixas de diálogo comuns
- caixas de diálogo comuns
- Caixa de diálogo Localizar
- Caixa de diálogo Substituir
- personalização da caixa de diálogo Encontrar
- personalização da caixa de diálogo Substituir
- caixas de diálogo predefinidos
- caixas de diálogo,Encontrar
- caixas de diálogo, Substituir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59bc5da5a8780a4f08bbf4bf757e1703d8d9120fdefe9d1730e515ffc6feae40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503475"
---
# <a name="find-and-replace-dialog-boxes"></a>Caixas de diálogo Encontrar e Substituir

Exibe uma caixa de diálogo sem modo que permite que o usuário especifique uma cadeia de caracteres a ser pesquisada, bem como opções a serem usadas ao pesquisar texto em um documento. A **caixa de** diálogo Substituir permite que o usuário especifique uma cadeia de caracteres para pesquisar e uma cadeia de caracteres de substituição, bem como opções para controlar a operação.

Você cria e exibe uma **caixa** de diálogo Encontrar inicializando uma estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passando a estrutura para a [**função FindText.**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) A ilustração a seguir mostra uma caixa de **diálogo** Encontrar típica.

![caixa de diálogo find](images/finddialogboxxp.png)

Você cria e exibe uma **caixa de** diálogo Substituir inicializando uma estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passando a estrutura para a [**função ReplaceText.**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) A ilustração a seguir mostra uma caixa de **diálogo** Substituir típica.

![caixa de diálogo substituir](images/replacedialogboxxp.png)

Ao contrário de outras caixas de diálogo comuns, as **caixas** **de** diálogo Encontrar e Substituir não têm modo. Uma caixa de diálogo sem modo permite que o usuário alternar entre a caixa de diálogo e a janela que a criou. Isso é útil para permitir que o usuário pesquise uma cadeia de caracteres, mude para a janela do aplicativo para trabalhar na cadeia de caracteres e volte para a caixa de diálogo para pesquisar outra cadeia de caracteres sem repetir o comando necessário para abrir a caixa de diálogo.

Se a [**função FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) [**ou ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) criar com êxito a caixa de diálogo, ela retornará um handle para a caixa de diálogo. Você pode usar esse alça para mover e se comunicar com a caixa de diálogo. Se a função não puder criar a caixa de diálogo, ela retornará **NULL.** Você pode determinar a causa de um erro chamando a [**função CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

Esta seção discute os tópicos a seguir.

-   [A mensagem registrada FINDMSGSTRING](#the-findmsgstring-registered-message)
-   [Personalização da caixa de diálogo Encontrar ou Substituir](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>A mensagem registrada FINDMSGSTRING

Antes de **criar** uma caixa de diálogo Encontrar ou Substituir, você deve chamar a [**função RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter um identificador de mensagem para a mensagem [**registrada FINDMSGSTRING.**](findmsgstring.md)  Em seguida, você pode usar o identificador para detectar e processar mensagens enviadas da caixa de diálogo. Quando o usuário clica no botão  Encontrar Próximo **,** Substituir ou Substituir Tudo em uma caixa de diálogo, o procedimento da caixa de diálogo envia uma mensagem **FINDMSGSTRING** para o procedimento de janela da janela do proprietário. Quando você cria a caixa de diálogo, o **membro hwndOwner** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) identifica a janela do proprietário.

O *parâmetro lParam* de uma mensagem [**FINDMSGSTRING**](findmsgstring.md) é um ponteiro para a estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que você especificou quando criou a caixa de diálogo. Antes de enviar a mensagem, a caixa de diálogo define os membros dessa estrutura com a entrada mais recente do usuário, incluindo a cadeia de caracteres a ser pesquisada, a cadeia de caracteres de substituição (se há) e as opções para a operação de local e substituição.

Em uma [**mensagem FINDMSGSTRING,**](findmsgstring.md) o membro **Flags** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) inclui um dos sinalizadores a seguir para indicar o evento que causou a mensagem.



| Sinalizador               | Significado                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DIALOGTERM** | A caixa de diálogo está sendo fechada. Depois que a janela do proprietário processa essa mensagem, um alça para a caixa de diálogo não é mais válido.                                                                                    |
| **FR \_ FINDNEXT**   | O usuário clicou no **botão Encontrar Próximo** em uma caixa de **diálogo** Encontrar **ou** Substituir. O **membro lpstrFindWhat** especifica a cadeia de caracteres a ser pesquisada.                                                         |
| **FR \_ REPLACE**    | O usuário clicou no **botão Substituir** em uma **caixa de diálogo** Substituir. O **membro lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o **membro lpstrReplaceWith** especifica a cadeia de caracteres de substituição.     |
| **FR \_ REPLACEALL** | O usuário clicou no **botão Substituir Tudo** em uma caixa de **diálogo** Substituir. O **membro lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o **membro lpstrReplaceWith** especifica a cadeia de caracteres de substituição. |



 

Para uma **mensagem Encontrar Próximo** ou Substituir **Tudo,** o membro **Sinalizadores** pode incluir qualquer combinação dos sinalizadores a seguir para indicar as opções de pesquisa.



| Sinalizador              | Significado                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ DOWN**      | Se definido, o **botão Para** baixo dos botões de opção de direção será selecionado, indicando que o usuário deseja pesquisar do local atual até o final do documento. Se **FR \_ DOWN** não estiver definido, o **botão Para** cima será selecionado para que o usuário queira pesquisar até o início do documento.       |
| **FR \_ MATCHCASE** | Se definido, a **caixa de seleção** Caso de Ocorrência será marcada, indicando que o usuário deseja que a pesquisa seja sensível a minúsculas. Se **FR \_ MATCHCASE não** estiver definido, a caixa de seleção será deseleitada para que a pesquisa não possa não ter maiúsculas de minúsculas.                                                                       |
| **FR \_ WHOLEWORD** | Se definido, **a** caixa de seleção Corresponder Somente Palavra Inteira será marcada, indicando que o usuário deseja pesquisar apenas palavras inteiras que corresponderem à cadeia de caracteres de pesquisa. Se **FR \_ WHOLEWORD** não estiver definido, a caixa de seleção será deseleitada, portanto, você também deverá pesquisar fragmentos de palavras que corresponderem à cadeia de caracteres de pesquisa. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Personalização da caixa de diálogo Encontrar ou Substituir

Para personalizar uma **caixa de** **diálogo** Encontrar ou Substituir, você pode usar qualquer um dos seguintes métodos:

-   Especificar valores na estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) ao criar a caixa de diálogo
-   Fornecer um modelo personalizado
-   Fornecer um procedimento de gancho

Ao criar **uma**  caixa de diálogo Encontrar ou Substituir, você pode definir sinalizadores no membro **Flags** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para ocultar ou desabilitar qualquer um dos controles de opção de pesquisa. Por exemplo, você pode definir o sinalizador FR NOMATCHCASE para desabilitar a caixa de seleção Caso de Corresponder ou definir o \_ sinalizador FR  \_ HIDEMATCHCASE para o ocultar.

Você pode fornecer um modelo  personalizado para **uma** caixa de diálogo Encontrar ou Substituir, por exemplo, se quiser incluir controles adicionais exclusivos para seu aplicativo. As [**funções FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) [**e ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) usam seu modelo personalizado no lugar do modelo padrão.

**Para fornecer um modelo personalizado para uma caixa de diálogo Encontrar ou Substituir**

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Findtext.dlg. Os identificadores de controle usados  no modelo de caixa de diálogo **Padrão Encontrar** ou Substituir são definidos no arquivo Dlgs.h.
2.  Use a [**estrutura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para habilitar o modelo da seguinte forma:
    -   -   Se o modelo personalizado for um recurso em um aplicativo ou biblioteca de vínculo dinâmico, de definir o sinalizador FR \_ ENABLETEMPLATE no **membro Sinalizadores.** Use os **membros hInstance** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso.

            -Ou-

        -   Se o modelo personalizado já estiver na memória, de definir o sinalizador FR \_ ENABLETEMPLATEHANDLE. Use o **membro hInstance** para identificar o objeto de memória que contém o modelo.

Você pode fornecer um procedimento de gancho [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) para uma **caixa de diálogo** Encontrar **ou** Substituir. O procedimento de gancho pode processar mensagens enviadas para a caixa de diálogo. Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho para processar a entrada para seus controles.

**Para habilitar um procedimento de gancho para uma caixa de diálogo Encontrar ou Substituir**

1.  De definir o sinalizador FR \_ ENABLEHOOK no **membro Flags** da [**estrutura FINDREPLACE.**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
2.  Especifique o endereço do procedimento de gancho no **membro lpfnHook.**

Depois de processar sua [**mensagem WM \_ INITDIALOG,**](wm-initdialog.md) o procedimento da caixa de diálogo envia uma mensagem **WM \_ INITDIALOG** para o procedimento de gancho. O *parâmetro lParam* dessa mensagem é um ponteiro para a estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) usada para inicializar a caixa de diálogo.

Se o procedimento de gancho retornar **FALSE** em resposta à mensagem [**WM \_ INITDIALOG,**](wm-initdialog.md) a caixa de diálogo não será mostrada, a menos que o procedimento de gancho a exibir. Para fazer isso, primeiro execute qualquer outra operação de pintura e, em seguida, chame as funções [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) e [**UpdateWindow.**](/windows/desktop/api/winuser/nf-winuser-updatewindow) O código a seguir mostra um exemplo:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 