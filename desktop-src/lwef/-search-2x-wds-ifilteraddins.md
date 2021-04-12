---
title: Desenvolvendo suplementos do IFilter
description: Você pode estender o Microsoft Windows Desktop Search (WDS) com suplementos de filtro, componentes que implementam o IFilterinterface, para incluir novos tipos de arquivo.
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f846cf2101eefc17b1e92fbd7992529a06fb43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454042"
---
# <a name="developing-ifilter-add-ins"></a>Desenvolvendo suplementos do IFilter

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

Você pode estender o Microsoft Windows Desktop Search (WDS) com suplementos de filtro, componentes que implementam a interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter), para incluir novos tipos de arquivo. Os filtros são responsáveis por acessar e analisar dados em arquivos e retornar pares de propriedades e valores, bem como partes de texto para indexação. Durante o processo de indexação, o WDS chama o filtro apropriado com a URL para cada arquivo ou item. O filtro primeiro extrai metadados que correspondem às propriedades que são marcadas como recuperáveis no esquema do WDS, como título, tamanho do arquivo e data da última modificação. Em seguida, ele quebra o conteúdo do item em partes do texto. O WDS adiciona as propriedades e o texto retornado pelo filtro ao catálogo. O WDS pode indexar qualquer tipo de arquivo para o qual ele tenha um filtro registrado.

Em algumas circunstâncias, você não precisa escrever um novo filtro. O WDS 2. x contém filtros para mais de 200 tipos de itens (incluindo itens de texto sem formatação, como HTML, XML e arquivos de código-fonte) e usa a mesma tecnologia de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que os serviços do SharePoint. Se você já tiver filtros instalados para os tipos de arquivo, o WDS poderá usar esses filtros existentes para indexar esses dados. Além disso, o WDS inclui um filtro geral para tipos de arquivos que são baseados em texto sem formatação. Se você tiver um tipo de arquivo que possa ser processado por um filtro existente dos serviços do SharePoint ou o filtro de texto não criptografado, poderá adicionar a extensão de nome de arquivo e o GUID de filtro ao registro para que o WDS possa localizá-lo e usá-lo (consulte [para registrar um suplemento de filtro](#to-register-a-filter-add-in) para obter mais informações).

No entanto, se você tiver um formato de arquivo ou dados sem texto não criptografado e proprietário, escrever uma implementação de filtro personalizado será a única maneira de garantir que o WDS possa indexar o formato de arquivo no catálogo. Você pode ter apenas um suplemento de filtro para um tipo de arquivo, portanto, é possível substituir um filtro existente ou fazer com que outro filtro substitua seu para um tipo de arquivo específico.

Esta seção contém os seguintes tópicos:

-   [Interfaces de filtro necessárias](#required-filter-interfaces)
    -   [Interface IFilter](#ifilter-interface)
    -   [IPersistStream](#ipersiststream)
    -   [IPersistFile](#ipersistfile)
    -   [IPersistStorage](#ipersiststorage)
-   [Propriedades de saída com filtros](#outputting-properties-with-filters)
    -   [Valores de propriedade](#property-values)
-   [Instalação do suplemento de filtro](#filter-add-in-installation)
    -   [CLSIDs necessários para o registro](#clsids-required-for-registration)
    -   [Modelo de registro](#registration-model)
    -   [Para registrar um suplemento de filtro](#to-register-a-filter-add-in)
-   [Tópicos relacionados](#related-topics)

## <a name="required-filter-interfaces"></a>Interfaces de filtro necessárias

Um suplemento de filtro deve implementar a interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e uma das seguintes interfaces:

-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -para carregar dados de um fluxo. Isso é mais seguro do que usar arquivos porque nada é gravado em disco. A interface IPersistStream é o método preferencial para a compatibilidade de encaminhamento com o Windows Vista.
-   [Interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) – para carregar dados de um arquivo. Não há suporte para essa interface no Windows Vista.
-   [Interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) – para carregar dados de um armazenamento estruturado com OLE.

Um suplemento de filtro usa essas interfaces para obter o conteúdo do item e retorná-los iterativamente para o índice até que o final do arquivo seja atingido. Um suplemento de filtro deve ser o mais robusto possível para lidar com arquivos corrompidos e aqueles que não atendem aos formatos de entrada esperados.

### <a name="ifilter-interface"></a>Interface IFilter

Esta é uma interface necessária para uma implementação de filtro. Para obter mais informações, consulte a referência de interface do [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).



| Método       | Descrição                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| Init ()       | Inicializa uma sessão de filtragem.                                                       |
| GetChunk ()   | Posiciona o filtro no início da primeira ou próxima parte e retorna um descritor. |
| Gettext ()    | Recupera o texto da parte atual.                                                 |
| GetValue ()   | Recupera os valores de propriedade da parte atual.                                      |
| BindRegion() | Atualmente reservado para uso interno; Não implementar. Esse método retorna E \_ NOTIMPL. |



 

### <a name="ipersiststream"></a>IPersistStream

Essa interface carrega um arquivo de um fluxo para um processamento mais seguro do que a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) porque o contexto no qual um filtro [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) é executado não precisa dos direitos para abrir arquivos no disco ou pela rede. Dos dois métodos para acessar um único arquivo, esse é o método preferencial para a compatibilidade de encaminhamento com o Windows.



| Método       | Descrição                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| IsDirty ()    | Verifica se houve uma alteração. Esse método retorna E \_ NOTIMPL em filtros.                                                                      |
| InitNew()    | Cria um novo armazenamento. Esse método retorna E \_ NOTIMPL em filtros.                                                                                  |
| Carregar ()       | Inicializa um objeto do fluxo de onde ele foi salvo anteriormente.                                                                               |
| Salvar ()       | Salva um objeto no fluxo especificado e indica se o objeto deve redefinir seu sinalizador sujo. Esse método retorna E \_ NOTIMPL em filtros. |
| GetSizeMax() | Retorna o tamanho em bytes do fluxo necessário para salvar o objeto. Esse método retorna E \_ NOTIMPL em filtros.                                      |



 

### <a name="ipersistfile"></a>IPersistFile

Essa interface carrega um arquivo por caminho absoluto e não tem suporte no Windows Vista.



| Método          | Descrição                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| GetCurFile()    | Obtém o nome atual do arquivo associado ao objeto. Retorna o caminho especificado em Load ().                          |
| Carregar ()          | Abre o arquivo especificado e inicializa um objeto do conteúdo do arquivo. Você pode atrasar a abertura do arquivo até precisar dele. |
| GetClassID ()    | Retorna o identificador de classe (CLSID) para o novo tipo de arquivo. Você deve usar uuidgen.exe para gerar um CLSID exclusivo.           |
| IsDirty ()       | Só é necessário retornar E \_ NOTIMPL em filtros                                                                                       |
| Salvar ()          | Só é necessário retornar E \_ NOTIMPL em filtros                                                                                       |
| SaveCompleted() | Só é necessário retornar E \_ NOTIMPL em filtros                                                                                       |



 

### <a name="ipersiststorage"></a>IPersistStorage

Essa interface dá suporte ao modelo de armazenamento estruturado, no qual cada objeto contido tem seu próprio armazenamento aninhado dentro do armazenamento do contêiner. Assim como a [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile), essa interface é carregada por caminho absoluto e não tem suporte no Windows Vista.



| Método            | Descrição                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| IsDirty ()         | Verifica se houve uma alteração. Esse método retorna E \_ NOTIMPL em filtros.                                 |
| InitNew()         | Cria um novo armazenamento. Esse método retorna E \_ NOTIMPL em filtros.                                             |
| Carregar ()            | Salva o armazenamento. Esse método retorna E \_ NOTIMPL em filtros.                                                 |
| Salvar ()            | Retorna o tamanho em bytes do fluxo necessário para salvar o objeto. Esse método retorna E \_ NOTIMPL em filtros. |
| SaveCompleted()   | Reservado para uso interno. Esse método retorna E \_ NOTIMPL em filtros.                                         |
| HandsOffStorage() | Reservado para uso interno. Esse método retorna E \_ NOTIMPL em filtros.                                         |



 

## <a name="outputting-properties-with-filters"></a>Propriedades de saída com filtros

A finalidade de um filtro é extrair o conteúdo e as propriedades dos arquivos para inclusão no índice de texto completo. O WDS primeiro chama o método Load nas implementações IPersistFile, IPersistStream ou IPersistStorage e, em seguida, invoca o método Init da implementação do IFilter. **GetChunk** é chamado para recuperar partes de dados de valor de texto ou propriedade e, em seguida, **gettext** ou **GetValue** é chamado quantas vezes forem necessárias para recuperar todos os valores de texto ou propriedade associados à parte. Esse processo se repete até que **GetChunk** relate que não há mais partes no documento.

O método **GetChunk** recupera informações sobre o primeiro ou o próximo bloco lógico de informações do arquivo que está sendo filtrado e retorna essas informações em uma estrutura de partes de estatística \_ , incluindo uma ID de parte de aumento monotônico, informações de status sobre como a parte atual está relacionada à parte anterior, um sinalizador que indica se a parte contém texto ou um valor, a localidade da parte e a especificação de A especificação de propriedade é um [**FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) que consiste em um CLSID e um identificador de propriedade de cadeia de caracteres ou inteiro (por exemplo, D5CDD505-2E9C-101B-9397-08002B2CF9AE/percebidotype). Ele identifica o tipo de propriedade em vez do próprio valor da propriedade.

O identificador de localidade da parte é usado para escolher um separador de palavras apropriado e é muito importante que você o identifique corretamente. Se o filtro não puder determinar a localidade do texto, ele deverá assumir a localidade do sistema padrão, disponível usando **GetSystemDefaultLCID**. Se você controlar o formato de arquivo e ele não contiver informações de localidade, você deverá adicionar um recurso de usuário para habilitar a identificação de localidade adequada. Usar um separador de palavras incompatível pode levar a uma experiência de consulta inadequada para o usuário.

**GetChunk** só gerencia o acesso a partes e não retorna o valor de texto ou propriedade. Em vez disso, as chamadas subsequentes para **gettext** e **GetValue** recuperam o corpo da parte. **Gettext** retorna partes de texto, que são cadeias de caracteres Unicode, da parte de texto da parte atual \_ . Se a parte atual for muito grande, mais de uma chamada para o método **gettext** poderá ser necessária. Cada chamada para o método **gettext** recupera o texto que segue imediatamente o texto da última chamada para o método **gettext** . Por exemplo, o último caractere de uma chamada pode estar no meio de uma palavra, e o primeiro caractere na próxima chamada continuaria a palavra. Os mecanismos de pesquisa devem lidar com essa situação.

**GetValue** retorna valores de propriedade para a parte do valor da parte atual \_ em estruturas PROPVARIANT, que pode conter uma ampla variedade de tipos de dados. **GetValue** deve alocar a estrutura PROPVARIANT em si usando CoTaskMemAlloc. O chamador de **GetValue** é responsável por liberar memória apontada pelo PROPVARIANT usando PropVariantClear e para liberar a estrutura em si com CoTaskMemFree. Para obter mais informações sobre o PROPVARIANTs, consulte a referência do [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

### <a name="property-values"></a>Valores da propriedade

Os filtros devem produzir no mínimo as propriedades a seguir, que são as colunas padrão na exibição de resultados do WDS.



| GUID                                 | PROPSPEC      | Nome amigável  | Descrição                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 2             | PrimaryTitle   | Título que é exibido para este item.                                                                                                              |
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 4             | PrimaryAuthors | Pessoa mais associada a este item.                                                                                                          |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PrimaryDate   | PrimaryDate    | Data mais importante para o item, como data de recebimento de email ou modificado para arquivos.                                                               |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PerceivedType | PerceivedType  | Tipo de arquivo que está sendo analisado. Deve corresponder a um dos tipos de pesquisa da área de trabalho do Windows listados no [tipo percebido](-search-2x-wds-perceivedtype.md)pelo WDS. |



 

Para itens de texto não criptografado, o WDS extrai todas as propriedades definidas pelo sistema e pelo texto, como tamanho do arquivo ou extensão, incluindo novos tipos de arquivo de texto sem formatação para o índice). Outros tipos de propriedades que podem ser retornadas para o índice incluem:

-   Para arquivos: autor, título, status, palavras-chave
-   Para mídia: álbum, gênero, marca de câmera, data de uso
-   Para comunicações: de, para, CC, importância
-   Para contatos: cargo, telefone comercial, empresa

A lista acima agrupa as propriedades comuns a um tipo percebido especificado; no entanto, qualquer propriedade pode ser usada independentemente do tipo. Por exemplo, a empresa pode ser usada para o nome do empregador de um contato e também pode ser usada para se referir ao nome de um cliente ao qual o arquivo está relacionado. Muitas dessas propriedades são usadas para exibir os resultados da pesquisa no modo de exibição de resultados do WDS. Por exemplo, a propriedade título de um arquivo é mostrada como a coluna principal na exibição de resultados padrão. Os objetos IFilter devem gerar todas as propriedades relacionadas ao tipo de item que estão analisando. As propriedades personalizadas não podem ser adicionadas no WDS 2. x. Para obter uma lista completa das propriedades disponíveis, consulte o [esquema do WDS](-search-2x-wds-schematable.md).

## <a name="filter-add-in-installation"></a>Instalação do suplemento de filtro

A instalação do filtro envolve copiar a DLL para um local apropriado no diretório arquivos de programas e registrá-lo. Os filtros devem implementar o auto-registro para instalação e devem seguir estas diretrizes:

-   O instalador deve usar o EXE ou o instalador MSI.
-   As notas de versão devem ser fornecidas.
-   Uma entrada **Adicionar/remover programas** deve ser criada para cada suplemento instalado.
-   O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.
-   Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.
-   Se um suplemento mais recente tiver substituído o suplemento anterior, deverá haver a capacidade de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão para esse tipo de arquivo ou armazenar novamente.

### <a name="clsids-required-for-registration"></a>CLSIDs necessários para o registro

Há três identificadores de classe, ou CLSIDs, associados a cada filtro. Você precisará gerar um ou mais desses (use uuidgen.exe) para registrar seu suplemento de filtro.

-   O primeiro identifica o manipulador persistente de todos os filtros, o IFilter de IID \_ , que é {89BCB740-6119-101A-BCB7-00DD010655AF}. Esse CLSID é constante para todos os filtros que implementam IFilter.
-   O segundo (o valor da \_ chave IFilter do IID) identifica a implementação do IFilter para o tipo de arquivo. Essa chave contém um valor InprocServer32 que especifica o nome da DLL por caminho e o modelo de Threading. Se o filtro estiver no caminho do sistema, como o diretório system32, um nome de arquivo será suficiente. Caso contrário, esse valor deve ter uma especificação de caminho completo.
-   O terceiro identifica o tipo de arquivo que o filtro processa e é retornado pelo método GetClassID em sua interface IPersist.

> [!Note]
>
> Em versões futuras dos sistemas operacionais da Microsoft, a instalação de arquivos no diretório system32 pode ser mais difícil, portanto, recomendamos que você os instale em arquivos de programas e inclua um caminho completo para o filtro no registro. Por motivos de segurança, também é prudente especificar um caminho completo para a DLL no registro. Caso contrário, uma versão de "cavalo de Troia" de sua DLL poderia ser carregada se estiver no caminho do processo antes da sua versão.

 

### <a name="registration-model"></a>Modelo de registro

Quando o WDS está pronto para filtrar um arquivo, ele procura no registro na extensão do arquivo para determinar qual filtro deve ser carregado. Em seguida, ele segue uma série de links de registro para localizar o nome da DLL de filtro, nesta ordem:

1.  De CLSIDs localizados em:

    **HKEY \_ Current \_ user \\ software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ override \\ RSApp**

    **HKEY \_ Current \_ user \\ software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

2.  No tipo de conteúdo arquivo em:

    **HKEY \_ local \_ Machine \\ software \\ classes \\ \\ tipo de conteúdo de banco de dados MIME \\**

3.  Na extensão de nome de arquivo (igual à API loadifilter do Win32) em:

    **HKEY \_ Current \_ user \\ software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ override \\ RSApp**

    **HKEY \_ Current \_ user \\ software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

    **HKEY \_ classes \_ raiz \\ EXTPERSISTENTHANDLER->CLSID->IFilter do IID \_ ->CLSID**

4.  De padrão em:

    **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

### <a name="to-register-a-filter-add-in"></a>Para registrar um suplemento de filtro

Você precisa fazer um total de oito entradas no registro para registrar seu suplemento de filtro, em que:

-   **. ext** é a nova extensão de nome de arquivo
-   O **GUID \_ 1** pode ser qualquer novo GUID gerado para esta extensão
-   **89BCB740-6119-101A-BCB7-00DD010655AF** é o GUID da interface do IFilter, que é uma constante para todas as implementações de IFilter.

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

2.  Registre a implementação do IFilter com as seguintes chaves e valores:

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  Registre a implementação do IFilter com o Windows Desktop Search com a seguinte chave e valor:

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Esquematable](-search-2x-wds-schematable.md)
</dt> <dt>

[Tipos observados](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Visio**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 