---
description: 'ICE05 valida que determinadas tabelas contêm entradas necessárias. Isso inclui, mas não está restrito a, verificando a tabela de propriedades para as propriedades necessárias: ProductName, ProductLanguage, ProductVersion, ProductCode e manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94766ed0a311243b47c2214ea21de89576d533f0d1fa76f776dedfa3afdc7da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142554"
---
# <a name="ice05"></a>ICE05

ICE05 valida que determinadas tabelas contêm entradas necessárias. Isso inclui, mas não está restrito a, verificando a [tabela](property-table.md) de propriedades para as propriedades necessárias: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)e [**manufacturer**](manufacturer.md).

## <a name="result"></a>Resultado

ICE05 lançará um erro se uma entrada necessária estiver ausente.

## <a name="example"></a>Exemplo

Para o exemplo mostrado, ICE05 relataria que a entrada: ' ProductVersion ' é necessária na tabela ' Property '.

[Tabela de propriedades](property-table.md) (parcial)



| Propriedade                           | Valor     |
|------------------------------------|-----------|
| [**NomeDoProduto**](productname.md) | MyProduct |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



