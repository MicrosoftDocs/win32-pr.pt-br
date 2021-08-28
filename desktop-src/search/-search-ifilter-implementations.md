---
description: A Microsoft fornece vários filtros padrão com Windows Search. Os clientes chamam esses manipuladores de filtro (que são implementações da interface IFilter) para extrair texto e propriedades de um documento.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Manipuladores de filtros que são Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a245978482e0334d91e35031aa80186fd2cb32
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624362"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Manipuladores de filtros que são Windows

A Microsoft fornece vários filtros padrão com Windows Search. Os clientes chamam esses manipuladores de filtro (que são implementações da interface [**IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) para extrair texto e propriedades de um documento.

Este tópico é organizado da seguinte forma:

- [Windows Notas de implementação de pesquisa](#windows-search-implementation-notes)
  - [Windows implementação 7 e 10](#windows-7-and-10-implementation)
  - [Windows Implementação do Vista](#windows-vista-implementation)
  - [Implementação herdda](#legacy-implementation)
- [Windows Filtros de pesquisa](#filter-handlers-that-ship-with-windows)
  - [Manipulador de filtro MIME](#mime-filter-handler)
  - [Manipulador de filtro HTML](#html-filter-handler)
  - [Manipulador de filtro de documento](#document-filter-handler)
  - [Manipulador de filtro de texto sem-texto](#plain-text-filter-handler)
  - [Manipulador de filtro binário ou nulo](#binary-or-null-filter-handler)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

## <a name="windows-search-implementation-notes"></a>Windows Notas de implementação de pesquisa

No Windows 7 e posteriores, os filtros gravados em código gerenciado são explicitamente bloqueados. Os filtros DEVEM ser escritos em código nativo devido a possíveis problemas de versão do CLR com o processo em que vários complementos são executados.

### <a name="windows-7-and-10-implementation"></a>Windows implementação 7 e 10

No Windows 7 e posterior, há um novo comportamento que ocorre ao registrar um manipulador de filtros, um manipulador de propriedades ou uma nova extensão. Quando um novo manipulador de propriedades e/ou manipulador de filtro é instalado, os arquivos com as extensões correspondentes são automaticamente indexados.

No Windows 7 e posteriores, recomendamos que você instale um manipulador de filtro em conjunto com seus manipuladores de propriedades correspondentes e registre o manipulador de filtro antes do manipulador de propriedades. O registro do manipulador de propriedades inicia a re indexação imediata de arquivos indexados anteriormente sem primeiro exigir uma reinicialização e aproveita os manipuladores de filtro registrados anteriormente para fins de indexação de conteúdo.

Se apenas um manipulador de filtros for instalado sem um manipulador de propriedades correspondente, a rein indexação automática ocorrerá após uma reinicialização do serviço de indexação ou uma reinicialização do sistema.

Para obter sinalizadores de descrição de propriedade específicos Windows 7, consulte os seguintes tópicos de referência: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC \_ COLUMNINDEX \_ TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) e [PROPDESC \_ SEARCHINFO \_ FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Windows Implementação do Vista

No Windows Vista e anterior, a instalação de um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou manipulador de propriedades não inicia uma nova indexação de itens existentes, a menos que um ISV (fornecedor independente de software) chama explicitamente uma recomposição ou nova indexação de URLs correspondentes.

Há duas diferenças principais entre aplicativos herdados, como o Serviço de Indexação e aplicativos mais novos, como o Windows Search, que você deve estar ciente ao implementar filtros:

- Uso da interface [IPersistStream.](/windows/win32/api/objidl/nn-objidl-ipersiststream)
- Uso de manipuladores de propriedade.

Primeiro, Windows Vista e Windows Search 3.0 e posterior exigem que você use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pelos seguintes motivos:

- Para garantir o desempenho e a compatibilidade futura.
- Para ajudar a aumentar a segurança. Os filtros implementados com [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) são mais seguros porque o contexto no qual o filtro é executado não precisa dos direitos para abrir arquivos no disco ou pela rede.

Embora Windows Search use apenas [IPersistStream,](/windows/win32/api/objidl/nn-objidl-ipersiststream)você também pode incluir implementações da Interface IPersistFile e/ou [interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) em seus filtros para compatibilidade com o [IPersist.](/windows/win32/api/objidl/nn-objidl-ipersistfile)

A segunda grande diferença é que Windows Vista e Windows Search 3.0 [](../properties/building-property-handlers.md) e posteriores têm um novo Sistema de Propriedades que usa manipuladores de propriedades para enumerar propriedades de itens.

No entanto, há ocasiões em que você precisa implementar um filtro que trata o conteúdo e as propriedades para:

- Suporte a implementações herddas do MSSearch.
- Percorrer links.
- Preservar informações de idioma.
- Filtrar itens inseridos recursivamente.

Nessas situações, você precisa de uma implementação de filtro completo, incluindo o [**método IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) para acessar valores de propriedade.

### <a name="legacy-implementation"></a>Implementação herdda

Conforme visto anteriormente, Windows Vista e Windows Search incluem um novo sistema de propriedades que encapsula as propriedades de um item separado do conteúdo de um item. Esse sistema de propriedades não existe em versões anteriores do Microsoft Windows WDS (Desktop Search) 2.x. Se o filtro precisar dar suporte a outros aplicativos, conforme descrito acima, talvez seja necessário lidar com o conteúdo e as propriedades.

Para obter mais informações sobre como desenvolver um filtro compatível, consulte os tópicos a seguir, [IFilter (para](/windows/win32/api/filter/nn-filter-ifilter)aplicativos herdáveis) e Desenvolvendo complementos de filtro [(para aplicativos herdáveis).](../lwef/-search-2x-wds-ifilteraddins.md)

## <a name="windows-search-filters"></a>Windows Filtros de pesquisa

A Microsoft fornece vários filtros padrão com Windows Search. O conteúdo da DLL de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  é resumido na tabela a seguir. Clicar no nome de um manipulador de filtro leva você para a descrição dessa implementação **de IFilter.**

| Manipulador de filtro                                                  | Arquivos filtrados                              | IFilter DLL  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Manipulador de filtro MIME](#mime-filter-handler)                     | MIME (Extensão multipropósico do Internet Mail) | mimefilt.dll |
| [Manipulador de filtro HTML](#html-filter-handler)                     | HTML 3.0 ou anterior                         | nlhtml.dll   |
| [Manipulador de filtro de documento](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Manipulador de filtro de texto sem-texto](#plain-text-filter-handler)         | Arquivos de texto sem-texto – IFilter padrão          | query.dll    |
| [Manipulador de filtro binário ou nulo](#binary-or-null-filter-handler) | Arquivos binários – IFilter nulo                 | query.dll    |

### <a name="mime-filter-handler"></a>Manipulador de filtro MIME

O manipulador de filtro MIME (em mimefilt.dll) extrai informações de texto e propriedade de arquivos com as extensões .eml, .mht e .mhtml.

### <a name="html-filter-handler"></a>Manipulador de filtro HTML

O manipulador de filtro HTML (em nlhtml.dll) extrai informações de texto e propriedade da classe "htmlfiles" para que ele possa ser indexado por Windows Search. Para ver uma descrição da associação entre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e o tipo de arquivo, consulte "Localizar a DLL de IFilter para um arquivo" em [Registrando manipuladores de filtro.](-search-ifilter-registering-filters.md)

Você pode usar o recurso `META` de marca de documentos HTML para transmitir solicitações de manipulação especiais para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)HTML. `META` As marcas ocorrem perto do início de um arquivo html dentro `HEAD ... /HEAD` das marcas, conforme ilustrado no exemplo a seguir.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Algumas marcas HTML são mapeadas automaticamente para valores de ID de propriedade (PID) e conjunto de propriedades conhecidos para que as consultas nessas propriedades pesquisem o conteúdo `META` mapeado. Alguns exemplos são listados na tabela a seguir. Para ver uma lista das propriedades do sistema que você pode usar para seus formatos de arquivo, consulte Propriedades definidas pelo sistema [para formatos de arquivo personalizados.](-shell-systemdefinedpropertiesforfileformats.md)

| Exemplo de propriedade                              | Mapeado para                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta name="author" content="rut"             | A propriedade author no conjunto de propriedades Informações resumidas.            |
| meta name="subject" content="word processing" | A propriedade subject no conjunto de propriedades Informações resumidas.           |
| meta name="keywords" content="fonts, serif"   | A propriedade de palavra-chave no conjunto de propriedades Informações resumidas.           |
| meta name="ms.category" content="filme"     | A propriedade category no conjunto de propriedades Informações de Resumo do documento. |

Alguns recursos do [**HTML IFilter**](/windows/win32/api/filter/nn-filter-ifilter) são listados na tabela a seguir.

[comment]: # (Essa tabela precisa ser HTML para que os exemplos sejam formatado corretamente)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Use a <code>META NAME=&quot;DESCRIPTION&quot;...</code> marca para instruir o <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter a</strong></a> usar a cadeia de caracteres após a <code>CONTENT</code> palavra-chave como o resumo do documento.
<blockquote>
[!Note]<br />
O processo de filtragem pode gerar resumos para cada arquivo filtrado, cujo padrão é um conjunto de caracteres no início do arquivo.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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
<col  />
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
<col  />
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

O manipulador de filtro de documento (no offilt.dll) filtra arquivos para algumas extensões de documentos no Microsoft Office. Isso inclui arquivos com as extensões .doc,. mdb, .ppt e. xlt, por exemplo.

### <a name="plain-text-filter-handler"></a>Manipulador de filtro de texto sem formatação

para arquivos de texto sem formatação, Windows pesquisa usa o manipulador de filtro de texto, que filtra as propriedades do sistema (como nomes de arquivo) e o conteúdo de um arquivo. quando um tipo de arquivo não tem uma associação de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no registro, Windows pesquisa indexa apenas as propriedades do Shell para o arquivo. No entanto, o usuário pode usar as **Opções avançadas** no painel de controle de **Opções de indexação** para **indexar Propriedades** ou **indexar Propriedades e conteúdo do arquivo**.

![captura de tela mostrando a caixa de diálogo Opções avançadas](images/ifilteradvancedoptions.png)

Se o usuário escolher essa opção para um tipo de arquivo sem um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associado, o manipulador de filtro de texto será usado para extrair o conteúdo do arquivo. O manipulador de filtro de texto não "entende" nenhum formato de documento; ao filtrar o conteúdo de um arquivo, ele trata o arquivo como uma sequência de caracteres. Ele verifica a marca de ordem de byte Unicode no início do arquivo.

### <a name="binary-or-null-filter-handler"></a>Manipulador de filtro binário ou nulo

Quando um arquivo binário registrado é encontrado, o manipulador de filtro nulo é usado. O manipulador de filtro nulo recupera apenas as propriedades do sistema. O conteúdo de um arquivo binário não é filtrado. Exemplos de propriedades do sistema são **filename**, **LastWriteTime**, **filesize** e **Attributes**.

## <a name="additional-resources"></a>Recursos adicionais

- o exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível em [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstra como criar uma classe base IFilter para implementar a interface [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[sobre manipuladores de filtro na pesquisa Windows](-search-ifilter-about.md)

[práticas recomendadas para a criação de manipuladores de filtro na pesquisa Windows](-search-3x-wds-extidx-filters.md)

[Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)

[implementando manipuladores de filtro na pesquisa Windows](-search-ifilter-constructing-filters.md)

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)
