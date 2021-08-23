---
description: A tabela ODBCattribute contém informações sobre os atributos de drivers e tradutores de ODBC (Open Database Connectivity).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabela ODBCattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e67cde1625812d1c5b8af7dc3bd24347891d3a769e24deeb02db7cc44396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943174"
---
# <a name="odbcattribute-table"></a>Tabela ODBCattribute

A tabela ODBCattribute contém informações sobre os atributos de drivers e tradutores de ODBC (Open Database Connectivity).

A tabela ODBCattribute tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Driver\_  | [Identificador](identifier.md) | Y   | N        |
| Atributo | [Text](text.md)             | Y   | N        |
| Valor     | [Binário](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_
</dt> <dd>

Nome de token interno para um driver. Uma chave primária para a tabela. Uma chave estrangeira na [tabela ODBCDriver](odbcdriver-table.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute
</dt> <dd>

Nome do atributo do driver. Uma chave primária para a tabela.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de cadeia de caracteres localizável para o atributo.

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
</dl>

 

 



