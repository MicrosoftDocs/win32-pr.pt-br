---
title: Usuário interativo
description: O usuário interativo é o usuário que está conectado no momento ao computador em que o servidor COM está em execução.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294521"
---
# <a name="interactive-user"></a>Usuário interativo

O *usuário interativo* é o usuário que está conectado no momento ao computador em que o servidor com está em execução. Se a identidade for definida para ser o usuário interativo, todos os clientes usarão a mesma instância do servidor se o servidor registrar sua fábrica de classes como um uso múltiplo. Se nenhum usuário estiver conectado, o servidor não será executado. Se o servidor tiver uma GUI (interface gráfica do usuário) que o cliente precisa ver, você deverá usar o usuário interativo para a identidade do servidor. No entanto, a escolha dessa identidade tem alguns riscos de segurança porque o servidor é executado sob a identidade do usuário conectado sem o conhecimento ou consentimento do usuário conectado. Além disso, um aplicativo de serviço não pode exibir uma interface do usuário. Para obter mais informações, consulte [serviços interativos](/windows/desktop/Services/interactive-services).

Se um servidor COM estiver configurado para ser executado como usuário interativo, em um ambiente de serviços de terminal, o servidor será iniciado na sessão interativa que corresponde à identidade de usuário do cliente. No entanto, o aplicativo cliente pode usar o moniker de sessão para fazer referência a um objeto fornecido pelo servidor em uma sessão que não corresponde à identidade do cliente. Quando isso é usado, o aplicativo cliente pode especificar qualquer sessão; nesse caso, o servidor será executado como o usuário que possui a sessão, não o usuário que está iniciando. As permissões de acesso padrão nesse cenário não permitem que o usuário de inicialização Chame métodos no servidor. No entanto, os seguintes riscos de segurança permanecem:

-   Se o servidor COM expõe interfaces que não são controladas pelo COM, como portas TCP, pipes nomeados, portas LPC, seções de memória compartilhada e assim por diante, elas podem ser usadas pelo usuário que está iniciando para influenciar o servidor. Objetos COM configurados para execução como o usuário interativo devem reduzir essa superfície de ataque o máximo possível.
-   Objetos COM são livres para definir suas próprias permissões de acesso. Se o objeto definir permissões de acesso, em seu registro AppID ou chamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), para permitir o acesso de usuário de inicialização, o usuário poderá iniciar o servidor para ser executado como outro usuário e, em seguida, acessar o objeto.

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

 

 