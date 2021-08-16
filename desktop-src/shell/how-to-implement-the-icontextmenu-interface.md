---
description: IContextMenu é a interface mais poderosa, mas também a interface mais complicada a ser implementada.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Como implementar a interface IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44ec65d95a4f6d67a9f15e10f5720be21c3b6c57fba5d0cf920bd12be54f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223463"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Como implementar a interface IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) é a interface mais poderosa, mas também a interface mais complicada a ser implementada. É recomendável que você implemente um verbo usando um dos métodos de verbo estáticos. Para obter mais informações, consulte [Escolhendo um método de menu de atalho estático ou dinâmico](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tem três métodos, [**GetCommandString,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)que são discutidos aqui em detalhes.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   C++

### <a name="prerequisites"></a>Pré-requisitos

-   Verbo estático
-   Menu de atalho

## <a name="instructions"></a>Instruções

### <a name="icontextmenugetcommandstring-method"></a>Método IContextMenu::GetCommandString

O método [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) do manipulador é usado para retornar o nome canônico de um verbo. Esse método é opcional. No Windows XP e versões anteriores do Windows, quando o Windows Explorer tem uma barra de Status, esse método é usado para recuperar o texto de ajuda exibido na barra de Status de um item de menu.

O *parâmetro idCmd* contém o deslocamento do identificador do comando que foi definido quando [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) foi chamado. Se uma cadeia de caracteres de ajuda for solicitada, *uFlags* será definido como **GCS \_ HELPTEXTW.** Copie a cadeia de caracteres de ajuda para o buffer *pszName,* lançando-a em um **PWSTR.** A cadeia de caracteres de verbo é solicitada definindo *uFlags* como **GCS \_ VERBW**. Copie a cadeia de caracteres apropriada *para pszName,* assim como com a cadeia de caracteres de ajuda. Os **sinalizadores GCS \_ VALIDATEA** e **GCS \_ VALIDATEW** não são usados por manipuladores de menu de atalho.

O exemplo a seguir mostra uma implementação simples de [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde ao exemplo [**QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) dado na seção Método [IContextMenu::QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) deste tópico. Como o manipulador adiciona apenas um item de menu, há apenas um conjunto de cadeias de caracteres que pode ser retornado. O método testa se *idCmd é* válido e, se for, retorna a cadeia de caracteres solicitada.

A [**função StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) é usada para copiar a cadeia de caracteres solicitada para *pszName* para garantir que a cadeia de caracteres copiada não exceda o tamanho do buffer especificado por *cchName.* Este exemplo implementa o suporte somente para os valores Unicode de *uFlags*, porque somente aqueles que foram usados no Windows Explorer desde Windows 2000.


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a>Método IContextMenu::InvokeCommand

Esse método é chamado quando um usuário clica em um item de menu para dizer ao manipulador para executar o comando associado. O *parâmetro pici* aponta para uma estrutura que contém as informações necessárias para executar o comando.

Embora *a pici* seja declarada em Shlobj.h como uma estrutura [**CMINVOKECOMMANDINFO,**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) na prática, ela geralmente aponta para uma estrutura [**CMINVOKECOMMANDINFOEX.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) Essa estrutura é uma versão estendida **de CMINVOKECOMMANDINFO** e tem vários membros adicionais que possibilitam passar cadeias de caracteres Unicode.

Verifique o **membro cbSize** do *pici* para determinar qual estrutura foi passada. Se for uma estrutura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e o membro **fMask** tiver o sinalizador **\_ \_ UNICODE DE MÁSCARA CMIC** definido, *casti* para **CMINVOKECOMMANDINFOEX**. Isso permite que seu aplicativo use as informações Unicode contidas nos últimos cinco membros da estrutura.

O membro **lpVerb** ou **lpVerbW** da estrutura é usado para identificar o comando a ser executado. Os comandos são identificados de uma das duas maneiras a seguir:

-   Pela cadeia de caracteres de verbo do comando
-   Pelo deslocamento do identificador do comando

Para distinguir entre esses dois casos, verifique a palavra de ordem alta **de lpVerb** para o caso ANSI ou **lpVerbW** para o caso Unicode. Se a palavra de ordem alta for não zero, **lpVerb** ou **lpVerbW** manterá uma cadeia de caracteres de verbo. Se a palavra de ordem alta for zero, o deslocamento de comando será na palavra de ordem baixa **de lpVerb**.

O exemplo a seguir mostra uma implementação simples de [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde aos exemplos [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) dados antes e depois desta seção. O método primeiro determina qual estrutura está sendo passada. Em seguida, ele determina se o comando é identificado por seu deslocamento ou seu verbo. Se **lpVerb** ou **lpVerbW** tiver um verbo ou deslocamento válido, o método exibirá uma caixa de mensagem.


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a>Método IContextMenu::QueryContextMenu

O Shell chama [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar o manipulador de menu de atalho para adicionar seus itens de menu ao menu. Ele passa o **alça HMENU** no *parâmetro hmenu.* O *parâmetro indexMenu* é definido como o índice a ser usado para o primeiro item de menu a ser adicionado.

Todos os itens de menu adicionados pelo manipulador devem ter identificadores que se enquadram entre os valores nos parâmetros *idCmdFirst* e *idCmdLast.* Normalmente, o primeiro identificador de comando é definido como *idCmdFirst*, que é incrementado em um (1) para cada comando adicional. Essa prática ajuda você a evitar exceder *idCmdLast* e maximiza o número de identificadores disponíveis no caso de o Shell chamar mais de um manipulador.

O deslocamento de comando de um *identificador* de item é a diferença entre o identificador e o valor *em idCmdFirst.* Armazene o deslocamento de cada item que o manipulador adiciona ao menu de atalho, pois o Shell poderá usar o deslocamento para identificar o item se ele chamar [**posteriormente IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) [**ou IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

Você também deve atribuir um [verbo](launch.md) a cada comando que adicionar. Um verbo é uma cadeia de caracteres que pode ser usada em vez do deslocamento para identificar o comando [**quando InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é chamado. Ele também é usado por funções como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para executar comandos de menu de atalho.

Há três sinalizadores que podem ser passados por meio do parâmetro *uFlags* que são relevantes para manipuladores de menu de atalho. Eles são descritos na tabela a seguir.



| Sinalizador             | Descrição                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | O usuário selecionou o comando padrão, geralmente clicando duas vezes no objeto . [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve retornar o controle ao Shell sem modificar o menu. |
| CMF \_ NODEFAULT   | Nenhum item no menu deve ser o item padrão. O método deve adicionar seus comandos ao menu.                                                                                                                          |
| CMF \_ NORMAL      | O menu de atalho será exibido normalmente. O método deve adicionar seus comandos ao menu.                                                                                                                            |



 

Use [**InsertMenu ou**](/windows/win32/api/winuser/nf-winuser-insertmenua) [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para adicionar itens de menu à lista. Em seguida, **retorne um valor HRESULT** com a severidade definida como SEVERITY \_ SUCCESS. De definir o valor do código como o deslocamento do maior identificador de comando que foi atribuído, mais um (1). Por exemplo, suponha que *idCmdFirst* seja definido como 5 e você adicione três itens ao menu com identificadores de comando 5, 7 e 8. O valor de retorno deve ser MAKE \_ HRESULT(SEVERITY \_ SUCCESS, 0, 8 + 1).

O exemplo a seguir mostra uma implementação simples [**de QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que insere um único comando. O deslocamento do identificador para o comando é IDM \_ DISPLAY, que é definido como zero. As **variáveis m \_ pszVerb** e **m \_ pwszVerb** são variáveis privadas usadas para armazenar a cadeia de caracteres de verbo independente de idioma associada nos formatos ANSI e Unicode.


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a>Comentários

Para outras tarefas de implementação de verbo, consulte [Criando manipuladores de menu de atalho.](context-menu-handlers.md)

 

 
