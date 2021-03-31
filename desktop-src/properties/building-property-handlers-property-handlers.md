---
description: Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: Inicializando manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8eb11bc44217e508313bfb477c65925b44216e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169748"
---
# <a name="initializing-property-handlers"></a>Inicializando manipuladores de propriedade

Este tópico explica como criar e registrar manipuladores de propriedade para trabalhar com o sistema de propriedades do Windows.

Este tópico é organizado da seguinte maneira:

-   [Manipuladores de propriedade](#property-handlers)
-   [Antes de começar](#before-you-begin)
-   [Inicializando manipuladores de propriedade](#initializing-property-handlers)
-   [Armazenamento de propriedades na memória](#in-memory-property-store)
-   [Lidando com valores de PROPVARIANT-Based](#dealing-with-propvariant-based-values)
-   [Suporte a metadados abertos](#supporting-open-metadata)
-   [Conteúdo de texto completo](#full-text-contents)
-   [Fornecendo valores para propriedades](#providing-values-for-properties)
-   [Gravando valores de volta](#writing-back-values)
-   [Implementando IPropertyStoreCapabilities](#implementing-ipropertystorecapabilities)
-   [Registrando e distribuindo manipuladores de propriedade](#registering-and-distributing-property-handlers)
-   [Tópicos relacionados](#related-topics)

## <a name="property-handlers"></a>Manipuladores de propriedade

Manipuladores de propriedade são uma parte crucial do sistema de propriedades. Eles são invocados em processo pelo indexador para ler e indexar valores de propriedade e também são invocados pelo Windows Explorer em processo para ler e gravar valores de propriedade diretamente nos arquivos. Esses manipuladores precisam ser cuidadosamente escritos e testados para evitar o degradamento do desempenho ou a perda de dados nos arquivos afetados. Para obter mais informações sobre considerações específicas do indexador que afetam a implementação do manipulador de propriedades, consulte [desenvolvendo manipuladores de propriedade para o Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

Este tópico discute um exemplo de formato de arquivo baseado em XML que descreve uma receita com uma extensão de nome de arquivo. recipe. A extensão de nome de arquivo. recipe é registrada como seu próprio formato de arquivo distinto, em vez de depender do formato de arquivo mais genérico. xml, cujo manipulador usa um fluxo secundário para armazenar propriedades. Recomendamos que você registre extensões de nome de arquivo exclusivas para seus tipos de arquivo.

## <a name="before-you-begin"></a>Antes de começar

Manipuladores de propriedade são objetos COM que criam a abstração [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para um formato de arquivo específico. Eles lêem (analisam) e gravam esse formato de arquivo de forma que esteja em conformidade com sua especificação. Alguns manipuladores de propriedades fazem seu trabalho com base em APIs que abstraim o acesso a um formato de arquivo específico. Antes de desenvolver um manipulador de propriedades para seu formato de arquivo, você precisa entender como o formato de arquivo armazena propriedades e como essas propriedades (nomes e valores) são mapeadas para a abstração de armazenamento de propriedade.

Ao planejar sua implementação, lembre-se de que os manipuladores de propriedade são componentes de nível baixo que são carregados no contexto de processos como o Windows Explorer, o indexador do Windows Search e os aplicativos de terceiros que usam o modelo de programação de item de Shell. Como resultado, os manipuladores de propriedade não podem ser implementados em código gerenciado e devem ser implementados em C++. Se o seu manipulador usar quaisquer APIs ou serviços para fazer seu trabalho, você deve garantir que esses serviços possam funcionar corretamente no (s) ambiente (es) em que o manipulador de propriedades está carregado.

> [!Note]  
> Manipuladores de propriedade sempre são associados a tipos de arquivo específicos; Portanto, se o formato de arquivo contiver propriedades que exigem um manipulador de propriedade personalizada, você sempre deverá registrar uma extensão de nome de arquivo exclusiva para cada formato de arquivo.

 

## <a name="initializing-property-handlers"></a>Inicializando manipuladores de propriedade

Antes que uma propriedade seja usada pelo sistema, ela é inicializada chamando uma implementação de [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream). O manipulador de propriedades deve ser inicializado fazendo com que o sistema atribua um fluxo em vez de deixar essa atribuição para a implementação do manipulador. Esse método de inicialização garante as seguintes coisas:

-   O manipulador de propriedades pode ser executado em um processo restrito (um recurso de segurança importante) sem ter direitos de acesso para ler ou gravar arquivos diretamente, em vez de acessar seu conteúdo por meio do fluxo.
-   O sistema pode ser confiável para lidar com o arquivo oplocks corretamente, que é uma medida de confiabilidade importante.
-   O sistema de propriedades fornece um serviço de salvamento seguro automático sem nenhuma funcionalidade extra necessária da implementação do manipulador de propriedades. Consulte a seção [redação de valores](#writing-back-values) para obter mais informações sobre fluxos.
-   O uso do [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstrai sua implementação dos detalhes do sistema de arquivos. Isso permite que o manipulador ofereça suporte à inicialização por meio de armazenamentos alternativos, como uma pasta protocolo FTP (FTP) ou um arquivo compactado com uma extensão de nome de arquivo. zip.

Há casos em que a inicialização com fluxos não é possível. Nessas situações, há duas interfaces adicionais que os manipuladores de propriedade podem implementar: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) e [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem). Se um manipulador de propriedades não implementar o [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), ele deverá recusar a execução no processo isolado no qual o indexador do sistema o colocaria por padrão se houvesse uma alteração no fluxo. Para recusar esse recurso, defina o valor do registro a seguir.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

No entanto, é muito melhor implementar [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) e fazer uma inicialização baseada em fluxo. O manipulador de propriedades será mais seguro e confiável como resultado. Desabilitar o isolamento de processo geralmente é destinado apenas a manipuladores de propriedade herdados e deve ser strenuously evitado por qualquer código novo.

Para examinar a implementação de um manipulador de propriedades em detalhes, examine o exemplo de código a seguir, que é uma implementação de [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize). O manipulador é inicializado carregando um documento de receita baseado em XML por meio de um ponteiro para a instância [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) associada do documento. A variável **\_ spDocEle** usada perto do final do exemplo de código é definida anteriormente no exemplo como um MSXML2:: IXMLDOMElementPtr.

> [!Note]  
> O seguinte e todos os exemplos de código subsequentes são obtidos do exemplo de manipulador de receita incluído no SDK (Software Development Kit) do Windows. .

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



Â 

Depois que o próprio documento é carregado, as propriedades a serem exibidas no Windows Explorer são carregadas chamando o método **\_ GetProperties** protegido, conforme ilustrado no exemplo de código a seguir. Esse processo é examinado em detalhes na próxima seção.


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



Se o fluxo for somente leitura, mas o parâmetro *grfMode* contiver o \_ sinalizador ReadWrite STGM, a inicialização deverá falhar e retornar STG \_ e \_ ACCESSDENIED. Sem essa verificação, o Windows Explorer mostra os valores de propriedade como graváveis, embora não estejam, levando a uma experiência confusa para o usuário final.

O manipulador de propriedades é inicializado apenas uma vez em seu tempo de vida. Se uma segunda inicialização for solicitada, o manipulador deverá retornar `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` .

## <a name="in-memory-property-store"></a>Armazenamento de propriedades In-Memory

Antes de examinar a implementação de **\_**, você deve entender a matriz **PropertyMap** usada no exemplo para mapear Propriedades no documento XML para as propriedades existentes no sistema de propriedades por meio de seus valores de pkey.

Você não deve expor todos os elementos e atributos no arquivo XML como uma propriedade. Em vez disso, selecione apenas aqueles que você acredita que serão úteis para os usuários finais na organização de seus documentos (neste caso, receitas). Esse é um conceito importante para ter em mente ao desenvolver seus manipuladores de propriedade: a diferença entre as informações que são verdadeiramente úteis para cenários organizacionais e informações que pertencem aos detalhes do arquivo e que podem ser vistas abrindo o próprio arquivo. As propriedades não se destinam a ser uma duplicação completa de um arquivo XML.


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



Aqui está a implementação completa do método **\_ LoadProperties** chamado por [**IInitializeWithStream:: Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



O **\_ método** chama a função auxiliar do Shell [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para criar um repositório de propriedades na memória (cache) para as propriedades manipuladas. Usando um cache, as alterações são controladas para você. Isso libera você do rastreamento se um valor de propriedade foi alterado no cache, mas ainda não foi salvo no armazenamento persistente. Ele também libera você de manter desnecessariamente os valores de propriedade que não foram alterados.

O método **\_ LoadProperties** também chama **\_ LoadProperty** cuja implementação é ilustrada no código a seguir) uma vez para cada propriedade mapeada. **\_ LoadProperty** Obtém o valor da propriedade conforme especificado no elemento **PropertyMap** no fluxo XML e o atribui ao cache na memória por meio de uma chamada para [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate). O \_ sinalizador normal do PSC na chamada para **IPropertyStoreCache:: SetValueAndState** indica que o valor da propriedade não foi alterado desde a hora em que inseriu o cache.


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a>Lidando com valores de PROPVARIANT-Based

Na implementação de **\_ LoadProperty**, um valor de propriedade é fornecido na forma de um [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Um conjunto de APIs no Software Development Kit (SDK) é fornecido para converter de tipos primitivos como **PWSTR** ou **int** para ou de tipos **PROPVARIANT** . Essas APIs são encontradas em Propvarutil. h.

Por exemplo, para converter um [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) em uma cadeia de caracteres, você pode usar [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) conforme ilustrado aqui.


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



Para inicializar um PROPVARIANT de uma cadeia de caracteres, você pode usar [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



Como você pode ver em qualquer um dos arquivos de receita incluídos no exemplo, pode haver mais de uma palavra-chave em cada arquivo. Para considerar isso, o sistema de propriedades dá suporte a cadeias de caracteres com valores múltiplos representados como um vetor de cadeias de caracteres (por exemplo, "VT \_ vector \| VT \_ LPWSTR"). O método **\_ loadvetorproperty** no exemplo usa valores baseados em vetor.


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



Se um valor não existir no arquivo, não retorne um erro. Em vez disso, defina o valor como VT \_ vazio e retorne **S \_ OK**. \_O VT vazio indica que o valor da propriedade não existe.

## <a name="supporting-open-metadata"></a>Suporte a metadados abertos

Este exemplo usa um formato de arquivo baseado em XML. Seu esquema pode ser estendido para dar suporte a propriedades que não foram consideradas durante developmet, por exemplo. Esse sistema é conhecido como metadados abertos. Este exemplo estende o sistema de propriedades criando um nó sob o elemento **recipe** chamado **ExtendedProperties**, conforme ilustrado no exemplo de código a seguir.


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



Para carregar propriedades estendidas persistentes durante a inicialização, implemente o método **\_ extendeproperties** , conforme ilustrado no exemplo de código a seguir.


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



As APIs de serialização declaradas em propsys. h são usadas para serializar e desserializar os tipos [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) em blobs de dados e a codificação Base64 é usada para serializar esses BLOBs em cadeias de caracteres que podem ser salvas no XML. Essas cadeias de caracteres são armazenadas no atributo **EncodedValue** do elemento **ExtendedProperties** . O seguinte método de utilitário, implementado no arquivo util. cpp de exemplo, executa a serialização. Ele começa com uma chamada para a função [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) para executar a serialização binária, conforme ilustrado no exemplo de código a seguir.


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



Em seguida, a função [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â, declarada em Wincrypt. h, executa a conversão base64.


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



A função **DeserializePropVariantFromString** , também encontrada em util. cpp, reverte a operação, desserializando valores do arquivo XML.

Para obter informações sobre o suporte para metadados abertos, consulte "tipos de arquivo que dão suporte a metadados abertos" em [tipos de arquivo](../shell/fa-file-types.md).

## <a name="full-text-contents"></a>Conteúdo do Full-Text

Os manipuladores de propriedade também podem facilitar uma pesquisa de texto completo do conteúdo do arquivo, e eles são uma maneira fácil de fornecer essa funcionalidade se o formato de arquivo não for excessivamente complicado. Há uma maneira alternativa e mais eficiente de fornecer o texto completo do arquivo por meio da implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

A tabela a seguir resume os benefícios de cada abordagem usando o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou o [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).



| Funcionalidade                                   | Visio                      | IPropertyStore |
|----------------------------------------------|------------------------------|----------------|
| Permite write-back em arquivos?                  | Não                           | Sim            |
| Fornece uma combinação de conteúdo e propriedades?      | Sim                          | Sim            |
| Multilíngüe?                                | Sim                          | Não             |
| MIME/inserido?                               | Sim                          | Não             |
| Limites de texto?                             | Sentença, parágrafo, capítulo | Nenhum           |
| Implementação com suporte para SPS/SQL Server? | Sim                          | Não             |
| Implementação                               | Complex                      | Simples         |



 

No exemplo de manipulador de receitas, o formato de arquivo de receita não tem requisitos complexos, portanto, somente [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) foi implementado para suporte de texto completo. A pesquisa de texto completo é implementada para os nós XML nomeados na matriz a seguir.


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



O sistema de propriedades contém a `System.Search.Contents` \_ Propriedade (conteúdo de pesquisa PKEY \_ ), que foi criada para fornecer conteúdo de texto completo ao indexador. O valor dessa propriedade nunca é exibido diretamente na interface do usuário; o texto de todos os nós XML nomeados na matriz acima é concatenado em uma única cadeia de caracteres. Essa cadeia de caracteres é fornecida ao indexador como o conteúdo de texto completo do arquivo de receita por meio de uma chamada para [**IPropertyStoreCache:: SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) , conforme ilustrado no exemplo de código a seguir.


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a>Fornecendo valores para propriedades

Quando usado para ler valores, os manipuladores de propriedades geralmente são invocados por um dos seguintes motivos:

-   Para enumerar todos os valores de propriedade.
-   Para obter o valor de uma propriedade específica.

Para enumeração, um manipulador de propriedades é solicitado a enumerar suas propriedades durante a indexação ou quando a caixa de diálogo Propriedades solicita que as propriedades sejam exibidas no **outro** grupo. A indexação passa constantemente como uma operação em segundo plano. Sempre que um arquivo é alterado, o indexador é notificado e ele indexa novamente o arquivo solicitando que o manipulador de propriedades enumere suas propriedades. Portanto, é essencial que os manipuladores de propriedade sejam implementados com eficiência e retornam valores de propriedade o mais rápido possível. Enumere todas as propriedades para as quais você tem valores, assim como faria para qualquer coleção, mas não enumere propriedades que envolvem cálculos de uso intensivo de memória ou solicitações de rede que poderiam torná-los lentos para serem recuperados.

Ao escrever um manipulador de propriedades, normalmente você precisa considerar os dois conjuntos de propriedades a seguir.

-   Propriedades primárias: Propriedades às quais o tipo de arquivo dá suporte nativamente. Por exemplo, um manipulador de propriedade de foto para metadados de EXIF (arquivo de imagem intercambiável) dá suporte nativo `System.Photo.FNumber` .
-   Propriedades estendidas: Propriedades às quais o tipo de arquivo dá suporte como parte dos metadados abertos.

Como o exemplo usa o cache na memória, a implementação de métodos [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) é apenas uma questão de delegar a esse cache, conforme ilustrado no exemplo de código a seguir.


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



Se você optar por não delegar ao cache na memória, deverá implementar seus métodos para fornecer> seguinte comportamento esperado:

-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): se não houver propriedades, esse método retornará **S \_ OK**.
-   [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): se *iProp* for maior ou igual a *CProps*, esse método retornará e \_ INVALIDARG e a estrutura apontada pelo parâmetro *PKEY* será preenchida com zeros.
-   [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) e [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) refletem o estado atual do manipulador de propriedades. Se um [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) é adicionado ou removido do arquivo por meio de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), esses dois métodos devem refletir que mudam na próxima vez que forem chamados.
-   [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): se esse método for solicitado para um valor que não existe, ele retornará **S \_ OK** com o valor relatado como VT \_ vazio.

## <a name="writing-back-values"></a>Gravando valores de volta

Quando o manipulador de propriedades grava o valor de uma propriedade usando [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), ele não grava o valor no arquivo até que [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) seja chamado. O cache na memória pode ser útil para implementar esse esquema. No código de exemplo, a implementação **IPropertyStore:: SetValue** simplesmente define o novo valor no cache na memória e define o estado dessa propriedade como PSC \_ sujo.


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



Em qualquer implementação de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , o seguinte comportamento é esperado de [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):

-   Se a propriedade já existir, o valor da propriedade será definido.
-   Se a propriedade não existir, a nova propriedade será adicionada e seu valor definido.
-   Se o valor da propriedade não puder ser persistido com a mesma precisão fornecida (por exemplo, truncamento devido a limitações de tamanho no formato de arquivo), o valor será definido o máximo possível e os S inplaces \_ \_ serão retornados.
-   Se a propriedade não for suportada pelo manipulador de propriedade, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` será retornado.
-   Se houver outro motivo pelo qual o valor da propriedade não pode ser definido, como o arquivo que está sendo bloqueado ou falta de direitos para editar através de ACLs (listas de controle de acesso), STG \_ E \_ ACCESSDENIED será retornado.

Uma grande vantagem de usar fluxos, como o exemplo, é a confiabilidade. Os manipuladores de propriedades sempre devem considerar que não podem deixar um arquivo em um estado inconsistente no caso de uma falha catastrófica. É óbvio que a corrupção dos arquivos de um usuário deve ser evitada e a melhor maneira de fazer isso é com um mecanismo de "cópia na gravação". Se o seu manipulador de propriedades usar um fluxo para acessar um arquivo, você obterá esse comportamento automaticamente; o sistema grava todas as alterações no fluxo, substituindo o arquivo pela nova cópia somente durante a operação de confirmação.

Para substituir esse comportamento e controlar o processo de salvamento de arquivos manualmente, você pode recusar o comportamento de salvamento seguro definindo o valor ManualSafeSave na entrada do registro do manipulador, conforme ilustrado aqui.

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

Quando um manipulador Especifica o valor de ManualSafeSave, o fluxo com o qual ele é inicializado não é um fluxo transacionado (STGM \_ transacionado). O próprio manipulador deve implementar a função de salvamento seguro para garantir que o arquivo não seja corrompido se a operação de salvamento for interrompida. Se o manipulador implementar a gravação in-loco, ele gravará no fluxo que ele recebeu. Se o manipulador não oferecer suporte a esse recurso, ele deverá recuperar um fluxo com o qual gravar a cópia atualizada do arquivo usando [**IDestinationStreamFactory:: GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream). Depois que o manipulador terminar a gravação, ele deverá chamar [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) no fluxo original para concluir a operação e substituir o conteúdo do fluxo original pela nova cópia do arquivo.

ManualSafeSave também será a situação padrão se você não inicializar o manipulador com um fluxo. Sem um fluxo original para receber o conteúdo do fluxo temporário, você deve usar o [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) para executar uma substituição atômica do arquivo de origem.

Formatos de arquivo grandes que serão usados de forma que produza arquivos maiores que 1 MB devem implementar o suporte para a gravação de propriedades in-loco; caso contrário, o comportamento de desempenho não atende às expectativas dos clientes do sistema de propriedades. Nesse cenário, o tempo necessário para gravar propriedades não deve ser afetado pelo tamanho do arquivo.

Para arquivos muito grandes, por exemplo, um arquivo de vídeo de 1 GB ou mais, uma solução diferente é necessária. Se não houver espaço suficiente no arquivo para executar a gravação in-loco, o manipulador poderá falhar na atualização da propriedade se a quantidade de espaço reservado para gravação de propriedades in-loco tiver sido esgotada. Essa falha ocorre para evitar o mau desempenho resultante de 2 GB de e/s (1 para ler, 1 para gravar). Devido a essa falha em potencial, esses formatos de arquivo devem reservar espaço suficiente para a gravação de propriedades in-loco.

Se o arquivo tiver espaço suficiente em seu cabeçalho para gravar metadados e se a gravação desses metadados não fizer com que o arquivo aumente ou diminua, talvez seja seguro gravar no local. Recomendamos 64 KB como ponto de partida. Gravar no local é equivalente ao manipulador solicitando ManualSafeSave e chamando [**IStream:: Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) na implementação de [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))e tem um desempenho muito melhor do que a cópia em gravação. Se o tamanho do arquivo for alterado devido a alterações no valor da propriedade, a gravação in-loco não deve ser tentada devido ao potencial de um arquivo corrompido no caso de um encerramento anormal.

> [!Note]  
> Por motivos de desempenho, recomendamos que a opção ManualSafeSave seja usada com manipuladores de propriedade que trabalham com arquivos que são 100 KB ou maiores.

 

Conforme ilustrado na implementação de exemplo a seguir de [**IPropertyStore:: Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), o manipulador para ManualSafeSave é registrado para ilustrar a opção de salvamento seguro manual. O método **\_ SaveCacheToDom** grava os valores de propriedade armazenados no cache na memória para o objeto XMLdocument.


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



Em seguida, pergunte se o pecificada dá suporte a [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



Em seguida, confirme o fluxo original, que grava os dados de volta no arquivo original de maneira segura.


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



Em seguida, examine a implementação de **\_ SaveCacheToDom** .


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



Em seguida, obtenha o número de propriedades armazenadas no cache na memória.


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



Agora, itere pelas propriedades para determinar se o valor de uma propriedade foi alterado desde que foi carregado na memória.


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



O método [**IPropertyStoreCache:: GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) Obtém o estado da propriedade no cache. O \_ sinalizador incorreto do PSC, que foi definido na implementação [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) , marca uma propriedade como alterada.


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



Mapeie a propriedade para o nó XML, conforme especificado na matriz de **exemplo \_ rgPropertyMap** .


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



Se uma propriedade não estiver no mapa, ela será uma nova propriedade que foi definida pelo Windows Explorer. Como há suporte para metadados abertos, salve a nova propriedade na seção **ExtendedProperties** do XML.


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a>Implementando IPropertyStoreCapabilities

[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informa a interface do usuário do Shell se uma determinada propriedade pode ser editada na interface do usuário do Shell. É importante observar que isso se refere apenas à capacidade de editar a propriedade na interface do usuário, não se você pode chamar [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) com êxito na propriedade. Uma propriedade que provokes um valor de retorno de S \_ false de [**IPropertyStoreCapabilities:: IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) ainda pode ser capaz de ser definida por meio de um aplicativo.


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) retorna **S \_ OK** para indicar que os usuários finais devem ter permissão para editar a propriedade diretamente; S \_ false indica que eles não deveriam. \_O falso pode significar que os aplicativos são responsáveis por gravar a propriedade, não pelos usuários. O Shell desabilita os controles de edição conforme apropriado, com base nos resultados de chamadas para esse método. Um manipulador que não implementa [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) é considerado para dar suporte a metadados abertos por meio do suporte para a gravação de qualquer propriedade.

Se você estiver criando um manipulador que manipula somente as propriedades somente leitura, deverá implementar o método **Initialize** ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)ou [**IINITIALIZEWITHFILE**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) para que ele retorne STG \_ E \_ ACCESSDENIED quando chamado com o sinalizador de STGM \_ ReadWrite.

Algumas propriedades têm seu atributo [isInnate](./propdesc-schema-typeinfo.md) definido como **true**. As propriedades inato têm as seguintes características:

-   A propriedade geralmente é calculada de alguma forma. Por exemplo, `System.Image.BitDepth` é calculado a partir da própria imagem.
-   A alteração da propriedade não faz sentido sem alterar o arquivo. Por exemplo, `System.Image.Dimensions` a alteração não redimensionaria a imagem, portanto, não faz sentido permitir que o usuário a altere.
-   Em alguns casos, essas propriedades são fornecidas automaticamente pelo sistema. Os exemplos incluem `System.DateModified` , que é fornecido pelo sistema de arquivos, e `System.SharedWith` , que se baseia em quem o usuário está compartilhando o arquivo.

Devido a essas características, as propriedades marcadas como *IsInnate* são fornecidas ao usuário na interface de usuário do Shell somente como propriedades somente leitura. Se uma propriedade estiver marcada como *IsInnate*, o sistema de propriedades não armazenará essa propriedade no manipulador de propriedades. Portanto, os manipuladores de propriedade não precisam de código especial para considerar essas propriedades em suas implementações. Se o valor do atributo *IsInnate* não for explicitamente declarado para uma determinada propriedade, o valor padrão será **false**.

## <a name="registering-and-distributing-property-handlers"></a>Registrando e distribuindo manipuladores de propriedade

Com o manipulador de propriedade implementado, ele deve ser registrado e sua extensão de nome de arquivo associada ao manipulador. Para obter mais informações, consulte [registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre manipuladores de propriedade](./building-property-handlers-properties.md)
</dt> <dt>

[Usando nomes de tipos](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
