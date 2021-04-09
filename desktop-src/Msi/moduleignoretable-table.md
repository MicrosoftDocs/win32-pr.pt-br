---
description: Se uma tabela no módulo de mesclagem estiver listada na tabela ModuleIgnoreTable, ela não será mesclada no arquivo. msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Tabela ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171492"
---
# <a name="moduleignoretable-table"></a>Tabela ModuleIgnoreTable

Se uma tabela no módulo de mesclagem estiver listada na tabela ModuleIgnoreTable, ela não será mesclada no arquivo. msi. Se a tabela já existir no arquivo. msi, ela não será modificada pela mesclagem. As tabelas no ModuleIgnoreTable podem, portanto, conter dados desnecessários após a mesclagem.

A tabela ModuleIgnoreTable tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Tabela  | [Identificador](identifier.md) | S   | Não       |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Nome da tabela no módulo de mesclagem que não deve ser mesclado no arquivo. msi.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para minimizar o tamanho do arquivo. msm, é recomendável que os desenvolvedores removam tabelas não utilizadas de módulos destinados a redistribuição, em vez de listar essas tabelas na tabela ModuleIgnoreTable.

 

 



