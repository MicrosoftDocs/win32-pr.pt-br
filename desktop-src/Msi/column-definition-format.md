---
description: MsiViewGetColumnInfo e a Propriedade ColumnInfo do objeto View usam o formato a seguir para descrever as definições de coluna do banco de dados.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato de definição de coluna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e43e7f70c942fda32bf5003571fa687250e971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169869"
---
# <a name="column-definition-format"></a>Formato de definição de coluna

[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) e a [**Propriedade ColumnInfo**](view-columninfo.md) do objeto [**View**](view-object.md) usam o formato a seguir para descrever as definições de coluna do banco de dados. Cada coluna é descrita por uma cadeia de caracteres no campo de registro correspondente retornado pela função ou propriedade. A cadeia de caracteres de definição consiste em uma única letra que representa o tipo de dados seguido pela largura da coluna (em caracteres quando aplicável; caso contrário, bytes). Uma largura de zero designa uma largura não associada (por exemplo, campos de texto longo e fluxos). Uma letra maiúscula indica que valores nulos são permitidos na coluna.



| Descritor de coluna | Cadeia de caracteres de definição                 |
|-------------------|-----------------------------------|
| &?                | Cadeia de caracteres, comprimento variável (? = 1-255) |
| S0                | Cadeia de caracteres, comprimento variável           |
| i2                | Inteiro curto                     |
| i4                | Long integer                      |
| V0                | Fluxo binário                     |
| m?                | Cadeia de caracteres temporária (? = 0-255)        |
| j?                | Inteiro temporário (? = 0, 1, 2, 4)     |
| O0                | Objeto temporário                  |



 

As cadeias de caracteres usadas para descrever as colunas têm a seguinte relação com as cadeias de caracteres de consulta SQL usadas por CREATE e ALTER. Para obter mais informações, consulte [sintaxe SQL](sql-syntax.md).



| Valor retornado | Sintaxe SQL                |
|----------------|---------------------------|
| S0             | LONGCHAR                  |
| L0             | LONGCHAR LOCALIZÁVEL      |
| & \#           | CHAR ( \# )                  |
| & \#           | CARACTERE ( \# )             |
| debug \#           | CHAR ( \# ) localizável      |
| debug \#           | CARACTERE ( \# ) localizável |
| i2             | BAIXO                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| V0             | OBJECT                    |



 

Se a letra não estiver em letras maiúsculas, a instrução SQL deverá ser anexada com NOT NULL.



| Valor retornado | Sintaxe SQL        |
|----------------|-------------------|
| S0             | LONGCHAR NÃO NULO |



 

O instalador não limita internamente o comprimento de colunas para o valor especificado pelo formato de definição de coluna. Se os dados inseridos em um campo excederem o comprimento de coluna especificado, o pacote não passará na [validação do pacote](package-validation.md). Para passar a validação nesse caso, os dados ou o esquema de banco de dados devem ser alterados. O único meio de alterar o tamanho da coluna de uma tabela padrão é exportando a tabela usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editando o arquivo. IDT exportado e, em seguida, importando a tabela usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Os autores não podem alterar os tipos de dados de coluna, a nulidade ou os atributos de localização de colunas em tabelas padrão. Os autores podem criar tabelas personalizadas com colunas com qualquer atributo de coluna.

Ao usar o [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para mesclar um banco de dados de referência em um banco de dados de destino, os nomes de coluna, o número de chaves primárias e os tipos de dado de coluna devem corresponder. **MsiDatabaseMerge** ignora os atributos de comprimento de coluna e localização. Se uma coluna no banco de dados de referência tiver um comprimento que seja 0 ou maior do que o comprimento da coluna no banco de dados de destino, **MsiDatabaseMerge** aumentará o tamanho da coluna no banco de dados de destino para o comprimento no banco de dados de referência.

Ao usar Mergmod.dll versão 2,0, o aplicativo de um módulo de mesclagem para um arquivo. msi nunca altera o comprimento das colunas ou os tipos de coluna de uma tabela de banco de dados existente. O aplicativo de um módulo de mesclagem pode, no entanto, alterar o esquema de uma tabela de banco de dados existente se o módulo adicionar novas colunas a uma tabela para a qual ela é válida para adicionar colunas. Ao usar uma versão Mergemod.dll inferior à versão 2,0, o aplicativo de um módulo de mesclagem nunca altera o comprimento das colunas e nunca altera o esquema do banco de dados de destino.

 

 



