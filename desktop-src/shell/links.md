---
description: um link do shell é um objeto de dados que contém informações usadas para acessar outro objeto no namespace do Shell&\# 8212; ou seja, qualquer objeto visível por meio do Windows Explorer.
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Links do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f9f5e639cfa3619d5c79b011ab101af7c25ed1813db1c96b9f5422504f8c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859018"
---
# <a name="shell-links"></a>Links do Shell

um *link do Shell* é um objeto de dados que contém informações usadas para acessar outro objeto no namespace do Shell, ou seja, qualquer objeto visível por meio do Windows Explorer. Os tipos de objetos que podem ser acessados por meio de links do Shell incluem arquivos, pastas, unidades de disco e impressoras. Um link do Shell permite que um usuário ou um aplicativo acesse um objeto de qualquer lugar no namespace. O usuário ou o aplicativo não precisa saber o nome atual e o local do objeto.

-   [Sobre links do Shell](#about-shell-links)
    -   [Resolução de link](#link-resolution)
    -   [Vincular arquivos](#link-files)
    -   [Identificadores de item e listas de identificadores](#item-identifiers-and-identifier-lists)
-   [Usando links do Shell](#using-shell-links)
    -   [Criação de um atalho e um atalho de pasta para um arquivo](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [Resolvendo um atalho](#resolving-a-shortcut)
    -   [Criando um atalho para um objeto não arquivo](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a>Sobre links do Shell

O usuário cria um link do Shell escolhendo o comando **criar atalho** no menu de atalho de um objeto. O sistema cria automaticamente um ícone para o link do Shell combinando o ícone do objeto com uma pequena seta (conhecida como ícone de sobreposição de link definido pelo sistema) que aparece no canto inferior esquerdo do ícone. Um link do shell que tem um ícone é chamado de atalho; no entanto, os termos link e atalho do shell são frequentemente usados de maneira intercambiável. Normalmente, o usuário cria atalhos para obter acesso rápido a objetos armazenados em subpastas ou em pastas compartilhadas em outros computadores. por exemplo, um usuário pode criar um atalho para um documento Microsoft Word que está localizado em uma subpasta e posicionar o ícone de atalho na área de trabalho. Em seguida, o usuário pode abrir o documento clicando duas vezes no ícone de atalho. Se o documento for movido ou renomeado depois que o atalho for criado, o sistema tentará atualizar o atalho na próxima vez que o usuário o selecionar.

Os aplicativos também podem criar e usar links e atalhos do Shell. Por exemplo, um aplicativo de processamento de texto pode criar um link do Shell para implementar uma lista dos documentos usados mais recentemente. Um aplicativo cria um link do shell usando a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para criar um objeto de link do Shell. O aplicativo usa a interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) para armazenar o objeto em um arquivo ou fluxo.

> [!Note]  
> Você não pode usar [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para criar um link para uma URL.

 

Esta visão geral descreve a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) e explica como usá-la para criar e resolver links de Shell de dentro de um aplicativo baseado no Microsoft Win32. Como o design de links do Shell se baseia no COM (Component Object Model OLE), você deve estar familiarizado com os conceitos básicos da programação COM e OLE antes de ler essa visão geral.

### <a name="link-resolution"></a>Resolução de link

Se um usuário criar um atalho para um objeto e o nome ou o local do objeto for alterado posteriormente, o sistema executará automaticamente as etapas para atualizar ou resolver o atalho na próxima vez que o usuário o selecionar. No entanto, se um aplicativo criar um link do Shell e o armazenar em um fluxo, o sistema não tentará resolver automaticamente o link. O aplicativo deve resolver o link chamando o método [**IShellLink:: resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) .

Quando um link do Shell é criado, o sistema salva as informações sobre o link. Ao resolver um link, seja automaticamente ou com uma chamada [**IShellLink:: resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) — o sistema primeiro recupera o caminho associado ao link do shell usando um ponteiro para a lista de identificadores do link do Shell. Para obter mais informações sobre a lista de identificadores, consulte [identificadores de item e listas de identificadores](#item-identifiers-and-identifier-lists). O sistema pesquisa o objeto associado nesse caminho e, se encontrar o objeto, resolve o link. Se o sistema não conseguir localizar o objeto, ele chamará o serviço de [rastreamento de link distribuído e](../fileio/distributed-link-tracking-and-object-identifiers.md) de DLT (identificadores de objeto), se disponível, para localizar o objeto. Se o serviço DLT não estiver disponível ou não puder localizar o objeto, o sistema examinará o mesmo diretório em busca de um objeto com o mesmo tempo e atributos de criação de arquivo, mas com um nome diferente. Esse tipo de pesquisa resolve um link para um objeto que foi renomeado.

Se o sistema ainda não conseguir localizar o objeto, ele pesquisará os diretórios, a área de trabalho e os volumes locais, olhando recursivamente, embora a árvore de diretórios de um objeto com o mesmo nome ou hora de criação. Se o sistema ainda não encontrar uma correspondência, ele exibirá uma caixa de diálogo solicitando ao usuário um local. Um aplicativo pode suprimir a caixa de diálogo especificando o **SLR nenhum valor de \_ interface do \_ usuário** em uma chamada para [**IShellLink:: resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).

### <a name="initialization-of-the-component-object-library"></a>Inicialização da biblioteca de objetos de componente

Antes que um aplicativo possa criar e resolver atalhos, ele deve inicializar a biblioteca de objetos de componente chamando a função [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) . Cada chamada para **CoInitialize** requer uma chamada correspondente para a função [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , que um aplicativo deve chamar quando termina. A chamada para **CoUninitialize** garante que o aplicativo não seja encerrado até que tenha recebido todas as suas mensagens pendentes.

### <a name="location-independent-names"></a>Nomes de Location-Independent

O sistema fornece nomes independentes de local para links de Shell para objetos armazenados em pastas compartilhadas. Se o objeto for armazenado localmente, o sistema fornecerá o caminho local e o nome do arquivo para o objeto. Se o objeto for armazenado remotamente, o sistema fornecerá um nome de recurso de rede UNC (Convenção de nomenclatura universal) para o objeto. Como o sistema fornece nomes independentes de local, um link de shell pode servir como um nome universal para um arquivo que pode ser transferido para outros computadores.

### <a name="link-files"></a>Vincular arquivos

quando o usuário cria um atalho para um objeto escolhendo o comando **criar atalho** no menu de atalho do objeto, Windows armazena as informações necessárias para acessar o objeto em um arquivo de link — um arquivo binário que tem a extensão de nome de arquivo. lnk. Um arquivo de link contém as seguintes informações:

-   O local (caminho) do objeto referenciado pelo atalho (chamado de objeto correspondente).
-   O diretório de trabalho do objeto correspondente.
-   A lista de argumentos que o sistema passa para o objeto correspondente quando o método [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) é ativado para o atalho.
-   O comando show usado para definir o estado de exibição inicial do objeto correspondente. Esse é um dos valores de SW \_ descritos em [**conwindow**](/windows/win32/api/winuser/nf-winuser-showwindow).
-   O local (caminho e índice) do ícone do atalho.
-   A cadeia de caracteres de descrição do atalho.
-   O atalho de teclado para o atalho.

Quando um arquivo de link é excluído, o objeto correspondente não é afetado.

Se você criar um atalho para outro atalho, o sistema simplesmente copiará o arquivo de link em vez de criar um novo arquivo de link. Nesse caso, os atalhos não serão independentes um do outro.

Um aplicativo pode registrar uma extensão de nome de arquivo como um tipo de arquivo de atalho. Se um arquivo tiver uma extensão de nome de arquivo que tenha sido registrada como um tipo de arquivo de atalho, o sistema adicionará automaticamente o ícone de sobreposição de link definido pelo sistema (uma pequena seta) ao ícone do arquivo. Para registrar uma extensão de nome de arquivo como um tipo de arquivo de atalho, você deve adicionar o valor IsShortcut à descrição do registro da extensão de nome de arquivo, conforme mostrado no exemplo a seguir. Observe que o Shell deve ser reiniciado para que o ícone de sobreposição entre em vigor. IsShortcut não tem valor de dados.

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a>Nomes de atalho

O nome do atalho, que é uma cadeia de caracteres que aparece abaixo do ícone de link do Shell, é, na verdade, o nome do arquivo do próprio atalho. O usuário pode editar a cadeia de caracteres de descrição selecionando-a e inserindo uma nova cadeia de caracteres.

### <a name="location-of-shortcuts-in-the-namespace"></a>Local dos atalhos no namespace

Um atalho pode existir na área de trabalho ou em qualquer lugar no namespace do Shell. Da mesma forma, o objeto que está associado ao atalho também pode existir em qualquer lugar no namespace do Shell. Um aplicativo pode usar o método [**IShellLink:: SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) para definir o caminho e o nome de arquivo para o objeto associado e o método [**IShellLink:: GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) para recuperar o caminho atual e o nome do arquivo para o objeto.

### <a name="shortcut-working-directory"></a>Diretório de trabalho de atalho

O diretório de trabalho é o diretório em que o objeto correspondente de um atalho carrega ou armazena arquivos quando o usuário não identifica um diretório específico. Um arquivo de link contém o nome do diretório de trabalho para o objeto correspondente. Um aplicativo pode definir o nome do diretório de trabalho para o objeto correspondente usando o método [**IShellLink:: SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) e pode recuperar o nome do diretório de trabalho atual para o objeto correspondente usando o método [**IShellLink:: GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) .

### <a name="shortcut-command-line-arguments"></a>Argumentos de linha de comando de atalho

Um arquivo de link contém argumentos de linha de comando que o Shell passa para o objeto correspondente quando o usuário seleciona o link. Um aplicativo pode definir os argumentos de linha de comando para um atalho usando o método [**IShellLink:: SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) . É útil definir argumentos de linha de comando quando o aplicativo correspondente, como um vinculador ou compilador, usa sinalizadores especiais como argumentos. Um aplicativo pode recuperar os argumentos de linha de comando de um atalho usando o método [**IShellLink:: Getarguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) .

### <a name="shortcut-show-commands"></a>Comandos show de atalho

Quando o usuário clica duas vezes em um atalho, o sistema inicia o aplicativo associado ao objeto correspondente e define o estado de exibição inicial do aplicativo com base no comando show especificado pelo atalho. O comando show pode ser qualquer um dos valores de SW \_ incluídos na descrição da função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) . Um aplicativo pode definir o comando show para um atalho usando o método [**IShellLink:: SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) e pode recuperar o comando show atual usando o método [**IShellLink:: GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) .

### <a name="shortcut-icons"></a>Ícones de atalho

Assim como outros objetos do Shell, um atalho tem um ícone. O usuário acessa o objeto associado a um atalho clicando duas vezes no ícone do atalho. Quando o sistema cria um ícone para um atalho, ele usa o bitmap do objeto correspondente e adiciona o ícone de sobreposição de link definido pelo sistema (uma seta pequena) no canto inferior esquerdo. Um aplicativo pode definir o local (caminho e índice) do ícone de um atalho usando o método [**IShellLink:: SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) . Um aplicativo pode recuperar esse local usando o método [**IShellLink:: GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) .

### <a name="shortcut-descriptions"></a>Descrições de atalho

Os atalhos têm descrições, mas o usuário nunca as vê. Um aplicativo pode usar uma descrição para armazenar qualquer informação de texto. As descrições são definidas usando o [**método IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) e recuperadas usando o [**método IShellLink::GetDescription.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription)

### <a name="shortcut-keyboard-shortcuts"></a>Atalhos de teclado de atalho

Um objeto de atalho pode ter um atalho de teclado associado a ele. Atalhos de teclado permitem que um usuário pressione uma combinação de teclas para ativar um atalho. Um aplicativo pode definir o atalho de teclado para um atalho usando o método [**IShellLink::SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) e pode recuperar o atalho de teclado atual usando o método [**IShellLink::GetHotkey.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey)

### <a name="item-identifiers-and-identifier-lists"></a>Identificadores de item e listas de identificadores

O Shell usa identificadores de objeto dentro do namespace do Shell. Todos os objetos visíveis no Shell (arquivos, diretórios, servidores, grupos de trabalho e assim por diante) têm identificadores exclusivos entre os objetos dentro de sua pasta pai. Esses identificadores são chamados de identificadores de item e têm o tipo de dados [**DEMID,**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) conforme definido no arquivo de header Shtypes.h. Um identificador de item é um fluxo de byte de comprimento variável que contém informações que identificam um objeto dentro de uma pasta. Somente o criador de um identificador de item sabe o conteúdo e o formato do identificador. A única parte de um identificador de item que o Shell usa é os dois primeiros bytes, que especificam o tamanho do identificador.

Cada pasta pai tem seu próprio identificador de item que o identifica dentro de sua própria pasta pai. Portanto, qualquer objeto Shell pode ser identificado exclusivamente por uma lista de identificadores de item. Uma pasta pai mantém uma lista de identificadores para os itens que ela contém. A lista tem o [**tipo de dados ITEMIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) As listas de identificadores de item são alocadas pelo Shell e podem ser passadas entre interfaces do Shell, como [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder). É importante lembrar que cada identificador em uma lista de identificadores de item só é significativo dentro do contexto de sua pasta pai.

Um aplicativo pode definir uma lista de identificadores de item de atalho usando o [**método IShellLink::SetIDList.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) Esse método é útil ao definir um atalho para um objeto que não é um arquivo, como uma impressora ou unidade de disco. Um aplicativo pode recuperar a lista de identificadores de item de um atalho usando o [**método IShellLink::GetIDList.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist)

## <a name="using-shell-links"></a>Usando links do Shell

Esta seção contém exemplos que demonstram como criar e resolver atalhos de dentro de um aplicativo baseado em Win32. Esta seção pressupo que você está familiarizado com a programação Win32, C++e OLE COM.

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a>Criando um atalho e um atalho de pasta para um arquivo

A função de exemplo CreateLink no exemplo a seguir cria um atalho. Os parâmetros incluem um ponteiro para o nome do arquivo para vincular, um ponteiro para o nome do atalho que você está criando e um ponteiro para a descrição do link. A descrição consiste na cadeia de caracteres " Atalho para **o** nome do arquivo ", em que nome de arquivo **é** o nome do arquivo ao qual vincular.

Para criar um atalho de pasta usando a função de exemplo CreateLink, chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usando CLSID FolderShortcut, em vez de \_ CLSID \_ ShellLink (o CLSID FolderShortcut dá suporte a \_ IShellLink). Todos os outros códigos permanecem os mesmos.

Como CreateLink chama a [**função CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) supõe-se que a [**função CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) já tenha sido chamada. CreateLink usa a interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para salvar o atalho e a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) para armazenar o nome e a descrição do arquivo.


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a>Resolvendo um atalho

Um aplicativo pode precisar acessar e manipular um atalho criado anteriormente. Essa operação é conhecida como resolução do atalho.

A função ResolveIt definida pelo aplicativo no exemplo a seguir resolve um atalho. Seus parâmetros incluem um identificador de janela, um ponteiro para o caminho do atalho e o endereço de um buffer que recebe o novo caminho para o objeto. O identificador de janela identifica a janela pai para todas as caixas de mensagem que o Shell talvez precise exibir. Por exemplo, o Shell poderá exibir uma caixa de mensagem se o link estiver em mídia não compartilhada, se ocorrerem problemas de rede, se o usuário precisar inserir um disquete e assim por diante.

A função ResolveIt chama a [**função CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e assume que a [**função CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) já foi chamada. Observe que ResolveIt precisa usar a interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) para armazenar as informações de link. **IPersistFile** é implementado pelo [**objeto IShellLink.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) As informações de link devem ser carregadas antes que as informações de caminho sejam recuperadas, o que é mostrado posteriormente no exemplo. A falha ao carregar as informações de link faz com que as chamadas para as funções membro [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) e [**IShellLink::GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) falhem.


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a>Criando um atalho para um objeto nonfile

A criação de um atalho para um objeto não arquivo, como uma impressora, é semelhante à criação de um atalho para um arquivo, exceto que, em vez de definir o caminho para o arquivo, você deve definir a lista de identificadores para a impressora. Para definir a lista de identificadores, chame o [**método IShellLink::SetIDList,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) especificando o endereço de uma lista de identificadores.

Cada objeto dentro do namespace do Shell tem um identificador de item. O Shell geralmente concatena identificadores de item em listas terminadas em nulo que consistem em qualquer número de identificadores de item. Para obter mais informações sobre identificadores de item, consulte [Identificadores de item e listas de identificadores](#item-identifiers-and-identifier-lists).

Em geral, se você precisar definir um atalho para um item que não tem um nome de arquivo, como uma impressora, você já terá um ponteiro para a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) do objeto. **IShellFolder é** usado para criar extensões de namespace.

Depois de ter o identificador de classe [**para IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), você pode chamar a [**função CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para recuperar o endereço da interface. Em seguida, você pode chamar a interface para enumerar os objetos na pasta e recuperar o endereço do identificador de item para o objeto que você está procurando. Por fim, você pode usar o endereço em uma chamada para a função membro [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) para criar um atalho para o objeto .

 

 
