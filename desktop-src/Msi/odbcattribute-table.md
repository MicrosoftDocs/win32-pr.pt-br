---
description: A tabela ODBCattribute contém informações sobre os atributos de drivers e tradutores de ODBC (Open Database Connectivity).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabela ODBCattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090939"
---
# <a name="odbcattribute-table"></a>Tabela ODBCattribute

A tabela ODBCattribute contém informações sobre os atributos de drivers e tradutores de ODBC (Open Database Connectivity).

A tabela ODBCattribute tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Driver\_  | [Identificador](identifier.md) | S   | N        |
| Atributo | [Text](text.md)             | S   | N        |
| Valor     | [Binário](formatted.md)   | N   | S        |



 

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

 

 



