---
title: Caixas de diálogo Localizar e substituir
description: Exibe uma caixa de diálogo sem janela restrita que permite ao usuário especificar uma cadeia de caracteres a ser pesquisada, bem como as opções a serem usadas durante a pesquisa de texto em um documento.
ms.assetid: c8c035bf-795d-42a7-abc6-168dea43e6e9
keywords:
- Interface do usuário do Windows, entrada do usuário
- Interface do usuário do Windows, biblioteca de caixa de diálogo comum
- entrada do usuário, biblioteca de caixa de diálogo comum
- capturando entrada do usuário, biblioteca de caixa de diálogo comum
- Biblioteca de caixa de diálogo comum
- caixas de diálogo comuns
- Caixa de diálogo Localizar
- Caixa de diálogo Substituir
- Personalizando a caixa de diálogo Localizar
- Personalizando a caixa de diálogo de substituição
- caixas de diálogo predefinidas
- caixas de diálogo, encontre
- caixas de diálogo, substituir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3cf2c5217d586c0a5ada74fb7dd72aaca5f804
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566045"
---
# <a name="find-and-replace-dialog-boxes"></a>Caixas de diálogo Localizar e substituir

Exibe uma caixa de diálogo sem janela restrita que permite ao usuário especificar uma cadeia de caracteres a ser pesquisada, bem como as opções a serem usadas durante a pesquisa de texto em um documento. A caixa de diálogo **substituir** permite que o usuário especifique uma cadeia de caracteres para pesquisar e uma cadeia de caracteres de substituição, bem como opções para controlar a operação.

Você cria e exibe uma caixa de diálogo **Localizar** inicializando uma estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passando a estrutura para a função [**LocalizarTexto**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) . A ilustração a seguir mostra uma caixa de diálogo de **localização** típica.

![caixa de diálogo Localizar](images/finddialogboxxp.png)

Você cria e exibe uma caixa de diálogo de **substituição** inicializando uma estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e passando a estrutura para a função [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) . A ilustração a seguir mostra uma caixa de diálogo de **substituição** típica.

![caixa de diálogo Substituir](images/replacedialogboxxp.png)

Ao contrário de outras caixas de diálogo comuns, as caixas de diálogo **Localizar** e **substituir** são sem janela restrita. Uma caixa de diálogo sem janela restrita permite que o usuário alterne entre a caixa de diálogo e a janela que a criou. Isso é útil para permitir que o usuário procure uma cadeia de caracteres, alterne para a janela do aplicativo para trabalhar na cadeia de caracteres e volte para a caixa de diálogo para pesquisar outra cadeia de caracteres sem repetir o comando necessário para abrir a caixa de diálogo.

Se a função [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) ou [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) criar com êxito a caixa de diálogo, ela retornará um identificador para a caixa de diálogo. Você pode usar esse identificador para mover e se comunicar com a caixa de diálogo. Se a função não puder criar a caixa de diálogo, ela retornará **NULL**. Você pode determinar a causa de um erro chamando a função [**CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido.

Esta seção aborda os tópicos a seguir.

-   [A mensagem registrada FINDMSGSTRING](#the-findmsgstring-registered-message)
-   [Personalizando a caixa de diálogo Localizar ou substituir](#customizing-the-find-or-replace-dialog-box)

## <a name="the-findmsgstring-registered-message"></a>A mensagem registrada FINDMSGSTRING

Antes de criar uma caixa de diálogo **Localizar** ou **substituir** , você deve chamar a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter um identificador de mensagem para a mensagem registrada [**FINDMSGSTRING**](findmsgstring.md) . Você pode usar o identificador para detectar e processar mensagens enviadas da caixa de diálogo. Quando o usuário clica no botão **Localizar próximo**, **substituir** ou **substituir tudo** em uma caixa de diálogo, o procedimento da caixa de diálogo envia uma mensagem **FINDMSGSTRING** para o procedimento de janela da janela do proprietário. Quando você cria a caixa de diálogo, o membro **hwndOwner** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) identifica a janela do proprietário.

O parâmetro *lParam* de uma mensagem [**FINDMSGSTRING**](findmsgstring.md) é um ponteiro para a estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) que você especificou quando criou a caixa de diálogo. Antes de enviar a mensagem, a caixa de diálogo define os membros dessa estrutura com a entrada de usuário mais recente, incluindo a cadeia de caracteres a ser pesquisada, a cadeia de caracteres de substituição (se houver) e as opções para a operação de localização e substituição.

Em uma mensagem [**FINDMSGSTRING**](findmsgstring.md) , o membro **flags** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) inclui um dos sinalizadores a seguir para indicar o evento que causou a mensagem.



| Sinalizador               | Significado                                                                                                                                                                                                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DIALOGTERM fr** | A caixa de diálogo está fechando. Depois que a janela do proprietário processa essa mensagem, um identificador para a caixa de diálogo não é mais válido.                                                                                    |
| **\_LOCALIZARPRÓXIMO fr**   | O usuário clicou no botão **Localizar próximo** em uma caixa de diálogo **Localizar** ou **substituir** . O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser pesquisada.                                                         |
| **\_substituir fr**    | O usuário clicou no botão **substituir** em uma caixa de diálogo **substituir** . O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o membro **lpstrReplaceWith** especifica a cadeia de caracteres de substituição.     |
| **\_REPLACEALL fr** | O usuário clicou no botão **substituir tudo** em uma caixa de diálogo **substituir** . O membro **lpstrFindWhat** especifica a cadeia de caracteres a ser substituída e o membro **lpstrReplaceWith** especifica a cadeia de caracteres de substituição. |



 

Para uma mensagem **Localizar próximo** ou **substituir tudo** , o membro **sinalizadores** pode incluir qualquer combinação dos sinalizadores a seguir para indicar as opções de pesquisa.



| Sinalizador              | Significado                                                                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FR \_ para baixo**      | Se definido, o botão **para baixo** da direção botões de opção é selecionado, indicando que o usuário deseja pesquisar do local atual até o final do documento. Se **fr \_ baixo** não estiver definido, o botão para **cima** será selecionado para que o usuário queira Pesquisar até o início do documento.       |
| **\_MATCHCASE fr** | Se definido, a caixa de seleção **diferenciar maiúsculas de minúsculas** é marcada, indicando que o usuário quer que a pesquisa faça distinção entre maiúsculas e minúsculas. Se **fr \_ MATCHCASE** não estiver definido, a caixa de seleção será desmarcada para que a pesquisa possa não diferenciar maiúsculas de minúsculas.                                                                       |
| **\_WHOLEWORD fr** | Se definido, a caixa de seleção **corresponder somente palavra inteira** estará marcada, indicando que o usuário deseja pesquisar apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa. Se **fr \_ WHOLEWORD** não for definido, a caixa de seleção será desmarcada, de modo que você também deverá Pesquisar fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa. |



 

## <a name="customizing-the-find-or-replace-dialog-box"></a>Personalizando a caixa de diálogo Localizar ou substituir

Para personalizar uma caixa de diálogo **Localizar** ou **substituir** , você pode usar qualquer um dos seguintes métodos:

-   Especificar valores na estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) ao criar a caixa de diálogo
-   Fornecer um modelo personalizado
-   Fornecer um procedimento de gancho

Ao criar uma caixa de diálogo **Localizar** ou **substituir** , você pode definir sinalizadores no membro **flags** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para ocultar ou desabilitar qualquer um dos controles de opção de pesquisa. Por exemplo, você pode definir o \_ sinalizador fr NOMATCHCASE para desabilitar a caixa de seleção **diferenciar maiúsculas de minúsculas** ou definir o \_ sinalizador fr HIDEMATCHCASE para ocultá-lo.

Você pode fornecer um modelo personalizado para uma caixa de diálogo **Localizar** ou **substituir** , por exemplo, se desejar incluir controles adicionais que são exclusivos do seu aplicativo. As funções [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) e [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) usam o modelo personalizado no lugar do modelo padrão.

**Para fornecer um modelo personalizado para uma caixa de diálogo Localizar ou substituir**

1.  Crie o modelo personalizado modificando o modelo padrão especificado no arquivo LocalizarTexto. Dlg. Os identificadores de controle usados no modelo de caixa de diálogo **Localizar** ou **substituir** padrão são definidos no arquivo Dlgs. h.
2.  Use a estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) para habilitar o modelo da seguinte maneira:
    -   -   Se o modelo personalizado for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina o \_ sinalizador de habilitação fr no membro **flags** . Use os membros **HINSTANCE** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso.

            -Ou-

        -   Se o modelo personalizado já estiver na memória, defina o \_ sinalizador fr ENABLETEMPLATEHANDLE. Use o membro **HINSTANCE** para identificar o objeto de memória que contém o modelo.

Você pode fornecer um procedimento de gancho [**FRHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc) para uma caixa de diálogo **Localizar** ou **substituir** . O procedimento de gancho pode processar mensagens enviadas para a caixa de diálogo. Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um procedimento de gancho para processar a entrada para seus controles.

**Para habilitar um procedimento de gancho para uma caixa de diálogo Localizar ou substituir**

1.  Defina o \_ sinalizador fr ENABLEHOOK no membro **flags** da estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .
2.  Especifique o endereço do procedimento de gancho no membro **lpfnHook** .

Depois de processar sua mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) , o procedimento da caixa de diálogo envia uma mensagem do **WM \_ INITDIALOG** para o procedimento de gancho. O parâmetro *lParam* dessa mensagem é um ponteiro para a estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) usada para inicializar a caixa de diálogo.

Se o procedimento de gancho retornar **false** em resposta à mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) , a caixa de diálogo não será mostrada a menos que o procedimento de gancho o exiba. Para fazer isso, primeiro execute qualquer outra operação de pintura e, em seguida, chame as funções de [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) e de [**subjanela**](/windows/desktop/api/winuser/nf-winuser-showwindow) . O código a seguir mostra um exemplo:


```
// We've returned FALSE in response to WM_INITDIALOG. 
// We've performed any other paint operations. 
// Now we display the dialog box. 
ShowWindow(hDlg, SW_SHOWNORMAL); 
UpdateWindow(hDlg); 
```



 

 