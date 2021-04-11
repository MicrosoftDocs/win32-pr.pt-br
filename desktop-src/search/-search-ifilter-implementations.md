---
description: A Microsoft fornece vários filtros padrão com o Windows Search. Os clientes chamam esses manipuladores de filtro (que são implementações da interface IFilter) para extrair texto e propriedades de um documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Manipuladores de filtro que acompanham o Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090080"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Manipuladores de filtro que acompanham o Windows

A Microsoft fornece vários filtros padrão com o Windows Search. Os clientes chamam esses manipuladores de filtro (que são implementações da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para extrair texto e propriedades de um documento.

Este tópico é organizado da seguinte maneira:

- [Notas de implementação da pesquisa do Windows](#windows-search-implementation-notes)
  - [Implementação do Windows 7 e 10](#windows-7-and-10-implementation)
  - [Implementação do Windows Vista](#windows-vista-implementation)
  - [Implementação herdada](#legacy-implementation)
- [Filtros de pesquisa do Windows](#filter-handlers-that-ship-with-windows)
  - [Manipulador de filtro MIME](#mime-filter-handler)
  - [Manipulador de filtro HTML](#html-filter-handler)
  - [Manipulador de filtro de documento](#document-filter-handler)
  - [Manipulador de filtro de texto sem formatação](#plain-text-filter-handler)
  - [Manipulador de filtro binário ou nulo](#binary-or-null-filter-handler)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

## <a name="windows-search-implementation-notes"></a>Notas de implementação da pesquisa do Windows

No Windows 7 e posterior, os filtros gravados em código gerenciado são explicitamente bloqueados. Os filtros devem ser escritos em código nativo devido a possíveis problemas de controle de versão do CLR com o processo em que vários suplementos são executados.

### <a name="windows-7-and-10-implementation"></a>Implementação do Windows 7 e 10

No Windows 7 e posterior, há um novo comportamento que ocorre ao registrar um manipulador de filtro, um manipulador de propriedades ou uma nova extensão. Quando um manipulador de propriedades novo e/ou manipulador de filtro é instalado, os arquivos com as extensões correspondentes são reindexados automaticamente.

No Windows 7 e posterior, recomendamos que você instale um manipulador de filtro em conjunto com seus manipuladores de propriedade correspondentes e que registre o manipulador de filtro antes do manipulador de propriedade. O registro do manipulador de propriedades inicia a reindexação imediata de arquivos indexados anteriormente sem precisar primeiro de uma reinicialização e aproveita os manipuladores de filtro registrados anteriormente para fins de indexação de conteúdo.

Se apenas um manipulador de filtro for instalado sem um manipulador de propriedades correspondente, a reindexação automática ocorrerá após uma reinicialização do serviço de indexação ou uma reinicialização do sistema.

Para sinalizadores de descrição de propriedade específicos para o Windows 7, consulte os seguintes tópicos de referência: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC \_ COLUMNINDEX \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) e [PROPDESC \_ SEARCHINFO \_ flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Implementação do Windows Vista

No Windows Vista e versões anteriores, a instalação de um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou manipulador de propriedades não inicia uma reindexação de itens existentes, a menos que um ISV (fornecedor independente de software) chame explicitamente uma recompilação ou reindexação de URLs correspondentes.

Há duas diferenças principais entre aplicativos herdados, como serviço de indexação e aplicativos mais recentes, como o Windows Search, que você deve saber ao implementar filtros:

- Uso da interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .
- Uso de manipuladores de propriedade.

Primeiro, o Windows Vista e o Windows Search 3,0 e posterior exigem que você use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pelos seguintes motivos:

- Para garantir o desempenho e a compatibilidade futura.
- Para ajudar a aumentar a segurança. Os filtros implementados com [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) são mais seguros porque o contexto no qual o filtro é executado não precisa dos direitos para abrir arquivos no disco ou pela rede.

Embora o Windows Search Use apenas [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), você também pode incluir a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e/ou implementações de [interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) em seus filtros para compatibilidade com versões anteriores.

A segunda grande diferença é que o Windows Vista e o Windows Search 3,0 e posterior têm um novo [sistema de propriedades](../properties/building-property-handlers.md) que usa manipuladores de propriedade para enumerar Propriedades de itens.

No entanto, há ocasiões em que você precisa implementar um filtro que lide com o conteúdo e as propriedades para:

- Suporte a implementações de MSSearch herdado.
- Atravessar links.
- Preservar informações de idioma.
- Filtrar itens inseridos recursivamente.

Nessas situações, você precisa de uma implementação completa de filtro, incluindo o método [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) para acessar os valores de propriedade.

### <a name="legacy-implementation"></a>Implementação herdada

Como observado anteriormente, o Windows Vista e o Windows Search incluem um novo sistema de propriedades que encapsula as propriedades de um item que é separado do conteúdo de um item. Este sistema de propriedades não existe em versões anteriores do Microsoft Windows Desktop Search (WDS) 2. x. Se o filtro precisar dar suporte a outros aplicativos, conforme descrito acima, talvez seja necessário lidar com o conteúdo e as propriedades.

Para obter mais informações sobre como desenvolver um filtro compatível, consulte os tópicos a seguir, [IFilter (para aplicativos herdados)](/windows/win32/api/filter/nn-filter-ifilter)e [desenvolvendo suplementos de filtro (para aplicativos herdados)](../lwef/-search-2x-wds-ifilteraddins.md).

## <a name="windows-search-filters"></a>Filtros de pesquisa do Windows

A Microsoft fornece vários filtros padrão com o Windows Search. O conteúdo da dll do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  é resumido na tabela a seguir. Clicar no nome de um manipulador de filtro leva você para a descrição dessa implementação do **IFilter** .

| Manipulador de filtro                                                  | Arquivos filtrados                              | DLL do IFilter  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Manipulador de filtro MIME](#mime-filter-handler)                     | MIME (Multipurpose Internet Mail Extension) | mimefilt.dll |
| [Manipulador de filtro HTML](#html-filter-handler)                     | HTML 3,0 ou anterior                         | nlhtml.dll   |
| [Manipulador de filtro de documento](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Manipulador de filtro de texto sem formatação](#plain-text-filter-handler)         | Arquivos de texto sem formatação – IFilter padrão          | query.dll    |
| [Manipulador de filtro binário ou nulo](#binary-or-null-filter-handler) | Arquivos binários-IFilter nulo                 | query.dll    |

### <a name="mime-filter-handler"></a>Manipulador de filtro MIME

O manipulador de filtro MIME (em mimefilt.dll) extrai informações de texto e propriedade de arquivos com as extensões. eml,. mht e. mhtml.

### <a name="html-filter-handler"></a>Manipulador de filtro HTML

O manipulador de filtro HTML (em nlhtml.dll) extrai informações de texto e propriedade da classe "htmlfiles" para que ela possa ser indexada pelo Windows Search. Para obter uma descrição da associação entre o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e o tipo de arquivo, consulte "localizando a DLL do IFilter para um arquivo" em [Registrando manipuladores de filtro](-search-ifilter-registering-filters.md).

Você pode usar o `META` recurso de marca de documentos HTML para transmitir solicitações de tratamento especial para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)HTML. `META` as marcas ocorrem próximo ao início de um arquivo HTML dentro das `HEAD ... /HEAD` marcas, conforme ilustrado no exemplo a seguir.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Algumas `META` marcas HTML são mapeadas automaticamente para valores bem conhecidos de conjunto de propriedades e ID de propriedade (PID)) para que as consultas nessas propriedades pesquisem o conteúdo mapeado. Alguns exemplos são listados na tabela a seguir. Para obter uma lista das propriedades do sistema que você pode usar para os formatos de arquivo, consulte [Propriedades definidas pelo sistema para formatos de arquivo personalizados](-shell-systemdefinedpropertiesforfileformats.md).

| Exemplo da propriedade                              | Mapeado para                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta name = "Author" content = "Ruth"             | A propriedade autor no conjunto de propriedades de informações resumidas.            |
| meta name = "Subject" content = "processamento de texto" | A propriedade Subject no conjunto de propriedades de informações resumidas.           |
| meta name = "palavras-chave" content = "fonts, serif"   | A Propriedade Keyword no conjunto de propriedades de informações resumidas.           |
| meta name = "MS. Category" content = "ficção"     | A propriedade Category no conjunto de propriedades informações de resumo do documento. |

Alguns recursos do [**IFILTER**](/windows/win32/api/filter/nn-filter-ifilter) HTML são listados na tabela a seguir.

[comment]: # (Esta tabela precisa ser HTML para que os exemplos sejam formatados corretamente)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarefa</th>
<th>Ação</th>
<th>Exemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Criando resumos especiais de arquivos</td>
<td>Use a <code>META NAME=&quot;DESCRIPTION&quot;...</code> marca para instruir o <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> a usar a cadeia de caracteres após a <code>CONTENT</code> palavra-chave como o resumo do documento.
<blockquote>
[!Note]<br />
O processo de filtragem pode gerar resumos para cada arquivo filtrado, cujo padrão é um conjunto de caracteres no início do arquivo.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Impedindo que arquivos individuais sejam filtrados</td>
<td>Adicione uma <code>meta name</code> marca ao arquivo.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Configurando o código de idioma para um arquivo (para garantir que o sistema escolha os arquivos de palavras de som e de ruído do idioma correto)</td>
<td>Adicione a seguinte <code>meta name</code> marcação ao arquivo, em que o campo de conteúdo especifica o código de idioma apropriado (em caracteres ou usando o valor de localidade).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a>Manipulador de filtro de documento

O manipulador de filtro de documento (no offilt.dll) filtra arquivos para algumas extensões de documentos no Microsoft Office. Isso inclui arquivos com extensões. doc,. mdb,. ppt e. xlt, por exemplo.

### <a name="plain-text-filter-handler"></a>Manipulador de filtro de texto sem formatação

Para arquivos de texto sem formatação, o Windows Search usa o manipulador de filtro de texto, que filtra as propriedades do sistema (como nomes de arquivo) e o conteúdo de um arquivo. Quando um tipo de arquivo não tem uma associação de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no registro, o Windows Search indexa apenas as propriedades do Shell para o arquivo. No entanto, o usuário pode usar as **Opções avançadas** no painel de controle de **Opções de indexação** para **indexar Propriedades** ou **indexar Propriedades e conteúdo do arquivo**.

![captura de tela mostrando a caixa de diálogo Opções avançadas](images/ifilteradvancedoptions.png)

Se o usuário escolher essa opção para um tipo de arquivo sem um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associado, o manipulador de filtro de texto será usado para extrair o conteúdo do arquivo. O manipulador de filtro de texto não "entende" nenhum formato de documento; ao filtrar o conteúdo de um arquivo, ele trata o arquivo como uma sequência de caracteres. Ele verifica a marca de ordem de byte Unicode no início do arquivo.

### <a name="binary-or-null-filter-handler"></a>Manipulador de filtro binário ou nulo

Quando um arquivo binário registrado é encontrado, o manipulador de filtro nulo é usado. O manipulador de filtro nulo recupera apenas as propriedades do sistema. O conteúdo de um arquivo binário não é filtrado. Exemplos de propriedades do sistema são **filename**, **LastWriteTime**, **filesize** e **Attributes**.

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[Sobre manipuladores de filtro no Windows Search](-search-ifilter-about.md)

[Práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)

[Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)

[Implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md)

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)
