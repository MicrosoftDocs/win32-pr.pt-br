---
description: A tabela ODBCSourceAttribute contém informações sobre os atributos de fontes de dados.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Tabela ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d84ca19dfd059df4ff8f79d9409ef23288800f09e84d45e1b55d81bc8641e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082706"
---
# <a name="odbcsourceattribute-table"></a>Tabela ODBCSourceAttribute

A tabela ODBCSourceAttribute contém informações sobre os atributos de fontes de dados.

A tabela ODBCSourceAttribute tem as colunas a seguir.



| Coluna       | Tipo                         | Chave | Nullable |
|--------------|------------------------------|-----|----------|
| Fonte\_ | [Identificador](identifier.md) | Y   | N        |
| Atributo    | [Text](text.md)             | Y   | N        |
| Valor        | [Binário](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>Fonte\_
</dt> <dd>

Nome do token interno para a fonte de dados. Uma chave primária para a tabela.

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute
</dt> <dd>

Nome do atributo de fonte de dados. Uma chave primária para a tabela.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

O valor de cadeia de caracteres localizável para o atributo.

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

 

 



