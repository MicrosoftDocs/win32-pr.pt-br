---
description: O ICE36 valida que cada ícone na tabela Icon está listado pelo menos uma vez na propriedade ARPPRODUCTICON ou nas tabelas Classe, ProgId ou Atalho.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c3d951e90ac9f3dc46a564757c1a1d5a1737bf054740e3109a26c8c7b91055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635299"
---
# <a name="ice36"></a>ICE36

ICE36 valida que cada ícone na tabela Ícone está listado pelo menos uma vez na propriedade [**ARPPRODUCTICON**](arpproducticon.md) ou nas tabelas [Classe](class-table.md), [ProgId](progid-table.md)ou [Atalho.](shortcut-table.md)

Durante o anúncio, o instalador instala todos os ícones listados na tabela [Ícone](icon-table.md) no computador do usuário. Ter ícones não .msi na tabela Ícone não impede que a instalação seja executado, no entanto, ele aumenta desnecessariamente o tamanho do arquivo .msi e o tempo e o espaço necessários para anunciar um recurso.

Se um ícone não for referenciado na propriedade ou tabela e não houver nenhuma interface do usuário fornecida para criar uma referência em tempo de execução, você deverá remover o ícone para obter um melhor desempenho.

## <a name="result"></a>Result

ICE36 posta uma mensagem se houver um ícone na tabela Icon que não seja referenciado nas tabelas [Classe](class-table.md), [ProgId](progid-table.md)ou [Atalho](shortcut-table.md) e se não houver nenhuma interface do usuário fornecida para criar essa referência em tempo de run.

## <a name="example"></a>Exemplo

ICE36 relata o seguinte erro para o exemplo mostrado.

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

[Tabela de ícones](icon-table.md) (parcial)



| Name  | Dados     |
|-------|----------|
| Icon1 | Control1 |
| Icon2 | Control2 |
| Icon3 | Control3 |
| Icon4 | Control4 |



 

[Tabela ProgID](progid-table.md) (parcial)



| ProgID    |
|-----------|
| Property1 |



 

[Tabela de Classe](class-table.md) (parcial)



| CLSID                                  |
|----------------------------------------|
| {3E469ABA-3644-11d2-8892-00A0C981B015} |



 

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Ícone\_ |
|-----------|--------|
| Atalho1 | Icon2  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



