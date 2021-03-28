---
description: Os manipuladores de menu de atalho também são conhecidos como manipuladores de menu de contexto ou manipuladores de verbo. Um manipulador de menu de atalho é um tipo de manipulador de tipo de arquivo.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalizando um menu de atalho usando verbos dinâmicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968058"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Personalizando um menu de atalho usando verbos dinâmicos

Os manipuladores de menu de atalho também são conhecidos como manipuladores de menu de contexto ou manipuladores de verbo. Um manipulador de menu de atalho é um tipo de manipulador de tipo de arquivo.

Este tópico é organizado da seguinte maneira:

-   [Sobre verbos estáticos e dinâmicos](#about-static-and-dynamic-verbs)
-   [Como os manipuladores de menu de atalho funcionam com verbos dinâmicos](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Evitando colisões devido a nomes de verbo não qualificados](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Registrando um manipulador de menu de atalho com um verbo dinâmico](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implementando a interface IContextMenu](#implementing-the-icontextmenu-interface)
    -   [Método IContextMenu:: GetCommandString](#icontextmenugetcommandstring-method)
    -   [Método IContextMenu:: InvokeCommand](#icontextmenuinvokecommand-method)
    -   [Método IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method)
-   [Tópicos relacionados](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>Sobre verbos estáticos e dinâmicos

Recomendamos que você implemente um menu de atalho usando um dos métodos de verbo estáticos. Recomendamos que você siga as instruções fornecidas na seção "Personalizando um menu de atalho usando verbos estáticos" de [criando manipuladores de menu de contexto](context-menu-handlers.md). Para obter um comportamento dinâmico para verbos estáticos no Windows 7 e posterior, consulte "obtendo comportamento dinâmico para verbos estáticos" na [criação de manipuladores de menu de contexto](context-menu-handlers.md). Para obter detalhes sobre a implementação de verbo estático e quais verbos dinâmicos evitar, consulte [escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md).

Se você precisar estender o menu de atalho para um tipo de arquivo registrando um verbo dinâmico para o tipo de arquivo, siga as instruções fornecidas mais adiante neste tópico.

> [!Note]  
> Há considerações especiais para o Windows de 64 bits ao registrar manipuladores que funcionam no contexto de aplicativos de 32 bits: quando os verbos do shell são invocados no contexto de um aplicativo de 32 bits, o subsistema WOW64 redireciona o acesso ao sistema de arquivos para alguns caminhos. Se o manipulador. exe for armazenado em um desses caminhos, ele não estará acessível neste contexto. Portanto, como uma solução alternativa, armazene seu. exe em um caminho que não seja redirecionado ou armazene uma versão de stub do seu. exe que inicia a versão real.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Como os manipuladores de menu de atalho funcionam com verbos dinâmicos

Além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), os manipuladores de menu de atalho exportam as seguintes interfaces adicionais para lidar com as mensagens necessárias para implementar os itens de menu desenhados pelo proprietário:

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obrigatório)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obrigatório)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (opcional)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (opcional)

Para obter mais informações sobre itens de menu de desenho proprietário, consulte a seção *criando Owner-Drawn itens de menu* em [usando menus](../menurc/using-menus.md).

O Shell usa a interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para inicializar o manipulador. Quando o Shell chama [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), ele passa um objeto de dados com o nome do objeto e um ponteiro para uma PIDL (lista de identificadores de item) da pasta que contém o arquivo. O parâmetro *hkeyProgID* é o local do registro sob o qual o identificador do menu de atalho é registrado. O método **IShellExtInit:: Initialize** deve extrair o nome do arquivo do objeto de dados e armazenar o nome e o ponteiro da pasta para uma PIDL (lista de identificadores de item) para uso posterior. Para obter mais informações sobre a inicialização do manipulador, consulte [implementando IShellExtInit](handlers.md).

Quando os verbos são apresentados em um menu de atalho, eles são descobertos primeiro, apresentados ao usuário e finalmente invocados. A lista a seguir descreve essas três etapas mais detalhadamente:

1.  O Shell chama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), que retorna um conjunto de verbos que podem ser baseados no estado dos itens ou do sistema.
2.  O sistema passa um identificador **HMENU** que o método pode usar para adicionar itens ao menu de atalho.
3.  Se o usuário clicar em um dos itens do manipulador, o Shell chamará [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand). O manipulador pode então executar o comando apropriado.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Evitando colisões devido a nomes de verbo não qualificados

Como os verbos são registrados por tipo, o mesmo nome de verbo pode ser usado para verbos em itens diferentes. Isso permite que os aplicativos façam referência a verbos comuns independentes do tipo de item. Embora essa funcionalidade seja útil, o uso de nomes não qualificados pode resultar em colisões com vários fornecedores independentes de software (ISVs) que escolhem o mesmo nome de verbo. Para evitar isso, sempre Prefixe os verbos com o nome do ISV da seguinte maneira:

`ISV_Name.verb`

Sempre use um ProgID específico do aplicativo. A adoção da Convenção de mapeamento da extensão de nome de arquivo para um ProgID fornecido pelo ISV evita colisões em potencial. No entanto, como alguns tipos de item não usam esse mapeamento, há uma necessidade de nomes exclusivos de fornecedor. Ao adicionar um verbo a um ProgID existente que pode já ter esse verbo registrado, você deve primeiro remover a chave do registro do verbo antigo antes de adicionar seu próprio verbo. Você deve fazer isso para evitar a mesclagem das informações de verbo dos dois verbos. A falha em fazer isso resulta em um comportamento imprevisível.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Registrando um manipulador de menu de atalho com um verbo dinâmico

Os manipuladores de menu de atalho são associados a um tipo de arquivo ou a uma pasta. Para tipos de arquivo, o manipulador é registrado na subchave a seguir.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Para associar um manipulador de menu de atalho a um tipo de arquivo ou uma pasta, primeiro crie uma subchave na subchave **ContextMenuHandlers** . Nomeie a subchave para o manipulador e defina o valor padrão da subchave como a forma de cadeia de caracteres do GUID do identificador de classe (CLSID) do manipulador.

Em seguida, para associar um manipulador de menu de atalho a diferentes tipos de pastas, registre o manipulador da mesma maneira que você faria para um tipo de arquivo, mas sob a subchave *FolderType* , conforme mostrado no exemplo a seguir.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Para obter mais informações sobre a quais tipos de pasta você pode registrar manipuladores, consulte [Registrando manipuladores de extensão de shell](handlers.md).

Se um tipo de arquivo tiver um menu de atalho associado a ele, clicar duas vezes em um objeto normalmente iniciará o comando padrão e o método [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) do manipulador não será chamado. Para especificar que o método **IContextMenu:: QueryContextMenu** do manipulador deve ser chamado quando um objeto for clicado duas vezes, crie uma subchave na subchave **CLSID** do manipulador, conforme mostrado aqui.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Quando um objeto associado ao manipulador é clicado duas vezes, [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) é chamado com o **sinalizador \_ DefaultOnly CMF** definido no parâmetro *uFlags* .

Os manipuladores de menu de atalho devem definir a subchave **MayChangeDefaultMenu** somente se talvez precisem alterar o verbo padrão do menu de atalho. Definir essa subchave força o sistema a carregar a DLL do manipulador quando um item associado é clicado duas vezes. Se o seu manipulador não alterar o verbo padrão, você não deverá definir essa subchave porque fazer isso faz com que o sistema carregue sua DLL desnecessariamente.

O exemplo a seguir ilustra as entradas do registro que habilitam um manipulador de menu de atalho para um tipo de arquivo. MYP. A subchave **CLSID** do manipulador inclui uma subchave **MayChangeDefaultMenu** para garantir que o manipulador seja chamado quando o usuário clicar duas vezes em um objeto relacionado.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a>Implementando a interface IContextMenu

O [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) é o mais potente, mas também o método mais complicado para implementar. É altamente recomendável que você implemente um verbo usando um dos métodos de verbo estáticos. Para obter mais informações, consulte [escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) tem três métodos, **GetCommandString**, **InvokeCommand** e **QueryContextMenu**, que são discutidos aqui em detalhes.

### <a name="icontextmenugetcommandstring-method"></a>Método IContextMenu:: GetCommandString

O método [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) do manipulador é usado para retornar o nome canônico de um verbo. Esse método é opcional. No Windows XP e em versões anteriores do Windows, quando o Windows Explorer tem uma barra de status, esse método é usado para recuperar o texto de ajuda que é exibido na barra de status de um item de menu.

O parâmetro *idCmd* contém o deslocamento do identificador do comando que foi definido quando [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) foi chamado. Se uma cadeia de caracteres de ajuda for solicitada, *uFlags* será definido como **GCS \_ HELPTEXTW**. Copie a cadeia de caracteres de ajuda para o buffer *pszName* , convertê-lo em um **PWSTR**. A cadeia de caracteres de verbo é solicitada definindo *uFlags* para **GCS \_ VERBW**. Copie a cadeia de caracteres apropriada para *pszName*, assim como com a cadeia de caracteres de ajuda. Os sinalizadores do **\_ VALIDATEW** de **\_ validação de GCS** e GCS não são usados pelos manipuladores de menu de atalho.

O exemplo a seguir mostra uma implementação simples de [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) que corresponde ao exemplo [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornecido na seção do [método IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method) deste tópico. Como o manipulador adiciona apenas um item de menu, há apenas um conjunto de cadeias de caracteres que podem ser retornadas. O método testa se *idCmd* é válido e, se for, retorna a cadeia de caracteres solicitada.

A função [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) é usada para copiar a cadeia de caracteres solicitada para *pszName* para garantir que a cadeia de caracteres copiada não exceda o tamanho do buffer especificado por *cchName*. Este exemplo só implementa suporte para os valores Unicode de *uFlags*, pois apenas aqueles foram usados no Windows Explorer desde o Windows 2000.


```C++
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
                // to discover the canonical name for the verb passed in
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



### <a name="icontextmenuinvokecommand-method"></a>Método IContextMenu:: InvokeCommand

Esse método é chamado quando um usuário clica em um item de menu para instruir o manipulador a executar o comando associado. O parâmetro *Pici* aponta para uma estrutura que contém as informações necessárias.

Embora *Pici* seja declarado em shlobj. h como uma estrutura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , na prática geralmente aponta para uma estrutura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Essa estrutura é uma versão estendida do **CMINVOKECOMMANDINFO** e tem vários membros adicionais que possibilitam a passagem de cadeias de caracteres Unicode.

Verifique o membro **cbSize** de *Pici* para determinar qual estrutura foi passada. Se for uma estrutura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e o membro **fMask** tiver o sinalizador **\_ \_ Unicode de máscara CMIC** definido, converta *Pici* para **CMINVOKECOMMANDINFOEX**. Isso permite que seu aplicativo use as informações de Unicode contidas nos últimos cinco membros da estrutura.

O membro **lpVerb** ou **lpVerbW** da estrutura é usado para identificar o comando a ser executado. Os comandos são identificados de uma das duas maneiras a seguir:

-   Pela cadeia de caracteres de verbo do comando
-   Pelo deslocamento do identificador do comando

Para distinguir entre esses dois casos, verifique a palavra de ordem superior de **lpVerb** para o caso ANSI ou **lpVerbW** para o caso Unicode. Se a palavra de ordem superior for diferente de zero, **lpVerb** ou **lpVerbW** manterá uma cadeia de caracteres de verbo. Se a palavra de ordem superior for zero, o deslocamento de comando estará na palavra de ordem inferior de **lpVerb**.

O exemplo a seguir mostra uma implementação simples de [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) que corresponde aos exemplos de [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) fornecidos antes e depois desta seção. O método determina primeiro qual estrutura está sendo passada. Em seguida, ele determina se o comando é identificado por seu deslocamento ou seu verbo. Se **lpVerb** ou **lpVerbW** mantiver um verbo ou um deslocamento válido, o método exibirá uma caixa de mensagem.


```C++
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



### <a name="icontextmenuquerycontextmenu-method"></a>Método IContextMenu:: QueryContextMenu

O Shell chama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para habilitar o manipulador de menu de atalho para adicionar seus itens de menu ao menu. Ele passa o identificador **HMENU** no parâmetro *HMENU* . O parâmetro *indexMenu* é definido como o índice a ser usado para o primeiro item de menu a ser adicionado.

Todos os itens de menu que são adicionados pelo manipulador devem ter identificadores que se enquadram entre os valores nos parâmetros *idCmdFirst* e *idCmdLast* . Normalmente, o primeiro identificador de comando é definido como *idCmdFirst*, que é incrementado em um (1) para cada comando adicional. Essa prática ajuda a evitar exceder o *idCmdLast* e maximiza o número de identificadores disponíveis caso o Shell chame mais de um manipulador.

Um *deslocamento de comando* do identificador de item é a diferença entre o identificador e o valor em *idCmdFirst*. Armazene o deslocamento de cada item que seu manipulador adiciona ao menu de atalho porque o Shell pode usá-lo para identificar o item se ele posteriormente chamar [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ou [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

Você também deve atribuir um [verbo](launch.md) a cada comando que adicionar. Um verbo é uma cadeia de caracteres que pode ser usada em vez do deslocamento para identificar o comando quando [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é chamado. Ele também é usado por funções como [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) para executar comandos de menu de atalho.

Há três sinalizadores que podem ser passados por meio do parâmetro *uFlags* que são relevantes para manipuladores de menu de atalho. Eles são descritos na tabela a seguir.



| Sinalizador             | Descrição                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_somente CMF | O usuário selecionou o comando padrão, normalmente clicando duas vezes no objeto. [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve retornar o controle para o shell sem modificar o menu. |
| CMF \_ padrão   | Nenhum item no menu deve ser o item padrão. O método deve adicionar seus comandos ao menu.                                                                                                                          |
| CMF \_ normal      | O menu de atalho será exibido normalmente. O método deve adicionar seus comandos ao menu.                                                                                                                            |



 

Use [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) ou [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para adicionar itens de menu à lista. Em seguida, retorne um valor **HRESULT** com a severidade definida como **\_ êxito de severidade**. Defina o valor do código para o deslocamento do maior identificador de comando que foi atribuído, além de um (1). Por exemplo, suponha que *idCmdFirst* seja definido como 5 e você adicione três itens ao menu com identificadores de comando de 5, 7 e 8. O valor de retorno deve ser `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .

O exemplo a seguir mostra uma implementação simples de [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) que insere um único comando. O deslocamento do identificador para o comando é \_ tela de IDM, que é definido como zero. As variáveis **m \_ pszVerb** e **m \_ pwszVerb** são variáveis privadas usadas para armazenar a cadeia de caracteres verbo independente de idioma associada nos formatos ANSI e Unicode.


```C++
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

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



Para outras tarefas de implementação de verbo, consulte [criando manipuladores de menu de contexto](context-menu-handlers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Verbos e associações de arquivo](fa-verbs.md)
</dt> <dt>

[Escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md)
</dt> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla](verbs-best-practices.md)
</dt> <dt>

[Criando manipuladores de menu de atalho](context-menu-handlers.md)
</dt> <dt>

[Referência do menu de atalho](context-menu-reference.md)
</dt> </dl>

 

 
