---
description: ICE52 verifica as propriedades particulares na tabela AppSearch. Consulte sobre propriedades.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829475"
---
# <a name="ice52"></a>ICE52

ICE52 verifica as propriedades particulares na [tabela AppSearch](appsearch-table.md). Consulte [sobre propriedades](about-properties.md).

Ao usar o Windows 2000, todas as propriedades definidas na coluna propriedade da tabela AppSearch devem ser propriedades públicas.

## <a name="result"></a>Resultado

ICE52 posta um aviso se houver uma propriedade privada na tabela AppSearch.

## <a name="example"></a>Exemplo

ICE52 posta o seguinte aviso para o exemplo mostrado.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[Tabela AppSearch](appsearch-table.md)



| Propriedade  | Assinatura  |
|-----------|------------|
| PROPERTY1 | Signature1 |
| Property2 | Signature2 |



 

Para corrigir esse aviso, altere para a propriedade pública personalizada: PROPERTY2.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



