---
description: Como o instalador usa um banco de dados relacional, há funções para fazer linguagem SQL (SQL) no banco de dados. O procedimento a seguir descreve como usar o SQL consultar um banco de dados.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Trabalhando com consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b6ea5a2f0b962b195fde531216f4b57fd5834162e31c1e34fc9ff1dd3695df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942121"
---
# <a name="working-with-queries"></a>Trabalhando com consultas

Como o instalador usa um banco de dados relacional, há funções para fazer linguagem SQL (SQL) no banco de dados. O procedimento a seguir descreve como usar o SQL consultar um banco de dados.

**Para consultar um banco de dados com SQL**

1.  Abra o [**objeto View,**](view-object.md) com a instrução SQL apropriada, chamando a [**função MsiDatabaseOpenView.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)

    Um [**objeto**](view-object.md) View é a tabela lógica criada aplicando uma consulta a um conjunto de tabelas. SQL consultas devem aderir à [sintaxe SQL fornecida](sql-syntax.md) pelo instalador. Essa SQL pode conter marcadores de parâmetro que não são especificados até que o **objeto View** seja executado.

2.  Execute o [**objeto View**](view-object.md) chamando a [**função MsiViewExecute.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)
3.  Recupere o próximo registro de um [**objeto View**](view-object.md) chamando a [**função MsiViewFetch.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)
4.  Modifique [**o objeto**](view-object.md) View chamando a função [**MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)

    Você também pode validar dados com [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) passando os sinalizadores apropriados. Se **MsiViewModify retornar** DADOS INVÁLIDOS DE ERRO de uma solicitação de \_ \_ validação, os dados subjacentes serão corrompidos.

5.  Obtenha informações de erro detalhadas sobre [**o objeto View**](view-object.md) chamando a função [**MsiViewGetError.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)
6.  Feche o [**objeto View**](view-object.md) chamando a [**função MsiViewClose.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)

Para obter mais informações, consulte [Exemplos de consultas de banco de dados usando SQL script e .](examples-of-database-queries-using-sql-and-script.md)

 

 



