---
description: ICE98 verifica o campo de descrição da tabela ODBCDataSource para uma fonte de dados ODBC. Ele usa a função SQLValidDSN para verificar se somente caracteres válidos são usados e se a descrição não excede o comprimento máximo permitido.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170056"
---
# <a name="ice98"></a>ICE98

ICE98 verifica o campo de descrição da [tabela ODBCDataSource](odbcdatasource-table.md) para uma fonte de dados ODBC. Ele usa a função **SQLValidDSN** para verificar se somente caracteres válidos são usados e se a descrição não excede o comprimento máximo permitido.

## <a name="result"></a>Resultado

ICE98 posta os seguintes avisos.



| Aviso de ICE98                    | Descrição                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O nome da fonte de dados é inválido. | O valor na coluna Descrição da [tabela ODBCDataSource](odbcdatasource-table.md) contém caracteres inválidos ou é muito longo, o que significa que ele excede o \_ comprimento máximo \_ \_ de DSN do SQL de 32. |



 

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

 

 



