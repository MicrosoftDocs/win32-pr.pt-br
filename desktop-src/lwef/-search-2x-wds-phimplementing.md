---
title: Implementando um manipulador de protocolo para o WDS
description: A criação de um manipulador de protocolo envolve a implementação de ISearchProtocol para gerenciar objetos UrlAccessor, IUrlAccessor para gerar metadados sobre e identificar os filtros apropriados para os itens no armazenamento de dados, IProtocolHandlerSite para instanciar um objeto SearchProtocol e identificar os filtros apropriados e IFilterto filtrar arquivos proprietários ou enumerar e filtrar arquivos armazenados hierarquicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084492"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implementando um manipulador de protocolo para o WDS

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

A criação de um manipulador de protocolo envolve a implementação de [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) para gerenciar objetos UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) para gerar metadados sobre e identificar os filtros apropriados para os itens no armazenamento de dados, IProtocolHandlerSite para instanciar um objeto SearchProtocol e identificar os filtros apropriados e o [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para filtrar arquivos proprietários ou para enumerar e filtrar arquivos armazenados hierarquicamente. O manipulador de protocolo deve ser multithread.

Estas seções contêm os seguintes tópicos:

-   [Observação sobre URLs](#note-on-urls)
-   [Interfaces de manipulador de protocolo](#protocol-handler-interfaces)
-   [IFilters para contêineres](#ifilters-for-containers)
-   [Adicionando funcionalidade de opções de manipulador de protocolo](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [Tópicos relacionados](#related-topics)

## <a name="note-on-urls"></a>Observação sobre URLs

O Microsoft Windows Desktop Search (WDS) usa URLs para identificar exclusivamente os itens em um sistema de arquivos, dentro de uma loja do tipo banco de dados ou na Web. Uma URL que define um nó de entrada é chamada de página inicial; O WDS começa nessa página inicial e rastreia recursivamente o armazenamento de dados. A estrutura de URL típica é:

`protocol://host/path/name.extension`

> [!Note]
>
> Quando desejar adicionar um novo armazenamento de dados, você precisará selecionar um nome para identificá-lo que não entre em conflito com os atuais. Recomendamos esta Convenção de nomenclatura: companyName. Scheme.

 

## <a name="protocol-handler-interfaces"></a>Interfaces de manipulador de protocolo

**ISearchProtocol**

A interface [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) invoca, inicializa e gerencia objetos UrlAccessor. Para obter mais informações sobre como implementar a interface ISearchProtocol, consulte **referência de interface ISearchProtocol**.

**IUrlAccessor**

Para uma URL especificada, a interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) gera metadados sobre a estrutura de local, bem como itens contidos, e vincula esses itens a um filtro. O objeto **IUrlAccessor** é instanciado e inicializado por um objeto SearchProtocol; no entanto, você também pode implementar um método de inicialização interno para que o objeto **IUrlAccessor** possa executar tarefas de inicialização específicas para seu manipulador de protocolo, como validar a URL de um item que está sendo acessado ou verificar a hora da última modificação para determinar se um arquivo deve ser processado no rastreamento atual.

> [!Note]
>
> Os horários modificados para diretórios são ignorados. O objeto [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) deve enumerar os objetos filho para determinar se houve modificações ou exclusões.

 

Grande parte do design do objeto **UrlAccessor** depende se a estrutura é hierárquica ou baseada em link. Para armazenamentos de dados hierárquicos, o objeto **UrlAccessor** deve encontrar um filtro que possa enumerar seu conteúdo. Outra distinção entre os manipuladores de protocolo hierárquico e baseado em link é o uso do método IsDirectory. Em manipuladores de protocolo baseado em link, esse método deve retornar S \_ false. Os manipuladores de protocolo hierárquicos devem retornar S \_ OK para contêineres.

Para obter mais instruções sobre como implementar uma interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , consulte a referência da [**Interface IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .

**IProtocolHandlerSite**

Essa interface é usada para criar uma instância de um objeto **SearchProtocol** e também fornece o objeto **UrlAccessor** com um filtro apropriado para uma ID de classe especificada (CLSID).

## <a name="ifilters-for-containers"></a>IFilters para contêineres

Se você estiver implementando um manipulador de protocolo hierárquico, deverá implementar um componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contêiner que enumere URLs que representam contêineres ou pastas. O processo de enumeração é um loop pelos métodos **GetChunk** e **GetValue** da interface IFilter que retornam uma lista de URLs que representam cada item no contêiner.

Primeiro, **GetChunk** retorna um FULLPROSPEC com o conjunto de propriedades coletar \_ propset e:

-   PID \_ GTHR \_ DIRLINK, a URL para o item sem a hora da última modificação ou
-   PID \_ GTHR \_ DIRLINK \_ com \_ tempo, a URL junto com a hora da última modificação

O GUID do conjunto de propriedades para coletar \_ propset é 0B63E343-9CCC-11D0-BCDB-00805FCCCE04. A propriedade PROPSPEC é PID \_ GTHR \_ DIRLINK = 2 ou PID \_ GTHR \_ DIRLINK \_ com \_ time = 12 decimal.

Retornar o PID \_ GTHR \_ DIRLINK \_ com \_ tempo é mais eficiente, pois o indexador pode determinar imediatamente se o item precisa ser indexado sem chamar os métodos ISearchProtocol->CreateUrlAccessor () e IUrlAccessor->GetLastModified ().

Em seguida, **GetValue** retorna um PROPVARIANT para a URL (e a hora da última modificação, se usado), como:

-   VT \_ LPWStr, a URL do item filho ou
-   Vetor da URL seguido por um FILETIME

O código de exemplo a seguir demonstra como criar o PID \_ GTHR \_ DIRLINK adequado \_ com \_ tempo.

> [!Note]
>
> **ESSE CÓDIGO E AS INFORMAÇÕES SÃO FORNECIDOS "NO ESTADO EM QUE SE ENCONTRAM", SEM GARANTIAS DE QUALQUER TIPO, EXPRESSAS OU IMPLÍCITAS, INCLUINDO, MAS NÃO SE LIMITANDO ÀS GARANTIAS IMPLÍCITAS DE COMERCIALIZAÇÃO E/OU ADEQUAÇÃO A UMA FINALIDADE ESPECÍFICA.**
>
> Copyright (C) Microsoft. Todos os direitos reservados.

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> Um componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)do contêiner sempre deve enumerar todas as URLs filho, mesmo que as URLs filho não tenham sido alteradas, pois o indexador detecta as exclusões por meio do processo de enumeração. Se a saída de data em um DIR \_ links \_ com o \_ tempo indicar que os dados não foram alterados, o indexador não atualizará os dados para essa URL.

 

A URL física é a URL que o objeto **UrlAccessor** processa. Se o filtro não emitir um DisplayUrl amigável para o usuário, o WDS exibirá a URL física para o usuário como parte dos resultados da pesquisa. O esquema do WDS contém duas propriedades para controlar o que é exibido para o usuário final, conforme mostrado na tabela a seguir.



| GUID                                 | PROPSPEC      | Descrição                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Caminho da pasta exibido para o usuário nos resultados da pesquisa |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Nome de exibição da pasta pai                   |



 

Se o seu código não emitir um DisplayFolder ou nome_da_pasta, esses valores serão computados a partir do DisplayUrl. As barras invertidas na URL denotam contêineres na loja ou no sistema de arquivos.

## <a name="adding-protocol-handler-options-functionality"></a>Adicionando funcionalidade de opções de manipulador de protocolo

Para que o manipulador de protocolo tenha uma página inicial padrão (e a URL do nó de entrada), você deve implementar a interface **ISearchProtocolOptions** . Em versões futuras do WDS, essa interface fornecerá ganchos para a caixa de diálogo de opções para uma experiência de usuário aprimorada. Essa interface fornece a seguinte funcionalidade:

-   Determina se os requisitos para seu manipulador de protocolo são atendidos. Por exemplo, o armazenamento do manipulador de protocolo pode exigir acesso a um determinado aplicativo para indexar corretamente os dados do aplicativo, mas esse aplicativo não está disponível.
-   Identifica os requisitos mínimos que seu manipulador de protocolo precisa para processar um item. Os requisitos podem ser expressos em uma descrição independente do usuário, localizada, como "Microsoft Outlook 2000 ou superior".
-   Define as URLs que seu manipulador de protocolo deve processar por padrão.

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

A tabela a seguir descreve os métodos que você precisa implementar para a interface **ISearchProtocolOptions** .



| Método               | Descrição                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | Determina se os requisitos mínimos de um manipulador de protocolo personalizado são atendidos                             |
| GetDefaultCrawlScope | Retorna uma lista de URLs padrão em um repositório especificado para um manipulador de protocolo personalizado                   |
| Getrequirements      | Identifica uma descrição independente do usuário e localizada de requisitos mínimos para um manipulador de protocolo personalizado |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Notificando o índice das alterações](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Adicionando ícones, visualizações e menus de contexto com extensões de Shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Instalando e Registrando manipuladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 