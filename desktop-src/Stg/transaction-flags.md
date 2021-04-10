---
title: Sinalizadores de transação
description: Um objeto pode ser aberto no modo direto ou transacionado.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159982"
---
# <a name="transaction-flags"></a>Sinalizadores de transação

Um objeto pode ser aberto no modo direto ou transacionado. Quando um objeto é aberto no modo direto, as alterações são feitas imediatamente e permanentemente. Quando um objeto é aberto no modo transacionado, as alterações são armazenadas em buffer para que possam ser explicitamente confirmadas ou revertidas quando a edição for concluída. As alterações confirmadas são salvas no objeto enquanto as alterações revertidas são descartadas. O modo direto é o modo de acesso padrão.

O modo transacionado não é necessário em um objeto de armazenamento pai para usá-lo em um elemento aninhado. Uma transação para um elemento aninhado, no entanto, é aninhada dentro da transação para seu objeto de armazenamento pai. Portanto, as alterações feitas em um objeto filho não podem ser confirmadas até que as feitas no pai sejam confirmadas e ambas permaneçam não confirmadas até que o objeto de armazenamento raiz (o pai de nível superior) seja realmente gravado no disco. Em outras palavras, as alterações se movem para fora: os objetos internos publicam alterações nas transações de seus contêineres imediatos.

 

 




