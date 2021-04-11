---
description: O Microsoft Windows Search usa manipuladores de propriedade para extrair os valores de propriedades de itens e usa o esquema do sistema de propriedades para determinar como uma propriedade específica deve ser indexada.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Desenvolvendo manipuladores de propriedade para o Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164342"
---
# <a name="developing-property-handlers-for-windows-search"></a>Desenvolvendo manipuladores de propriedade para o Windows Search

O Microsoft Windows Search usa manipuladores de propriedade para extrair os valores de propriedades de itens e usa o esquema do sistema de propriedades para determinar como uma propriedade específica deve ser indexada. Para ler e indexar valores de propriedade, os manipuladores de propriedade são invocados fora do processo pelo Windows Search para melhorar a segurança e a robustez. Por outro lado, os manipuladores de propriedade são invocados em processo pelo Windows Explorer para ler e gravar valores de propriedade.

Este tópico complementa o tópico [sistema de propriedades](../properties/building-property-handlers.md) com informações específicas ao Windows Search e contém as seguintes seções:

-   [Decisões de design para manipuladores de propriedade](#design-decisions-for-property-handlers)
    -   [Decisões de propriedade](#property-decisions)
    -   [Suporte de texto completo](#full-text-support)
    -   [Considerações de Implementatation do sistema operacional](#operating-system-implementatation-considerations)
-   [Gravando arquivos de descrição da propriedade](#writing-property-description-files)
-   [Implementando manipuladores de propriedade](#implementing-property-handlers)
    -   [IInitializeWithStream](#iinitializewithstream)
    -   [IPropertyStore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [Garantindo que seus itens sejam indexados](#ensuring-your-items-get-indexed)
-   [Instalando e Registrando manipuladores de propriedade](#installing-and-registering-property-handlers)
-   [Manipuladores de propriedades de teste e solução de problemas](#testing-and-troubleshooting-property-handlers)
    -   [Testes de instalação e instalação](#installation-and-setup-tests)
    -   [Solucionando problemas de manipuladores de propriedade](#troubleshooting-property-handlers)
-   [Usando manipuladores de propriedade System-Supplied](#using-system-supplied-property-handlers)
-   [Tópicos relacionados](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Decisões de design para manipuladores de propriedade

A implementação de manipuladores de propriedade envolve as seguintes etapas:

1.  Tomar decisões de design em relação às propriedades às quais você deseja dar suporte.
2.  Criando um arquivo de descrição de propriedade (. propDesc) para propriedades que ainda não estão no sistema de propriedades.
3.  Implementando e testando o manipulador de propriedades.
4.  Instalando e registrando o manipulador de propriedades e os arquivos de descrição da propriedade.
5.  Testando a instalação e o registro do manipulador de propriedades.

Antes de começar, você precisa considerar as seguintes perguntas de design:

-   Quais propriedades o formato de arquivo deve dar suporte?
-   Essas propriedades já estão no esquema do sistema?
-   Posso usar um manipulador de propriedades existente fornecido pelo sistema?
-   Quais propriedades podem ser exibidas aos usuários finais?
-   Quais propriedades os usuários podem editar?
-   O suporte para a pesquisa de texto completo é proveniente de um manipulador de propriedades ou de um filtro?
-   Preciso oferecer suporte a aplicativos herdados? Em caso afirmativo, o que devo implementar?

> [!Note]  
> Antes de continuar, consulte [usando System-Supplied manipuladores de propriedade](#using-system-supplied-property-handlers) para ver se você pode usar um manipulador de propriedade fornecido pelo sistema, economizando os recursos de tempo e desenvolvimento.

 

Depois de tomar essas decisões, você pode escrever descrições formais de suas propriedades personalizadas para que o mecanismo de pesquisa do Windows possa começar a indexar seus arquivos e propriedades. Essas descrições formais são arquivos XML, descritos no [esquema de descrição da propriedade](/previous-versions//cc144127(v=vs.85)).

### <a name="property-decisions"></a>Decisões de propriedade

Ao considerar quais propriedades oferecer suporte, você deve identificar as necessidades de indexação e pesquisa de seus usuários. Por exemplo, você pode identificar 100 propriedades potencialmente úteis para o tipo de arquivo, mas os usuários podem estar interessados em Pesquisar apenas alguns. Além disso, talvez você queira exibir um grupo diferente, maior ou menor, dessas propriedades para os usuários no Windows Explorer e permitir que os usuários editem apenas um subconjunto dessas propriedades exibidas.

O tipo de arquivo pode dar suporte a todas as propriedades personalizadas que você definir, bem como um conjunto de propriedades definidas pelo sistema. Antes de criar uma propriedade personalizada, examine [as propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) para ver se a propriedade que você deseja dar suporte já está definida por uma propriedade do sistema. Sempre certifique-se de que você oferece suporte às propriedades definidas pelo sistema mais importantes.

É recomendável usar uma matriz para ajudá-lo a criar suas propriedades:



| Nome da propriedade | É indexável? | É exibível? | É editável? |
|---------------|---------------|-----------------|--------------|
| {1&gt;property&lt;1}{2&gt;1&lt;2}     | S             | S               | N            |
| Propriedade...   | S             | S               | N            |
| Propriedade     | N             | N               | N            |



 

Para cada uma dessas propriedades, você precisa determinar quais atributos ele deve ter e, em seguida, descreva-os formalmente em arquivos XML de descrição de propriedade (. propDesc). Os atributos incluem o tipo de dados da propriedade, o rótulo, a cadeia de caracteres da ajuda e muito mais. Para propriedades indexáveis, você deve prestar atenção especial aos seguintes atributos de propriedade encontrados no elemento XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   do arquivo de descrição da propriedade.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Opcional. Indica se um valor de propriedade da cadeia de caracteres deve ser dividido em palavras e em cada palavra armazenada no índice invertido. O índice invertido permite a pesquisa eficiente de palavras e frases sobre o valor da propriedade usando CONTAINS ou FREETEXT (por exemplo, SELECT... ONDE contém &quot; SomeText &quot; ). Se definido como <strong>false</strong>, as pesquisas são feitas em toda a cadeia de caracteres. A maioria das propriedades de cadeia de caracteres deve ter essa definição como <strong>true</strong>; as propriedades que não são de cadeia de caracteres devem ter essa definição como <strong>false</strong>. O padrão é <strong>false</strong>.</td>
</tr>
<tr class="even">
<td>IsColumn</td>
<td>Opcional. Indica se a propriedade deve ser armazenada no banco de dados do Windows Search como uma coluna. Armazenar a propriedade como uma coluna permite recuperar, classificar, agrupar e filtrar (ou seja, usar qualquer predicado exceto CONTAINS ou FREETEXT) no valor da coluna inteira. As propriedades exibidas para o usuário devem ter essa definição como <strong>true</strong> , a menos que seja uma propriedade textual muito grande (como o corpo de um documento) que seria pesquisado no índice invertido. O padrão é <strong>false</strong>.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Opcional. Indica se uma propriedade não ocupa espaço se o valor for <strong>nulo</strong>. Uma propriedade não esparsa usa espaço para cada item, mesmo se o valor for <strong>nulo</strong>. Se a propriedade tiver valores múltiplos, esse atributo será sempre <strong>verdadeiro</strong>. Esse atributo deve ser <strong>falso</strong> somente se um valor estiver presente para cada item. O padrão é <strong>true</strong>.</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Opcional. Para otimizar a consulta, o mecanismo de pesquisa do Windows pode criar índices secundários para propriedades que têm IsColumn =<strong>true</strong>. Isso requer mais processamento e espaço em disco durante a indexação, mas melhora o desempenho durante a consulta. Se a propriedade tende a ser classificada, agrupada ou filtrada (ou seja, usando =,! =, <, >, LIKE, corresponde) frequentemente pelos usuários, esse atributo deve ser definido como em &quot; disco &quot; . O padrão é não &quot; indexado &quot; . Os seguintes valores são válidos:
<ul>
<li>Não indexado: nenhum índice secundário é criado.</li>
<li>Em disco: Crie e armazene um índice secundário no disco.</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>Opcional. Indica o tamanho máximo permitido para o valor de propriedade armazenado no banco de dados do Windows Search. Esse limite se aplica aos elementos indvidual de um vetor, não ao vetor como um todo. Os valores que ultrapassam esse tamanho são truncados. O padrão é &quot; 128 &quot; (bytes).<br/> Atualmente, o Windows Search não usa maxSize ao calcular a quantidade de dados que ele aceita de um arquivo. Em vez disso, o limite que o Windows Search usa é o produto do tamanho do arquivo e o MaxGrowFactor (tamanho do arquivo N * MaxGrowFactor) lido no registro em HKEY_LOCAL_MACHINE->software->Microsoft->Windows Search->coletando Manager->MaxGrowFactor. O MaxGrowFactor padrão é quatro (4). Consequentemente, se o tipo de arquivo tende a ser pequeno no tamanho total, mas tiver Propriedades maiores, o Windows Search poderá não aceitar todos os dados de propriedade que você deseja emitir. No entanto, você pode aumentar o MaxGrowFactor para atender às suas necessidades. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Para o atributo columnIndexType, o benefício de consultas mais rápidas precisa ser avaliado em relação ao maior tempo de indexação e aos custos de espaço que os índices secundários podem incorrer. No entanto, esse custo só é pago por itens que têm um valor não **nulo** , portanto, para a maioria das propriedades, esse atributo pode ser definido como "em disco".

 

### <a name="full-text-support"></a>Suporte de texto completo

Em termos gerais, a pesquisa de texto completo é suportada por componentes chamados [filtros](-search-3x-wds-extidx-filters.md); no entanto, para tipos de arquivo baseados em texto com formatos de arquivo não complicados, os manipuladores de propriedades podem fornecer essa funcionalidade com menos esforço de desenvolvimento. Você deve examinar a seção de [conteúdo de texto completo](../properties/building-property-handlers-property-handlers.md) para uma comparação de funcionalidade de filtro e manipulador de propriedades para ajudá-lo a decidir o que é melhor para o tipo de arquivo. De importância específica é o fato de que os filtros podem manipular vários LCIDs (identificadores de código de idioma) por arquivo, enquanto os manipuladores de propriedade não podem.

> [!Note]  
> Como os manipuladores de propriedade não podem dividir o conteúdo da maneira como os filtros podem, arquivos grandes (mesmo que sejam formatos de arquivo não complicados) devem ser completamente carregados na memória.

 

### <a name="operating-system-implementatation-considerations"></a>Considerações de Implementatation do sistema operacional

### <a name="implementation-information-for-windows-7"></a>Informações de implementação para o Windows 7

No Windows 7 e posterior, há um novo comportamento ao registrar um manipulador de propriedades, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)ou nova extensão. Quando um novo manipulador de propriedades e/ou **IFilter** é instalado, os arquivos com as extensões correspondentes são reindexados automaticamente.

No Windows 7, é recomendável que um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) seja instalado em conjunto com seus manipuladores de propriedade correspondentes e que o **IFilter** seja registrado antes do manipulador de propriedades. O registro do manipulador de propriedades inicia a reindexação imediata de arquivos indexados anteriormente sem precisar primeiro de uma reinicialização e aproveita os IFilters previamente registrados para fins de indexação de conteúdo.

Se apenas um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) estiver instalado, sem um manipulador de propriedades correspondente, a reindexação automática ocorrerá após uma reinicialização do serviço de indexação ou uma reinicialização do sistema.

Para sinalizadores de descrição de propriedade específicos para o Windows 7, consulte os seguintes tópicos de referência:

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [\_tipo de COLUMNINDEX PROPDESC \_](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [\_sinalizadores PROPDESC SEARCHINFO \_](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Informações de implementação para o Windows Vista e versões anteriores

Antes do Windows Vista, os filtros forneciam suporte para analisar e enumerar o conteúdo e as propriedades do arquivo. Com a introdução do sistema de propriedades, os manipuladores de propriedade lidam com as propriedades do arquivo enquanto os filtros manipulam o conteúdo do arquivo. Para o Windows Vista, você precisa desenvolver apenas uma implementação parcial da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)em coordenação com um manipulador de propriedades, conforme descrito em [práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md).

Embora o sistema de propriedades também esteja incluído com a instalação do Windows Search para Windows XP, aplicativos de terceiros e herdados podem exigir que os filtros manipulem o conteúdo e as propriedades. Portanto, se você estiver desenvolvendo na plataforma Windows XP, deverá fornecer uma implementação de filtro completa, bem como um manipulador de propriedades para o tipo de arquivo ou a propriedade personalizada.

 

## <a name="writing-property-description-files"></a>Gravando arquivos de descrição da propriedade

A estrutura de arquivos XML de descrição de propriedade (. propDesc) é descrita no tópico [propertyDescription](../properties/propdesc-schema-propertydescription.md) . De interesse particular para pesquisa estão os atributos do elemento [searchInfo](../properties/propdesc-schema-searchinfo.md) . Depois de decidir quais propriedades dar suporte, você precisa criar e registrar arquivos de descrição de propriedade para cada propriedade. Quando você registra seus arquivos. propDesc, eles são incluídos na lista Descrição da Propriedade do esquema e se tornam nomes de coluna no repositório de propriedades do mecanismo de pesquisa.

Você pode registrar suas descrições de propriedade personalizadas usando a função [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , uma API de wrapper que chama o IPropertySystem:: RegisterPropertySchema do subsistema de esquema. Essa função informa o subsistema de esquema da adição de arquivos de esquema de descrição de propriedade (. propDesc), usando caminho (s) de arquivo para os arquivos. propDesc no computador local, geralmente o diretório de instalação do aplicativo em "arquivos de programas". Normalmente, uma instalação ou um aplicativo (por exemplo, o instalador do manipulador de propriedades) chamará esse método depois de instalar os arquivos. propDesc.

 

## <a name="implementing-property-handlers"></a>Implementando manipuladores de propriedade

Desenvolver um manipulador de propriedade envolve a implementação das seguintes interfaces:

-   IInitialzeWithStream: fornece inicialização baseada em fluxo de seu manipulador de propriedade.
-   IPropertyStore: enumera, obtém e define os valores de propriedade.
-   IPropertyStoreCapabilities: opcional. Identifica se os usuários podem editar uma propriedade de uma interface do usuário.

### <a name="iinitializewithstream"></a>IInitializeWithStream

Conforme descrito no tópico do [sistema de propriedades](../properties/building-property-handlers.md) , é altamente recomendável implementar manipuladores de propriedade com **IInitializeWithStream** para realizar a inicialização baseada em fluxo. Se você optou por não implementar IInitializeWithStream, o manipulador de propriedades deverá recusar a execução no processo de isolamento definindo o sinalizador DisableProcessIsolation na chave do registro do manipulador de propriedades. Desabilitar o isolamento de processo geralmente é destinado apenas a manipuladores de propriedade herdados e deve ser strenuously evitado por qualquer código novo.

### <a name="ipropertystore"></a>IPropertyStore

Para criar um manipulador de propriedades, você deve implementar a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) com os métodos a seguir.



| Método   | Descrição                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Salva uma alteração de propriedade no arquivo.                                |
| GetAt    | Recupera uma chave de propriedade da matriz de propriedades de um item.        |
| GetCount | Obtém o número de propriedades anexadas ao arquivo.                 |
| GetValue | Recupera dados para uma propriedade específica.                             |
| SetValue | Define um novo valor de propriedade ou substitui ou remove um valor existente. |



 

 

 

Considerações importantes para implementar essa interface estão incluídas na documentação do [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

> [!Note]  
> Se o manipulador de propriedades emitir vários valores para a mesma propriedade para um determinado item, somente o último valor emitido será armazenado no catálogo.

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

Os manipuladores de propriedade podem, opcionalmente, implementar essa interface para desabilitar a capacidade do usuário de editar propriedades específicas. Essas propriedades normalmente são editáveis na página de detalhes e no painel, mas não é permitido editá-las no manipulador de propriedade de implementação. Implementar essa interface corretamente fornece uma experiência de usuário melhor do que a alternativa – um erro de tempo de execução simples do Shell.

 

## <a name="ensuring-your-items-get-indexed"></a>Garantindo que seus itens sejam indexados

Agora que você implementou seu manipulador de propriedades, você deseja certificar-se de que os itens que seu manipulador está registrado para serem indexados. Você pode usar o [Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) para iniciar a reindexação e também pode usar o [Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md) para configurar regras padrão indicando as URLs que você deseja que o indexador rastreie. Outra opção é seguir o exemplo de código de reindexação nos [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Para obter mais informações, consulte [usando o Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Instalando e Registrando manipuladores de propriedade

Com o manipulador de propriedade implementado, ele deve ser registrado e sua extensão de nome de arquivo associada ao manipulador. O exemplo a seguir mostra as chaves do registro e os valores necessários para fazer isso.

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

 

## <a name="testing-and-troubleshooting-property-handlers"></a>Manipuladores de propriedades de teste e solução de problemas

A lista a seguir fornece conselhos sobre os tipos de testes que você deve executar:

-   Teste obtendo a saída de cada propriedade única com suporte no tipo de arquivo.
-   Use valores de propriedade Big, por exemplo, use uma marca de meta grande em documentos HTML.
-   Verifique se o manipulador de propriedade não vaza identificadores de arquivo editando-o depois de obter a saída do manipulador de propriedade ou usando uma ferramenta como oh.exe antes e depois de enumerar as propriedades do arquivo.
-   Teste todos os tipos de arquivo associados ao manipulador de propriedades. Por exemplo, verifique se o filtro HTML funciona com os tipos de arquivo. htm e. html.
-   Teste com arquivos corrompidos. O manipulador de propriedades deve falhar normalmente.
-   Se um aplicativo oferecer suporte à criptografia, teste se o manipulador de propriedade não dá saída ao texto criptografado.
-   Se o manipulador de propriedades oferecer suporte à pesquisa de texto completo:
    -   Use vários caracteres Unicode especiais no conteúdo do arquivo e teste para sua saída.
    -   Teste a manipulação de documentos muito grandes para garantir que o manipulador de propriedades funcione conforme o esperado.

### <a name="installation-and-setup-tests"></a>Testes de instalação e instalação

Por fim, você precisa testar suas rotinas de instalação e desinstalação.

-   A instalação deve se recuperar de instalações com falha (por exemplo, de cancelar e reiniciar a instalação).
-   A desinstalação deve excluir todos os arquivos associados ao manipulador de propriedades.
-   A desinstalação não deve excluir arquivos diferentes daqueles associados à instalação do manipulador de propriedades.
-   As chaves do registro associadas ao manipulador de propriedades devem ser removidas quando desinstaladas.
-   A desinstalação deve funcionar mesmo que os arquivos sejam excluídos do diretório de instalação.

### <a name="troubleshooting-property-handlers"></a>Solucionando problemas de manipuladores de propriedade

A seguir estão alguns erros comuns feitos ao desenvolver manipuladores de propriedade:

-   Instalando arquivos. propDesc ou DLLs em um diretório de usuário.
-   Registrando componentes usando caminhos relativos.
-   Registrando componentes em HKEY \_ Current \_ User, em vez de hKey \_ local \_ Machine.
-   Esquecendo de definir DisableProcessIsolation para manipuladores que não são de fluxo.
-   Colocando o arquivo de teste em um local não indexado.

Se você estiver tendo problemas para obter o manipulador de propriedades trabalhando com o indexador, aqui estão algumas dicas para ajudá-lo a solucionar problemas:

-   Verifique se as descrições de propriedade (arquivos. propDesc) estão marcadas como IsColumn = "**true**", isviewable = "**true**" e IsQuery = "**true**", conforme apropriado.
-   Verifique se os arquivos. propDesc estão em um local global.
-   Verifique se você registrou seus arquivos. propDesc usando caminhos absolutos.
-   Verifique se o log de eventos não registrou nenhuma falha ao registrar o arquivo. propDesc.
-   Verifique se suas DLLs estão em um local global (e não em seu perfil de usuário).
-   Verifique se suas DLLs estão registradas em HKEY \_ local \_ Machine \\ software \\ classes.
-   Verifique se suas DLLs estão registradas usando caminhos completos (ou \_ as \_ cadeias de caracteres reg expande sz que se expandem para caminhos absolutos usando variáveis de ambiente conhecidas pela conta do sistema).
-   Verifique se o manipulador de propriedades funciona no Windows Explorer.
-   Embora seja recomendável usar IInitializeWithStream, se você precisar usar IInitializeWithFile ou IInitializeWithItem, verifique se você especificou DisableProcessIsolation.
-   Verifique se o painel de controle de opções de indexação lista o tipo de arquivo como um tipo de arquivo indexado.
-   Verifique se o arquivo de teste está em um local indexado.
-   Verifique se o arquivo de teste foi modificado desde que você instalou o manipulador de propriedades.

Se o arquivo de teste estiver em um local indexado e o indexador já tiver rastreado esse local, você precisará modificar o arquivo de alguma forma para disparar uma reindexação do arquivo.

 

## <a name="using-system-supplied-property-handlers"></a>Usando manipuladores de propriedade System-Supplied

O Windows inclui vários manipuladores de propriedade fornecidos pelo sistema que você pode usar se o formato do seu tipo de arquivo for compatível. Se você definir uma nova extensão de arquivo que usa um desses formatos, poderá usar os manipuladores fornecidos pelo sistema registrando o identificador de classe do manipulador (CLSID) para sua extensão de arquivo.

Você pode usar o CLSID listado na tabela a seguir para registrar os manipuladores de propriedade fornecidos pelo sistema para o tipo de formato de arquivo.



| Formatar          | CLSID                                  |
|-----------------|----------------------------------------|
| DOCFILE OLE     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| Salvar o XML do jogo   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| Manipulador XPS/OPC | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Antes de criar uma propriedade personalizada, você deve ter certeza de que não há uma propriedade definida pelo sistema que possa ser usada em seu lugar. Você pode enumerar as propriedades definidas pelo sistema chamando [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) ou usando a ferramenta de linha de comando prop.exe.

O esquema do sistema define como essas propriedades interagem com o indexador e você não pode alterá-las. Além disso, o aplicativo que você usa para criar, editar e salvar seu tipo de arquivo precisa estar em conformidade com determinado comportamento também. Por exemplo, se o aplicativo implementar o salvamento seguro (no qual um arquivo temporário é criado durante a edição e, em seguida, ReplaceFile () for usado para trocar a nova versão para o antigo), ele deverá transferir todas as propriedades do arquivo original para o novo arquivo. A falha em fazer significa que o arquivo perde propriedades adicionadas por usuários ou outros aplicativos.

 

**Exemplo**

O seguinte mostra o registro do manipulador OLE DOCFILE fornecido pelo sistema para um tipo de arquivo com um. Extensão OLEDocFile.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

O seguinte mostra o registro das informações da lista de propriedades para propriedades de. Os arquivos OLEDocFile são exibidos na guia detalhes e no painel.

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

**Conceitua**
</dt> <dt>

[Práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)
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

[Exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
