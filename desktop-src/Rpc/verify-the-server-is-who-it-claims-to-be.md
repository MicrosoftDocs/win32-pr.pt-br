---
title: Verifique se o servidor é quem alega ser
description: É melhor usar a autenticação mútua e, assim, verificar a identidade do servidor.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635927"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a>Verifique se o servidor é quem alega ser

É melhor usar a autenticação mútua e, assim, verificar a identidade do servidor. Um exemplo de um erro comum que não faz isso é os aplicativos que têm um serviço local no qual os clientes chamam. Em algumas configurações, um administrador pode decidir que o serviço do sistema não é realmente útil e pode optar por interrompê-lo. Um invasor inventivo em um computador do Terminal Server pode iniciar um processo que escuta no mesmo ponto de extremidade e, quando um cliente se conecta a um ponto de extremidade, permitindo a representação no servidor sem autenticar mutuamente o servidor, o invasor pode representar o cliente e acessar os dados do cliente ou fazer chamadas de rede em nome do cliente. A maioria dos serviços do sistema é executada em uma conta bem conhecida, como LocalSysyem, LocalService ou NetworkService, que pode ser verificada usando a autenticação mútua.

 

 




