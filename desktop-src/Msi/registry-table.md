---
description: A tabela Registro contém as informações do Registro que o aplicativo precisa definir no registro do sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabela do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b76fbc52357cdba68dfdcdda37e6edb3032086bf101788db0cdc69c0281264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128986"
---
# <a name="registry-table"></a>Tabela do Registro

A tabela Registro contém as informações do Registro que o aplicativo precisa definir no registro do sistema.

A tabela Registro tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Registro    | [Identificador](identifier.md) | Y   | N        |
| Root        | [Inteiro](integer.md)       | N   | N        |
| Chave         | [RegPath](regpath.md)       | N   | N        |
| Nome        | [Formatado](formatted.md)   | N   | Y        |
| Valor       | [Formatado](formatted.md)   | N   | Y        |
| Componente\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registro
</dt> <dd>

Chave primária usada para identificar um registro do Registro.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Raiz
</dt> <dd>

A chave raiz predefinida para o valor do Registro. Insira um valor de -1 neste campo para tornar a chave raiz dependente do tipo de instalação. Insira um dos outros valores na tabela a seguir para forçar o valor do Registro a ser gravado em uma chave raiz específica.



| Constante                          | Hexadecimal | Decimal | Chave raiz                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nenhum)                            | \- 0x001    | -1      | Se esta for uma instalação por usuário, o valor do Registro será gravado em **HKEY \_ CURRENT \_ USER**. Se esta for uma instalação por computador, o valor do Registro será gravado em **HKEY \_ LOCAL \_ MACHINE.** Observe que uma instalação por computador é especificada definindo a [**propriedade ALLUSERS**](allusers.md) como 1.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ ROOT** O instalador grava ou remove o valor do hive classes **de \\ software \\ HKCU** durante a instalação no contexto de instalação [por usuário.](installation-context.md)<br/> O instalador grava ou remove o valor do hive classes **\\ de software \\ HKLM** durante instalações por computador.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **USUÁRIO ATUAL DO HKEY \_ \_**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **COMPUTADOR LOCAL HKEY \_ \_**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **USUÁRIOS \_ DO HKEY**                                                                                                                                                                                                                                                                                                                              |



 

Observe que é recomendável que as entradas do Registro escritas no hive **HKCU** referenciam um componente com o bit RegistryKeyPath definido na coluna Atributos da [tabela Componente](component-table.md). Isso garante que o instalador grava as entradas necessárias do Registro quando há vários usuários no mesmo computador.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chave
</dt> <dd>

A chave localizável para o valor do Registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Essa coluna contém o nome do valor do Registro (localizável). Se for Nulo, os dados inseridos na coluna Valor serão gravados na chave do Registro padrão.

Se a coluna Valor for Null, as cadeias de caracteres mostradas na tabela a seguir na coluna Nome terão significância especial.



| String | Significado                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | A chave deve ser criada, se ausente, quando o componente é instalado.                                                                                                                            |
| \-     | A chave deve ser excluída, se presente, com todos os seus valores e subkeys, quando o componente for desinstalado.                                                                                     |
| \*     | A chave deve ser criada, se ausente, quando o componente é instalado. Além disso, a chave deve ser excluída, se presente, com todos os seus valores e subkeys, quando o componente for desinstalado. |



 

Observe que a [tabela RemoveRegistry](removeregistry-table.md) deverá ser usada se uma chave do Registro instalada for excluída, com seus valores e subkeys, quando o componente for instalado.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Essa coluna é o valor localizável do Registro. O campo é [Formatado.](formatted.md) Se o valor estiver anexado a um dos prefixos a seguir (ou seja, valor ), o valor será interpretado conforme \# % descrito na tabela. Observe que cada prefixo começa com um sinal de número ( \# ). Se o valor começar com dois ou mais sinais de número consecutivos ( ), o primeiro será ignorado e o valor será interpretado e \# armazenado como uma cadeia de \# caracteres.



| Prefixo | Significado                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#X    | O valor é interpretado e armazenado como um valor hexadecimal (REG \_ BINARY).      |
| \#%    | O valor é interpretado e armazenado como uma cadeia de caracteres expansível (REG \_ EXPAND \_ SZ). |
| \#     | O valor é interpretado e armazenado como um inteiro (REG \_ DWORD).                |



 

-   Se o valor contiver o til de sequência , o valor será interpretado como uma lista de cadeias de caracteres delimitada por nulo \[ ~ \] (REG \_ MULTI \_ SZ). Por exemplo, para especificar uma lista que contém as três cadeias de caracteres a, b e c, use "a \[ ~ \] b \[ ~ \] c".
-   A sequência \[ ~ \] dentro do valor separa as cadeias de caracteres individuais e é interpretada e armazenada como um caractere Nulo.
-   Se um \[ ~ \] preceder a lista de cadeias de caracteres, as cadeias de caracteres deverão ser anexadas a qualquer cadeia de caracteres de valor do Registro existente. Se uma cadeia de caracteres pendente já ocorrer no valor do Registro, a ocorrência original da cadeia de caracteres será removida.
-   Se um seguir o final da lista de cadeias de \[ caracteres, as cadeias de caracteres deverão ser anexadas a qualquer cadeia de caracteres de valor do Registro ~ \] existente. Se uma cadeia de caracteres de prependência já ocorrer no valor do registro, a ocorrência original da cadeia de caracteres será removida.
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

 

 




