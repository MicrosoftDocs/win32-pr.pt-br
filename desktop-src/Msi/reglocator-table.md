---
description: A tabela RegLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando o registro ou para procurar uma própria entrada de registro em si. Esta tabela tem as seguintes colunas.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Tabela RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756894"
---
# <a name="reglocator-table"></a>Tabela RegLocator

A tabela RegLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando o registro ou para procurar uma própria entrada de registro em si. Esta tabela tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificador](identifier.md) | S   | N        |
| Root        | [Inteiro](integer.md)       | N   | N        |
| Chave         | [RegPath](regpath.md)       | N   | N        |
| Nome        | [Binário](formatted.md)   | N   | Y        |
| Tipo        | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

O valor no campo assinatura \_ representa uma assinatura exclusiva que é uma chave externa na coluna um da tabela de [assinatura](signature-table.md) . Se essa assinatura estiver presente na tabela de assinatura, a pesquisa será para um arquivo. Se essa assinatura estiver ausente da tabela de assinatura e o valor da coluna de tipo for **msidbLocatorTypeRawValue**, a pesquisa será para o nome da chave do registro apontado pela tabela RegLocator. Caso contrário, a pesquisa será para um diretório apontado pela tabela RegLocator.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Básica
</dt> <dd>

A chave raiz predefinida para o valor do registro.



| Constante                          | Hexadecimal | Decimal | Chave raiz             |
|-----------------------------------|-------------|---------|----------------------|
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | \_raiz de classes hKey \_  |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | HKEY \_ Current \_ User  |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | \_máquina local \_ HKEY |
| **msidbRegistryRootUsers**        | 0x003       | 3       | usuários de HKEY \_          |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves
</dt> <dd>

A chave para o valor do registro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

O nome do valor do registro. Se esse valor for NULL, o valor do valor padrão ou não nomeado da chave, se houver, será recuperado.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

Um valor que determina se o valor do registro é um nome de arquivo, um local de diretório ou um valor de registro bruto.

A tabela a seguir lista os valores válidos. Defina um dos três primeiros valores e **msidbLocatorType64bit** , se necessário. Se a entrada nesse campo estiver ausente, o tipo será definido como 1.



| Constante                      | Hexadecimal | Decimal | Descrição                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | O caminho da chave é um diretório.                                                                                                                                           |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | O caminho da chave é um nome de arquivo.                                                                                                                                           |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | O caminho da chave é um valor do registro.                                                                                                                                      |
| **msidbLocatorType64bit**     | 0x010       | 16      | Defina este bit para que o instalador pesquise a parte de 64 bits do registro. Não defina esse bit para que o instalador pesquise a parte de 32 bits do registro. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que, se o valor no campo Type for **msidbLocatorTypeRawValue**, o instalador definirá o valor da propriedade especificada no campo de propriedade da tabela [AppSearch](appsearch-table.md) como o valor do registro. O instalador adiciona um prefixo ao valor do registro que identifica o tipo de valor do registro. Para obter mais informações sobre tipos de valores de registro, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md).



| Tipo de Registro   | Prefixo adicionado pelo instalador                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| REG \_ sz         | Nenhum, mas se o primeiro caractere do valor do registro for \# , o instalador escapará o caractere prefixando um outro \# .            |
| DWORD           | " \# ", opcionalmente seguido por ' + ' ou '-'                                                                                                  |
| REG \_ expande \_ sz | "\#%"                                                                                                                                   |
| REG \_ multi \_ sz  | Nulo. O instalador define a propriedade com um valor que começa com um NULL e termina com NULL.                                          |
| \_binário reg     | " \# x" no caso de reg \_ Binary, o instalador converte e salva cada dígito hexadecimal (Nibble) como um caractere ASCII prefixado por " \# x". |



 

Normalmente, as colunas nesta tabela não são localizadas. Se um autor decidir procurar produtos em vários idiomas, deverá haver uma entrada separada incluída na tabela para cada idioma.

Observe que não é possível usar a tabela RegLocator para verificar apenas a presença da chave. No entanto, você pode pesquisar o valor padrão de uma chave e recuperar seu valor se ele não estiver vazio.

Para obter mais informações, consulte [pesquisando aplicativos existentes, arquivos, entradas de registro ou entradas de arquivo. ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE80](ice80.md)  
</dl>

 

 
