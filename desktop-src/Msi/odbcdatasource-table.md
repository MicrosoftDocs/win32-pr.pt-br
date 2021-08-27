---
description: A tabela ODBCDataSource lista as fontes de dados que pertencem à instalação.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Tabela ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43426ba7f2dd1214dc205213aa632558bbc44d81db5e6e32f7f7d66f82d30641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082716"
---
# <a name="odbcdatasource-table"></a>Tabela ODBCDataSource

A tabela ODBCDataSource lista as fontes de dados que pertencem à instalação.

A tabela ODBCDataSource tem as colunas a seguir.



| Coluna            | Tipo                         | Chave | Nullable |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Identificador](identifier.md) | Y   | N        |
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

A descrição registrada para esta fonte de dados. Este valor não pode ser localizado. as descrições da fonte de dados ODBC não podem exceder SQL \_ comprimento máximo do \_ DSN \_ .

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

 

 



