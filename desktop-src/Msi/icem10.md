---
description: ICEM10 verifica se um módulo de mesclagem contém apenas propriedades que são permitidas na Tabela de Propriedades.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb9634ecec212954031e665fa0ebdc3c19856a9bcd02d894eb6e579455d059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129406"
---
# <a name="icem10"></a>ICEM10

ICEM10 verifica se um módulo de mesclagem contém apenas as propriedades permitidas na [Tabela de Propriedades](property-table.md). As seguintes propriedades específicas do produto não são permitidas na Tabela de Propriedades:

-   [**Propriedade ProductLanguage**](productlanguage.md)
-   [**Propriedade ProductCode**](productcode.md)
-   [**Propriedade ProductVersion**](productversion.md)
-   [**Propriedade ProductName**](productname.md)
-   [**Propriedade Manufacturer**](manufacturer.md)

## <a name="result"></a>Resultado

ICEM10 posta um erro quando um módulo de mesclagem contém uma propriedade que não é permitida na [Tabela de Propriedades](property-table.md).

## <a name="example"></a>Exemplo

ICEM10 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

A tabela a seguir mostra uma Tabela de [Propriedades parcial](property-table.md).



| Propriedade                                   | Valores    |
|--------------------------------------------|-----------|
| Color                                      | Vermelho       |
| [**Fabricante**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 1046      |



 

O procedimento a seguir mostra como corrigir erros.

**Para corrigir os erros**

1.  Remova a propriedade '[**Manufacturer**](manufacturer.md)' da [Tabela de Propriedades](property-table.md).
2.  Remova a propriedade '[**ProductLanguage**](productlanguage.md)' da [Tabela de Propriedades](property-table.md).

## <a name="table-used-during-execution"></a>Tabela usada durante a execução

A [Tabela de Propriedades](property-table.md) é usada durante a execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência ice do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



