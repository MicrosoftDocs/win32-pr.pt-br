---
description: O Shell fornece várias maneiras de gerenciar sistemas de arquivos.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Gerenciando o sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64bce2bea08794451d80fc4b1921baa21ee0fc26544b62ed9412d13b9bcb242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049225"
---
# <a name="managing-the-file-system"></a>Gerenciando o sistema de arquivos

O Shell fornece várias maneiras de gerenciar sistemas de arquivos. O Shell fornece uma função, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), que permite que um aplicativo mova, copie, renomeie e exclua programaticamente arquivos. O Shell também dá suporte a alguns recursos adicionais de gerenciamento de arquivos.

-   Documentos HTML podem ser *conectados* a arquivos relacionados, como arquivos gráficos ou folhas de estilo. Quando o documento é movido ou copiado, os arquivos conectados também são movidos automaticamente ou copiados.
-   Para sistemas que estão disponíveis para mais de um usuário, os arquivos podem ser gerenciados por usuário. Os usuários têm acesso fácil aos seus arquivos de dados, mas não aos arquivos que pertencem a outros usuários.
-   Se os arquivos de documento forem adicionados ou modificados, eles poderão ser adicionados à lista de documentos recentes do Shell. quando o usuário clica no comando **documentos** na menu Iniciar, uma lista de links para os documentos é exibida.

Este documento discute como essas tecnologias de gerenciamento de arquivos funcionam. Em seguida, descreve como usar o Shell para mover, copiar, renomear e excluir arquivos e como gerenciar objetos na lixeira.

-   [Gerenciamento de arquivos por usuário](#per-user-file-management)
-   [Pastas meus documentos e minhas imagens](#my-documents-and-my-pictures-folders)
-   [Arquivos conectados](#connected-files)
-   [Movendo, copiando, renomeando e excluindo arquivos](#moving-copying-renaming-and-deleting-files)
    -   [Notificando o Shell](#notifying-the-shell)
-   [Exemplo simples de gerenciamento de arquivos com o SHFileOperation](#simple-example-of-managing-files-with-shfileoperation)
-   [Adicionando arquivos à lista de documentos recentes do Shell](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a>Gerenciamento de arquivos Per-User

o Windows Shell 2000 permite que os arquivos sejam associados a um usuário específico para que os arquivos permaneçam ocultos de outros usuários. em termos do sistema de arquivos, os arquivos são armazenados na pasta de perfil do usuário, normalmente C: \\ documents e Configurações \\ *nome de usuário* \\ em sistemas Windows 2000. Esse recurso permite que muitos indivíduos usem o mesmo computador, mantendo a privacidade de seus arquivos de outros usuários. Diferentes usuários podem ter programas diferentes disponíveis. Ele também fornece uma maneira simples para os administradores e aplicativos armazenarem coisas como arquivos de inicialização (.ini) ou link (. lnk). Assim, os aplicativos podem preservar um estado diferente para cada usuário e recuperar facilmente esse estado em particular quando necessário. Também há uma pasta de perfil para armazenar informações comuns a todos os usuários.

Como é inconveniente determinar qual usuário está conectado e onde seus arquivos estão localizados, as pastas padrão por usuário são pastas especiais e são identificadas por uma [**CSIDL**](csidl.md). Por exemplo, a CSIDl para a pasta arquivos de programas por usuário são os programas CSIDl \_ . Se seu aplicativo chamar [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com um dos CSIDLs por usuário, a função retornará o ponteiro para uma PIDL (lista de identificadores de item) ou caminho apropriado para o usuário conectado no momento. Se seu aplicativo precisar recuperar o caminho ou PIDL da pasta de perfil, seu CSIDl será o **\_ perfil CSIDL**.

## <a name="my-documents-and-my-pictures-folders"></a>Pastas meus documentos e minhas imagens

Um dos ícones padrão encontrados na área de trabalho é **meus documentos**. Quando você abre essa pasta, ela contém os arquivos de documento atuais do usuário. A instância de área de trabalho de meus documentos é uma pasta virtual — um alias para o local do sistema de arquivos usado para armazenar fisicamente os documentos do usuário — localizado imediatamente abaixo da área de trabalho na hierarquia de namespace.

A finalidade das pastas meus documentos e minhas imagens é fornecer uma maneira direta e segura para que os usuários acessem seus arquivos de documento e imagem em um sistema que possa ter vários usuários. Cada usuário recebe pastas separadas do sistema de arquivos para seus arquivos. por exemplo, o local da pasta documentos de um usuário no sistema de arquivos normalmente é algo como C: \\ documents e Configurações \\ *nome de usuário* \\ My documents. Não há necessidade de que os usuários saibam nada sobre o local físico de suas pastas do sistema de arquivos. Eles simplesmente acessam seus arquivos por meio do ícone meus documentos.

> [!Note]  
> Meus documentos permite que um usuário acesse seus próprios arquivos, mas não aqueles de qualquer outro usuário. Se vários indivíduos usarem o mesmo computador, um administrador poderá bloquear os usuários fora da parte do sistema de arquivos onde os arquivos reais estão armazenados. Portanto, os usuários poderão trabalhar em seus próprios documentos por meio da pasta meus documentos, mas não em documentos que pertençam a outros usuários.

 

Normalmente, não há necessidade de que um aplicativo saiba qual usuário está conectado ou no sistema de arquivos em que a pasta meus documentos do usuário está localizada. Em vez disso, seu aplicativo pode recuperar o PIDL do ícone meus documentos na área de trabalho chamando o método IShellFolder da área de trabalho [**::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) . O nome de análise usado para identificar a pasta meus documentos não é um caminho de arquivo, mas sim: {450d8fba-ad25-11D0-98a8-0800361b1103}. A expressão entre colchetes é a forma de texto do GUID meus documentos. Por exemplo, para recuperar o PIDL de meus documentos, seu aplicativo deve usar essa chamada para **IShellFolder::P arsedisplayname**.


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



Depois que o aplicativo tiver os meus documentos PIDL, ele poderá manipular a pasta da mesma forma que faria com uma pasta normal do sistema de arquivos, enumerando itens, analisando, vinculando e executando qualquer outra operação de pasta válida. O Shell mapeia automaticamente as alterações em meus documentos ou em suas subpastas nas pastas apropriadas do sistema de arquivos.

Se seu aplicativo precisar de acesso à pasta do sistema de arquivos real que contém os documentos do usuário atual, passe CSIDl \_ pessoal para [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation). A função retorna o PIDL da pasta do sistema de arquivos que é exibida na pasta meus documentos do usuário atual.

## <a name="connected-files"></a>Arquivos conectados

documentos HTML geralmente têm um número de arquivos gráficos associados, um arquivo de folha de estilos, vários arquivos do Microsoft JScript (compatíveis com a especificação de linguagem ECMA 262) e assim por diante. Ao mover ou copiar o documento HTML primário, normalmente, você também deseja mover ou copiar seus arquivos associados para evitar a interrupção dos links. Infelizmente, não houve uma maneira fácil até agora determinar quais arquivos estão relacionados a qualquer documento HTML específico, a não ser pela análise de seu conteúdo. para aliviar esse problema, Windows 2000 fornece uma maneira simples de *conectar* um documento HTML primário ao seu grupo de arquivos associados. Se a conexão de arquivo estiver habilitada, quando o documento for movido ou copiado, todos os seus arquivos conectados irão para ele.

Para criar um grupo de arquivos conectados, o documento primário deve ter uma extensão de nome de arquivo .htm ou .html. Crie uma subpasta da pasta pai do documento primário. O nome da subpasta deve ser o nome do documento primário, menos a .htm ou .html extensão, seguido de uma das extensões listadas abaixo. As extensões usadas com mais frequência são ". Files" ou " \_ Files". Por exemplo, se o documento primário for denominado MyDoc.htm, nomear a subpasta " \_ arquivos MyDoc" definirá a subpasta como o contêiner para os arquivos conectados do documento. Se o documento primário for movido ou copiado, a subpasta e seus arquivos também serão movidos ou copiados.

Para alguns idiomas, é possível usar um equivalente localizado de " \_ arquivos" para criar uma subpasta para arquivos conectados. A tabela a seguir lista as cadeias de caracteres válidas que podem ser acrescentadas a um nome de documento para criar uma subpasta arquivos conectados. Observe que algumas dessas cadeias de caracteres têm '-' como seu primeiro caractere em vez de ' \_ ' ou '. '.



:::row:::
   :::column span="":::
      " \_ archivos"
   :::column-end:::
   :::column span="":::
      " \_ arquivos"
   :::column-end:::
   :::column span="":::
      " \_ befique"
   :::column-end:::
   :::column span="":::
      " \_ bylos"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      "-Dateien"
   :::column-end:::
   :::column span="":::
      " \_ datoteke"
   :::column-end:::
   :::column span="":::
      " \_ dosyalar"
   :::column-end:::
   :::column span="":::
      " \_ elemei"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ failid"
   :::column-end:::
   :::column span="":::
      " \_ falha"
   :::column-end:::
   :::column span="":::
      " \_ fajlovi"
   :::column-end:::
   :::column span="":::
      " \_ ficheiros"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ fichiers"
   :::column-end:::
   :::column span="":::
      "-Filer"
   :::column-end:::
   :::column span="":::
      ". Files"
   :::column-end:::
   :::column span="":::
      " \_ arquivos"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ arquivo"
   :::column-end:::
   :::column span="":::
      " \_ fitxers"
   :::column-end:::
   :::column span="":::
      " \_ fitxategiak"
   :::column-end:::
   :::column span="":::
      " \_ pliki"
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      " \_ soubory"
   :::column-end:::
   :::column span="":::
      " \_ tiedostot"
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> Esse recurso é sensível ao caso da extensão. Por exemplo, para os exemplos fornecidos acima, uma subpasta denominada " \_ arquivos MyDoc" não será conectada a MyDoc.htm.

 

Se a conexão de arquivo está habilitada ou desabilitada é controlada por um valor **reg \_ DWORD** , NoFileFolderConnection, da seguinte chave do registro.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

Esse valor normalmente não está definido e a conexão do arquivo está habilitada. Se necessário, você pode desabilitar a conexão de arquivo adicionando esse valor à chave e definindo-o como 1. Para habilitar a conexão de arquivo novamente, defina NoFileFolderConnection como zero.

> [!Note]  
> A conexão de arquivo normalmente deve ser habilitada porque outros aplicativos podem depender dela. Desabilite a conexão de arquivos somente se for absolutamente necessário.

 

## <a name="moving-copying-renaming-and-deleting-files"></a>Movendo, copiando, renomeando e excluindo arquivos

O namespace não é estático e os aplicativos geralmente precisam gerenciar o sistema de arquivos executando uma das operações a seguir.

-   Copiando um objeto para outra pasta.
-   Movendo um objeto para outra pasta.
-   Excluindo um objeto .
-   Renomeando um objeto .

Todas essas operações são executadas com [**SHFileOperation.**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) Essa função pega um ou mais arquivos de origem e produz arquivos de destino correspondentes. No caso da operação de exclusão, o sistema tenta colocar os arquivos excluídos no Lixeira.

Também é possível mover arquivos usando a [funcionalidade do "arrastar e](dragdrop.md) soltar".

Para usar a função , você deve preencher os membros de uma estrutura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) e passá-la para [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa). Os principais membros da estrutura são **pFrom** e **pTo.**

O **membro pFrom** é uma cadeia **de** caracteres terminada em nulo duplo que contém um ou mais nomes de arquivo de origem. Esses nomes podem ser caminhos totalmente qualificados ou curingas padrão do DOS, como \* \* . Embora esse membro seja declarado como uma **cadeia** de caracteres terminada em nulo, ele é usado como um buffer para manter vários nomes de arquivo. Cada nome de arquivo deve ser encerrado pelo caractere **NULL único** normal. Um caractere **NULL** adicional deve ser anexado ao final do nome final para indicar o final de **pFrom**.

O **membro pTo** é uma cadeia **de** caracteres terminada em nulo duplo, assim como **pFrom**. O **membro pTo** contém os nomes de um ou mais nomes de destino totalmente qualificados. Eles são empacotados **em pTo** da mesma maneira que são para **pFrom**. Se **pTo** contiver vários nomes, você também deverá definir o **sinalizador FOF \_ MULTIESTFILES** no **membro fFlags.** O uso de **pTo** depende da operação, conforme descrito aqui.

-   Para operações de cópia e movimentação, se todos os arquivos estão indo para um único diretório, **pTo** contém o nome do diretório totalmente qualificado. Se os arquivos estão indo para destinos diferentes, **pTo** também pode conter um diretório totalmente qualificado ou um nome de arquivo para cada arquivo de origem. Se um diretório não existir, o sistema o criará.
-   Para operações de renomeação, **pTo** contém um caminho totalmente qualificado para cada arquivo de origem **em pFrom**.
-   Para operações de exclusão, **pTo** não é usado.

### <a name="notifying-the-shell"></a>Notificando o Shell

Notifique o Shell sobre a alteração depois de usar [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para mover, copiar, renomear ou excluir arquivos ou depois de tomar qualquer outra ação que afete o namespace. As ações que devem ser acompanhadas pela notificação incluem o seguinte:

-   Adicionar ou excluir arquivos ou pastas.
-   Movendo, copiando ou renomeando arquivos ou pastas.
-   Alterando uma associação de arquivo.
-   Alterando atributos de arquivo.
-   Adicionar ou remover unidades ou mídia de armazenamento.
-   Criar ou desabilitar uma pasta compartilhada.
-   Alterando a lista de imagens do sistema.

Um aplicativo notifica o Shell chamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) com os detalhes do que foi alterado. Em seguida, o Shell pode atualizar sua imagem do namespace para refletir com precisão seu novo estado.

## <a name="simple-example-of-managing-files-with-shfileoperation"></a>Exemplo simples de gerenciamento de arquivos com SHFileOperation

O aplicativo de console de exemplo a seguir ilustra o uso de [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) para copiar arquivos de um diretório para outro. Os diretórios de origem e destino, C: Meus Documentos e \\ \_ C: Meus Documentos2, são codificados no aplicativo \\ \_ para simplificar.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



O aplicativo primeiro recupera um ponteiro para a interface [**IShellFolder da**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) área de trabalho. Em seguida, ele recupera o PIDL do diretório de origem passando seu caminho totalmente qualificado para [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname). Observe que **IShellFolder::P arseDisplayName** requer que o caminho do diretório seja uma cadeia de caracteres Unicode. Em seguida, o aplicativo se vincula ao diretório de origem e usa sua interface **IShellFolder** para recuperar a interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) de um objeto enumerador.

Como cada arquivo no diretório de origem é enumerado, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) é usado para recuperar seu nome. O sinalizador SHGDN FORPARSING está definido, o que faz com que \_ **IShellFolder::GetDisplayNameOf** retorne o caminho totalmente qualificado do arquivo. Os caminhos de arquivo, incluindo os caracteres **NULL** de terminação, são concatenados em uma única matriz, *szSourceFiles*. Um segundo **caractere NULL** é anexado ao caminho final para encerrar a matriz corretamente.

Depois que a enumeração for concluída, o aplicativo atribuirá valores a uma estrutura [**SHFILEOPSTRUCT.**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) Observe que a matriz atribuída a **pTo** para especificar o destino também deve ser encerrada por um NULL **duplo.** Nesse caso, ele é simplesmente incluído na cadeia de caracteres atribuída a **pTo**. Como esse é um aplicativo de console, os sinalizadores \_ FOF SILENT, FOF \_ NOCONFIRMATION e FOF NOCONFIRMMKDIR são definidos para suprimir as caixas de diálogo que possam \_ aparecer. Depois [**que SHFileOperation retorna,**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) é chamado para notificar o Shell sobre a alteração. Em seguida, o aplicativo executa a limpeza normal e retorna.

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a>Adicionando arquivos à lista de documentos recentes do shell

O Shell mantém uma lista de documentos recém-adicionados ou modificados para cada usuário. O usuário pode exibir uma lista de links para esses arquivos clicando em Documentos no menu Iniciar. Assim como Meus Documentos, cada usuário tem um diretório do sistema de arquivos para manter os links reais. Para recuperar o PIDL do diretório Recente do usuário atual, seu aplicativo pode chamar [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) com CSIDL RECENT ou chamar \_ [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para recuperar seu caminho.

Seu aplicativo pode enumerar o conteúdo da pasta Recente usando as técnicas discutidas anteriormente neste documento. No entanto, um aplicativo não deve modificar o conteúdo da pasta como se fosse uma pasta normal do sistema de arquivos. Se isso acontecer, a lista de documentos recentes do Shell não será atualizada corretamente e as alterações não serão refletidas no menu Iniciar. Em vez disso, para adicionar um link de documento à pasta Recente de um usuário, seu aplicativo pode chamar [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). O Shell adicionará um link à pasta do sistema de arquivos apropriada, bem como atualizará sua lista de documentos recentes e a menu Iniciar. Você também pode usar essa função para limpar a pasta.

 

 
