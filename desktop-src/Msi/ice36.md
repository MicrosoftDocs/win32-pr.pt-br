---
description: ICE36 valida que cada ícone na tabela de ícones é listado pelo menos uma vez na propriedade ARPPRODUCTICON ou nas tabelas de classe, ProgId ou atalho.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011296"
---
# <a name="ice36"></a>ICE36

ICE36 valida que cada ícone na tabela de ícones é listado pelo menos uma vez na propriedade [**ARPPRODUCTICON**](arpproducticon.md) ou nas tabelas de [classe](class-table.md), [ProgID](progid-table.md)ou [atalho](shortcut-table.md) .

Durante o anúncio, o instalador instala todos os ícones listados na [tabela de ícones](icon-table.md) no computador do usuário. Ter ícones não utilizados na tabela de ícones não impede que a instalação seja executada, no entanto, ele aumenta desnecessariamente o tamanho do arquivo. msi e a hora e o espaço necessários para anunciar um recurso.

Se um ícone não for referenciado na propriedade ou tabela e não houver interface do usuário fornecida para criar uma referência em tempo de execução, você deverá remover o ícone para obter um melhor desempenho.

## <a name="result"></a>Resultado

ICE36 posta uma mensagem se houver um ícone na tabela de ícones que não é referenciado nas tabelas de [classe](class-table.md), [ProgID](progid-table.md)ou [atalho](shortcut-table.md) e se não houver nenhuma interface do usuário fornecida para criar essa referência em tempo de execução.

## <a name="example"></a>Exemplo

ICE36 relata o seguinte erro para o exemplo mostrado.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Tabela de ícones](icon-table.md) (parcial)



| Nome  | Dados     |
|-------|----------|
| Icon1 | Control1 |
| Icon2 | Control2 |
| Icon3 | Control3 |
| Icon4 | Control4 |



 

[Tabela ProgID](progid-table.md) (parcial)



| ProgID    |
|-----------|
| Property1 |



 

[Tabela de classes](class-table.md) (parcial)



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | ícone\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



