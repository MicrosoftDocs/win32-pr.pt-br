---
description: A tabela de registro contém as informações de registro que o aplicativo precisa definir no registro do sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabela do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921637"
---
# <a name="registry-table"></a>Tabela do registro

A tabela de registro contém as informações de registro que o aplicativo precisa definir no registro do sistema.

A tabela de registro tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Registro    | [Identificador](identifier.md) | S   | N        |
| Root        | [Inteiro](integer.md)       | N   | N        |
| Chave         | [RegPath](regpath.md)       | N   | N        |
| Nome        | [Binário](formatted.md)   | N   | S        |
| Valor       | [Binário](formatted.md)   | N   | S        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry
</dt> <dd>

Chave primária usada para identificar um registro de registro.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Básica
</dt> <dd>

A chave raiz predefinida para o valor do registro. Insira um valor de-1 neste campo para tornar a chave raiz dependente do tipo de instalação. Insira um dos outros valores na tabela a seguir para forçar o valor do registro a ser gravado em uma chave de raiz específica.



| Constante                          | Hexadecimal | Decimal | Chave raiz                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nenhum)                            | \- 0x001    | -1      | Se essa for uma instalação por usuário, o valor do registro será gravado em **HKEY \_ Current \_ User**. Se essa for uma instalação por máquina, o valor do registro será gravado em **HKEY \_ local \_ Machine**. Observe que uma instalação por computador é especificada definindo a propriedade [**AllUsers**](allusers.md) como 1.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ \_Raiz de classes** o instalador grava ou remove o valor do hive de **\\ \\ classes de software HKCU** durante a instalação no [contexto de instalação](installation-context.md)por usuário.<br/> O instalador grava ou remove o valor do hive **de \\ \\ classes de software HKLM** durante instalações por máquina.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ Current \_ User**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **\_máquina local \_ HKEY**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **usuários de HKEY \_**                                                                                                                                                                                                                                                                                                                              |



 

Observe que é recomendável que as entradas do registro gravadas no hive **HKCU** façam referência a um componente com o conjunto de bits RegistryKeyPath na coluna Attributes da [tabela Component](component-table.md). Isso garante que o instalador grave as entradas de Registro necessárias quando houver vários usuários no mesmo computador.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves
</dt> <dd>

A chave localizável para o valor do registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Esta coluna contém o nome do valor do registro (localizável). Se isso for nulo, os dados inseridos na coluna valor serão gravados na chave do registro padrão.

Se a coluna valor for nula, as cadeias de caracteres mostradas na tabela a seguir na coluna nome terão significado especial.



| String | Significado                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | A chave deve ser criada, se ausente, quando o componente é instalado.                                                                                                                            |
| \-     | A chave deve ser excluída, se estiver presente, com todos os seus valores e subchaves quando o componente for desinstalado.                                                                                     |
| \*     | A chave deve ser criada, se ausente, quando o componente é instalado. Além disso, a chave deve ser excluída, se estiver presente, com todos os seus valores e subchaves, quando o componente for desinstalado. |



 

Observe que a [tabela RemoveRegistry](removeregistry-table.md) deve ser usada se uma chave do registro instalada for excluída, com seus valores e subchaves, quando o componente for instalado.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta coluna é o valor de registro localizável. O campo está [formatado](formatted.md). Se o valor for anexado a um dos seguintes prefixos (ou seja \# % , *valor*), o valor será interpretado conforme descrito na tabela. Observe que cada prefixo começa com um sinal numérico ( \# ). Se o valor começar com dois ou mais sinais numéricos consecutivos ( \# ), o primeiro \# será ignorado e o valor será interpretado e armazenado como uma cadeia de caracteres.



| Prefixo | Significado                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#w.x.y.    | O valor é interpretado e armazenado como um valor hexadecimal (REG \_ Binary).      |
| \#%    | O valor é interpretado e armazenado como uma cadeia de caracteres expansível (REG \_ Expand \_ SZ). |
| \#     | O valor é interpretado e armazenado como um inteiro (REG \_ DWORD).                |



 

-   Se o valor contiver o til da sequência \[ ~ \] , o valor será interpretado como uma lista delimitada por nulo de cadeias de caracteres (reg \_ multi \_ SZ). Por exemplo, para especificar uma lista contendo as três cadeias de caracteres a, b e c, use "a \[ ~ \] b \[ ~ \] c".
-   A sequência \[ ~ \] dentro do valor separa as cadeias de caracteres individuais e é interpretada e armazenada como um caractere nulo.
-   Se um \[ ~ \] precede a lista de cadeias de caracteres, as cadeias devem ser acrescentadas a qualquer cadeia de caracteres de valor de registro existente. Se uma cadeia de caracteres de acréscimo já ocorrer no valor do registro, a ocorrência original da cadeia de caracteres será removida.
-   Se a \[ ~ \] seguir o final da lista de cadeias de caracteres, as cadeias devem ser precedidas a quaisquer cadeias de caracteres de valor de registro existentes. Se uma cadeia de caracteres de prependência já ocorrer no valor do registro, a ocorrência original da cadeia de caracteres será removida.
-   Se um \[ ~ \] estiver no início e no fim ou não no início nem no final da lista de cadeias de caracteres, as cadeias serão substituídas por qualquer cadeia de caracteres de valor de registro existente.
-   Caso contrário, o valor será interpretado e armazenado como uma cadeia de caracteres (REG \_ SZ).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [componentes](component-table.md) que faz referência ao componente que controla a instalação do valor do registro.

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [WriteRegistryValues](writeregistryvalues-action.md) e [RemoveRegistryValues](removeregistryvalues-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

As informações do registro são gravadas no registro do sistema quando o componente correspondente foi selecionado para ser instalado localmente ou executado da origem.

Observe que o instalador remove uma chave do registro depois de remover o último valor ou subchave sob a chave. Para impedir que uma chave de registro vazia seja removida durante a desinstalação, grave um valor fictício sob a chave que você precisa manter e digite + na coluna nome. Se \* estiver na coluna nome, a chave será excluída, com todos os seus valores e subchaves, quando o componente for removido.

Uma ação personalizada pode ser usada para adicionar linhas à tabela do registro durante uma instalação, desinstalação ou Repair Transaction. Essas linhas não persistem na tabela do registro e as informações só estão disponíveis durante a transação atual. A ação personalizada deve, portanto, ser executada em cada instalação, desinstalação ou reparo de transação que exija as informações nessas linhas adicionais. A ação personalizada deve vir antes das ações [RemoveRegistryValues](removeregistryvalues-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) na sequência de ação.

Para obter informações sobre como proteger uma chave do registro, consulte a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) e a [Tabela LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE49](ice49.md)  
[ICE53](ice53.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE70](ice70.md)  
[ICE80](ice80.md)  
</dl>

 

 




