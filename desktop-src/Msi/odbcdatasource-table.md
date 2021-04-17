---
description: A tabela ODBCDataSource lista as fontes de dados que pertencem à instalação.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabela ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754349"
---
# <a name="odbcdatasource-table"></a>Tabela ODBCDataSource

A tabela ODBCDataSource lista as fontes de dados que pertencem à instalação.

A tabela ODBCDataSource tem as colunas a seguir.



| Coluna            | Tipo                         | Chave | Nullable |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Identificador](identifier.md) | S   | N        |
| Componente\_       | [Identificador](identifier.md) | N   | N        |
| Descrição       | [Text](text.md)             | N   | N        |
| DriverDescription | [Text](text.md)             | N   | N        |
| Registro      | [Inteiro](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>Fonte
</dt> <dd>

Nome do token interno para a fonte de dados. Uma chave primária para a tabela.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na [tabela de componentes](component-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

A descrição registrada para esta fonte de dados. Este valor não pode ser localizado. As descrições da fonte de dados ODBC não podem exceder o \_ comprimento máximo do DSN do SQL \_ \_ .

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription
</dt> <dd>

Driver associado que pode ser preexistente. Este valor não pode ser localizado.

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Falta
</dt> <dd>

Este campo especifica o tipo de registro para a fonte de dados.



| Constante                                      | Hexadecimal | Decimal | Descrição                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **msidbODBCDataSourceRegistrationPerMachine** | 0x000       | 0       | A fonte de dados é registrada por computador. |
| **msidbODBCDataSourceRegistrationPerUser**    | 0x001       | 1       | A fonte de dados é registrada por usuário.    |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



