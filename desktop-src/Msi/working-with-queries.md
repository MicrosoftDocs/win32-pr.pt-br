---
description: Como o instalador usa um banco de dados relacional, há funções para fazer consultas de linguagem SQL (SQL) para o banco de dados. O procedimento a seguir descreve como usar o SQL para consultar um banco de dados.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Trabalhando com consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921957"
---
# <a name="working-with-queries"></a>Trabalhando com consultas

Como o instalador usa um banco de dados relacional, há funções para fazer consultas de linguagem SQL (SQL) para o banco de dados. O procedimento a seguir descreve como usar o SQL para consultar um banco de dados.

**Para consultar um banco de dados com SQL**

1.  Abra o objeto [**View**](view-object.md) , com a instrução SQL apropriada, chamando a função [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .

    Um objeto [**View**](view-object.md) é a tabela lógica criada pela aplicação de uma consulta a um conjunto de tabelas. As consultas SQL devem aderir à [sintaxe SQL](sql-syntax.md) fornecida pelo instalador. Essa instrução SQL pode conter marcadores de parâmetro que não são especificados até que o objeto de **exibição** seja executado.

2.  Execute o objeto [**View**](view-object.md) chamando a função [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .
3.  Recupere o próximo registro de um objeto [**View**](view-object.md) chamando a função [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .
4.  Modifique o objeto [**View**](view-object.md) chamando a função [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .

    Você também pode validar dados com o [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) passando os sinalizadores apropriados. Se **MsiViewModify** retornar \_ dados inválidos \_ de erro de uma solicitação de validação, os dados subjacentes serão corrompidos.

5.  Obtenha informações detalhadas de erro no objeto [**View**](view-object.md) chamando a função [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .
6.  Feche o objeto [**View**](view-object.md) chamando a função [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .

Para obter mais informações, consulte [exemplos de consultas de banco de dados usando SQL e script](examples-of-database-queries-using-sql-and-script.md).

 

 



