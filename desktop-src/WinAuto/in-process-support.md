---
title: Suporte a In-Process
description: A implementação atual da anotação dinâmica é inteiramente em processo e, consequentemente, permite que apenas elementos da interface do usuário sejam anotados pelo processo que possui os elementos da interface do usuário.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82deaa2edd9a5df9fd36bed745d1c07a5542e12837cd3fc97c3ac0bdeab098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614736"
---
# <a name="in-process-support"></a>Suporte a In-Process

A implementação atual da anotação dinâmica é inteiramente em processo e, consequentemente, permite que apenas elementos da interface do usuário sejam anotados pelo processo que possui os elementos da interface do usuário. Não é possível que um processo anote os elementos da interface do usuário de outro processo.

Observe que isso afeta apenas o ato de definir uma anotação; Ele não interfere na capacidade de os clientes acessarem as propriedades (anotadas ou de outra forma) dos elementos da interface do usuário em outros processos.

 

 




