---
description: ICEM10 verifica se um módulo de mesclagem contém apenas propriedades que são permitidas na tabela de propriedades.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752454"
---
# <a name="icem10"></a>ICEM10

ICEM10 verifica se um módulo de mesclagem contém apenas propriedades que são permitidas na [tabela de propriedades](property-table.md). As propriedades específicas do produto a seguir não são permitidas na tabela de propriedades:

-   [**Propriedade ProductLanguage**](productlanguage.md)
-   [**Propriedade ProductCode**](productcode.md)
-   [**Propriedade ProductVersion**](productversion.md)
-   [**Propriedade ProductName**](productname.md)
-   [**Propriedade manufacturer**](manufacturer.md)

## <a name="result"></a>Resultado

ICEM10 posta um erro quando um módulo de mesclagem contém uma propriedade que não é permitida na [tabela de propriedades](property-table.md).

## <a name="example"></a>Exemplo

ICEM10 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

A tabela a seguir mostra uma [tabela de propriedades](property-table.md)parcial.



| Propriedade                                   | Valores    |
|--------------------------------------------|-----------|
| Cor                                      | Vermelho       |
| [**Manufacturer**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 1046      |



 

O procedimento a seguir mostra como corrigir erros.

**Para corrigir os erros**

1.  Remova a propriedade '[**manufacturer**](manufacturer.md)' da [tabela de propriedades](property-table.md).
2.  Remova a propriedade '[**ProductLanguage**](productlanguage.md)' da [tabela de propriedades](property-table.md).

## <a name="table-used-during-execution"></a>Tabela usada durante a execução

A [tabela de propriedades](property-table.md) é usada durante a execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



