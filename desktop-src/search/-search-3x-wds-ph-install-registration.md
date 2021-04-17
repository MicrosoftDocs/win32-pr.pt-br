---
description: A instalação de um manipulador de protocolo envolve a cópia das DLLs para um local apropriado no diretório arquivos de programas e, em seguida, o registro do manipulador de protocolo por meio do registro.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Instalando e Registrando manipuladores de protocolo (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761782"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a>Instalando e Registrando manipuladores de protocolo (pesquisa do Windows)

A instalação de um manipulador de protocolo envolve a cópia das DLLs para um local apropriado no diretório arquivos de programas e, em seguida, o registro do manipulador de protocolo por meio do registro. O aplicativo de instalação também pode adicionar uma raiz de pesquisa e regras de escopo para definir um escopo de rastreamento padrão para a fonte de dados do Shell.

Este tópico é organizado da seguinte maneira:

-   [Sobre URLs](#about-urls)
-   [Implementando interfaces de manipulador de protocolo](#implementing-protocol-handler-interfaces)
    -   [ISearchProtocol e ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [IProtocolHandlerSite](#iprotocolhandlersite)
-   [Implementando manipuladores de filtro para contêineres](#implementing-filter-handlers-for-containers)
-   [Instalando e registrando um manipulador de protocolo](#installing-and-registering-a-protocol-handler)
    -   [Diretrizes para registrar um manipulador de protocolo](#guidelines-for-registering-a-protocol-handler)
    -   [Registrando um manipulador de protocolo](#installing-and-registering-a-protocol-handler)
    -   [Registrando o manipulador de tipo de arquivo do manipulador de protocolo](#registering-the-protocol-handlers-file-type-handler)
-   [Garantindo que seus itens sejam indexados](#ensuring-that-your-items-are-indexed)
-   [Tópicos relacionados](#related-topics)

## <a name="about-urls"></a>Sobre URLs

O Windows Search usa URLs para identificar exclusivamente os itens na hierarquia da fonte de dados do Shell. A URL que é o primeiro nó na hierarquia é chamada de [raiz de pesquisa](-search-3x-wds-extidx-csm-searchroots.md); O Windows Search começará a indexação na raiz da pesquisa, solicitando que o manipulador de protocolo enumere links filho para cada URL.

A estrutura de URL típica é:


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



A sintaxe da URL é descrita na tabela a seguir.



| Sintaxe           | Descrição                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | Identifica qual manipulador de protocolo deve ser invocado para a URL.                                                                                                                                                           |
| {SID de usuário}       | Identifica o contexto de segurança do usuário sob o qual o manipulador de protocolo é chamado. Se nenhum SID (identificador de segurança do usuário) for identificado, o manipulador de protocolo será chamado no contexto de segurança do serviço do sistema. |
| <path>     | Define a hierarquia do repositório, em que cada barra ('/') é um separador entre nomes de pasta.                                                                                                            |
| <ItemID>   | Representa uma cadeia de caracteres exclusiva que identifica o item filho (por exemplo, o nome do arquivo).                                                                                                                            |



 

O indexador de pesquisa do Windows corta a barra final de URLs. Como resultado, você não pode contar com a existência de uma barra final para identificar um diretório em vez de um item. Seu manipulador de protocolo deve ser capaz de lidar com essa sintaxe de URL. Verifique se o nome do protocolo que você selecionou para identificar a fonte de dados do shell não está em conflito com os atuais. Recomendamos esta Convenção de nomenclatura: `companyName.scheme` .

Para obter mais informações sobre como criar uma fonte de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="implementing-protocol-handler-interfaces"></a>Implementando interfaces de manipulador de protocolo

A criação de um manipulador de protocolo requer a implementação das três interfaces a seguir:

-   [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) para gerenciar objetos UrlAccessor.
-   [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) para expor propriedades e identificar os filtros apropriados para itens na fonte de dados do Shell.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para filtrar arquivos proprietários ou para enumerar e filtrar arquivos armazenados hierarquicamente.

Além das três interfaces obrigatórias listadas, as outras interfaces são opcionais e você está no Liberty para implementar qualquer interface opcional que seja mais apropriada para a tarefa em questão.

### <a name="isearchprotocol-and-isearchprotocol2"></a>ISearchProtocol e ISearchProtocol2

As interfaces SearchProtocol inicializam e gerenciam seus objetos UrlAccessor do manipulador de protocolo. A interface [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) é uma extensão opcional de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)e inclui um método extra para especificar mais informações sobre o usuário e o item.

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4

As interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) são descritas na tabela a seguir.



| Interface                                                 | Descrição                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | Para uma URL especificada, a interface [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fornece acesso às propriedades do item que é exposto na URL. Ele também pode associar essas propriedades a um filtro específico do manipulador de protocolo (ou seja, um filtro diferente daquele associado ao nome do arquivo). |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (opcional) | A interface [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) estende o [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) com métodos que obtêm uma página de código para as propriedades do item e sua URL de exibição e que obtêm o tipo de item na URL (documento ou diretório).                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (opcional) | A interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) estende o [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) com um método que obtém uma matriz de SIDs de usuário, permitindo que o host de protocolo de pesquisa represente esses usuários para indexar o item.                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (opcional) | A interface [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) estende a funcionalidade da interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) com um método que identifica se o conteúdo do item deve ser indexado.                                                                 |



 

O objeto UrlAccessor é instanciado e inicializado por um objeto SearchProtocol. As interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fornecem acesso a informações importantes por meio dos métodos descritos na tabela a seguir.



| Método                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | Retorna a hora em que a URL foi modificada pela última vez. Se esse tempo for mais recente do que a última vez que o indexador processou essa URL, os manipuladores de filtro (implementações da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) serão chamados para extrair os dados alterados (possivelmente) para esse item. Os horários modificados para diretórios são ignorados. |
| [**IUrlAccessor:: IsDirectory**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | Identifica se a URL representa uma pasta que contém URLs filho.                                                                                                                                                                                                                                                            |
| [**IUrlAccessor::BindToStream**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | Associa a uma [interface IStream](/windows/win32/api/objidl/nn-objidl-istream) que representa os dados de um arquivo em um repositório de dados personalizado.                                                                                                                                                                           |
| [**IUrlAccessor::BindToFilter**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | Associa a um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)específico do manipulador de protocolo, que pode expor propriedades para o item.                                                                                                                                                                                                                 |
| [**IUrlAccessor4::ShouldIndexItemContent**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | Identifica se o conteúdo do item deve ser indexado.                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>IProtocolHandlerSite

A interface [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) é usada para criar uma instância de um manipulador de filtro, que é hospedado em um processo isolado. O manipulador de filtro apropriado é obtido para um CLSID (identificador de classe persistente) especificado, uma classe de armazenamento de documentos ou uma extensão de nome de arquivo. O benefício de fazer com que o processo de host se vincule ao [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é que o processo de host pode gerenciar o processo de localização de um manipulador de filtro apropriado e controlar a segurança envolvida na chamada do manipulador.

## <a name="implementing-filter-handlers-for-containers"></a>Implementando manipuladores de filtro para contêineres

Se você estiver implementando um manipulador de protocolo hierárquico, deverá implementar um manipulador de filtro para um contêiner que enumere URLs filho. Um manipulador de filtro é uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . O processo de enumeração é um loop pelos métodos [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) e [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) da interface **IFilter** ; cada URL filho é exposta como o valor da propriedade.

[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retorna as propriedades do contêiner. Para enumerar URLs filho, **IFilter:: GetChunk** retorna um dos seguintes:

-   [PKEY \_ Pesquisar \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):

    A URL para o item sem a hora da última modificação. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retorna um PROPVARIANT que contém a URL filho.

-   [PKEY \_ Pesquisar \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):

    A URL e a hora da última modificação. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retorna um PROPVARIANT contendo um vetor da URL filho e a hora da última modificação.

Retornar [PKEY \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) é mais eficiente porque o indexador pode determinar imediatamente se o item precisa ser indexado sem chamar os métodos [**ISearchProtocol:: createaccess**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) e [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .

O código de exemplo a seguir demonstra como retornar a propriedade [ \_ \_ UrlToIndexWithModificationTime de pesquisa PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) .

> [!IMPORTANT]
>
> Copyright (c) Microsoft Corporation. Todos os direitos reservados.

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> Um componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) do contêiner sempre deve enumerar todas as URLs filho, mesmo que as URLs filho não tenham sido alteradas, pois o indexador detecta as exclusões por meio do processo de enumeração. Se a saída de data em um [PKEY de \_ pesquisa \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicar que os dados não foram alterados, o indexador não atualizará os dados dessa URL.

 

## <a name="installing-and-registering-a-protocol-handler"></a>Instalando e registrando um manipulador de protocolo

A instalação de manipuladores de protocolo envolve copiar as DLLs para um local apropriado no diretório arquivos de programas e, em seguida, registrar as DLLs. Os manipuladores de protocolo devem implementar o auto-registro para instalação. O aplicativo de instalação também pode adicionar uma raiz de pesquisa e regras de escopo para definir um escopo de rastreamento padrão para a fonte de dados do Shell, que é discutido para [garantir que seus itens sejam indexados](#ensuring-that-your-items-are-indexed) no final deste tópico.

### <a name="guidelines-for-registering-a-protocol-handler"></a>Diretrizes para registrar um manipulador de protocolo

Você deve seguir estas diretrizes ao registrar um manipulador de protocolo:

-   O instalador deve usar o EXE ou o instalador MSI.
-   As notas de versão devem ser fornecidas.
-   Uma entrada adicionar/remover programas deve ser criada para cada suplemento instalado.
-   O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.
-   Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.
-   Se um suplemento mais recente tiver substituído o suplemento anterior, deverá haver a capacidade de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão para esse tipo de arquivo novamente.
-   O instalador deve definir um escopo de rastreamento padrão para o indexador adicionando uma raiz de pesquisa e regras de escopo usando o Gerenciador de escopo de rastreamento (CSM).

### <a name="registering-a-protocol-handler"></a>Registrando um manipulador de protocolo

Você precisa fazer quatorze entradas no registro para registrar o componente de manipulador de protocolo, em que:

-   *Ver \_ IND \_ ProgID* é o ProgID independente de versão da implementação do manipulador de protocolo.
-   *Ver \_ O Dep \_ ProgID* é o ProgID dependente da versão da implementação do manipulador de protocolo.
-   *CLSID \_ 1* é o CLSID da implementação do manipulador de protocolo.

**Para registrar um manipulador de protocolo:**

1.  Registre o ProgID independente de versão com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  Registre o ProgID dependente de versão com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  Registre o CLSID do manipulador de protocolo com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  Registre o manipulador de protocolo no Windows Search. No exemplo a seguir, <Protocol Name> é o nome do próprio protocolo, como arquivo, MAPI e assim por diante:

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    Antes do Windows Vista:

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a>Registrando o manipulador de tipo de arquivo do manipulador de protocolo

Você precisa fazer duas entradas no registro para registrar o manipulador de tipo de arquivo do manipulador de protocolo (que também é conhecido como extensão do Shell).

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a>Garantindo que seus itens sejam indexados

Depois de implementar o manipulador de protocolo, você deve especificar quais itens do Shell seu manipulador de protocolo será indexado. Você pode usar o Gerenciador de catálogo para iniciar a reindexação (para obter mais informações, consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md)). Ou você também pode usar o Gerenciador de escopo de rastreamento (CSM) para configurar regras padrão indicando as URLs que você deseja que o indexador rastreie (para obter mais informações, consulte [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md) e [regras de escopo de gerenciamento](-search-3x-wds-extidx-csm-scoperules.md)). Você também pode adicionar uma raiz de pesquisa (para obter mais informações, consulte [Gerenciando raízes de pesquisa](-search-3x-wds-extidx-csm-searchroots.md)). Outra opção disponível para você é seguir o procedimento no exemplo reindexar em [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

A interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fornece métodos que notificam o mecanismo de pesquisa de contêineres para rastreamento e/ou inspeção e itens sob esses contêineres para incluir ou excluir ao rastrear ou assistir. No Windows 7 e posterior, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) estende **ISearchCrawlScopeManager** com o método [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) que obtém a versão, que informa aos clientes se o estado do CSM foi alterado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Noções básicas sobre manipuladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notificando o índice das alterações](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Adicionando ícones e menus de contexto](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemplo de código: extensões de Shell para manipuladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Criando um conector de pesquisa para um manipulador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Depuração de manipuladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
