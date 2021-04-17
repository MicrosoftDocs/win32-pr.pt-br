---
title: Suporte a In-Process
description: A implementação atual da anotação dinâmica é inteiramente em processo e, consequentemente, permite que apenas elementos da interface do usuário sejam anotados pelo processo que possui os elementos da interface do usuário.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291926"
---
# <a name="in-process-support"></a>Suporte a In-Process

A implementação atual da anotação dinâmica é inteiramente em processo e, consequentemente, permite que apenas elementos da interface do usuário sejam anotados pelo processo que possui os elementos da interface do usuário. Não é possível que um processo anote os elementos da interface do usuário de outro processo.

Observe que isso afeta apenas o ato de definir uma anotação; Ele não interfere na capacidade de os clientes acessarem as propriedades (anotadas ou de outra forma) dos elementos da interface do usuário em outros processos.

 

 




