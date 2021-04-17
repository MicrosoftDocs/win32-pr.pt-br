---
title: Usuário especificado
description: Usuário especificado
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790626"
---
# <a name="specified-user"></a>Usuário especificado

A especificação de um usuário específico (e a senha do usuário) é a identidade preferida para servidores COM. A razão pela qual essa identidade é preferida é que ninguém precisa ser registrado no computador onde o servidor está sendo executado para que o servidor seja executado, e cada cliente se comunica com a mesma instância do servidor se o servidor registrar sua fábrica de classes como multiutilização. Se o servidor tiver uma GUI, você não deverá escolher essa identidade; Se você fizer isso, o usuário não poderá ver a interface do usuário.

Esse tipo de servidor tem um token primário e pode acessar recursos remotos em que um servidor com a identidade de usuário de inicialização pode não ser capaz de fazer isso. Para obter mais informações sobre representação e tokens de acesso, consulte [níveis de representação](impersonation-levels.md) e [encobrimento](cloaking.md).

A execução como uma conta de usuário fixa é mais segura do que a identidade do usuário interativo, pois essa identidade pode ser atribuída ao aplicativo somente por alguém que tenha a senha do usuário específico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Identidade do Aplicativo](application-identity.md)
</dt> <dt>

[Usuário interativo](interactive-user.md)
</dt> <dt>

[Iniciando usuário](launching-user.md)
</dt> <dt>

[Identidade do serviço](service-identity.md)
</dt> </dl>

 

 




