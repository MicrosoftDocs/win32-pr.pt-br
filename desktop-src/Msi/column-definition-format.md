---
description: MsiViewGetColumnInfo e a propriedade ColumnInfo do objeto View usam o formato a seguir para descrever definições de coluna de banco de dados.
ms.assetid: 77379664-26f2-4c1d-8c44-d9be2376efa9
title: Formato de definição de coluna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f0fcad09d0c87b766022602b152c09f466b4d6cddc87467b89ff02793240b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077906"
---
# <a name="column-definition-format"></a>Formato de definição de coluna

[**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) e a [**propriedade ColumnInfo**](view-columninfo.md) do objeto [**View**](view-object.md) usam o formato a seguir para descrever definições de coluna de banco de dados. Cada coluna é descrita por uma cadeia de caracteres no campo de registro correspondente retornado pela função ou propriedade . A cadeia de caracteres de definição consiste em uma única letra que representa o tipo de dados seguido pela largura da coluna (em caracteres quando aplicável, bytes caso contrário). Uma largura de zero designa uma largura não unidas (por exemplo, fluxos e campos de texto longos). Uma letra maiúscula indica que valores nulos são permitidos na coluna.



| Descritor de coluna | Cadeia de caracteres de definição                 |
|-------------------|-----------------------------------|
| s?                | Cadeia de caracteres, comprimento variável (?=1-255) |
| s0                | Cadeia de caracteres, comprimento variável           |
| i2                | Inteiro curto                     |
| i4                | Long integer                      |
| v0                | Fluxo binário                     |
| G?                | Cadeia de caracteres temporária (?=0-255)        |
| J?                | Inteiro temporário (?=0,1,2,4)     |
| O0                | Objeto temporário                  |



 

As cadeias de caracteres usadas para descrever colunas têm a seguinte relação com as SQL de consulta usadas por CREATE e ALTER. Para obter mais informações, [consulte Sintaxe SQL .](sql-syntax.md)



| Valor retornado | Sintaxe SQL                |
|----------------|---------------------------|
| s0             | Longchar                  |
| l0             | LONGCHAR LOCALIZÁVEL      |
| s \#           | CHAR( \# )                  |
| s \#           | CHARACTER( \# )             |
| L \#           | CHAR( \# ) LOCALIZÁVEL      |
| L \#           | CHARACTER( \# ) LOCALIZÁVEL |
| i2             | Curto                     |
| i2             | INT                       |
| i2             | INTEGER                   |
| i4             | LONG                      |
| v0             | OBJECT                    |



 

Se a letra não for maiúscula, a SQL de texto deverá ser anexada com NOT NULL.



| Valor retornado | Sintaxe SQL        |
|----------------|-------------------|
| s0             | LONGCHAR NOT NULL |



 

O instalador não limita internamente o comprimento das colunas ao valor especificado pelo formato de definição de coluna. Se os dados inseridos em um campo excederem o comprimento da coluna especificado, o pacote não passará na [validação do pacote.](package-validation.md) Para passar na validação nesse caso, os dados ou o esquema de banco de dados devem ser alterados. O único meio de alterar o comprimento da coluna de uma tabela padrão é exportando a tabela usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), editando o arquivo .idt exportado e importando a tabela usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Os autores não podem alterar os tipos de dados de coluna, a nulidade ou os atributos de localização de nenhuma coluna em tabelas padrão. Os autores podem criar tabelas personalizadas com colunas que têm atributos de coluna.

Ao usar [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para mesclar um banco de dados de referência em um banco de dados de destino, os nomes de coluna, o número de chaves primárias e os tipos de dados de coluna devem corresponder. **MsiDatabaseMerge** ignora os atributos de localização e comprimento da coluna. Se uma coluna no banco de dados de referência tiver um comprimento 0 ou maior que o comprimento dessa coluna no banco de dados de destino, **MsiDatabaseMerge** aumentará o comprimento da coluna no banco de dados de destino para o comprimento no banco de dados de referência.

Ao usar Mergmod.dll versão 2.0, a aplicação de um módulo de mesclagem para um arquivo .msi nunca altera o comprimento das colunas ou os tipos de coluna de uma tabela de banco de dados existente. No entanto, a aplicação de um módulo de mesclagem poderá alterar o esquema de uma tabela de banco de dados existente se o módulo adicionar novas colunas a uma tabela para a qual é válido adicionar colunas. Ao usar uma Mergemod.dll versão inferior à versão 2.0, a aplicação de um módulo de mesclagem nunca altera o comprimento das colunas e nunca altera o esquema do banco de dados de destino.

 

 



