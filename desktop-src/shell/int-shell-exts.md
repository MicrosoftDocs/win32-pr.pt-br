---
description: Grande parte da implementação de um objeto de manipulador de extensão de Shell é ditada por seu tipo. No entanto, há alguns elementos comuns. Este tópico discute os aspectos da implementação que são compartilhados por todos os manipuladores de extensão do Shell.
ms.assetid: ce21ca0f-157c-4f69-bcf9-dc259c3bac80
title: Inicializando manipuladores de extensão do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a27b6273c5e342dc4caf545fb3593cdad66261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968207"
---
# <a name="initializing-shell-extension-handlers"></a>Inicializando manipuladores de extensão do Shell

Grande parte da implementação de um objeto de manipulador de extensão de Shell é ditada por seu tipo. No entanto, há alguns elementos comuns. Este tópico discute os aspectos da implementação que são compartilhados por todos os manipuladores de extensão do Shell.

Todos os manipuladores de extensão do shell são objetos COM (Component Object Model) em processo. Eles devem ser atribuídos a um GUID e registrados conforme descrito em [Registrando manipuladores de extensão do Shell](handlers.md). Eles são implementados como DLLs e devem exportar as seguintes funções padrão:

-   [**DllMain**](../dlls/dllmain.md). O ponto de entrada padrão para a DLL.
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject). Expõe a fábrica de classes do objeto.
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow). COM chama essa função para determinar se o objeto está atendendo a clientes. Caso contrário, o sistema pode descarregar a DLL e liberar a memória associada.

Como todos os objetos COM, os manipuladores de extensão do Shell devem implementar uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e uma [fábrica de classes](../com/implementing-iclassfactory.md). A maioria também deve implementar uma interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ou [**ISHELLEXTINIT**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) no Windows XP ou anterior. Elas foram substituídas por [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) e [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile) no Windows Vista. O Shell usa essas interfaces para inicializar o manipulador.

A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) deve ser implementada pelo seguinte:

-   Manipuladores de ícone
-   Manipuladores de dados
-   Descartar manipuladores

A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) deve ser implementada pelo seguinte:

-   Manipuladores de menu de atalho
-   Manipuladores de arrastar e soltar
-   Manipuladores de folha de propriedades

Os seguintes assuntos são discutidos no restante deste tópico:

-   [Implementando IPersistFile](#implementing-ipersistfile)
-   [Implementando IShellExtInit](#implementing-ishellextinit)
-   [Personalização de InfoTip](#infotip-customization)
-   [Tópicos relacionados](#related-topics)

## <a name="implementing-ipersistfile"></a>Implementando IPersistFile

A interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) foi projetada para permitir que um objeto seja carregado ou salvo em um arquivo de disco. Ele tem seis métodos além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), cinco de sua própria e o método [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) que ele herda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist). Com extensões de Shell, **IPersist** é usado apenas para inicializar um objeto de manipulador de extensão de Shell. Como normalmente não há necessidade de ler ou gravar no disco, somente os métodos **GetClassID** e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) exigem uma implementação sem token.

O Shell chama [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) primeiro e a função retorna o identificador de classe (CLSID) do objeto do manipulador de extensão. Em seguida, o Shell chama [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) e passa em dois valores. O primeiro, *pszFile*, é uma cadeia de caracteres Unicode com o nome do arquivo ou da pasta em que o Shell está prestes a operar. O segundo é *dwMode*, que indica o modo de acesso do arquivo. Como normalmente não há necessidade de acessar arquivos, o *dwMode* geralmente é zero. O método armazena esses valores conforme necessário para referência posterior.

O fragmento de código a seguir ilustra como um manipulador de extensão de shell típico implementa os métodos [**GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) e [**Load**](/windows/win32/api/objidl/nf-objidl-ipersistfile-load) . Ele foi projetado para lidar com ANSI ou Unicode. CLSID \_ SampleExtHandler é o GUID do objeto do manipulador de extensão e CSampleShellExtension é o nome da classe usada para implementar a interface. As variáveis **m \_ szFileName** e **m \_ dwMode** são variáveis privadas que são usadas para armazenar o nome do arquivo e os sinalizadores de acesso.


```C++
class CSampleShellExtension : public IPersistFile
{
    // Method declarations not included

    private:
    WCHAR m_szFileName[MAX_PATH];    // The file name
    DWORD m_dwMode;                  // The file access mode
}

IFACEMETHODIMP CSampleShellExtension::GetClassID(__out CLSID *pCLSID)
{
    *pCLSID = CLSID_SampleExtHandler;
}

IFACEMETHODIMP CSampleShellExtension::Load(PCWSTR pszFile, DWORD dwMode)
{
    m_dwMode = dwMode;
    return StringCchCopy(m_szFileName, ARRAYSIZE(m_szFileName), pszFile); 
}

// The implementation sample is continued in the next section.
```



## <a name="implementing-ishellextinit"></a>Implementando IShellExtInit

A interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) tem apenas um método, [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). O método tem três parâmetros que o Shell pode usar para passar vários tipos de informações. Os valores passados dependem do tipo de manipulador e alguns podem ser definidos como **NULL**.

-   *pidlFolder* mantém o ponteiro de uma pasta para uma lista de identificadores de item (PIDL). Este é um PIDL absoluto. Para extensões de folha de propriedades, esse valor é **NULL**. Para extensões de menu de atalho, é o PIDL da pasta que contém o item cujo menu de atalho está sendo exibido. Para manipuladores do tipo "arrastar e soltar" não padrão, é o PIDL da pasta de destino.
-   *pDataObject* mantém um ponteiro para a interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de um objeto de dados. O objeto de dados contém um ou mais nomes de arquivo no formato [CF \_ HDROP](dragdrop.md) .
-   *hRegKey* mantém uma chave do registro para o tipo de objeto ou pasta de arquivo.

O método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) armazena o nome do arquivo, o ponteiro do [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) e a chave do registro conforme necessário para uso posterior. O fragmento de código a seguir ilustra uma implementação de **IShellExtInit:: Initialize**. Para simplificar, este exemplo supõe que o objeto de dados contenha apenas um único arquivo. Em geral, o objeto de dados pode conter vários arquivos, cada um deles precisará ser extraído.


```C++
// This code continues the CSampleShellExtension sample shown in the
// "Implementing IPersistFile" section above.

class CSampleShellExtension : public IShellExtInit
{
    // Method declarations not included
    
    private:
    // IDList of the folder for extensions invoked on the folder, such as 
    // background context menu handlers or nondefault drag-and-drop handlers. 
    PIDLIST_ABSOLUTE m_pidlFolder;
    
    // The data object contains an expression of the items that the handler is 
    // being initialized for. Use SHCreateShellItemArrayFromDataObject to 
    // convert this object to an array of items. Use SHGetItemFromObject if you
    // are only interested in a single Shell item. If you need a file system
    // path, use IShellItem::GetDisplayName(SIGDN_FILESYSPATH, ...).
    IDataObject *m_pdtobj;
    
    // For context menu handlers, the registry key provides access to verb 
    // instance data that might be stored there. This is a rare feature to use 
    // so most extensions do not need this variable.
    HKEY m_hRegKey;             
}
    
// This method must be very efficient. Do not do any unnecessary work here.
// Use Initialize to acquire resources that will be used later.

IFACEMETHODIMP CSampleShellExtension::Initialize(__in_opt PCIDLIST_ABSOLUTE pidlFolder,
                                                 __in_opt IDataObject *pDataObject, 
                                                 __in_opt HKEY hRegKey) 
{ 
    // In some cases, handlers are initialized multiple times. Therefore, 
    // clear any previous state here.
    CoTaskMemFree(m_pidlFolder);
    m_pidlFolder = NULL;
    
    if (m_pdtobj)
    { 
        m_pdtobj->Release(); 
    }
    
    if (m_hRegKey)
    {
        RegCloseKey(m_hRegKey);
        m_hRegKey = NULL;
    }
    
    // Capture the inputs for use later.
    HRESULT hr = S_OK;
    
    if (pidlFolder)
    {
        m_pidlFolder = ILClone(pidlFolder);   // Make a copy to use later.
        hr = m_pidlFolder ? S_OK : E_OUTOFMEMORY;
    }
    
    if (SUCCEEDED(hr))
    {
        // If a data object pointer was passed into the method, save it and
        // extract the file name. 
        if (pDataObject) 
        { 
            m_pdtobj = pDataObject; 
            m_pdtobj->AddRef(); 
        }
    
        // It is uncommon to use the registry handle, but if you need it,
        // duplicate it now.
        if (hRegKey)
        {
            LSTATUS const result = RegOpenKeyEx(hRegKey, NULL, 0, KEY_READ, &m_hRegKey); 
            hr = HRESULT_FROM_WIN32(result);
        }
    }
    
    return hr;
}
```



## <a name="infotip-customization"></a>Personalização de InfoTip

Há duas maneiras de personalizar o Infotips. Uma maneira é implementar um objeto que dê suporte a [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) e, em seguida, registrar o objeto sob a subchave apropriada no registro (veja abaixo). Como alternativa, você pode especificar uma cadeia de caracteres fixa ou uma lista de determinadas propriedades de arquivo a serem exibidas.

Para exibir uma cadeia de caracteres fixa para uma extensão de namespace, crie uma subchave chamada **InfoTip** abaixo da chave CLSID de sua extensão de namespace. Defina os dados dessa subchave como a cadeia de caracteres que você deseja exibir.

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID}
         InfoTip = InfoTip string for your namespace extension
```

Para exibir uma cadeia de caracteres fixa para um tipo de arquivo, crie uma subchave chamada **InfoTip** abaixo da chave **ProgID** do tipo de arquivo para o qual você deseja fornecer Infotips. Defina os dados dessa subchave como a cadeia de caracteres que você deseja exibir.

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = InfoTip string for all files of this type
```

Se você quiser que o Shell mostre determinadas propriedades de arquivo em InfoTip para um tipo de arquivo específico, crie uma subchave chamada **InfoTip** abaixo da chave **ProgID** desse tipo de arquivo. Defina os dados dessa subchave como uma lista delineada por ponto-e-vírgula de nomes de propriedade canônicas ou {fmtid}, pares de PID em que *propName* é um nome de propriedade canônica e *{fmtid}, PID* é um [**par fmtid/PID**](./objects.md).

```
HKEY_CLASSES_ROOT
   ProgID
      InfoTip = propname;propname;{fmtid},pid;{fmtid},pid
```

Os nomes de propriedade a seguir podem ser usados.



| Nome da propriedade    | Descrição                   | Recuperado de                                                                            |
|------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| Autor           | Autor do documento        | [**autor do PIDSI \_**](../stg/the-summary-information-property-set.md)                             |
| Título            | Título do documento         | [**título do PIDSI \_**](../stg/the-summary-information-property-set.md)                              |
| Assunto          | Resumo do assunto               | [**assunto do PIDSI \_**](../stg/the-summary-information-property-set.md)                            |
| Comentário          | Comentários do documento             | [**PIDSI \_**](../stg/the-summary-information-property-set.md) Propriedades de comentário ou pasta/unidade |
| PageCount        | Número de páginas               | [**PIDSI \_ PageCount**](../stg/the-summary-information-property-set.md)                          |
| Name             | Nome amigável                 | Exibição de pasta padrão                                                                      |
| OriginalLocation | Local do arquivo original     | Pasta do porta-arquivos e pasta lixeira                                                   |
| DateDeleted      | O arquivo de data foi excluído         | Pasta da lixeira                                                                        |
| Tipo             | Tipo de arquivo                  | Exibição de detalhes da pasta padrão                                                              |
| Tamanho             | Tamanho do arquivo                  | Exibição de detalhes da pasta padrão                                                              |
| SyncCopyIn       | O mesmo que OriginalLocation      | O mesmo que OriginalLocation                                                                  |
| Modificado         | Data da última modificação            | Exibição de detalhes da pasta padrão                                                              |
| Criado          | Data de criação                  | Exibição de detalhes da pasta padrão                                                              |
| Acessíveis         | Data do último acesso            | Exibição de detalhes da pasta padrão                                                              |
| Inpasta         | Diretório que contém o arquivo | Resultados da pesquisa de documentos                                                                   |
| Rank             | Qualidade de correspondência de pesquisa       | Resultados da pesquisa de documentos                                                                   |
| FreeSpace        | Espaço de armazenamento disponível       | Unidades de disco                                                                               |
| NumberOfVisits   | Número de visitas              | Pasta Favoritos                                                                          |
| Atributos       | Atributos do arquivo               | Exibição de detalhes da pasta padrão                                                              |
| Empresa          | Nome da empresa                  | [**\_empresa PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)   |
| Categoria         | Categoria do documento             | [**\_categoria PIDDSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md)  |
| Direitos autorais        | Direitos autorais da mídia               | [**\_direitos autorais do PIDMSI**](../stg/the-documentsummaryinformation-and-userdefined-property-sets.md) |
| HTMLInfoTipFile  | Arquivo InfoTip HTML             | Arquivo de Desktop.ini para a pasta                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando manipuladores de extensão do Shell](reg-shell-exts.md)
</dt> </dl>

 

 
