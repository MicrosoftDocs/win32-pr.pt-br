---
title: Desenvolvendo complementos de IFilter
description: Você pode estender o Microsoft Windows WDS (Desktop Search) com complementos de filtro, componentes que implementam o IFilterinterface, para incluir novos tipos de arquivo.
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497d4bffdb9564e0737bee3cd0b63fa8026633a2cc81aad37cb989423e460487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480890"
---
# <a name="developing-ifilter-add-ins"></a>Desenvolvendo complementos de IFilter

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

Você pode estender o WDS (Microsoft Windows Desktop Search) com complementos de filtro, componentes que implementam a interface [**IFilter,**](/windows/desktop/api/filter/nn-filter-ifilter)para incluir novos tipos de arquivo. Os filtros são responsáveis por acessar e analisar dados em arquivos e por retornar pares de propriedades e valores, bem como partes de texto para indexação. Durante o processo de indexação, o WDS chama o filtro apropriado com a URL para cada arquivo ou item. O filtro primeiro extrai metadados que correspondem às propriedades marcadas como recuperáveis no esquema WDS, como título, tamanho do arquivo e data da última modificação. Em seguida, ele divide o conteúdo do item em partes de texto. O WDS adiciona as propriedades e o texto retornados pelo filtro ao catálogo. O WDS pode indexar qualquer tipo de arquivo para o qual tenha um filtro registrado.

Em algumas circunstâncias, você não precisa escrever um novo filtro. O WDS 2.x contém filtros para mais de 200 tipos de itens (incluindo itens de texto não criptografado, como arquivos HTML, XML e código-fonte) e usa a mesma tecnologia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Se você já tiver filtros instalados para seus tipos de arquivo, o WDS poderá usar esses filtros existentes para indexar esses dados. Além disso, o WDS inclui um filtro geral para tipos de arquivo baseados em texto não criptografado. Se você tiver um tipo de arquivo que possa ser processado por um filtro SharePoint Services existente ou pelo filtro de texto não criptografado, poderá adicionar a extensão de nome de arquivo e o GUID de filtro ao Registro para que o WDS possa [localizá-lo e usá-lo](#to-register-a-filter-add-in) (consulte Para registrar um complemento de filtro para obter mais informações).

No entanto, se você tiver um formato de arquivo ou dados não simples e proprietários, escrever uma implementação de filtro personalizado será a única maneira de garantir que o WDS possa indexar o formato de arquivo no catálogo. Você pode ter apenas um complemento de filtro para um tipo de arquivo, portanto, é possível substituir um filtro existente ou fazer com que outro filtro substitua o seu por um tipo de arquivo específico.

Esta seção contém os seguintes tópicos:

-   [Interfaces de filtro necessárias](#required-filter-interfaces)
    -   [IFilter Interface](#ifilter-interface)
    -   [Ipersiststream](#ipersiststream)
    -   [Ipersistfile](#ipersistfile)
    -   [Ipersiststorage](#ipersiststorage)
-   [Saída de propriedades com filtros](#outputting-properties-with-filters)
    -   [Valores da propriedade](#property-values)
-   [Filtrar a instalação do complemento](#filter-add-in-installation)
    -   [CLSIDs necessárias para o registro](#clsids-required-for-registration)
    -   [Modelo de registro](#registration-model)
    -   [Para registrar um complemento de filtro](#to-register-a-filter-add-in)
-   [Tópicos relacionados](#related-topics)

## <a name="required-filter-interfaces"></a>Interfaces de filtro necessárias

Um complemento de filtro deve implementar a interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e uma das seguintes interfaces:

-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) – para carregar dados de um fluxo. Isso é mais seguro do que usar arquivos porque nada é gravado no disco. A interface IPersistStream é o método preferencial para compatibilidade direta com Windows Vista.
-   [Interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) – para carregar dados de um arquivo. Não há suporte para essa interface no Windows Vista.
-   [Interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) – para carregar dados de uma estrutura OLE COM Armazenamento.

Um complemento de filtro usa essas interfaces para obter o conteúdo do item e retorá-los iterativamente para o índice até que o final do arquivo seja atingido. Um complemento de filtro deve ser o mais robusto possível para lidar com arquivos corrompidos e aqueles que não atendem aos formatos de entrada esperados.

### <a name="ifilter-interface"></a>IFilter Interface

Essa é uma interface necessária para uma implementação de filtro. Para obter mais informações, consulte a referência da interface [**IFilter.**](/windows/desktop/api/filter/nn-filter-ifilter)



| Método       | Descrição                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| Init()       | Inicializa uma sessão de filtragem.                                                       |
| GetChunk()   | Posiciona o filtro no início da primeira ou da próxima parte e retorna um descritor. |
| GetText()    | Recupera o texto da parte atual.                                                 |
| GetValue()   | Recupera valores de propriedade da parte atual.                                      |
| BindRegion() | Atualmente reservado para uso interno; não implemente. Esse método retorna E \_ NOTIMPL. |



 

### <a name="ipersiststream"></a>Ipersiststream

Essa interface carrega um arquivo de um fluxo para um processamento mais seguro do que a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) porque o contexto no qual um [filtro IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) é executado não precisa dos direitos para abrir arquivos no disco ou pela rede. Dos dois métodos para acessar um único arquivo, esse é o método preferencial para compatibilidade de encaminhamento com Windows.



| Método       | Descrição                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| IsDirty()    | Verifica se houve uma alteração. Esse método retorna E \_ NOTIMPL em filtros.                                                                      |
| InitNew()    | Cria um novo armazenamento. Esse método retorna E \_ NOTIMPL em filtros.                                                                                  |
| Load()       | Inicializa um objeto do fluxo de onde ele foi salvo anteriormente.                                                                               |
| Save()       | Salva um objeto no fluxo especificado e indica se o objeto deve redefinir seu sinalizador sujo. Esse método retorna E \_ NOTIMPL em filtros. |
| GetSizeMax() | Retorna o tamanho em bytes do fluxo necessário para salvar o objeto. Esse método retorna E \_ NOTIMPL em filtros.                                      |



 

### <a name="ipersistfile"></a>Ipersistfile

Essa interface carrega um arquivo por caminho absoluto e não tem suporte no Windows Vista.



| Método          | Descrição                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| GetCurFile()    | Obtém o nome atual do arquivo associado ao objeto . Retorna o caminho especificado em Load().                          |
| Load()          | Abre o arquivo especificado e inicializa um objeto do conteúdo do arquivo. Você pode atrasar a abertura do arquivo até precisar dele. |
| GetClassID()    | Retorna o CLSID (identificador de classe) para o novo tipo de arquivo. Você deve usar uuidgen.exe para gerar um CLSID exclusivo.           |
| IsDirty()       | Só é necessário retornar E \_ NOTIMPL em filtros                                                                                       |
| Save()          | Só é necessário retornar E \_ NOTIMPL em filtros                                                                                       |
| SaveCompleted() | Só é necessário retornar E \_ NOTIMPL em filtros                                                                                       |



 

### <a name="ipersiststorage"></a>Ipersiststorage

Essa interface dá suporte ao modelo de armazenamento estruturado, no qual cada objeto contido tem seu próprio armazenamento aninhado no armazenamento do contêiner. Assim [como a Interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile), essa interface é carregada por caminho absoluto e não tem suporte no Windows Vista.



| Método            | Descrição                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| IsDirty()         | Verifica se houve uma alteração. Esse método retorna E \_ NOTIMPL em filtros.                                 |
| InitNew()         | Cria um novo armazenamento. Esse método retorna E \_ NOTIMPL em filtros.                                             |
| Load()            | Salva o armazenamento. Esse método retorna E \_ NOTIMPL em filtros.                                                 |
| Save()            | Retorna o tamanho em bytes do fluxo necessário para salvar o objeto. Esse método retorna E \_ NOTIMPL em filtros. |
| SaveCompleted()   | Reservado para uso interno. Esse método retorna E \_ NOTIMPL em filtros.                                         |
| HandsOffStorage() | Reservado para uso interno. Esse método retorna E \_ NOTIMPL em filtros.                                         |



 

## <a name="outputting-properties-with-filters"></a>Saída de propriedades com filtros

A finalidade de um filtro é extrair o conteúdo e as propriedades dos arquivos para inclusão no índice de texto completo. O WDS primeiro chama o método Load nas implementações IPersistFile, IPersistStream ou IPersistStorage e, em seguida, invoca o método Init da implementação de IFilter. **GetChunk** é chamado para recuperar partes de dados de texto ou valor da propriedade e, em seguida, **GetText** ou **GetValue** é chamado quantas vezes for necessário para recuperar todos os valores de texto ou propriedade associados à parte. Esse processo se repete até **que GetChunk** informe que não há mais partes no documento.

O método **GetChunk** recupera informações sobre o primeiro ou o próximo bloco lógico de informações do arquivo que está sendo filtrado e retorna essas informações em uma estrutura STAT CHUNK, incluindo uma ID de parte de aumento monotônica, informações de status sobre como a parte atual se relaciona com a parte anterior, um sinalizador que indica se a parte contém texto ou um valor, a localidade da parte e a especificação da propriedade da \_ parte. A especificação de propriedade é [**um FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) que consiste em um CLSID e um identificador de propriedade de cadeia de caracteres ou inteiro (por exemplo, D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType). Ele identifica o tipo de propriedade em vez do próprio valor da propriedade.

O identificador de localidade da parte é usado para escolher um disjuntor de palavras apropriado e é muito importante que você o identifique corretamente. Se o filtro não puder determinar a localidade do texto, ele deverá assumir a localidade padrão do sistema, disponível usando **GetSystemDefaultLCID**. Se você controlar o formato de arquivo e ele atualmente não contém informações de localidade, adicione um recurso de usuário para habilitar a identificação de localidade adequada. O uso de um disjuntor de palavras incompatibilidade pode levar a uma experiência de consulta ruim para o usuário.

**GetChunk** gerencia apenas partes de acesso e não retorna o texto ou o próprio valor da propriedade. Em vez disso, as chamadas **subsequentes para GetText** e **GetValue** recuperam o corpo da parte. **GetText** retorna partes de texto, que são cadeias de caracteres Unicode, da parte ATUAL DE \_ TEXTO CHUNK. Se a parte atual for muito grande, mais de uma chamada para o **método GetText** poderá ser necessária. Cada chamada para o **método GetText** recupera o texto que segue imediatamente o texto da última chamada para o **método GetText.** Por exemplo, o último caractere de uma chamada pode estar no meio de uma palavra e o primeiro caractere na próxima chamada continuará essa palavra. Os mecanismos de pesquisa devem lidar com essa situação.

**GetValue** retorna valores de propriedade para a parte CHUNK VALUE atual em estruturas PROPVARIANT, que podem conter uma ampla \_ variedade de tipos de dados. **GetValue** deve alocar a própria estrutura PROPVARIANT usando CoTaskMemAlloc. O chamador de **GetValue** é responsável por liberar memória apontada pelo PROPVARIANT usando PropVariantClear e por liberar a própria estrutura com CoTaskMemFree. Para obter mais informações sobre PROPVANARTs, consulte a [referência PROPVARIANT.](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

### <a name="property-values"></a>Valores da propriedade

Os filtros devem ser produzidos no mínimo as propriedades a seguir, que são as colunas padrão na exibição de resultados do WDS.



| GUID                                 | PROPSPEC      | Nome amigável  | Descrição                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 2             | PrimaryTitle   | Título exibido para este item.                                                                                                              |
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 4             | PrimaryAuthors | Pessoa mais associada a este item.                                                                                                          |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PrimaryDate   | PrimaryDate    | Data mais importante para o item, como a data recebida para email ou modificada para arquivos.                                                               |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PerceivedType | PerceivedType  | Tipo de arquivo que está sendo analisado. Deve corresponder a um dos tipos Windows Desktop Search [](-search-2x-wds-perceivedtype.md)listados em Tipo Percebido do WDS. |



 

Para itens de texto não criptografado, o WDS extrai todas as propriedades definidas pelo sistema e texto, como tamanho do arquivo ou extensão, incluindo novos tipos de arquivo de texto não criptografado para o índice). Outros tipos de propriedades que podem ser retornados ao índice incluem:

-   Para arquivos: autor, título, status, palavras-chave
-   Para mídia: álbum, gênero, make da câmera, data tomada
-   Para comunicações: de, para, cc, importância
-   Para contatos: cargo, telefone comercial, empresa

A lista acima grupos propriedades comuns a um tipo percebido especificado; no entanto, qualquer propriedade pode ser usada independentemente do tipo. Por exemplo, a empresa pode ser usada para o nome do funcionário de um contato e também pode ser usada para se referir ao nome de um cliente ao que o arquivo está relacionado. Muitas dessas propriedades são usadas para exibir os resultados da pesquisa na exibição de resultados do WDS. Por exemplo, a propriedade Title de um arquivo é mostrada como a coluna principal na exibição de resultados padrão. Os objetos IFilter devem ter todas as propriedades relacionadas ao tipo de item que estão sendo analisados. As propriedades personalizadas não podem ser adicionadas no WDS 2.x. Para ver uma lista completa das propriedades disponíveis, consulte o [Esquema WDS](-search-2x-wds-schematable.md).

## <a name="filter-add-in-installation"></a>Filtrar a instalação do complemento

Instalar o filtro envolve copiar a DLL para um local apropriado no diretório Arquivos de Programas e registrá-la. Os filtros devem implementar o auto-registro para instalação e devem seguir estas diretrizes:

-   O instalador deve usar o instalador EXE ou MSI.
-   As notas de versão devem ser fornecidas.
-   Uma **entrada Adicionar/Remover Programas** deve ser criada para cada complemento instalado.
-   O instalador deve assumir todas as configurações do Registro para o tipo de arquivo ou armazenamento específico que o complemento atual entende.
-   Se um complemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.
-   Se um novo complemento tiver substituído o complemento anterior, deverá haver a capacidade de restaurar a funcionalidade do complemento anterior e torná-la o complemento padrão para esse tipo de arquivo ou armazenar novamente.

### <a name="clsids-required-for-registration"></a>CLSIDs necessárias para o registro

Há três identificadores de classe, ou CLSIDs, associados a cada filtro. Você precisará gerar um ou mais deles (use uuidgen.exe) para registrar o complemento de filtro.

-   O primeiro identifica o manipulador persistente de todos os filtros, IID IFilter, que é \_ {89BCB740-6119-101A-BCB7-00DD010655AF}. Essa CLSID é constante para todos os filtros que implementam IFilter.
-   O segundo (o valor da chave \_ IID IFilter) identifica a implementação de IFilter para o tipo de arquivo. Essa chave contém um valor InprocServer32 que especifica o nome da DLL por caminho e o modelo de threading. Se o filtro estiver no caminho do sistema, como o diretório system32, um nome de arquivo será suficiente. Caso contrário, esse valor deve ter uma especificação de caminho completo.
-   O terceiro identifica o tipo de arquivo que o filtro processa e é retornado pelo método GetClassID em sua interface IPersist.

> [!Note]
>
> Em versões futuras dos sistemas operacionais microsoft, a instalação de arquivos no diretório system32 pode ficar mais difícil, portanto, recomendamos instalá-los em Arquivos de Programas e incluir um caminho completo para o filtro no Registro. Por motivos de segurança, também é importante especificar um caminho completo para sua DLL no Registro. Caso contrário, uma versão de "cavalo de Troia" da sua DLL poderá ser carregada se ela estiver no caminho do processo antes da sua versão.

 

### <a name="registration-model"></a>Modelo de registro

Quando o WDS está pronto para filtrar um arquivo, ele procura no Registro sob a extensão do arquivo para determinar qual filtro carregar. Em seguida, ele segue uma série de links do Registro para encontrar o nome da DLL de filtro, nesta ordem:

1.  De CLSIDs localizadas em:

    **HKEY \_ CURRENT \_ USER \\ SOFTWARE \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ Override \\ RSApp**

    **Filtros HKEY \_ CURRENT USER SOFTWARE Microsoft \_ \\ \\ \\ RSSearch \\ ContentIndexCommon \\**

2.  No tipo de conteúdo do arquivo em:

    **Tipo de conteúdo de banco de dados \_ MIME classes \_ \\ DE SOFTWARE DO \\ \\ MACHINE \\ LOCAL \\ HKEY**

3.  Na extensão de nome de arquivo (igual à API LoadIFilter do Win32) em:

    **HKEY \_ CURRENT \_ USER \\ SOFTWARE \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ Override \\ RSApp**

    **Filtros HKEY \_ CURRENT USER SOFTWARE Microsoft \_ \\ \\ \\ RSSearch \\ ContentIndexCommon \\**

    **HKEY \_ CLASSES \_ ROOT \\ extpersistentHandler->CLSID->IID \_ IFilter->CLSID**

4.  De Padrão em:

    **Filtros HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ RSSearch \\ ContentIndexCommon \\**

### <a name="to-register-a-filter-add-in"></a>Para registrar um complemento de filtro

Você precisa fazer um total de oito entradas no Registro para registrar seu complemento de filtro, em que:

-   **.ext** é a nova extensão de nome de arquivo
-   **GUID \_ 1** pode ser qualquer novo GUID gerado para essa extensão
-   **89BCB740-6119-101A-BCB7-00DD010655AF** é o GUID da interface IFilter, que é uma constante para todas as implementações de IFilter.

1.  Registre o manipulador persistente para a extensão de nome de arquivo com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT\<.ext>\PersistentHandler
       (Default) = {GUID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}
       (Default) = <Persistent Handler Description>
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered
       (Default) = (Value Not Set)
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered\{89BCB740-6119-101A-BCB7-00DD010655AF}
       (Default) = {CLSID of IFilter implementation}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentHandler
       (Default) = {GUID_1}
    ```

2.  Registre a implementação de IFilter com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  Registre a implementação de IFilter com Windows Desktop Search com a seguinte chave e valor:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Tipos percebidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Ifilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 