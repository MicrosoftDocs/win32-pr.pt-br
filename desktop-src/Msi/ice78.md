---
description: ICE78 verifica se a tabela AdvtUISequence não existe ou está vazia. Isso é necessário porque nenhuma interface do usuário é permitida durante o anúncio.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39061872b716c9cc05e983d72615bf287683fd9c316df5661c3085e545169f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638116"
---
# <a name="ice78"></a>ICE78

ICE78 verifica se a [tabela AdvtUISequence](advtuisequence-table.md) não existe ou está vazia. Isso é necessário porque nenhuma interface do usuário é permitida durante o anúncio.

## <a name="result"></a>Resultado

ICE78 lançará um erro se a tabela AdvtUISequence existir e não estiver vazia.

## <a name="example"></a>Exemplo

ICE78 relata o seguinte erro para o exemplo:

Ação ' Action1 ' encontrada na tabela AdvtUISequence. Nenhuma interface do usuário é permitida durante o anúncio. Portanto, a tabela AdvtUISequence deve estar vazia ou não estar presente.

[Tabela AdvtUISequence](advtuisequence-table.md)(parcial)



| Ação  | Condição | Sequência |
|---------|-----------|----------|
| Action1 | TRUE      | 1        |



 

Para corrigir o erro, remova "Action1" da tabela ou remova a tabela.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



