---
title: Escolhendo quando criar objetos acessíveis
description: Os desenvolvedores de servidor podem criar todos os objetos acessíveis dentro de um contêiner quando o contêiner é criado ou podem criar objetos acessíveis dinamicamente.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005810"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Escolhendo quando criar objetos acessíveis

Os desenvolvedores de servidor podem criar todos os objetos acessíveis dentro de um contêiner quando o contêiner é criado ou podem criar objetos acessíveis dinamicamente.

Por exemplo, imagine uma caixa de diálogo com vários controles personalizados. Um servidor cria objetos acessíveis para todos os controles personalizados quando a caixa de diálogo é exibida. No entanto, se um dos controles for uma caixa de combinação personalizada, o servidor aguardará até que um usuário o Selecione para criar objetos acessíveis para os itens que a caixa de combinação contém.

Ao fazer com que o pai Crie objetos acessíveis dinamicamente, os aplicativos usam menos memória do que se todos os objetos acessíveis possíveis foram criados antecipadamente.

 

 




