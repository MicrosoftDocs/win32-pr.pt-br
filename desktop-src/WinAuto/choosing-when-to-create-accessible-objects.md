---
title: Escolhendo quando criar objetos acessíveis
description: Os desenvolvedores de servidor podem criar todos os objetos acessíveis dentro de um contêiner quando o contêiner é criado ou podem criar objetos acessíveis dinamicamente.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a53ee02cb7de574242b3ba9986cdf0ce6068e8495e1ebaf638eed08e9c04b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325975"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Escolhendo quando criar objetos acessíveis

Os desenvolvedores de servidor podem criar todos os objetos acessíveis dentro de um contêiner quando o contêiner é criado ou podem criar objetos acessíveis dinamicamente.

Por exemplo, imagine uma caixa de diálogo com vários controles personalizados. Um servidor cria objetos acessíveis para todos os controles personalizados quando a caixa de diálogo é exibida. No entanto, se um dos controles for uma caixa de combinação personalizada, o servidor aguardará até que um usuário o Selecione para criar objetos acessíveis para os itens que a caixa de combinação contém.

Ao fazer com que o pai Crie objetos acessíveis dinamicamente, os aplicativos usam menos memória do que se todos os objetos acessíveis possíveis foram criados antecipadamente.

 

 




