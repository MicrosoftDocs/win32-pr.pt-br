---
description: Ações personalizadas destinadas a alterar o estado do sistema devem ser ações personalizadas de execução adiada.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Alterando o estado do sistema usando uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3ec2fafdc6f57041c087903da0c912327c967b3b188127ee1f2ff71db7c1af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086236"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Alterando o estado do sistema usando uma ação personalizada

Ações personalizadas destinadas a alterar o estado do sistema devem ser ações personalizadas de execução adiada. As ações personalizadas que definem propriedades, Estados de recursos, Estados de componentes ou diretórios de destino ou agendam operações do sistema inserindo linhas em tabelas de sequência podem usar a execução imediata com segurança. No entanto, as ações personalizadas que alteram o sistema diretamente ou chamam outro serviço do sistema devem ser adiadas para a hora em que o script de instalação é executado. Para obter mais informações, consulte [ações personalizadas de execução adiada](deferred-execution-custom-actions.md).

Você não deve tentar usar uma ação personalizada de execução imediata para alterar o estado do sistema, pois cada ação personalizada que altera o estado precisa ter uma ação personalizada de reversão correspondente para desfazer a alteração do estado do sistema em uma reversão de instalação. Todas as ações personalizadas de reversão também são medidas personalizadas adiadas e devem preceder a ação que eles desfazem. Para obter mais informações, consulte [Rollback Custom Actions](rollback-custom-actions.md).

 

 



