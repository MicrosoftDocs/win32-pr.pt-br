---
title: Iniciando usuário
description: Iniciando usuário
ms.assetid: ea5140b6-0a79-4149-b845-4f6388e89104
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6fb60652bff77eb27a33ec8a8a8d40db0f0023
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824004"
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

 

 