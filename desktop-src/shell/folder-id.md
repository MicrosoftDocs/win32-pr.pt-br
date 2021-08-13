---
description: Antes de usar um objeto namespace, você precisa de uma maneira de identificá-lo.
ms.assetid: 54225481-a147-4d29-a642-24c9b59fc3ac
title: Obtendo a ID de uma pasta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d75051d52f0dfcee54b6365a8f546d2cbda2c3b5f7c0f4b6fbbc19fa1e40c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459005"
---
# <a name="getting-a-folders-id"></a>Obtendo a ID de uma pasta

Antes de usar um objeto namespace, você precisa de uma maneira de identificá-lo. Isso significa obter o ponteiro para uma lista de identificadores de item (PIDL) ou, no caso de objetos do sistema de arquivos, seu caminho. Esta seção aborda duas das maneiras mais simples de obter IDs de objeto.

Para obter uma abordagem mais potente que funcionará com qualquer pasta, use a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Consulte [obtendo informações sobre o conteúdo de uma pasta](folder-info.md) para obter mais detalhes.

-   [A caixa de diálogo Openfiles](#the-openfiles-dialog-box)
-   [A caixa de diálogo SHBrowseForFolder](#the-shbrowseforfolder-dialog-box)
-   [Pastas especiais e CSIDLs](#special-folders-and-csidls)
-   [Um exemplo simples de como usar CSIDLs e SHBrowseForFolder](#a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder)

## <a name="the-openfiles-dialog-box"></a>A caixa de diálogo Openfiles

Para permitir que o usuário navegue no namespace e selecione uma pasta, seu aplicativo pode usar a interface [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) . Chamar essa interface com o sinalizador **FOS \_ PICKFOLDERS** inicia a caixa de diálogo [abrir arquivos](../dlgbox/open-and-save-as-dialog-boxes.md) comuns no modo "escolher pastas".

para o Windows Vista e posterior, essa é a maneira recomendada para escolher pastas.

## <a name="the-shbrowseforfolder-dialog-box"></a>A caixa de diálogo SHBrowseForFolder

Para permitir que o usuário navegue pelo namespace e selecione uma pasta, seu aplicativo pode simplesmente invocar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). Chamar essa função inicia uma caixa de diálogo com uma interface do usuário que funciona de certa forma com as caixas de diálogo [abrir ou salvar](../dlgbox/open-and-save-as-dialog-boxes.md) em comum.

Quando o usuário seleciona uma pasta, [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) retorna o PIDL totalmente qualificado da pasta e seu nome de exibição. Se a pasta estiver no sistema de arquivos, o aplicativo poderá converter o PIDL em um caminho chamando [**SHGetPathFromIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista). O aplicativo também pode restringir o intervalo de pastas que o usuário pode selecionar, especificando uma pasta raiz. Somente as pastas que estão abaixo dessa raiz no namespace serão exibidas. A ilustração a seguir mostra a caixa de diálogo **SHBrowseForFolder** , com a pasta raiz definida como arquivos de programas.

![captura de tela da caixa de diálogo Procurar pasta](images/shell1.png)

Um exemplo simples de como usar o [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) é fornecido posteriormente.

## <a name="special-folders-and-csidls"></a>Pastas especiais e CSIDLs

Várias pastas comumente usadas são designadas como *especiais* pelo sistema. Essas pastas têm uma finalidade bem definida e a maioria delas está presente em todos os sistemas. Mesmo que não estejam presentes inicialmente, seus nomes e locais ainda estão definidos, para que possam ser adicionados posteriormente. A coleção de pastas especiais inclui todas as pastas virtuais padrão do sistema, como impressoras, meus documentos e ambiente de rede. Ele também inclui várias pastas padrão do sistema de arquivos, como arquivos de programas e sistema.

Embora as pastas sejam um componente padrão de todos os sistemas, seus nomes e locais no namespace podem variar. por exemplo, o diretório do sistema é C: \\ Winnt \\ system32 em alguns sistemas e C: \\ Windows \\ System32 em outros. No passado, as variáveis de ambiente forneciam uma maneira de determinar o nome e o local de uma pasta especial em qualquer sistema específico. O Shell agora fornece uma maneira mais robusta e flexível de identificar pastas especiais, [**CSIDLs**](csidl.md). Geralmente, você deve usá-los em vez de variáveis de ambiente.

O CSIDLs fornece uma maneira uniforme de identificar e localizar pastas especiais, independentemente de seu nome ou local em um sistema específico. Ao contrário das variáveis de ambiente, CSIDLs pode ser usado com pastas virtuais, bem como pastas do sistema de arquivos. Cada pasta especial tem um CSID exclusivo atribuído a ela. Por exemplo, a pasta sistema de arquivos de arquivos de programas tem um CSIDl de **\_ \_ arquivos de programa CSIDL** e a pasta virtual de ambiente de rede tem uma CSIDL de **\_ rede CSIDL**.

Uma CSIDl é usada em conjunto com uma das várias funções de Shell para recuperar o PIDL de uma pasta especial ou um caminho de pasta do sistema de arquivos especial. Se a pasta não existir em um sistema, seu aplicativo poderá forçá-la a ser criada combinando seu CSIDl com o **sinalizador CSIDL \_ \_ criar**. O CSIDl pode ser passado para as seguintes funções:

-   [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), que recupera o PIDL de uma pasta especial.
-   [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha), que recupera o caminho de uma pasta especial do sistema de arquivos.

Observe que essas duas funções foram introduzidas com a versão 5,0 do Shell e substituem as funções [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation) e [**SHGetSpecialFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderpatha) .

## <a name="a-simple-example-of-how-to-use-csidls-and-shbrowseforfolder"></a>Um exemplo simples de como usar CSIDLs e SHBrowseForFolder

A seguinte função de exemplo, PidlBrowse, ilustra como usar CSIDLs para recuperar a PIDL de uma pasta e usar [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera) para que o usuário selecione uma pasta. Ele retorna o PIDL e o nome de exibição da pasta selecionada.


```
LPITEMIDLIST PidlBrowse(HWND hwnd, int nCSIDL, LPSTR pszDisplayName)
{
    LPITEMIDLIST pidlRoot = NULL;
    LPITEMIDLIST pidlSelected = NULL;
    BROWSEINFO bi = {0};

    if(nCSIDL)
    {
        SHGetFolderLocation(hwnd, nCSIDL, NULL, NULL, &pidlRoot);
    }

    else
    {
        pidlRoot = NULL;
    }

    bi.hwndOwner = hwnd;
    bi.pidlRoot = pidlRoot;
    bi.pszDisplayName = pszDisplayName;
    bi.lpszTitle = "Choose a folder";
    bi.ulFlags = 0;
    bi.lpfn = NULL;
    bi.lParam = 0;

    pidlSelected = SHBrowseForFolder(&bi);

    if(pidlRoot)
    {
        CoTaskMemFree(pidlRoot);
    }

    return pidlSelected;
}
```



O aplicativo de chamada passa em um identificador de janela, que é necessário para o [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera). O parâmetro *nCSIDL* é um CSIDL opcional que é usado para especificar uma pasta raiz. Somente as pastas abaixo da pasta raiz na hierarquia serão exibidas. A ilustração mostrada anteriormente foi gerada chamando essa função com *nCSIDL* definido como **arquivos de \_ programa \_ CSIDL**. O aplicativo de chamada também passa um buffer de cadeia de caracteres, *pszDisplayName*, para manter o nome de exibição da pasta selecionada quando PidlBrowse retorna. É responsabilidade do aplicativo de chamada liberar o IDList retornado pelo **SHBrowseForFolder** usando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

 

 
