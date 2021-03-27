---
description: Os recursos do Shell podem ser estendidos com entradas de registro e arquivos. ini.
ms.assetid: 74a81e4f-7357-4901-a118-ba44e8892f25
title: Criar Manipuladores de Extensão de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f3c1684b7491e2ad29fae29f48164ffdd47cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988988"
---
# <a name="creating-shell-extension-handlers"></a>Criar Manipuladores de Extensão de Shell

Os recursos do Shell podem ser estendidos com entradas de registro e arquivos. ini. Embora essa abordagem para estender o shell seja simples e adequada para muitas finalidades, ela é limitada. Por exemplo, se você usar o registro para especificar um ícone personalizado para um tipo de arquivo, o mesmo ícone será exibido para cada arquivo desse tipo. Estender o shell com o registro não permite que você varie o ícone para arquivos diferentes do mesmo tipo. Outros aspectos do Shell, como a folha de propriedades **Propriedades** que podem ser exibidas quando um arquivo é clicado com o botão direito do mouse, não podem ser modificados com o registro.

Uma abordagem mais poderosa e flexível para estender o Shell é implementar *manipuladores de extensão de shell*. Esses manipuladores podem ser implementados para uma variedade de ações que o Shell pode executar. Antes de executar a ação, o Shell consulta o manipulador de extensão, dando a ele a oportunidade de modificar a ação. Um exemplo comum é um manipulador de extensão de menu de atalho. Se um for implementado para um tipo de arquivo, ele será consultado toda vez que um dos arquivos for clicado com o botão direito do mouse. O manipulador pode, então, especificar itens de menu adicionais de acordo com o arquivo, em vez de ter o mesmo conjunto para todo o tipo de arquivo.

Este documento discute como implementar os manipuladores de extensão que permitem modificar uma variedade de ações de Shell. Os seguintes manipuladores estão associados a um tipo de arquivo específico e permitem que você especifique em uma base arquivo por arquivo:



| Manipulador                                               | Descrição                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manipulador de menu de atalho](context-menu-handlers.md)    | Chamado antes de o menu de atalho de um arquivo ser exibido. Ele permite que você adicione itens ao menu de atalho de acordo com o arquivo.                                               |
| [Manipulador de dados](how-to-create-data-handlers.md)       | Chamado quando uma operação de arrastar e soltar é executada em objetos dragShell. Ele permite que você forneça formatos de área de transferência adicionais para o destino de soltar.                        |
| [Descartar manipulador](how-to-create-drop-handlers.md)       | Chamado quando um objeto de dados é arrastado ou solto em um arquivo. Ele permite que você faça um arquivo em um destino de soltura.                                                          |
| [Manipulador de ícone](how-to-create-icon-handlers.md)       | Chamado antes do ícone de um arquivo ser exibido. Ele permite que você substitua o ícone padrão do arquivo por um ícone personalizado em cada arquivo.                                    |
| [Manipulador de folha de propriedades](propsheet-handlers.md)      | Chamado antes da exibição da folha de propriedades de **Propriedades** de um objeto. Ele permite que você adicione ou substitua páginas.                                                              |
| [**Manipulador de imagem em miniatura**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fornece uma imagem para representar o item.                                                                                                                                   |
| [**Manipulador de infodicas**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fornece texto pop-up quando o usuário passa o ponteiro do mouse sobre o objeto.                                                                                               |
| [**Manipulador de metadados**](/windows/win32/api/propsys/nn-propsys-ipropertystore)     | Fornece acesso de leitura e gravação a metadados (Propriedades) armazenados em um arquivo. Isso pode ser usado para estender a exibição de detalhes, infotips, a página de propriedades e agrupar recursos. |



 

Outros manipuladores não estão associados a um tipo de arquivo específico, mas são chamados antes de algumas operações de Shell:



| Manipulador                                                            | Descrição                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Manipulador de coluna](../lwef/column-handlers.md)                             | Chamado pelo Windows Explorer antes de exibir a exibição de detalhes de uma pasta. Ele permite que você adicione colunas personalizadas à exibição de detalhes.        |
| [Copiar manipulador de gancho](how-to-create-copy-hook-handlers.md)          | Chamado quando um objeto de pasta ou de impressora está prestes a ser movido, copiado, excluído ou renomeado. Ele permite que você aprove ou veta a operação.   |
| [Manipulador do tipo "arrastar e soltar"](context-menu-handlers.md)                 | Chamado quando um arquivo é arrastado com o botão direito do mouse. Ele permite que você modifique o menu de atalho que é exibido.                     |
| [Manipulador de sobreposição de ícone](how-to-implement-icon-overlay-handlers.md) | Chamado antes do ícone de um arquivo ser exibido. Ele permite que você especifique uma sobreposição para o ícone do arquivo.                                          |
| [Manipulador de pesquisa](../lwef/search-handlers.md)                             | Chamado para iniciar um mecanismo de pesquisa. Ele permite que você implemente um mecanismo de pesquisa personalizado acessível no menu **Iniciar** ou no Windows Explorer. |



 

Os detalhes de como implementar manipuladores de extensão específicos são abordados nas seções listadas acima. O restante deste documento aborda alguns problemas de implementação que são comuns a todos os manipuladores de extensão do Shell.

-   [Implementando manipuladores de extensão de Shell](#implementing-shell-extension-handlers)
    -   [Implementando IPersistFile](#implementing-ipersistfile)
    -   [Implementando IShellExtInit](#implementing-ishellextinit)
    -   [Personalização de InfoTip](#infotip-customization)
-   [Aprimorando o Windows Search com manipuladores de extensão de Shell](#enhancing-windows-search-with-shell-extension-handlers)
-   [Registrando manipuladores de extensão do Shell](#registering-shell-extension-handlers)
    -   [Nomes de manipuladores](#handler-names)
    -   [Objetos de shell predefinidos](#predefined-shell-objects)
    -   [Exemplo de um registro de manipulador de extensão](#example-of-an-extension-handler-registration)
-   [Tópicos relacionados](#related-topics)

## <a name="implementing-shell-extension-handlers"></a>Implementando manipuladores de extensão de Shell

Grande parte da implementação de um objeto de manipulador de extensão de shell depende de seu tipo. No entanto, há alguns elementos comuns. Esta seção aborda esses aspectos da implementação que são compartilhados por todos os manipuladores de extensão do Shell.

Muitos manipuladores de extensão de shell são objetos COM (Component Object Model) em processo. Eles devem ser atribuídos a um GUID e registrados conforme descrito em Registrando manipuladores de extensão do Shell. Eles são implementados como DLLs e devem exportar as seguintes funções padrão:

-   [**DllMain**](../dlls/dllmain.md). O ponto de entrada padrão para a DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expõe a fábrica de classes do objeto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM chama essa função para determinar se o objeto está atendendo a clientes. Caso contrário, o sistema pode descarregar a DLL e liberar a memória associada.

Como todos os objetos COM, os manipuladores de extensão do Shell devem implementar uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e uma [fábrica de classes](../com/implementing-iclassfactory.md). A maioria dos manipuladores de extensão também deve implementar uma interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) no Windows XP ou anterior. Elas foram substituídas por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) no Windows Vista. O Shell usa essas interfaces para inicializar o manipulador.

A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve ser implementada pelo seguinte:

-   Manipuladores de dados
-   Descartar manipuladores

No passado, os manipuladores de ícones também eram obrigados a implementar [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), mas isso não é mais verdade. Para manipuladores de ícones, **IPersistFile** agora é opcional e outras interfaces, como [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) , são preferenciais.

A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve ser implementada pelo seguinte:

-   Manipuladores de menu de atalho
-   Manipuladores de arrastar e soltar
-   Manipuladores de folha de propriedades

### <a name="implementing-ipersistfile"></a>Implementando IPersistFile

A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) destina-se a permitir que um objeto seja carregado ou salvo em um arquivo de disco. Ele tem seis métodos além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinco de sua própria e o método [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que ele herda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Com extensões de Shell, **IPersist** é usado apenas para inicializar um objeto de manipulador de extensão de Shell. Como normalmente não há necessidade de ler ou gravar no disco, somente os métodos **GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) exigem uma implementação sem token.

O Shell chama [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) primeiro e a função retorna o identificador de classe (CLSID) do objeto do manipulador de extensão. Em seguida, o Shell chama [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa em dois valores. O primeiro, *pszFileName*, é uma cadeia de caracteres Unicode com o nome do arquivo ou da pasta em que o Shell está prestes a operar. O segundo é *dwMode*, que indica o modo de acesso do arquivo. Como normalmente não há necessidade de acessar arquivos, o *dwMode* geralmente é zero. O método armazena esses valores conforme necessário para referência posterior.

O fragmento de código a seguir ilustra como um manipulador de extensão de shell típico implementa os métodos [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . Ele foi projetado para lidar com ANSI ou Unicode. CLSID \_ SampleExtHandler é o GUID do objeto do manipulador de extensão e CSampleExtHandler é o nome da classe usada para implementar a interface. As variáveis **m \_ szFileName** e **m \_ dwMode** são variáveis privadas que são usadas para armazenar o nome do arquivo e os sinalizadores de acesso.


```C++
wchar_t m_szFileName[MAX_PATH];    // The file name
DWORD m_dwMode;                  // The file access mode

CSampleExtHandler::GetClassID(CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

CSampleExtHandler::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(_szFileName, ARRAYSIZE(m_szFileName), pszFile);
}
```

### <a name="implementing-ishellextinit"></a>Implementando IShellExtInit

A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) tem apenas um método, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). O método tem três parâmetros que o Shell pode usar para passar vários tipos de informações. Os valores passados dependem do tipo de manipulador e alguns podem ser definidos como **NULL**.

-   *pIDFolder* mantém o ponteiro de uma pasta para uma lista de identificadores de item (PIDL). Para extensões de folha de propriedades, é **nulo**. Para extensões de menu de atalho, é o PIDL da pasta que contém o item cujo menu de atalho está sendo exibido. Para manipuladores do tipo "arrastar e soltar" não padrão, é o PIDL da pasta de destino.
-   *pDataObject* mantém um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de um objeto de dados. O objeto de dados contém um ou mais nomes de arquivo no formato [CF \_ HDROP](dragdrop.md) .
-   *hRegKey* mantém uma chave do registro para o tipo de objeto ou pasta de arquivo.

O método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) armazena o nome do arquivo, o ponteiro do [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e a chave do registro conforme necessário para uso posterior. O fragmento de código a seguir ilustra uma implementação de **IShellExtInit:: Initialize**. Para simplificar, este exemplo supõe que o objeto de dados contenha apenas um único arquivo. Em geral, ele pode conter vários arquivos que precisarão ser extraídos.


```C++
LPCITEMIDLIST  m_pIDFolder;           //The folder's PIDL
wchar_t        m_szFile[MAX_PATH];    //The file name
IDataObject   *m_pDataObj;            //The IDataObject pointer
HKEY           m_hRegKey;             //The file or folder's registry key

STDMETHODIMP CShellExt::Initialize(LPCITEMIDLIST pIDFolder, 
                                   IDataObject *pDataObj, 
                                   HKEY hRegKey) 
{ 
    // If Initialize has already been called, release the old PIDL
    ILFree(m_pIDFolder);
    m_pIDFolder = nullptr;

    // Store the new PIDL.
    if (pIDFolder)
    {
        m_pIDFolder = ILClone(pIDFolder);
    }
    
    // If Initialize has already been called, release the old
    // IDataObject pointer.
    if (m_pDataObj)
    { 
        m_pDataObj->Release(); 
    }
     
    // If a data object pointer was passed in, save it and
    // extract the file name. 
    if (pDataObj) 
    { 
        m_pDataObj = pDataObj; 
        pDataObj->AddRef(); 
      
        STGMEDIUM   medium;
        FORMATETC   fe = {CF_HDROP, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};
        UINT        uCount;

        if (SUCCEEDED(m_pDataObj->GetData(&fe, &medium)))
        {
            // Get the count of files dropped.
            uCount = DragQueryFile((HDROP)medium.hGlobal, (UINT)-1, NULL, 0);

            // Get the first file name from the CF_HDROP.
            if (uCount)
                DragQueryFile((HDROP)medium.hGlobal, 0, m_szFile, 
                              sizeof(m_szFile)/sizeof(TCHAR));

            ReleaseStgMedium(&medium);
        }
    }

    // Duplicate the registry handle. 
    if (hRegKey) 
        RegOpenKeyEx(hRegKey, nullptr, 0L, MAXIMUM_ALLOWED, &m_hRegKey); 
    return S_OK; 
}
```

CSampleExtHandler é o nome da classe usada para implementar a interface. As **variáveis \_ m pIDFolder**, **m \_ pDataObject**, **m \_ szFileName** e **m \_ hRegKey** são variáveis privadas usadas para armazenar as informações que são passadas. Para simplificar, este exemplo supõe que apenas um nome de arquivo será mantido pelo objeto de dados. Depois que a estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) é recuperada do objeto de dados, [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) é usado para extrair o nome do arquivo do membro **médio. HGLOBAL** da estrutura **FORMATETC** . Se uma chave do registro for passada, o método usará [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para abrir a chave e atribuir o identificador a **m \_ hRegKey**.

### <a name="infotip-customization"></a>Personalização de InfoTip

Há duas maneiras de personalizar o Infotips:

-   Implemente um objeto que dê suporte a [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e registre esse objeto sob a subchave apropriada no registro (consulte [Registrando manipuladores de extensão de shell](#registering-shell-extension-handlers) abaixo).
-   Especifique uma cadeia de caracteres fixa ou uma lista de propriedades de arquivo específicas a serem exibidas.

Para exibir uma cadeia de caracteres fixa para uma extensão de namespace, crie uma entrada chamada `InfoTip` na chave *{CLSID}* da extensão do namespace. Defina o valor dessa entrada como a cadeia de caracteres literal que você deseja exibir, como mostrado neste exemplo, ou uma cadeia de caracteres indireta que especifica um recurso e um índice dentro desse recurso (para fins de localização).

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Para exibir uma cadeia de caracteres fixa para um tipo de arquivo, crie uma entrada chamada `InfoTip` na chave *ProgID* desse tipo de arquivo. Defina o valor dessa entrada como a cadeia de caracteres literal que você deseja exibir ou uma cadeia de caracteres indireta que especifique um recurso e um índice dentro desse recurso (para fins de localização), conforme mostrado neste exemplo.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = Resource.dll, 3
```

Se você quiser que o Shell exiba Propriedades de arquivo específicas em InfoTip para um tipo de arquivo específico, crie uma entrada chamada `InfoTip` na chave *ProgID* para esse tipo de arquivo. Defina o valor dessa entrada como uma lista delineada por ponto-e-vírgula de nomes de propriedade canônicas, pares de identificadores de formato (FMTID)/Property (PID) ou ambos. Esse valor deve começar com "prop:" para identificá-lo como uma cadeia de caracteres da lista de propriedades. Se você omitir "prop:", o valor será visto como uma cadeia de caracteres literal e exibido como tal.

No exemplo a seguir, *propName* é um nome de propriedade canônico (como System. Date) e *{fmtid}, PID* é um par [**fmtid/PID**](./objects.md) .

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = prop:propname;propname;{fmtid},pid;{fmtid},pid
```

Os seguintes nomes de propriedade podem ser usados:



| Nome da propriedade    | Descrição                   | Recuperado de                                                                             |
|------------------|-------------------------------|--------------------------------------------------------------------------------------------|
| Autor           | Autor do documento        | [**autor do PIDSI \_**](../stg/the-summary-information-property-set.md)                              |
| Título            | Título do documento         | [**título do PIDSI \_**](../stg/the-summary-information-property-set.md)                               |
| Assunto          | Resumo do assunto               | [**assunto do PIDSI \_**](../stg/the-summary-information-property-set.md)                             |
| Comentário          | Comentários do documento             | [**PIDSI \_**](../stg/the-summary-information-property-set.md) Propriedades de comentário ou pasta/driver |
| PageCount        | Número de páginas               | [**PIDSI \_ PageCount**](../stg/the-summary-information-property-set.md)                           |
| Name             | Nome amigável                 | Exibição de pasta padrão                                                                       |
| OriginalLocation | Local do arquivo original     | Pasta do porta-arquivos e pasta lixeira                                                    |
| DateDeleted      | O arquivo de data foi excluído         | Pasta da lixeira                                                                         |
| Tipo             | Tipo de arquivo                  | Exibição de detalhes da pasta padrão                                                               |
| Tamanho             | Tamanho do arquivo                  | Exibição de detalhes da pasta padrão                                                               |
| SyncCopyIn       | O mesmo que OriginalLocation      | O mesmo que OriginalLocation                                                                   |
| Modificado         | Data da última modificação            | Exibição de detalhes da pasta padrão                                                               |
| Criado          | Data de criação                  | Exibição de detalhes da pasta padrão                                                               |
| Acessíveis         | Data do último acesso            | Exibição de detalhes da pasta padrão                                                               |
| Inpasta         | Diretório que contém o arquivo | Resultados da pesquisa de documentos                                                                    |
| Rank             | Qualidade de correspondência de pesquisa       | Resultados da pesquisa de documentos                                                                    |
| FreeSpace        | Espaço de armazenamento disponível       | Unidades de disco                                                                                |
| NumberOfVisits   | Número de visitas              | Pasta Favoritos                                                                           |
| Atributos       | Atributos do arquivo               | Exibição de detalhes da pasta padrão                                                               |
| Empresa          | Nome da empresa                  | [**\_empresa PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)    |
| Categoria         | Categoria do documento             | [**\_categoria PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Direitos autorais        | Direitos autorais da mídia               | [**\_direitos autorais do PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| HTMLInfoTipFile  | Arquivo InfoTip HTML             | Arquivo de Desktop.ini para a pasta                                                                |



 

## <a name="enhancing-windows-search-with-shell-extension-handlers"></a>Aprimorando o Windows Search com manipuladores de extensão de Shell

Os manipuladores de extensão do Shell podem ser usados para aprimorar a experiência do usuário fornecida por um manipulador de protocolo de pesquisa do Windows. Para habilitar esses aprimoramentos, o manipulador de extensão do Shell de suporte deve ser projetado para integrar com o manipulador de protocolo de pesquisa como uma fonte de dados. Para obter informações sobre como aprimorar um manipulador de protocolo de pesquisa do Windows por meio da integração com um manipulador de extensão de Shell, consulte [adicionando ícones, visualizações e menus de atalho](../search/-search-3x-wds-ph-ui-extensions.md). Para obter mais informações sobre os manipuladores de protocolo de pesquisa do Windows, consulte [desenvolvendo manipuladores de protocolo](../search/-search-3x-wds-phaddins.md).

## <a name="registering-shell-extension-handlers"></a>Registrando manipuladores de extensão do Shell

Um objeto de manipulador de extensão de Shell deve ser registrado antes que o Shell possa usá-lo. Esta seção é uma discussão geral sobre como registrar um manipulador de extensão de Shell.

Sempre que você criar ou alterar um manipulador de extensão de Shell, será importante notificar o sistema de que você fez uma alteração com [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), especificando o evento **SHCNE \_ assocchanged** . Se você não chamar **SHChangeNotify**, a alteração poderá não ser reconhecida até que o sistema seja reinicializado.

Assim como acontece com todos os objetos COM, você deve criar um GUID para o manipulador usando uma ferramenta como UUIDGEN.exe. Crie uma chave em **\_ classe HKEY \_ raiz** \\ **CLSID** cujo nome é a forma de cadeia de caracteres do GUID. Como os manipuladores de extensão do shell são servidores em processo, você deve criar uma chave **InprocServer32** na chave de GUID com o valor padrão definido como o caminho da dll do manipulador. Use o modelo de Threading Apartment.

Sempre que o Shell executar uma ação que possa envolver um manipulador de extensão de Shell, ele verificará a chave do registro apropriada. A chave sob a qual um manipulador de extensão é registrado, portanto, controla quando ele será chamado. Por exemplo, é uma prática comum ter um manipulador de menu de atalho chamado quando o Shell exibe um menu de atalho para um membro de um [tipo de arquivo](fa-file-types.md). Nesse caso, o manipulador deve ser registrado na chave **ProgID** do tipo de arquivo.

### <a name="handler-names"></a>Nomes de manipuladores

Para habilitar um manipulador de extensão de Shell, crie uma subchave com o nome da subchave do manipulador (veja abaixo) na subchave **shellex** do **ProgID** (para tipos de arquivo) ou o nome do tipo de objeto do Shell (para [objetos shell predefinidos](#predefined-shell-objects)).

Por exemplo, se você quisesse registrar um manipulador de extensão de menu de atalho para myprogram. 1, começaria criando a seguinte subchave:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Para os seguintes manipuladores, crie uma subchave sob a chave "nome da subchave do manipulador" cujo nome é a versão da cadeia de caracteres do CLSID da extensão do Shell. Várias extensões podem ser registradas na chave de nome da subchave do manipulador criando várias subchaves.



| Manipulador                                               | Interface          | Nome da subchave do manipulador       |
|-------------------------------------------------------|--------------------|---------------------------|
| Manipulador de menu de atalho                                 | IContextMenu       | **ContextMenuHandlers**   |
| Manipulador de Copyhook                                      | ICopyHook          | **CopyHookHandlers**      |
| Manipulador do tipo "arrastar e soltar"                                 | IContextMenu       | **DragDropHandlers**      |
| Manipulador de folha de propriedades                                | IShellPropSheetExt | **PropertySheetHandlers** |
| Manipulador de provedor de coluna (preterido no Windows Vista) | IColumnProvider    | **ColumnHandlers**        |



 

Para os seguintes manipuladores, o valor padrão da chave "nome da subchave do manipulador" é a versão da cadeia de caracteres do CLSID da extensão do Shell. Somente uma extensão pode ser registrada para esses manipuladores.



| Manipulador                 | Interface                                         | Nome da subchave do manipulador                        |
|-------------------------|---------------------------------------------------|--------------------------------------------|
| Manipulador de dados            | IDataObject                                       | **DataHandler**                            |
| Descartar manipulador            | IDropTarget                                       | **DropHandler**                            |
| Manipulador de ícone            | IExtractIconA/W                                   | **IconHandler**                            |
| Manipulador de imagem           | IExtractImage                                     | **{BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}** |
| Manipulador de imagem em miniatura | Manipuladordeminiaturai                                | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Manipulador de infodicas         | IQueryInfo                                        | **{00021500-0000-0000-C000-000000000046}** |
| Link do Shell (ANSI)      | IShellLinkA                                       | **{000214EE-0000-0000-C000-000000000046}** |
| Link do Shell (UNICODE)    | IShellLinkW                                       | **{000214F9-0000-0000-C000-000000000046}** |
| Armazenamento estruturado      | IStorage                                          | **{0000000B-0000-0000-C000-000000000046}** |
| Metadados                | IPropertyStore                                    | **PropertyHandler**                        |
| Metadados                | IPropertySetStorage (preterido no Windows Vista) | **PropertyHandler**                        |
| Fixar no menu iniciar       | IStartMenuPinnedList                              | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Fixar à barra de tarefas          |                                                   | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

As subchaves especificadas para adicionar **Pin ao menu iniciar** e **fixar à barra de tarefas** no menu de atalho de um item só são necessárias para tipos de arquivo que incluem a entrada [IsShortcut](./links.md) .

O suporte para manipuladores de provedor de coluna foi removido no Windows Vista. Além disso, a partir do Windows Vista, o [**IPropertySetStorage**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) foi preterido em favor do [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

Embora o [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) permaneça com suporte, o [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) é preferencial para o Windows Vista e posterior.

### <a name="predefined-shell-objects"></a>Objetos de shell predefinidos

O Shell define objetos adicionais na **\_ \_ raiz de classes hKey** que podem ser estendidas da mesma maneira que os tipos de arquivo. Por exemplo, para adicionar um manipulador de folha de propriedades para todos os arquivos, você pode registrar sob a chave **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

A tabela a seguir fornece as várias subchaves da **\_ \_ raiz de classes hKey** em que os manipuladores de extensão podem ser registrados. Observe que muitos manipuladores de extensão não podem ser registrados em todas as subchaves listadas. Para obter mais detalhes, consulte a documentação do manipulador específico.



| Subchave                    | Description                                                          | Possíveis manipuladores                                | Versão |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|---------|
| **\** _                    | Todos os arquivos                                                            | Menu de atalho, folha de propriedades, verbos (veja abaixo) | Tudo     |
| _ *AllFileSystemObjects**  | Todos os arquivos e pastas de arquivos                                           | Menu de atalho, folha de propriedades, verbos             | 4,71    |
| **Pasta**                | Todas as pastas                                                          | Menu de atalho, folha de propriedades, verbos             | Tudo     |
| **Active**             | Pastas de arquivos                                                         | Menu de atalho, folha de propriedades, verbos             | Tudo     |
| **Plano de fundo do diretório \\** | Plano de fundo da pasta de arquivos                                               | Somente menu de atalho                               | 4,71    |
| **Unidade**                 | Todas as unidades em MyComputer, como "C: \\ "                             | Menu de atalho, folha de propriedades, verbos             | Tudo     |
| **Rede**               | Rede inteira (em meus locais de rede)                             | Menu de atalho, folha de propriedades, verbos             | Tudo     |
| **Tipo de rede \\\\\#**     | Todos os objetos do tipo \# (veja abaixo)                                   | Menu de atalho, folha de propriedades, verbos             | 4,71    |
| **NetShare**              | Todos os compartilhamentos de rede                                                   | Menu de atalho, folha de propriedades, verbos             | 4,71    |
| **NetServer**             | Todos os servidores de rede                                                  | Menu de atalho, folha de propriedades, verbos             | 4,71    |
| *\_nome do provedor de rede \_* | Todos os objetos fornecidos pelo "*nome do \_ provedor \_ de rede*" do provedor de rede | Menu de atalho, folha de propriedades, verbos             | Tudo     |
| **Impressoras**              | Todas as impressoras                                                         | Menu de atalho, folha de propriedades                    | Tudo     |
| **AudioCD**               | CD de áudio na unidade de CD                                                 | Somente verbos                                       | Tudo     |
| **DVD**                   | Unidade de DVD (Windows 2000)                                             | Menu de atalho, folha de propriedades, verbos             | 4,71    |



 

Observações:

-   O menu de atalho de segundo plano da pasta de arquivo é acessado clicando com o botão direito do mouse em uma pasta de arquivo, mas não em qualquer conteúdo da pasta.
-   "Verbos" são comandos especiais registrados sob o verbo do Shell de subchave do **HKEY \_ classes \_ raiz** \\  \\  \\  .
-   Para o tipo de **rede** \\  \\ **\#** , " \# " é um código de tipo de provedor de rede em decimal. O código do tipo de provedor de rede é a palavra alta de um tipo de rede. A lista de tipos de rede é fornecida no arquivo de cabeçalho Winnetwk. h (WNNC \_ net \_ \* Values). Por exemplo, WNNC \_ net \_ Shiva é 0x00330000, portanto, a chave de tipo correspondente seria tipo de rede **\_ \_ raiz de classe HKEY** \\  \\  \\ **51** .
-   "*\_ \_ nome do provedor de rede*" é um nome de provedor de rede, conforme especificado por [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), com os espaços convertidos em sublinhados. Por exemplo, se o provedor de rede de rede da Microsoft estiver instalado, o nome do provedor será "rede do Microsoft Windows" e o *\_ \_ nome do provedor de rede* correspondente será a **\_ \_ rede do Microsoft Windows**.

### <a name="example-of-an-extension-handler-registration"></a>Exemplo de um registro de manipulador de extensão

Para habilitar um manipulador específico, crie uma subchave sob a chave do tipo de manipulador de extensão com o nome do manipulador. O shell não usa o nome do manipulador, mas ele deve ser diferente de todos os outros nomes nessa subchave de tipo. Defina o valor padrão da subchave Name para a forma de cadeia de caracteres do GUID do manipulador.

O exemplo a seguir ilustra as entradas do registro que habilitam manipuladores de extensão de folha de propriedades e menu de atalho, usando um tipo de arquivo de exemplo. MYP:

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

O procedimento de registro discutido nesta seção deve ser seguido para todos os sistemas Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes para implementar extensões de In-Process](shell-and-managed-code.md)
</dt> </dl>

 

 
