---
description: O procedimento para implementar uma extensão de namespace é semelhante ao de qualquer outro objeto COM (Component Object Model) em processo.
title: Implementando as interfaces de objeto de pasta básica
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a45b8011-5355-429b-8935-4a7bdb5d2316
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05f5d2e4c21a923856c7324ad2d407230fa7595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968013"
---
# <a name="implementing-the-basic-folder-object-interfaces"></a>Implementando as interfaces de objeto de pasta básica

O procedimento para implementar uma extensão de namespace é semelhante ao de qualquer outro objeto COM (Component Object Model) em processo. Todas as extensões devem dar suporte a três interfaces primárias que fornecem ao Windows Explorer as informações básicas necessárias para exibir as pastas da extensão no modo de exibição de árvore. No entanto, para fazer uso total dos recursos do Windows Explorer, sua extensão também deve expor uma ou mais interfaces opcionais que dão suporte a recursos mais sofisticados, como menus de atalho ou arrastar e soltar, e fornecer uma exibição de pasta.

Este documento discute como implementar as interfaces primárias e opcionais que o Windows Explorer chama para obter informações sobre o conteúdo de sua extensão. Para obter uma discussão sobre como implementar uma exibição de pasta e como personalizar o Windows Explorer, consulte [implementando uma exibição de pasta](../lwef/nse-folderview.md).

-   [Implementação e registro básicos](#basic-implementation-and-registration)
    -   [Registrando uma extensão](#registering-an-extension)
-   [Manipulando PIDLs](#handling-pidls)
    -   [Criando uma estrutura SHITEMID](#creating-an-shitemid-structure)
    -   [Construindo um PIDL](#constructing-a-pidl)
    -   [Interpretando PIDLs](#interpreting-pidls)
-   [Implementando as interfaces primárias](#implementing-the-primary-interfaces)
    -   [Interface IPersistFolder](#ipersistfolder-interface)
    -   [Interface IShellFolder](#ishellfolder-interface)
    -   [Interface IEnumIDList](#ienumidlist-interface)
-   [Implementando as interfaces opcionais](#implementing-the-optional-interfaces)
    -   [IExtractIcon](#iextracticon)
    -   [IContextMenu](#icontextmenu)
    -   [IQueryInfo](#iqueryinfo)
    -   [IDataObject e IDropTarget](#idataobject-and-idroptarget)
-   [Trabalhando com a implementação de exibição de pasta do shell padrão](#working-with-the-default-shell-folder-view-implementation)

## <a name="basic-implementation-and-registration"></a>Implementação e registro básicos

Como um servidor COM em processo, sua DLL deve expor várias funções e interfaces padrão:

-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)
-   [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Essas funções e interfaces são implementadas da mesma maneira que são para a maioria dos outros objetos COM. Para obter detalhes, consulte a [documentação com](../com/the-component-object-model.md).

### <a name="registering-an-extension"></a>Registrando uma extensão

Assim como acontece com todos os objetos COM, você deve criar um GUID de identificador de classe (CLSID) para sua extensão. Registre o objeto criando uma subchave do CLSID de **\_ \_ raiz de classes hKey** \\  nomeada para o CLSID de sua extensão. A DLL deve ser registrada como um servidor em processo e deve especificar o modelo de Threading Apartment. Você pode personalizar o comportamento da pasta raiz de uma extensão adicionando uma variedade de subchaves e valores à chave CLSID da extensão.

Vários desses valores se aplicam somente a extensões com pontos de junção virtuais. Esses valores não se aplicam a extensões cujos pontos de junção são pastas do sistema de arquivos. Para obter mais informações, consulte [especificando o local de uma extensão de namespace](nse-junction.md). Para modificar o comportamento de uma extensão com um ponto de junção virtual, adicione um ou mais dos seguintes valores à chave CLSID da extensão:

-   WantsFORPARSING. O nome de análise para uma extensão com um ponto de junção virtual normalmente terá o formato: {*GUID*}. As extensões desse tipo normalmente contêm itens virtuais. No entanto, algumas extensões, como meus documentos, realmente correspondem às pastas do sistema de arquivos, embora tenham pontos de junção virtuais. Se sua extensão representar objetos do sistema de arquivos dessa forma, você poderá definir o valor de WantsFORPARSING. O Windows Explorer solicitará o nome de análise da pasta raiz chamando o método [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) do objeto de pasta com *UFlags* definido como **SHGDN \_ FORPARSING** e *PIDL* definido como um único ponteiro vazio para uma lista de identificadores de item (PIDL). Um PIDL vazio contém apenas um terminador. O método deve retornar o nome da análise da pasta raiz: {*GUID*}.
-   HideFolderVerbs. Os verbos registrados na pasta **\_ \_ raiz de classes hKey** \\  normalmente estão associados a todas as extensões. Eles aparecem no menu de atalho da extensão e podem ser invocados por [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea). Para impedir que qualquer um desses verbos seja associado à sua extensão, defina o valor HideFolderVerbs.
-   HideAsDelete. Se um usuário tentar excluir sua extensão, o Windows Explorer ocultará a extensão.
-   HideAsDeletePerUser. Esse valor tem o mesmo efeito que HideAsDelete, mas em uma base por usuário. A extensão é ocultada apenas para os usuários que tentaram excluí-la. A extensão é visível para todos os outros usuários.
-   QueryForOverlay. Defina esse valor para indicar que o ícone da pasta raiz pode ter uma sobreposição de ícone. O objeto de pasta deve dar suporte à interface [**IShellIconOverlay**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishelliconoverlay) . Antes de o Windows Explorer exibir o ícone da pasta raiz, ele solicitará um ícone de sobreposição chamando um dos dois métodos **IShellIconOverlay** com *pidlItem* definido como um PIDL vazio.

Os valores e subchaves restantes se aplicam a todas as extensões:

-   Para especificar o nome de exibição da pasta do ponto de junção da extensão, defina o valor padrão da subchave CLSID da extensão para uma cadeia de caracteres apropriada.
-   Quando o cursor passa sobre uma pasta, normalmente é exibido um InfoTip que descreve o conteúdo da pasta. Para fornecer um InfoTip para a pasta raiz da extensão, crie um valor **de \_ registro** de configuração InfoTip para a chave CLSID da extensão e defina-o como uma cadeia de caracteres apropriada.
-   Para especificar um ícone personalizado para a pasta raiz da extensão, crie uma subchave da subchave CLSID da extensão chamada **DefaultIcon**. Defina o valor padrão de **DefaultIcon** como um valor de **\_ sz reg** contendo o nome do arquivo que contém o ícone, seguido por uma vírgula, seguido por um sinal de subtração, seguido pelo índice do ícone nesse arquivo.
-   Por padrão, o menu de atalho da pasta raiz da extensão conterá os itens definidos em **HKEY \_ classes \_ raiz \\ Folder**. Os itens **excluir**, **renomear** e **Propriedades** serão adicionados se você tiver definido os sinalizadores SFGAO \_ xxx apropriados. Você pode adicionar outros itens ao menu de atalho da pasta raiz ou substituir itens existentes, da mesma forma como faria com um [tipo de arquivo](fa-file-types.md). Crie uma subchave do **shell** na chave CLSID da extensão e defina os comandos conforme discutido na [extensão de menus de atalho](context.md).
-   Se você precisar de uma maneira mais flexível para manipular o menu de atalho da pasta raiz, poderá implementar um [manipulador de menu de atalho](context-menu-handlers.md). Para registrar o manipulador de menu de atalho, crie uma chave **shellex** sob a chave CLSID da extensão. Registre o CLSID do manipulador como você faria para [criar manipuladores de extensão de shell](handlers.md)convencionais.
-   Para adicionar uma página à folha de propriedades de propriedades da pasta raiz, dê à pasta o atributo **SFGAO \_ HASPROPSHEET** e implemente um [manipulador de folha de propriedades](propsheet-handlers.md). Para registrar o manipulador de folha de propriedades, crie uma chave **shellex** na chave CLSID da extensão. Registre o CLSID do manipulador como você faria para [criar manipuladores de extensão de shell](handlers.md)convencionais.
-   Para especificar os atributos da pasta raiz, adicione uma subchave **identificação ShellFolder** à subchave CLSID da extensão. Crie um valor de atributos e defina-o como a combinação apropriada de sinalizadores [**SFGAO \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) .

A tabela a seguir lista alguns atributos comumente usados para pastas raiz.



| Sinalizador                | Valor      | Descrição                                                                                                                                                                                                                                                                                                       |
|---------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_pasta SFGAO       | 0x20000000 | A pasta raiz da extensão contém um ou mais itens.                                                                                                                                                                                                                                                           |
| SFGAO \_ HASSUBFOLDER | 0x80000000 | A pasta raiz da extensão contém uma ou mais subpastas. O Windows Explorer coloca um sinal de mais (+) ao lado do ícone de pasta.                                                                                                                                                                               |
| canSFGAO \_ CANdelete    | 0x00000020 | A pasta raiz da extensão pode ser excluída pelo usuário. O menu de atalho da pasta terá um item de **exclusão** . Esse sinalizador deve ser definido para pontos de junção que são colocados em uma das [pastas virtuais](nse-junction.md).                                                                                 |
| SFGAO \_ renomear    | 0x00000010 | A pasta raiz da extensão pode ser renomeada pelo usuário. O menu de atalho da pasta terá um item de **renomeação** .                                                                                                                                                                                                   |
| SFGAO \_ HASPROPSHEET | 0x00000040 | A pasta raiz da extensão tem uma folha de propriedades **Propriedades** . O menu de atalho da pasta terá um item de **Propriedades** . Para fornecer a folha de propriedades, você deve implementar um [manipulador de folha de propriedades](propsheet-handlers.md). Registre o manipulador sob a chave CLSID da extensão, conforme discutido anteriormente. |



 

O exemplo a seguir mostra a entrada de Registro CLSID para uma extensão com um nome de exibição de MyExtension. A extensão tem um ícone personalizado que está contido na DLL da extensão com um índice de 1. Os atributos **SFGAO \_ Folder**, **SFGAO \_ HASSUBFOLDER** e **SFGAO \_ CanDelete** são definidos.

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         (Default) = MyExtension
         InfoTip = Some appropriate text
      DefaultIcon
         (Default) = c:\MyDir\MyExtension.dll,-1
      InProcServer32
         (Default) = c:\MyDir\MyExtension.dll
         ThreadingModel = Apartment
      ShellFolder
         Attributes = 0xA00000020
```

## <a name="handling-pidls"></a>Manipulando PIDLs

Cada item no namespace do Shell deve ter um PIDL exclusivo. O Windows Explorer atribui um PIDL à sua pasta raiz e passa o valor para sua extensão durante a inicialização. Em seguida, sua extensão é responsável por atribuir um PIDL construído corretamente a cada um de seus objetos e fornecer esses PIDLs ao Windows Explorer na solicitação. Quando o Shell usa um PIDL para identificar um dos objetos da extensão, sua extensão deve ser capaz de interpretar o PIDL e identificar o objeto específico. Sua extensão também deve atribuir um [**nome de exibição**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof) e um *nome de análise* a cada objeto. Como PIDLs são usados por praticamente cada interface de pasta, as extensões normalmente implementam um único *Gerenciador de PIDL* para lidar com todas essas tarefas.

O termo PIDL é curto para uma estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) ou um ponteiro para tal estrutura, dependendo do contexto. Como declarado, uma estrutura **ITEMIDLIST** tem um único membro, uma estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . A estrutura **ITEMIDLIST** de um objeto é, na verdade, uma matriz empacotada de duas ou mais estruturas **SHITEMID** . A ordem dessas estruturas define um caminho por meio do namespace, praticamente da mesma forma que c: \\ mydirectory \\ MyFile define um caminho por meio do sistema de arquivos. Normalmente, o PIDL de um objeto consistirá em uma série de estruturas **SHITEMID** que correspondem às pastas que definem o caminho do namespace, seguido pela estrutura **SHITEMID** do objeto, seguida por um terminador.

O terminador é uma estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , com o membro *CB* definido como **nulo**. O terminador é necessário porque o número de estruturas **SHITEMID** no PIDL de um objeto depende do local do objeto no namespace do Shell e do ponto de partida do caminho. Além disso, o tamanho das várias estruturas **SHITEMID** pode variar. Ao receber um PIDL, você não tem uma maneira simples de determinar seu tamanho ou até mesmo o número total de estruturas **SHITEMID** . Em vez disso, você deve "percorrer" a matriz empacotada, estrutura por estrutura, até chegar ao terminador.

Para criar um PIDL, seu aplicativo precisa:

1.  Crie uma estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) para cada um de seus objetos.
2.  Monte as estruturas [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) relevantes em um PIDL.

### <a name="creating-an-shitemid-structure"></a>Criando uma estrutura SHITEMID

A estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) de um objeto identifica exclusivamente o objeto dentro de sua pasta. Na verdade, um tipo de PIDL usado por muitos dos métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) consiste apenas na estrutura **SHITEMID** do objeto, seguido por um terminador. A definição de uma estrutura **SHITEMID** é:


```C++
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



O membro *abID* é o identificador do objeto. Como o comprimento de *abID* não está definido e pode variar, o membro *CB* é definido como o tamanho da estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , em bytes.

Como nem o comprimento nem o conteúdo de *abID* é padronizado, você pode usar qualquer esquema ao qual deseja atribuir valores de *abID* aos seus objetos. O único requisito é que você não possa ter dois objetos na mesma pasta com valores idênticos. No entanto, por motivos de desempenho, sua estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) deve ser alinhada em **DWORD**. Em outras palavras, você deve construir seus valores de *abID* de forma que *CB* seja um múltiplo integral de 4.

Normalmente, *abID* aponta para uma estrutura definida por extensão. Além da ID do objeto, essa estrutura costuma ser usada para manter uma variedade de informações relacionadas, como o tipo ou os atributos do objeto. Os objetos de pasta da extensão podem, então, extrair rapidamente as informações do PIDL em vez de ter que consultá-las.

> [!Note]  
> Um dos aspectos mais importantes da criação de uma estrutura de dados para um PIDL é tornar a estrutura persistente e transportável. No contexto de PIDLs, o significado desses termos é:
>
> -   Persistente. O sistema geralmente coloca PIDLs em vários tipos de armazenamento de longo prazo, como arquivos de atalho. Em seguida, ele pode recuperar esses PIDLs do armazenamento mais tarde, possivelmente após a reinicialização do sistema. Um PIDL que foi recuperado do armazenamento ainda deve ser válido e significativo para sua extensão. Esse requisito significa, por exemplo, que você não deve usar ponteiros ou identificadores em sua estrutura PIDL. O PIDLs que contém esse tipo de dados normalmente não fará sentido quando o sistema os recuperar posteriormente do armazenamento.
> -   Transportáveis. Um PIDL deve permanecer significativo quando transportado de um computador para outro. Por exemplo, um PIDL pode ser gravado em um arquivo de atalho, copiado para um disquete e transportado para outro computador. Esse PIDL ainda deve ser significativo para a extensão em execução no segundo computador. Por exemplo, para garantir que seus PIDLs sejam transportáveis, use caracteres ANSI ou Unicode explicitamente. Evite tipos de dados como **TCHAR** ou **LPTSTR**. Se você usar esses tipos de dados, um PIDL criado em um computador que executa uma versão Unicode de sua extensão não poderá ser lido por uma versão ANSI dessa extensão em execução em um computador diferente.

 

A declaração a seguir mostra um exemplo simples de uma estrutura de dados.


```C++
typedef struct tagMYPIDLDATA {
  USHORT cb;
  DWORD dwType;
  WCHAR wszDisplayName[40];
} MYPIDLDATA, *LPMYPIDLDATA;
```



O membro **CB** é definido como o tamanho da estrutura **MYPIDLDATA** . Esse membro faz **MYPIDLDATA** uma estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) válida, por si só. O restante dos membros são equivalentes ao membro **abID** de uma estrutura **SHITEMID** e contêm dados privados. O membro **dwType** é um valor definido pela extensão que indica o tipo de objeto. Para este exemplo, **dwType** é definido como **true** para pastas e **false** caso contrário. Esse membro permite, por exemplo, determinar rapidamente se o objeto é uma pasta ou não. O membro **wszDisplayName** contém o nome de exibição do objeto. Como você não atribuiria o mesmo nome de exibição a dois objetos diferentes na mesma pasta, o nome de exibição também serve como a ID de objeto. Neste exemplo, **wszDisplayName** é definido como 40 caracteres para garantir que a estrutura **SHITEMID** será alinhada em **DWORD**. Para limitar o tamanho de seu PIDLs, você pode usar uma matriz de caracteres de comprimento variável e ajustar o valor de CB de acordo. Preencha a cadeia de exibição com \\ caracteres ' 0 ' suficientes para manter o alinhamento de **DWORD** da estrutura. Outros membros que podem ser úteis para colocar na estrutura incluem o tamanho do objeto, os atributos ou o nome de análise.

### <a name="constructing-a-pidl"></a>Construindo um PIDL

Depois de definir as estruturas [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) para seus objetos, você poderá usá-las para construir um PIDL. O PIDLs pode ser construído para uma variedade de finalidades, mas a maioria das tarefas usa um dos dois tipos de PIDL. O mais simples, um PIDL de nível único, identifica o objeto relativo à sua pasta pai. Esse tipo de PIDL é usado por muitos dos métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Um PIDL de nível único contém a estrutura **SHITEMID** do objeto, seguida por um terminador. Um PIDL totalmente qualificado define um caminho por meio da hierarquia de namespace da área de trabalho para o objeto. Esse tipo de PIDL é iniciado na área de trabalho e contém uma estrutura **SHITEMID** para cada pasta no caminho, seguido pelo objeto e o terminador. Um PIDL totalmente qualificado identifica exclusivamente o objeto dentro de todo o namespace do Shell.

A maneira mais simples de construir um PIDL é trabalhar diretamente com a própria estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Crie uma estrutura de **ITEMIDLIST** , mas aloque memória suficiente para manter todas as estruturas [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . O endereço dessa estrutura apontará para a estrutura **SHITEMID** inicial. Defina valores para os membros dessa estrutura inicial e, em seguida, acrescente quantas estruturas **SHITEMID** adicionais forem necessárias, na ordem apropriada. O procedimento a seguir descreve como criar um PIDL de nível único. Ele contém duas estruturas **SHITEMID** , uma estrutura **MYPIDLDATA** seguida por um terminador:

1.  Use a função [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar memória para o PIDL. Aloque memória suficiente para seus dados particulares mais um **UShort** (dois bytes) para o terminador. Converta o resultado em LPMYPIDLDATA.
2.  Defina o membro CB da primeira estrutura **MYPIDLDATA** para o tamanho dessa estrutura. Para este exemplo, você definirá **CB** como sizeof (MYPIDLDATA). Se você quiser usar uma estrutura de comprimento variável, precisará calcular o valor de **CB**.
3.  Atribua valores apropriados aos membros de dados privados.
4.  Calcule o endereço da próxima estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . Converta o endereço da estrutura MYPIDLDATA atual em LPBYTE e adicione esse valor ao valor de **CB** determinado na etapa 3.
5.  Nesse caso, a próxima estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) é o terminador. Defina o membro **CB** da estrutura como zero.

Para obter mais PIDLs, aloque memória suficiente e repita as etapas de 3-5 para cada estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) adicional.

A função de exemplo a seguir usa o tipo de um objeto e o nome de exibição e retorna o PIDL de nível único do objeto. A função pressupõe que o nome de exibição, incluindo seu caractere **nulo** de terminação, não exceda o número de caracteres declarados para a estrutura **MYPIDLDATA** . Se essa suposição se tornar incorreta, a função [**StringCbCopyW**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) truncará o nome de exibição. A variável **g \_ pMalloc** é um ponteiro [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) criado em outro lugar e armazenado em uma variável global.


```C++
LPITEMIDLIST CreatePIDL(DWORD dwType, LPCWSTR pwszDisplayName)
{
    LPMYPIDLDATA   pidlOut;
    USHORT         uSize;

    pidlOut = NULL;

    //Calculate the size of the MYPIDLDATA structure.
    uSize = sizeof(MYPIDLDATA);

    // Allocate enough memory for the PIDL to hold a MYPIDLDATA structure 
    // plus the terminator
    pidlOut = (LPMYPIDLDATA)m_pMalloc->Alloc(uSize + sizeof(USHORT));

    if(pidlOut)
    {
       //Assign values to the members of the MYPIDLDATA structure
       //that is the PIDL's first SHITEMID structure
       pidlOut->cb = uSize;
       pidlOut->dwType = dwType;
       hr = StringCbCopyW(pidlOut->wszDisplayName, 
                          sizeof(pidlOut->wszDisplayName), pwszDisplayName);
       
       // TODO: Add error handling here to verify the HRESULT returned 
       // by StringCbCopyW.

       //Advance the pointer to the start of the next SHITEMID structure.
       pidlOut = (LPMYPIDLDATA)((LPBYTE)pidlOut + pidlOut->cb);

       //Create the terminating null character by setting cb to 0.
       pidlOut->cb = 0;
    }

    return pidlOut;
```



Um PIDL totalmente qualificado deve ter estruturas [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) para cada objeto da área de trabalho para seu objeto. Sua extensão recebe um PIDL totalmente qualificado para sua pasta raiz quando o Shell chama [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize). Para construir um PIDL totalmente qualificado para um objeto, pegue o PIDL que o Shell atribuiu à sua pasta raiz e acrescente as estruturas **SHITEMID** necessárias para levá-lo da pasta raiz para o objeto.

### <a name="interpreting-pidls"></a>Interpretando PIDLs

Quando o Shell ou um aplicativo chama uma das interfaces da extensão para solicitar informações sobre um objeto, ele geralmente identifica o objeto por um PIDL. Alguns métodos, como [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), usam PIDLs que são relativos à pasta pai e são simples de interpretar. No entanto, sua extensão provavelmente também receberá PIDLs totalmente qualificado. O Gerenciador de PIDL deve determinar a quais dos seus objetos o PIDL está se referindo.

O que complica a tarefa de associar um objeto a um PIDL totalmente qualificado é que uma ou mais das estruturas [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) iniciais no PIDL podem pertencer a objetos que ficam fora de sua extensão no namespace do Shell. Você não tem como interpretar o significado do membro *abID* dessas estruturas. O que sua extensão deve fazer é "percorrer" a lista de estruturas **SHITEMID** até chegar à estrutura que corresponde à sua pasta raiz. A partir de então, você saberá como interpretar as informações nas estruturas **SHITEMID** .

Para percorrer o PIDL, pegue o primeiro valor *CB* e adicione-o ao endereço do PIDL para avançar o ponteiro até o início da próxima estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . Em seguida, ele apontará para o membro *CB* da estrutura, que pode ser usado para avançar o ponteiro até o início da próxima estrutura **SHITEMID** e assim por diante. Cada vez que você avançar o ponteiro, examine a estrutura **SHITEMID** para determinar se você atingiu a raiz do namespace da extensão.

## <a name="implementing-the-primary-interfaces"></a>Implementando as interfaces primárias

Assim como acontece com todos os objetos COM, a implementação de uma extensão é basicamente uma questão de implementar uma coleção de interfaces. Esta seção aborda as três interfaces primárias que devem ser implementadas por todas as extensões. Eles são usados para inicialização e fornecem ao Windows Explorer informações básicas sobre o conteúdo da extensão. Essas interfaces, além de uma [exibição de pasta](../lwef/nse-folderview.md), são todas necessárias para uma extensão funcional. No entanto, para explorar totalmente os recursos do Windows Explorer, a maioria das extensões também implementa uma ou mais das interfaces opcionais.

### <a name="ipersistfolder-interface"></a>Interface IPersistFolder

A interface [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) é chamada para inicializar um novo objeto de pasta. O método [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) atribui um PIDL totalmente qualificado ao novo objeto. Armazene esse PIDL para uso posterior. Por exemplo, um objeto de pasta deve usar esse PIDL para construir PIDLs totalmente qualificado para os filhos do objeto. O criador do objeto de pasta também pode chamar [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) para solicitar o CLSID do objeto.

Normalmente, um objeto de pasta é criado e inicializado pelo método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) da pasta pai. No entanto, quando um usuário navega em sua extensão, o Windows Explorer cria e inicializa o objeto da pasta raiz da extensão. O PIDL que o objeto de pasta raiz recebe por meio de [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) contém o caminho da área de trabalho para a pasta raiz que você precisará para construir PIDLs totalmente qualificado para sua extensão.

### <a name="ishellfolder-interface"></a>Interface IShellFolder

O Shell trata uma extensão como uma coleção de objetos de pasta ordenada hierarquicamente. A interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) é o núcleo de qualquer implementação de extensão. Ele representa um objeto de pasta e fornece ao Windows Explorer muitas das informações necessárias para exibir o conteúdo da pasta.

[**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) normalmente é a única interface de pasta diferente de [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) que é diretamente exposta por um objeto Folder. Embora o Windows Explorer use uma variedade de interfaces obrigatórias e opcionais para obter informações sobre o conteúdo da pasta, ele obtém ponteiros para essas interfaces por meio do **IShellFolder**.

O Windows Explorer Obtém o CLSID da pasta raiz da extensão de várias maneiras. Para obter detalhes, consulte [especificando um local de extensão de namespace](nse-junction.md) ou [exibindo um Self-Contained exibição de uma extensão de namespace](nse-view.md). Em seguida, o Windows Explorer usa esse CLSID para criar e inicializar uma instância da pasta raiz e consultar uma interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Sua extensão cria um objeto de pasta para representar a pasta raiz e retorna a interface **IShellFolder** do objeto. A maior parte do restante da interação entre a extensão e o Windows Explorer ocorre por meio de **IShellFolder**. O Windows Explorer chama **IShellFolder** para:

-   Solicite um objeto que possa enumerar o conteúdo da pasta raiz.
-   Obtenha vários tipos de informações sobre o conteúdo da pasta raiz.
-   Solicite um objeto que expõe uma das interfaces opcionais. Essas interfaces podem, então, ser consultadas para obter informações adicionais, como ícones ou menus de atalho.
-   Solicite um objeto Folder que represente uma subpasta da pasta raiz.

Quando um usuário abre uma subpasta da pasta raiz, o Windows Explorer chama [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject). Sua extensão cria e inicializa um novo objeto de pasta para representar a subpasta e retorna sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Em seguida, o Windows Explorer chama essa interface para vários tipos de informações e assim por diante até que o usuário decida navegar em outro lugar no namespace do Shell ou fechar o Windows Explorer.

O restante desta seção aborda brevemente os métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) mais importantes e como implementá-los.

### <a name="enumobjects"></a>EnumObjects

Antes de exibir o conteúdo de uma pasta no modo de exibição de árvore, o Windows Explorer deve primeiro determinar o que a pasta contém chamando o método [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) . Esse método cria um objeto de enumeração OLE padrão que expõe uma interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) e retorna esse ponteiro de interface. A interface **IEnumIDList** permite que o Windows Explorer obtenha o PIDLs de todos os objetos contidos na pasta. Esses PIDLs são usados para obter informações sobre os objetos contidos na pasta. Para obter mais detalhes, consulte [interface IEnumIDList](#ienumidlist-interface).

> [!Note]  
> O método [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) deve retornar apenas PIDLs que são relativos à pasta pai. O PIDL deve conter apenas a estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) do objeto, seguido por um terminador.

 

### <a name="createviewobject"></a>CreateViewObject

Antes que o conteúdo de uma pasta seja exibido, o Windows Explorer chama esse método para solicitar um ponteiro para uma interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Essa interface é usada pelo Windows Explorer para gerenciar a exibição de pasta. Crie um objeto de exibição de pasta e retorne sua interface **IShellView** .

O método [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) também é chamado para solicitar uma das interfaces opcionais, como [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), para a própria pasta. A implementação desse método deve criar um objeto que expõe a interface solicitada e retorna o ponteiro de interface. Se o Windows Explorer precisar de uma interface opcional para um dos objetos contidos na pasta, ele chamará [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof).

### <a name="getuiobjectof"></a>GetUIObjectOf

Embora as informações básicas sobre o conteúdo de uma pasta estejam disponíveis por meio dos métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) , sua extensão também pode fornecer ao Windows Explorer vários tipos de informações adicionais. Por exemplo, você pode especificar ícones para o conteúdo de uma pasta ou menu de atalho de um objeto. O Windows Explorer chama o método [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) para tentar recuperar informações adicionais sobre um objeto contido em uma pasta. O Windows Explorer especifica para qual objeto ele deseja as informações e o IID da interface relevante. Em seguida, o objeto Folder cria um objeto que expõe a interface solicitada e retorna o ponteiro da interface.

Se sua extensão permitir que os usuários transfiram objetos com o recurso de arrastar e soltar ou a área de transferência, o Windows Explorer chamará [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) para solicitar uma interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ou [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Para obter detalhes, consulte [transferindo objetos do shell com o recurso de arrastar e soltar e a área de transferência](dragdrop.md).

O Windows Explorer chama [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) quando deseja o mesmo tipo de informação sobre a própria pasta.

### <a name="bindtoobject"></a>BindToObject

O Windows Explorer chama o método [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) quando um usuário tenta abrir uma das subpastas da extensão. Se *riid* estiver definido como IID \_ IShellFolder, você deverá criar e inicializar um objeto Folder que representa a subpasta e retornar a interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) do objeto.

> [!Note]  
> No momento, o Windows Explorer chama esse método somente para solicitar uma interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . No entanto, não assuma que esse será sempre o caso. Você sempre deve verificar o valor de *riid* antes de continuar.

 

### <a name="getdisplaynameof"></a>GetDisplayNameOf

O Windows Explorer chama o método [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para converter o PIDL de um dos objetos da pasta em um nome. Esse PIDL deve ser relativo à pasta pai do objeto. Em outras palavras, ele deve conter uma única estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) não **nula** . Como há mais de uma possível maneira de nomear objetos, o Windows Explorer especifica o tipo de nome definindo um ou mais sinalizadores [**SHGDNF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf) no parâmetro *uFlags* . Um dos dois valores, **SHGDN \_ normal** ou **SHGDN \_**, será definido para especificar se o nome deve ser relativo à pasta ou em relação à área de trabalho. Um dos outros três valores, **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** ou **SHGDN \_ FORPARSING**, pode ser definido para especificar para que o nome será usado.

Você deve retornar o nome na forma de uma estrutura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Se **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** e **SHGDN \_ FORPARSING** não estiverem definidos, retornará o nome de exibição do objeto. Se o sinalizador **SHGDN \_ FORPARSING** for definido, o Windows Explorer está solicitando um nome de análise. Os nomes de análise são passados para [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) para obter o PIDL de um objeto, embora ele possa estar localizado um ou mais níveis abaixo da pasta atual na hierarquia de namespace. Por exemplo, o nome de análise de um objeto do sistema de arquivos é seu caminho. Você pode passar o caminho totalmente qualificado de qualquer objeto no sistema de arquivos para o método IShellFolder da área de trabalho **::P arsedisplayname** , e retornará o PIDL totalmente qualificado do objeto.

Embora os nomes de análise sejam cadeias de caracteres de texto, eles não precisam necessariamente incluir o nome de exibição. Você deve atribuir nomes de análise com base no que funcionará mais eficientemente quando [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) for chamado. Por exemplo, muitas das pastas virtuais do shell não fazem parte do sistema de arquivos e não têm um caminho totalmente qualificado. Em vez disso, cada pasta recebe um GUID e o nome de análise tem o formato: {GUID}. Independentemente de qual esquema você usar, ele deve ser capaz de "viagem de ida e volta confiável". Por exemplo, se um chamador passar um nome de análise para **IShellFolder::P arsedisplayname** para recuperar o PIDL de um objeto e, em seguida, passar esse PIDL para [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) **com o sinalizador SHGDN FORPARSING \_** definido, o chamador deverá recuperar o nome de análise original.

### <a name="getattributesof"></a>GetAttributesOf

O Windows Explorer chama o método [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) para determinar os atributos de um ou mais itens contidos em um objeto Folder. O valor de *cidl* fornece o número de itens na consulta e *aPidl* aponta para uma lista de seus PIDLs.

Como os testes de alguns atributos podem ser demorados, o Windows Explorer normalmente restringe a consulta a um subconjunto dos sinalizadores disponíveis definindo seus valores em *rfgInOut*. Seu método deve testar somente os atributos cujos sinalizadores são definidos em *rfgInOut*. Deixe os sinalizadores válidos definidos e desmarque o restante. Se mais de um item for incluído na consulta, defina somente os sinalizadores que se aplicam a todos os itens.

> [!Note]  
> Os atributos devem ser definidos corretamente para que um item seja exibido corretamente. Por exemplo, se um item for uma pasta que contém subpastas, você deverá definir o sinalizador **SFGAO \_ HASSUBFOLDER** . Caso contrário, o Windows Explorer não exibirá um + próximo ao ícone do item no modo de exibição de árvore.

 

### <a name="parsedisplayname"></a>ParseDisplayName

O método [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) é, de certa forma, uma imagem espelho de [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). O uso mais comum desse método é converter o nome de análise de um objeto no PIDL associado. O nome de análise pode se referir a qualquer objeto que esteja abaixo da pasta na hierarquia de namespace. O PIDL retornado é relativo ao objeto Folder que expõe o método e geralmente não é totalmente qualificado. Em outras palavras, embora o PIDL possa conter várias estruturas [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , a primeira será a do próprio objeto ou a primeira subpasta no caminho da pasta para o objeto. O chamador terá que acrescentar esse PIDL ao PIDL totalmente qualificado da pasta para obter um PIDL totalmente qualificado para o objeto.

[**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) também pode ser chamado para solicitar os atributos de um objeto. Como a determinação de todos os atributos aplicáveis pode ser demorada, o chamador definirá apenas os sinalizadores [**SFGAO \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) que representam as informações que o chamador está interessado. Você deve determinar quais desses atributos são verdadeiros para o objeto e desmarcar os sinalizadores restantes.

### <a name="ienumidlist-interface"></a>Interface IEnumIDList

Quando o Windows Explorer precisa enumerar os objetos que estão contidos em uma pasta, ele chama [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects). O objeto Folder deve criar um objeto de enumeração que expõe a interface [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) e retornar esse ponteiro de interface. O Windows Explorer normalmente usará **IEnumIDList** para enumerar o PIDLs de todos os objetos contidos na pasta.

[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) é uma interface de enumeração OLE padrão e é implementada da maneira usual. Lembre-se, no entanto, de que o PIDLs retornado deve ser relativo à pasta e conter apenas a estrutura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) do objeto e um terminador.

## <a name="implementing-the-optional-interfaces"></a>Implementando as interfaces opcionais

Há várias interfaces de shell opcionais às quais os objetos de pasta da extensão podem dar suporte. Muitos deles, como o [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona), permitem que você personalize vários aspectos da maneira como o usuário exibe sua extensão. Outros, como [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), permitem que sua extensão dê suporte a recursos como arrastar e soltar.

Nenhuma das interfaces opcionais é exposta diretamente por um objeto Folder. Em vez disso, o Windows Explorer chama um dos dois métodos [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) para solicitar uma interface:

-   O Windows Explorer chama o [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) de um objeto de pasta para solicitar uma interface para um dos objetos contidos na pasta.
-   O Windows Explorer chama o [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) de um objeto de pasta para solicitar uma interface para a própria pasta.

Para fornecer as informações, o objeto Folder cria um objeto que expõe a interface solicitada e retorna o ponteiro da interface. Em seguida, o Windows Explorer chama essa interface para recuperar as informações necessárias. Esta seção aborda as interfaces opcionais usadas com mais frequência.

### <a name="iextracticon"></a>IExtractIcon

O Windows Explorer solicita uma interface [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) antes de exibir o conteúdo de uma pasta. A interface permite que sua extensão especifique ícones personalizados para os objetos contidos na pasta. Caso contrário, os ícones padrão de arquivo e pasta serão usados. Para fornecer um ícone personalizado, crie um objeto de extração de ícone que expõe **IExtractIcon** e retorne um ponteiro para essa interface. Para mais discussões, consulte a documentação de referência do **IExtractIcon** ou [criando manipuladores de ícones](./how-to-create-icon-handlers.md).

### <a name="icontextmenu"></a>IContextMenu

Quando um usuário clica com o botão direito do mouse em um objeto, o Windows Explorer solicita uma interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Para fornecer menus de atalho para seus objetos, crie um objeto de manipulador de menu e retorne sua interface **IContextMenu** .

Os procedimentos para criar um objeto de manipulador de menu são muito semelhantes aos usados para criar uma extensão de Shell de manipulador de menu. Para obter detalhes, consulte [criando manipuladores de menu de contexto](context-menu-handlers.md) ou a referência de [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)ou [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) .

### <a name="iqueryinfo"></a>IQueryInfo

O Windows Explorer chama a interface [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) para recuperar uma cadeia de caracteres de texto InfoTip.

### <a name="idataobject-and-idroptarget"></a>IDataObject e IDropTarget

Quando os objetos são exibidos pelo Windows Explorer, um objeto de pasta não tem uma maneira direta de saber quando um usuário está tentando recortar, copiar ou arrastar um objeto. Em vez disso, o Windows Explorer solicita uma interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Para permitir que o objeto seja transferido, crie um objeto de dados e retorne um ponteiro para a interface **IDataObject** .

Da mesma forma, um usuário pode tentar remover um objeto de dados em uma representação do Windows Explorer de um de seus objetos, como um ícone ou caminho da barra de endereços. Em seguida, o Windows Explorer solicita uma interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Para permitir que o objeto de dados seja removido, crie um objeto que expõe uma interface **IDropTarget** e retorne o ponteiro de interface.

A manipulação de transferência de dados é um dos aspectos mais complicados da gravação de extensões de namespace. Para obter uma discussão detalhada, consulte [transferindo objetos do shell com o recurso de arrastar e soltar e a área de transferência](dragdrop.md).

## <a name="working-with-the-default-shell-folder-view-implementation"></a>Trabalhando com a implementação de exibição de pasta do shell padrão

As fontes de dados que usam o objeto de exibição de pasta do shell padrão (DefView) devem implementar essas interfaces:

-   [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)
-   [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)
-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)
-   [**IPersistFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)

Opcionalmente, eles também podem implementar [**IPersistFolder3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3).

 

 
