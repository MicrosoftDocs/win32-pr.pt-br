---
description: ICE68 verifica se todos os tipos de ação personalizados necessários para uma instalação são válidos.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754641"
---
# <a name="ice68"></a>ICE68

ICE68 verifica se todos os tipos de ação personalizados necessários para uma instalação são válidos. Falha ao corrigir o erro relatado pelo ICE68 faz com que uma instalação que tenta executar a ação falhe. ICE68 emitirá um aviso se o atributo **msidbCustomActionTypeNoImpersonate** estiver definido sem definir também o atributo **msidbCustomActionTypeInScript** .

## <a name="result"></a>Resultado

ICE68 retornará um erro se um tipo de ação necessário para uma instalação for inválido.

## <a name="example"></a>Exemplo

ICE68 lança o seguinte aviso se uma ação personalizada tiver o conjunto de bits **msidbCustomActionTypeNoImpersonate** no campo tipo da tabela CustomAction sem o **msidbCustomActionTypeInScript** também definido.

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

Para corrigir esse aviso, inclua **msidbCustomActionTypeInScript** (0x400) se a ação personalizada incluir **msidbCustomActionTypeNoImpersonate** (0x800). Caso contrário, o instalador ignora o atributo **msidbCustomActionTypeNoImpersonate** . Para obter mais informações, consulte [Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md).

ICE68 relata o seguinte erro para o exemplo mostrado:

``` syntax
Invalid custom action type for action 'Action1'.
```

1027 não é um tipo de ação válido.

Para corrigir esse erro, escolha um tipo de ação personalizada válido.

[Tabela CustomAction](customaction-table.md) (parcial)



| Ação  | Tipo | Fonte   | Destino     |
|---------|------|----------|------------|
| Action1 | 1027 | Argumento | Component1 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



