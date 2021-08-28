---
title: Iniciando usuário
description: Iniciando usuário
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e04163d5229942abff55339d53ba37ec0f8bdc6e9ac60b0893f1d243b22643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736527"
---
# <a name="launching-user"></a>Iniciando usuário

Essa é a configuração padrão para a identidade do aplicativo. Quando o usuário de inicialização é escolhido para a identidade do aplicativo, cada conta de cliente obtém uma nova instância do servidor e cada servidor obtém sua própria [estação de janela](/windows/desktop/winstation/window-stations). Devido às instâncias de servidor separadas, iniciar usuário é a configuração de identidade de proteção de segurança de nível mais alto. No entanto, há limites finitos de consumo de recursos. Além disso, qualquer GUI que o servidor exibe não será vista pelo cliente.

Se o aplicativo tiver a identidade do usuário que está iniciando, ele será executado com um token de representação. Para obter mais informações sobre representação e tokens de acesso, consulte [níveis de representação](impersonation-levels.md) e [encobrimento](cloaking.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Identidade do Aplicativo](application-identity.md)
</dt> <dt>

[Usuário interativo](interactive-user.md)
</dt> <dt>

[Identidade do serviço](service-identity.md)
</dt> <dt>

[Usuário especificado](specified-user.md)
</dt> </dl>

 

 