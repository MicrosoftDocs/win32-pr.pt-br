---
description: Ao criar um pacote de instalação, você pode usar a função MsiViewModify ou o método View. Modify para garantir que os dados inseridos estejam sintaticamente corretos.
ms.assetid: c960e9df-dcd6-44d2-8662-40a1dea81f45
title: Validação interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44184a87f7d8bd28b3603d81bb83ae28ec68471e6c9c849bf9322dc5e968c886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043296"
---
# <a name="internal-validation"></a>Validação interna

Ao criar um pacote de instalação, você pode usar a função [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou o método View. Modify para garantir que os dados inseridos estejam sintaticamente corretos. Para obter mais informações, consulte [**Modificar método**](view-modify.md). No nível mais baixo, uma coluna de tabela de banco de dados pode armazenar inteiros (curtos ou longos), cadeias de caracteres ou dados binários. No entanto, um pacote de instalação requer números inteiros ou cadeias de caracteres específicos em determinadas tabelas. Essas especificações são mantidas na [ \_ tabela de validação](-validation-table.md). Por exemplo, a coluna FileName da [tabela File](file-table.md) é uma coluna de cadeia de caracteres, mas armazena especificamente um nome de arquivo. Portanto, não só se a sua entrada fosse uma cadeia de caracteres, mas também deve seguir os requisitos para nomear arquivos.

Os vários valores de enumeração de validação usados com a função [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) permitem a validação imediata em diferentes níveis. A \_ enumeração de campo MSIMODIFY Validate \_ pode ser usada para validar campos individuais de um registro. Ele não valida chaves estrangeiras. A \_ Enumeração Validate de MSIMODIFY valida uma linha inteira e inclui a validação de chave estrangeira. Se você estiver inserindo uma nova linha em uma tabela, use o MSIMODIFY \_ validar \_ nova enumeração para verificar se você está adicionando dados válidos, bem como usando chaves primárias exclusivas. Uma inserção falhará se as chaves primárias não forem exclusivas. Se uma chamada para **MsiViewModify** com uma das enumerações de validação retornar um erro, você poderá fazer chamadas repetidas para [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) para diagnosticar o problema. **MsiViewGetError** indica a coluna em que o erro ocorreu, bem como o valor de enumeração para ajudar a corrigir o problema. Para obter mais informações, consulte [**GetError Method**](view-geterror.md).

Você também pode usar a validação interna para garantir que outros autores insiram dados corretamente em sua tabela personalizada. Adicione cada uma das colunas da tabela personalizada à tabela de \_ validação usando o nome da tabela personalizada e o nome da coluna como a chave primária. Forneça uma descrição ou finalidade de cada coluna na coluna Descrição da tabela de \_ validação. Insira os requisitos aplicáveis para cada coluna usando as colunas Nullable, MinValue, MaxValue, keyTable, KeyColumn, Category e Set:

-   Se a coluna for anulável, insira um ' Y '. Caso contrário, insira um ' n'.
-   Se a coluna for uma coluna de inteiros e puder conter um intervalo de inteiros, insira esse intervalo usando as colunas MinValue e MaxValue.
-   As colunas de chave estrangeira são identificadas usando as colunas keyTable e KeyColumn.
-   Para colunas de cadeia de caracteres, especifique uma categoria como nome de arquivo, GUID ou identificador. Para obter mais informações, consulte [tipos de dados de coluna](column-data-types.md).
-   Se os dados só puderem pertencer a um número específico de valores (cadeia de caracteres ou inteiro), use a coluna definir para listar os valores aceitáveis.

A seguir está uma lista das colunas (além de tabela, coluna e descrição) na \_ tabela de validação que pode ser preenchida se a coluna for do tipo especificado. (Observe que você não precisa preencher todas as colunas.)



| Tipo    | Colunas                                                          |
|---------|------------------------------------------------------------------|
| Integer | Nullable, MinValue, MaxValue, keyTable, KeyColumn, Set           |
| String  | Nullable, keyTable, KeyColumn, Category, set, MinValue, MaxValue |
| Binário  | Permite valor nulo, categoria (a categoria deve ser "binary")                   |



 

Os ambientes de criação podem fazer uso de MSIMODIFY \_ validar \_ Delete. Essa enumeração pressupõe que você deseja excluir a linha. Nenhuma validação de campo ou de chave estrangeira é executada. Na verdade, essa enumeração executa uma validação de chave estrangeira inversa. Ele verifica a \_ tabela de validação em busca de referências nas colunas keyTable e KeyColumn da tabela à qual a linha "Deleted" pertence. Se houver colunas que listam a tabela que contém a linha "Deleted" como uma possível chave estrangeira, ela percorre essa coluna para ver se algum dos valores referencia valores na linha "Deleted". Um retorno de erro significa que você quebra a integridade relacional do banco de dados excluindo a linha.

 

 



