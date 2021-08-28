---
description: O Microsoft Windows Search usa manipuladores de propriedades para extrair os valores de propriedades de itens e usa o esquema do sistema de propriedades para determinar como uma propriedade específica deve ser indexada.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Desenvolvendo manipuladores de propriedades para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3933353d8bf00c3a68a2259daf94a1ce4f13d295
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627318"
---
# <a name="developing-property-handlers-for-windows-search"></a>Desenvolvendo manipuladores de propriedades para Windows Search

O Microsoft Windows Search usa manipuladores de propriedades para extrair os valores de propriedades de itens e usa o esquema do sistema de propriedades para determinar como uma propriedade específica deve ser indexada. Para ler e indexar valores de propriedade, os manipuladores de propriedades são invocados fora do processo pelo Windows Search para melhorar a segurança e a robustez. Por outro lado, os manipuladores de propriedades são invocados em processo Windows Explorer para ler e gravar valores de propriedade.

Este tópico complementa o tópico [Sistema de Propriedades](../properties/building-property-handlers.md) com informações específicas Windows Search e contém as seguintes seções:

-   [Decisões de design para manipuladores de propriedades](#design-decisions-for-property-handlers)
    -   [Decisões de propriedade](#property-decisions)
    -   [Suporte de texto completo](#full-text-support)
    -   [Considerações sobre a implementação do sistema operacional](#operating-system-implementatation-considerations)
-   [Escrevendo arquivos de descrição da propriedade](#writing-property-description-files)
-   [Implementando manipuladores de propriedade](#implementing-property-handlers)
    -   [Iinitializewithstream](#iinitializewithstream)
    -   [Ipropertystore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [Garantir que seus itens são indexados](#ensuring-your-items-get-indexed)
-   [Instalando e registrando manipuladores de propriedade](#installing-and-registering-property-handlers)
-   [Testando e solucionando problemas de manipuladores de propriedade](#testing-and-troubleshooting-property-handlers)
    -   [Testes de instalação e instalação](#installation-and-setup-tests)
    -   [Solucionando problemas de manipuladores de propriedade](#troubleshooting-property-handlers)
-   [Usando manipuladores System-Supplied propriedades](#using-system-supplied-property-handlers)
-   [Tópicos relacionados](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Decisões de design para manipuladores de propriedades

A implementação de manipuladores de propriedades envolve as seguintes etapas:

1.  Tomar decisões de design sobre as propriedades que você deseja dar suporte.
2.  Criando um arquivo de Descrição da Propriedade (.propdesc) para propriedades que ainda não estão no sistema de propriedades.
3.  Implementando e testando o manipulador de propriedades.
4.  Instalando e registrando o manipulador de propriedades e os arquivos de descrição da propriedade.
5.  Testar a instalação e o registro do manipulador de propriedades.

Antes de começar, você precisa considerar as seguintes perguntas de design:

-   Quais propriedades o formato de arquivo deve dar suporte?
-   Essas propriedades já estão no esquema do sistema?
-   Posso usar um manipulador de propriedades fornecido pelo sistema existente?
-   Quais propriedades podem ser exibidas aos usuários finais?
-   Quais propriedades os usuários podem editar?
-   O suporte para pesquisa de texto completo deve vir de um manipulador de propriedades ou de um filtro?
-   Preciso dar suporte a aplicativos herdáveis? Se sim, o que implemento?

> [!Note]  
> Antes de continuar, consulte [Usando manipuladores](#using-system-supplied-property-handlers) de System-Supplied para ver se você pode usar um manipulador de propriedades fornecido pelo sistema, economizando tempo e recursos de desenvolvimento.

 

Depois de tomar essas decisões, você pode escrever descrições formais de suas propriedades personalizadas para que o mecanismo Windows Search possa começar a indexar seus arquivos e propriedades. Essas descrições formais são arquivos XML, descritos em [Esquema de Descrição da Propriedade](/previous-versions//cc144127(v=vs.85)).

### <a name="property-decisions"></a>Decisões de propriedade

Ao considerar quais propriedades dar suporte, você deve identificar as necessidades de indexação e pesquisa dos usuários. Por exemplo, você pode identificar centenas de propriedades potencialmente úteis para seu tipo de arquivo, mas os usuários podem estar interessados em pesquisar apenas algumas. Além disso, talvez você queira exibir um grupo diferente, maior ou menor, dessas propriedades para os usuários no Windows Explorer e permitir que os usuários editem apenas um subconjunto dessas propriedades exibidas.

O tipo de arquivo pode dar suporte a todas as propriedades personalizadas que você definir, bem como a um conjunto de propriedades definidas pelo sistema. Antes de criar uma propriedade [](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) personalizada, revise Propriedades do Sistema para ver se a propriedade que você deseja dar suporte já está definida por uma propriedade do sistema. Sempre certifique-se de dar suporte às propriedades definidas pelo sistema mais importantes.

É recomendável usar uma matriz para ajudá-lo a criar suas propriedades:



| Nome da propriedade | É indexável? | É exibivel? | É editável? |
|---------------|---------------|-----------------|--------------|
| {1&gt;property&lt;1}{2&gt;1&lt;2}     | S             | S               | N            |
| Propriedade...   | S             | S               | N            |
| propertyn     | N             | N               | N            |



 

Para cada uma dessas propriedades, você precisa determinar quais atributos ela deve ter e, em seguida, descrevê-los formalmente em arquivos XML de Descrição da Propriedade (.propdesc). Os atributos incluem o tipo de dados da propriedade, rótulo, cadeia de caracteres de ajuda e muito mais. Para propriedades indexáveis, você deve prestar atenção especial aos seguintes atributos de propriedade encontrados no elemento [XML searchInfo](../properties/propdesc-schema-searchinfo.md)   do arquivo Descrição da Propriedade.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Opcional. Indica se um valor da propriedade de cadeia de caracteres deve ser dividido em palavras e cada palavra armazenada no índice invertido. O índice invertido permite a pesquisa eficiente de palavras e frases sobre o valor da propriedade usando CONTAINS ou FREETEXT (por exemplo, SELECT... WHERE CONTAINS &quot; sometext &quot; ). Se definido como <strong>FALSE,</strong>as pesquisas serão feitas em relação à cadeia de caracteres inteira. A maioria das propriedades de cadeia de caracteres deve ter esse conjunto definido como <strong>TRUE;</strong> propriedades que não são cadeias de caracteres devem ter esse conjunto definido como <strong>FALSE.</strong> O padrão é <strong>FALSE.</strong></td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Opcional. Indica se a propriedade deve ser armazenada no banco de dados Windows Search como uma coluna. O armazenamento da propriedade como uma coluna permite recuperar, classificar, agrupar e filtrar (ou seja, usando qualquer predicado, exceto CONTAINS ou FREETEXT) no valor inteiro da coluna. As propriedades exibidas para o usuário devem ter esse conjunto definido como <strong>TRUE,</strong> a menos que seja uma propriedade textual muito grande (como o corpo de um documento) que seria pesquisada no índice invertido. O padrão é <strong>FALSE.</strong></td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Opcional. Indica se uma propriedade não ocupa espaço se o valor é <strong>NULL.</strong> Uma propriedade não esparsa ocupa espaço para cada item, mesmo que o valor seja <strong>NULL.</strong> Se a propriedade tiver vários valores, esse atributo será sempre <strong>TRUE.</strong> Esse atributo deverá ser <strong>FALSE</strong> somente se um valor estiver presente para cada item. O padrão é <strong>TRUE.</strong></td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Opcional. Para otimizar a consulta, o mecanismo Windows Search pode criar índices secundários para propriedades que têm isColumn=<strong>TRUE.</strong> Isso requer mais processamento e espaço em disco durante a indexação, mas melhora o desempenho durante a consulta. Se a propriedade tende a ser classificação, agrupada ou filtrada (ou seja, usando =, !=, <, >, LIKE, MATCHES) com frequência pelos usuários, esse atributo deverá ser definido como &quot; OnDisk &quot; . O padrão é &quot; NotIndexed. &quot; Os seguintes valores são válidos:
<ul>
<li>NotIndexed: nenhum índice secundário é criado.</li>
<li>OnDisk: crie e armazene um índice secundário no disco.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maxsize</td>
<td>Opcional. Indica o tamanho máximo permitido para o valor da propriedade armazenado no banco de dados Windows pesquisa. Esse limite se aplica aos elementos indvidual de um vetor, não ao vetor como um todo. Valores além desse tamanho são truncados. O padrão é &quot; 128 &quot; (bytes).<br/> Atualmente, Windows Search não usa o maxSize ao calcular a quantidade de dados que ele aceita de um arquivo. Em vez disso, o limite que o Windows Search usa é o produto do tamanho do arquivo e o MaxGrowFactor (tamanho do arquivo N * MaxGrowFactor) lido do Registro em HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor. O MaxGrowFactor padrão é quatro (4). Consequentemente, se o tipo de arquivo tende a ser pequeno em tamanho total, mas tem propriedades maiores, o Windows Search pode não aceitar todos os dados de propriedade que você deseja emitir. No entanto, você pode aumentar o MaxGrowFactor para atender às suas necessidades. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Para o atributo columnIndexType, o benefício de consultas mais rápidas precisa ser ponderado em relação ao maior tempo de indexação e custos de espaço que os índices secundários podem incorrer. No entanto, esse custo é pago apenas por itens que têm um valor não nulo, portanto, para a maioria das propriedades pode ter esse atributo definido como "OnDisk".

 

### <a name="full-text-support"></a>Suporte de texto completo

Em termos gerais, a pesquisa de texto completo é suportada por componentes chamados [filtros](-search-3x-wds-extidx-filters.md); no entanto, para tipos de arquivo baseados em texto com formatos de arquivo nãocomplicados, os manipuladores de propriedades podem fornecer essa funcionalidade com menos esforço de desenvolvimento. Você deve revisar a seção Conteúdo de Texto Completo para ver uma comparação da funcionalidade do manipulador de propriedades e filtro para [ajudá-lo](../properties/building-property-handlers-property-handlers.md) a decidir o que é melhor para o tipo de arquivo. De particular importância é o fato de que os filtros podem lidar com vários LCIDs (identificadores de código de idioma) por arquivo, enquanto os manipuladores de propriedade não podem.

> [!Note]  
> Como os manipuladores de propriedades não podem fazer a parte do conteúdo da maneira como os filtros podem, arquivos grandes (mesmo que sejam formatos de arquivo nãocomplicados) devem ser completamente carregados na memória.

 

### <a name="operating-system-implementatation-considerations"></a>Considerações sobre a implementação do sistema operacional

### <a name="implementation-information-for-windows-7"></a>Informações de implementação para Windows 7

No Windows 7 e posterior, há um novo comportamento ao registrar um manipulador de propriedades, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)ou nova extensão. Quando um novo manipulador de propriedades e/ou **IFilter** é instalado, os arquivos com as extensões correspondentes são automaticamente reindexados.

No Windows 7, é recomendável que um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) seja instalado em conjunto com seus manipuladores de propriedades correspondentes e que o **IFilter** seja registrado antes do manipulador de propriedades. O registro do manipulador de propriedades inicia a re indexação imediata de arquivos indexados anteriormente sem primeiro exigir uma reinicialização e aproveita os IFilters registrados anteriormente para fins de indexação de conteúdo.

Se apenas um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) estiver instalado, sem um manipulador de propriedades correspondente, a reindexação automática ocorrerá após uma reinicialização do serviço de indexação ou uma reinicialização do sistema.

Para sinalizadores de descrição de propriedade específicos Windows 7, consulte os seguintes tópicos de referência:

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [TIPO PROPDESC \_ \_ COLUMNINDEX](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [SINALIZADORES \_ DE PROPDESC SEARCHINFO \_](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Informações de implementação para Windows Vista e Anterior

Antes do Windows Vista, os filtros da daam suporte para analisar e enumerar o conteúdo e as propriedades do arquivo. Com a introdução do sistema de propriedades, os manipuladores de propriedades lidam com propriedades de arquivo enquanto os filtros lidam com o conteúdo do arquivo. Por Windows Vista, você precisa desenvolver apenas uma implementação parcial da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)em coordenação com um manipulador de propriedades, conforme descrito em Práticas [recomendadas](-search-3x-wds-extidx-filters.md)para criar manipuladores de filtro no Windows Search .

Embora o sistema de propriedades também seja incluído na instalação do Windows Search para o Windows XP, aplicativos de terceiros e herdados podem exigir que os filtros lidam com conteúdo e propriedades. Portanto, se você estiver desenvolvendo na plataforma Windows XP, deverá fornecer uma implementação de filtro completo, bem como um manipulador de propriedades para seu tipo de arquivo ou propriedade personalizada.

 

## <a name="writing-property-description-files"></a>Escrevendo arquivos de descrição da propriedade

A estrutura de arquivos XML de descrição da propriedade (.propdesc) é descrita no [tópico propertyDescription.](../properties/propdesc-schema-propertydescription.md) De interesse específico para a pesquisa são os atributos do [elemento searchInfo.](../properties/propdesc-schema-searchinfo.md) Depois de decidir quais propriedades dar suporte, você precisará criar e registrar arquivos de descrição de propriedade para cada propriedade. Quando você registra seus arquivos .propdesc, eles são incluídos na lista de descrições de propriedade do esquema e se tornam nomes de coluna no armazenamento de propriedades do mecanismo de pesquisa.

Você pode registrar suas descrições de propriedade personalizadas usando a função [PSRegisterPropertySchema,](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) uma API de wrapper que chama iPropertySystem::RegisterPropertySchema do subsistema de esquema. Essa função informa o subsistema de esquema da adição de arquivos de esquema de descrição da propriedade (.propdesc), usando caminhos de arquivo para os arquivos .propdesc no computador local, geralmente o diretório de instalação do aplicativo em "Arquivos de Programas". Normalmente, uma instalação ou aplicativo (por exemplo, o instalador do manipulador de propriedades) chamará esse método depois de instalar os arquivos .propdesc.

 

## <a name="implementing-property-handlers"></a>Implementando manipuladores de propriedade

O desenvolvimento de um manipulador de propriedades envolve a implementação das seguintes interfaces:

-   IInitialzeWithStream: fornece inicialização baseada em fluxo do manipulador de propriedades.
-   IPropertyStore: enumera, obtém e define valores de propriedade.
-   IPropertyStoreCapabilities: opcional. Identifica se os usuários podem editar uma propriedade de uma interface do usuário.

### <a name="iinitializewithstream"></a>Iinitializewithstream

Conforme descrito no tópico [Sistema de Propriedades,](../properties/building-property-handlers.md) é recomendável implementar manipuladores de propriedade com **IInitializeWithStream** para fazer a inicialização baseada em fluxo. Se você optar por não implementar IInitializeWithStream, o manipulador de propriedades deverá não executar no processo de isolamento definindo o sinalizador DisableProcessIsolation na chave do Registro do manipulador de propriedades. A desabilitação do isolamento do processo geralmente destina-se apenas a manipuladores de propriedade herdados e deve ser evitada de forma monótona por qualquer novo código.

### <a name="ipropertystore"></a>Ipropertystore

Para criar um manipulador de propriedades, você deve implementar a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) com os métodos a seguir.



| Método   | Descrição                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Salva uma alteração de propriedade no arquivo.                                |
| Getat    | Recupera uma chave de propriedade da matriz de propriedades de um item.        |
| GetCount | Obtém o número de propriedades anexadas ao arquivo.                 |
| GetValue | Recupera dados para uma propriedade específica.                             |
| SetValue | Define um novo valor da propriedade ou substitui ou remove um valor existente. |



 

 

 

Considerações importantes para implementar essa interface estão incluídas na [**documentação do IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

> [!Note]  
> Se o manipulador de propriedades emitir vários valores para a mesma propriedade para um determinado item, somente o último valor emitido será armazenado no catálogo.

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

Os manipuladores de propriedades podem, opcionalmente, implementar essa interface para desabilitar a capacidade do usuário de editar propriedades específicas. Essas propriedades normalmente são editáveis na página e no painel Detalhes, mas editá-las não é permitida no manipulador de propriedades de implementação. Implementar essa interface corretamente fornece uma melhor experiência do usuário do que a alternativa, um erro de tempo de execução simples do Shell.

 

## <a name="ensuring-your-items-get-indexed"></a>Garantir que seus itens são indexados

Agora que você implementou o manipulador de propriedades, você deseja garantir que os itens que seu manipulador está registrado para são indexados. Você pode [](-search-3x-wds-mngidx-catalog-manager.md) usar o Gerenciador de Catálogo para iniciar a re indexação e também pode usar o [Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md) para configurar regras padrão indicando as URLs que você deseja que o Indexador rastreamento. Outra opção é seguir o exemplo de código ReIndex [nas amostras do SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)Windows Search.

Para obter mais informações, consulte [Usando o Gerenciador de Catálogo e](-search-3x-wds-mngidx-catalog-manager.md) Usando o [Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Instalando e registrando manipuladores de propriedade

Com o manipulador de propriedades implementado, ele deve ser registrado e sua extensão de nome de arquivo associada ao manipulador. O exemplo a seguir mostra as chaves e os valores do Registro necessários para fazer isso.

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a>Testando e solucionando problemas de manipuladores de propriedade

A lista a seguir fornece conselhos sobre os tipos de testes que você deve executar:

-   Teste a saída de cada propriedade única com suporte pelo tipo de arquivo.
-   Use valores de propriedade grandes, por exemplo, use uma metatag grande em documentos HTML.
-   Verifique se o manipulador de propriedades não vaza os manipuladores de arquivos editando-os depois de obter a saída do manipulador de propriedades ou usando uma ferramenta como oh.exe antes e depois de enumerar as propriedades do arquivo.
-   Teste todos os tipos de arquivo associados ao manipulador de propriedades. Por exemplo, verifique se o filtro HTML funciona com .htm e .html de arquivo.
-   Teste com arquivos corrompidos. O manipulador de propriedades deve falhar normalmente.
-   Se um aplicativo dá suporte à criptografia, teste se o manipulador de propriedades não saída texto criptografado.
-   Se o manipulador de propriedades for compatível com a pesquisa de texto completo:
    -   Use vários caracteres Unicode especiais no conteúdo do arquivo e teste sua saída.
    -   Teste a manipulação de documentos muito grandes para garantir que o manipulador de propriedades funcione conforme o esperado.

### <a name="installation-and-setup-tests"></a>Testes de instalação e instalação

Por fim, você precisa testar suas rotinas de instalação e desinstalação.

-   A instalação deve se recuperar de instalações com falha (por exemplo, do cancelamento e, em seguida, da reinicialização da instalação).
-   A desinstalação deve excluir todos os arquivos associados ao manipulador de propriedades.
-   A desinstalação não deve excluir arquivos diferentes dos associados à instalação do manipulador de propriedades.
-   As chaves do Registro associadas ao manipulador de propriedades devem ser removidas quando desinstaladas.
-   A desinstalação deve funcionar mesmo que os arquivos sejam excluídos do diretório de instalação.

### <a name="troubleshooting-property-handlers"></a>Solucionando problemas de manipuladores de propriedade

Veja a seguir alguns erros comuns feitos ao desenvolver manipuladores de propriedade:

-   Instalando arquivos .propdesc ou DLLs em um diretório de usuário.
-   Registrar componentes usando caminhos relativos.
-   Registrar componentes em HKEY \_ CURRENT USER em vez de \_ HKEY LOCAL \_ \_ MACHINE.
-   Esquecer de definir DisableProcessIsolation para manipuladores que não são de fluxo.
-   Colocar o arquivo de teste em um local não agendado.

Se você estiver tendo problemas para fazer seu manipulador de propriedades trabalhar com o indexador, aqui estão algumas dicas para ajudá-lo a solucionar problemas:

-   Verifique se suas descrições de propriedade (arquivos .propdesc) estão marcadas como isColumn="**true**", isViewable="**true**", e isQueryable="**true"** conforme apropriado.
-   Verifique se os arquivos .propdesc estão em um local global.
-   Verifique se você registrou seus arquivos .propdesc usando caminhos absolutos.
-   Verifique se o log de eventos não registrou nenhuma falha ao registrar o arquivo .propdesc.
-   Verifique se as DLLs estão em um local global (e não em seu perfil de usuário).
-   Verifique se as DLLs estão registradas em Classes de Software HKEY \_ LOCAL \_ \\ \\ MACHINE.
-   Verifique se as DLLs estão registradas usando caminhos completos (ou cadeias de caracteres SZ REG EXPAND que se expandem para caminhos absolutos usando variáveis de ambiente \_ \_ conhecidas pela conta do sistema).
-   Verifique se o manipulador de propriedades funciona no Windows Explorer.
-   Embora seja recomendável usar IInitializeWithStream, se você precisar usar IInitializeWithFile ou IInitializeWithItem, verifique se você especificou DisableProcessIsolation.
-   Verifique se as opções de indexação Painel de Controle o tipo de arquivo como um tipo de arquivo indexado.
-   Verifique se o arquivo de teste está em um local indexado.
-   Verifique se o arquivo de teste foi modificado desde que você instalou o manipulador de propriedades.

Se o arquivo de teste estiver em um local indexado e o indexador já tiver rastreado esse local, você precisará modificar o arquivo de alguma forma para disparar uma reindexação do arquivo.

 

## <a name="using-system-supplied-property-handlers"></a>Usando manipuladores System-Supplied propriedades

Windows inclui vários manipuladores de propriedade fornecidos pelo sistema que você poderá usar se o formato do tipo de arquivo for compatível. Se você definir uma nova extensão de arquivo que usa um desses formatos, poderá usar os manipuladores fornecidos pelo sistema registrando o CLSID (identificador de classe do manipulador) para sua extensão de arquivo.

Você pode usar o CLSID listado na tabela a seguir para registrar os manipuladores de propriedade fornecidos pelo sistema para o tipo de formato de arquivo.



| Formatar          | CLSID                                  |
|-----------------|----------------------------------------|
| OLE DocFile     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| Salvar XML do jogo   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| Manipulador XPS/OPC | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Antes de criar uma propriedade personalizada, você deve ter certeza de que não há uma propriedade definida pelo sistema que você possa usar. Você pode enumerar as propriedades definidas pelo sistema chamando [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) ou usando a prop.exe de linha de comando.

O esquema do sistema define como essas propriedades interagem com o indexador e você não pode alterar isso. Além disso, o aplicativo usado para criar, editar e salvar o tipo de arquivo também precisa estar em conformidade com determinado comportamento. Por exemplo, se o aplicativo implementar o safe save (pelo qual um arquivo temporário é criado durante a edição e, em seguida, ReplaceFile() for usado para trocar a nova versão para a antiga), ele deverá transferir todas as propriedades do arquivo original para o novo arquivo. Se não fizer isso, o arquivo perderá as propriedades adicionadas por usuários ou outros aplicativos.

 

**Exemplo**

O exemplo a seguir mostra o registro do manipulador OLE DocFile fornecido pelo sistema para um tipo de arquivo com um . Extensão OLEDocFile.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

O exemplo a seguir mostra o registro das informações da lista de propriedades para que as propriedades de . Os arquivos OLEDocFile são exibidos na guia e no painel Detalhes.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Mapeamentos de propriedade](-search-3x-wds-propertymappings.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Práticas recomendadas para criar manipuladores de filtro na Windows Search](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[O processo de indexação](-search-indexing-process-overview.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Propriedades definidas pelo sistema para formatos de arquivo personalizados](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Sistema de propriedades](../properties/building-property-handlers.md)
</dt> <dt>

[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Windows Pesquisar exemplos do SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
