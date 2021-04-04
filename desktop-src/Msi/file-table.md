---
description: A tabela de arquivos contém uma lista completa de arquivos de origem com seus diversos atributos, ordenados por um identificador exclusivo, não localizado.
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: File Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59838001101bbc65af50bff3f2b00b540976e4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829351"
---
# <a name="file-table"></a>File Table

A tabela de arquivos contém uma lista completa de arquivos de origem com seus diversos atributos, ordenados por um identificador exclusivo, não localizado. Os arquivos podem ser armazenados na mídia de origem como arquivos individuais ou compactados em um [*arquivo de gabinete*](c-gly.md). Para obter mais informações, consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

A tabela de arquivos tem as colunas a seguir.



| Coluna      | Tipo                               | Chave | Nullable |
|-------------|------------------------------------|-----|----------|
| Arquivo        | [Identificador](identifier.md)       | S   | N        |
| Componente\_ | [Identificador](identifier.md)       | N   | N        |
| FileName    | [Filename](filename.md)           | N   | N        |
| FileSize    | [DoubleInteger](doubleinteger.md) | N   | N        |
| Versão     | [Versão](version.md)             | N   | S        |
| Idioma    | [Idioma](language.md)           | N   | S        |
| Atributos  | [Inteiro](integer.md)             | N   | S        |
| Sequência    | [Inteiro](integer.md)             | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>Grupo
</dt> <dd>

Um token não localizado que identifica exclusivamente o arquivo. Este campo não diferencia maiúsculas de minúsculas. Não atribua identificadores a arquivos diferentes que diferem apenas em seu caso.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

A chave externa na primeira coluna da tabela de [componentes](component-table.md). Esse campo identifica o componente que controla o arquivo.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo
</dt> <dd>

O nome do arquivo usado para instalação. O nome pode ser localizado.

Como alguns servidores Web podem diferenciar maiúsculas de minúsculas, o nome de arquivo deve corresponder ao caso dos arquivos de origem exatamente para garantir o suporte a downloads da Internet.

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>Tamanho
</dt> <dd>

O tamanho do arquivo em bytes. Este deve ser um número não negativo.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versão
</dt> <dd>

Este campo é a cadeia de caracteres de versão para um arquivo com versão. Este campo está em branco para arquivos sem versão. A versão do arquivo inserida neste campo deve ser idêntica à versão do arquivo incluído no pacote de instalação.

O campo versão também pode ser definido para conter a chave primária de outro registro na tabela de arquivos. O arquivo referenciado determina a lógica de controle de versão para esse arquivo. Para obter mais informações, consulte [arquivos complementares](companion-files.md). Observe que, se esse arquivo for o caminho de chave para seu componente, ele não deverá ser especificado como um arquivo complementar.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma
</dt> <dd>

Uma lista de IDs de idiomas decimais separados por vírgulas.

Os arquivos de fonte não devem ser criados com uma ID de idioma, pois as fontes não têm um recurso de ID de idioma inserido. Portanto, essa coluna deve ser deixada como nula para arquivos de fonte.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

O inteiro que contém os sinalizadores de bits que representam os atributos do arquivo.

A tabela a seguir mostra a definição do campo de bits.



| Constante                             | Hexadecimal | Decimal | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbFileAttributesReadOnly**      | 0x000001    | 1       | Somente leitura                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbFileAttributesHidden**        | 0x000002    | 2       | Hidden                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesSystem**        | 0x000004    | 4       | Sistema                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesVital**         | 0x000200    | 512     | O arquivo é vital para a operação precisa do componente ao qual ele pertence. Se a instalação de um arquivo com o atributo msidbFileAttributesVital falhar, a instalação será interrompida e será revertida. Nesse caso, o instalador exibe uma caixa de diálogo sem um botão ignorar. Se esse atributo não estiver definido e a instalação do arquivo falhar, o instalador exibirá uma caixa de diálogo com um botão ignorar. Nesse caso, o usuário pode optar por ignorar a falha de instalação do arquivo e continuar. <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1024    | O arquivo contém uma [*soma de verificação*](c-gly.md)válida. Uma soma de verificação é necessária para reparar um arquivo que se tornou corrompido.                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbFileAttributesPatchAdded**    | 0x001000    | 4096    | Esse bit só deve ser adicionado por um patch e se o arquivo estiver sendo adicionado pelo patch.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbFileAttributesNoncompressed** | 0x002000    | 8192    | O tipo de origem do arquivo é descompactado. Se definido, ignore a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) . Se nenhum **msidbFileAttributesNoncompressed** ou **msidbFileAttributesCompressed** estiver definido, o estado de compactação do arquivo será especificado pela propriedade de **Resumo contagem de palavras** . Não defina **msidbFileAttributesNoncompressed** e **msidbFileAttributesCompressed**.                                                                                                                            |
| **msidbFileAttributesCompressed**    | 0x004000    | 16384   | O tipo de origem do arquivo é compactado. Se definido, ignore a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) . Se nenhum **msidbFileAttributesNoncompressed** ou **msidbFileAttributesCompressed** estiver definido, o estado de compactação do arquivo será especificado pela propriedade de **Resumo contagem de palavras** . Não defina **msidbFileAttributesNoncompressed** e **msidbFileAttributesCompressed**.                                                                                                                              |



 

Se o bit **msidbFileAttributesVital** dentro da coluna Attributes estiver definido, e se o componente ao qual o arquivo pertence for selecionado para instalação, o instalador deverá ser capaz de instalar esse arquivo para que a instalação seja concluída com êxito. Se o instalador não puder instalar o arquivo por algum motivo (por exemplo, se o arquivo de origem não puder ser localizado dentro da imagem de origem), uma caixa de diálogo de erro será exibida com as opções "repetir" ou "Cancelar". Para um arquivo que não tem **msidbFileAttributesVital** definido, as opções no caso de um erro de instalação serão "anular", "repetir" e "ignorar" (ou seja, o usuário terá a opção de concluir a instalação com êxito sem instalar o arquivo).

O bit **msidbFileAttributesChecksum** dentro da coluna Attributes deve ser definido para cada arquivo executável na instalação que tem uma [*soma de verificação*](c-gly.md) válida armazenada no cabeçalho do arquivo PE (executável portátil). Somente os arquivos que tiverem este conjunto de bits serão verificados quanto à soma de verificação válida durante uma reinstalação. Para obter mais informações, consulte [**REinstallmode**](reinstallmode.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

Posição da sequência desse arquivo nas imagens de mídia. Essa ordem deve corresponder à ordem dos arquivos no gabinete se os arquivos estiverem compactados. Os inteiros neste campo devem ser iguais ou maiores que 1.

Os números de sequência na coluna sequência são usados para especificar a ordem de instalação de arquivos e a mídia de origem na qual o arquivo está localizado (em conjunto com a [tabela de mídia](media-table.md)). Por exemplo, suponha que um arquivo tenha um número de sequência de 92. Para determinar o disco de origem no qual esse arquivo reside, procure na tabela de mídia a entrada com o menor valor da última sequência maior que 92.

Embora os arquivos compactados recebam números de sequência internos dentro dos gabinetes, esses números absolutos não precisam corresponder aos números de sequência dentro da tabela de arquivos. No entanto, é importante que a sequência de arquivos na tabela de arquivos seja idêntica à sequência dos arquivos dentro dos gabinetes.

Para arquivos que não são compactados, os números de sequência não precisam ser exclusivos. Por exemplo, se todos os arquivos forem descompactados e todos residirem em um disco, você poderá dar a todos os arquivos o mesmo número de sequência.

O limite máximo é de 32767 arquivos. Para criar um pacote de Windows Installer com mais arquivos, consulte [criando um pacote grande](authoring-a-large-package.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [InstallFiles](installfiles-action.md) e [RemoveFiles](removefiles-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

A tabela é gerada inicialmente na lista de arquivos, mas se a compactação de gabinete for usada, a tabela será regenerada a partir da saída do mecanismo de compactação. Para obter mais informações, consulte [arquivos de gabinete](cabinet-files.md).

Para mover um arquivo existente no computador do usuário durante a instalação, use a [ação MoveFiles](movefiles-action.md) e a [tabela MoveFile](movefile-table.md). Para instalar um arquivo em vários locais, use a [ação DuplicateFiles](duplicatefiles-action.md) e a [tabela replicafile](duplicatefile-table.md).

A tabela a seguir resume as possíveis combinações de valores na coluna versão e na coluna idioma. Para obter mais informações, consulte [regras de controle de versão de arquivo](file-versioning-rules.md).



| Versão | Linguagem | Descrição                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 1046     | A versão e o idioma.                                                       |
| 1.2.3.4 | Nulo   | A versão, mas não o idioma.                                                    |
| 1.2.3.4 | 0        | A versão e o idioma são neutros.                                           |
| TestDB  | Nulo   | O arquivo complementar sem idioma associado a ele.                         |
| TestDB  | 1046     | O arquivo e o idioma complementares.                                                |
| Nulo  | 1046     | Nenhuma versão, mas tem uma linguagem associada a ela (ou seja, TypeLib, HelpFile). |



 

Para obter mais informações, consulte a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) e a [Tabela LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE39](ice39.md)  
[ICE42](ice42.md)  
[ICE45](ice45.md)  
[ICE50](ice50.md)  
[ICE51](ice51.md)  
[ICE54](ice54.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE60](ice60.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE76](ice76.md)  
[ICE91](ice91.md)  
</dl>

 

 




