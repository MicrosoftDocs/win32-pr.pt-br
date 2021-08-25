---
title: Usuário interativo
description: O usuário interativo é o usuário que está conectado no momento ao computador em que o servidor COM está em execução.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d842a468634da0eba31b04317b66185b298fc5a2e44d3567f796dac52dbdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992726"
---
# <a name="interactive-user"></a>Usuário interativo

O *usuário interativo* é o usuário que está conectado no momento ao computador em que o servidor COM está em execução. Se a identidade for definida como o usuário interativo, todos os clientes usarão a mesma instância do servidor se o servidor registrar sua fábrica de classes como multiusuária. Se nenhum usuário estiver conectado, o servidor não será executado. Se o servidor tiver uma GUI (interface gráfica do usuário) que o cliente precisa ver, você deverá usar o usuário interativo para a identidade do servidor. No entanto, escolher essa identidade traz alguns riscos de segurança porque o servidor é executado sob a identidade do usuário conectado sem o conhecimento ou o consentimento do usuário conectado. Além disso, um aplicativo de serviço não pode exibir uma interface do usuário. Para obter mais informações, consulte [Serviços Interativos.](/windows/desktop/Services/interactive-services)

Se um servidor COM estiver configurado para ser executado como o usuário interativo, em um ambiente de serviços de terminal, o servidor será lançado na sessão interativa que corresponde à identidade do usuário do cliente. No entanto, o aplicativo cliente pode usar o moniker de sessão para referenciar um objeto fornecido pelo servidor em uma sessão que não corresponder à identidade do cliente. Quando isso é usado, o aplicativo cliente pode especificar qualquer sessão, caso em que o servidor será executado como o usuário proprietário da sessão, não o usuário inicial. As permissões de acesso padrão nesse cenário não permitiriam que o usuário de lançamento chamasse métodos no servidor. No entanto, os seguintes riscos de segurança permanecem:

-   Se o servidor COM expõe interfaces que não são controladas pelo COM, como portas TCP, pipes nomeados, portas LPC, seções de memória compartilhada e assim por diante, elas podem ser usadas pelo usuário de lançamento para influenciar o servidor. Objetos COM configurados para executar, pois o usuário interativo deve reduzir essa superfície de ataque o máximo possível.
-   Os objetos COM são gratuitos para definir suas próprias permissões de acesso. Se o objeto define permissões de acesso, seja em seu registro AppID ou chamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), para permitir o acesso do usuário de lançamento, o usuário poderá iniciar o servidor para ser executado como outro usuário e, em seguida, acessar o objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Identidade do Aplicativo](application-identity.md)
</dt> <dt>

[Iniciando usuário](launching-user.md)
</dt> <dt>

[Identidade do serviço](service-identity.md)
</dt> <dt>

[Usuário especificado](specified-user.md)
</dt> </dl>

 

 