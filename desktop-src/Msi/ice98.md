---
description: ICE98 verifica o campo de descrição da Tabela ODBCDataSource para uma fonte de dados ODBC. Ele usa a função SQLValidDSN para verificar se apenas caracteres válidos são usados e se a descrição não excede o comprimento máximo permitido.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f8a627b057e6c235fdb57a4f2d5d2b2cf6274e528ef4945c6a6323e1888427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894686"
---
# <a name="ice98"></a>ICE98

ICE98 verifica o campo de descrição da Tabela [ODBCDataSource](odbcdatasource-table.md) para uma fonte de dados ODBC. Ele usa a **função SQLValidDSN** para verificar se apenas caracteres válidos são usados e se a descrição não excede o comprimento máximo permitido.

## <a name="result"></a>Resultado

ICE98 posta os avisos a seguir.



| Aviso ICE98                    | Descrição                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O nome da fonte de dados é inválido. | O valor na coluna Descrição da Tabela [ODBCDataSource](odbcdatasource-table.md) contém caracteres inválidos ou é muito longo, o que significa que excede o tamanho máximo de \_ \_ 32 SQL DSN. \_ |



 

## <a name="example"></a>Exemplo

ICE98 relata os seguintes avisos para o exemplo:

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[Tabela ODBCDataSource](odbcdatasource-table.md) (parcial)



| DataSource | Descrição                      |
|------------|----------------------------------|
| BadChar    | !                                |
| TooLong    | <String of length > 32> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> <dt>

[Tabela ODBCDataSource](odbcdatasource-table.md)
</dt> </dl>

 

 



