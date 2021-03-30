---
title: Inserindo o estado carregado
description: Inserindo o estado carregado
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635549"
---
# <a name="entering-the-loaded-state"></a>Inserindo o estado carregado

Quando um objeto entra no estado Loaded, as estruturas na memória que representam o objeto são criadas para que as operações possam ser invocadas nele. O manipulador do objeto ou o servidor em processo é carregado. Esse processo, conhecido como *instanciação*, ocorre quando um objeto é carregado do armazenamento persistente (uma transição do passivo para o estado carregado) ou quando um objeto está sendo criado pela primeira vez.

Internamente, a instanciação é um processo de duas fases. Um objeto da classe apropriada é criado, após o qual um método nesse objeto é chamado para executar a inicialização e conceder acesso aos dados do objeto. O método de inicialização é definido em uma das interfaces com suporte do objeto. O método de inicialização específico chamado depende do contexto no qual o objeto está sendo instanciado e o local dos dados de inicialização.

 

 




