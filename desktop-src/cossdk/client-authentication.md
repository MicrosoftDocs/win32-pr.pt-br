---
description: A autenticação é o processo de determinar que os chamadores são, na verdade, quem eles dizem que são&8212; verificando a autenticidade de uma declaração \# de identidade.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Autenticação de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472f16e32cb99f9f2c89c21012f1faa7f96af17878c34d16400f7d505c324398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638986"
---
# <a name="client-authentication"></a>Autenticação de cliente

A autenticação é o processo de determinar que os chamadores são, na verdade, quem eles dizem ser , verificando a autenticidade de uma declaração de identidade. Em geral, isso pode ser feito pelo servidor e pelo cliente, cada um autenticando o outro. Mas é especialmente importante para um aplicativo de servidor que está autorizando clientes, assim como com a segurança baseada em função, a fazer autenticação também. A autenticação de clientes é um pré-requisito para uma política de autorização significativa. Você pode fazer toda a verificação de função que deseja, mas se você não tiver certeza de que a identidade do cliente que está verificando é autenticada, seu aplicativo dependerá basicamente do sistema de confiança.

Para aplicativos COM+, a autenticação é algo que você pode ativar e configurar administrativamente, após o qual ela funciona de forma transparente para o aplicativo. Especifique um nível de autenticação administrativamente usando a ferramenta administrativa serviços de componentes ou as funções Administrativas. Para obter detalhes sobre como definir a autenticação, consulte [Configurando](setting-an-authentication-level-for-a-server-application.md) um nível de autenticação para um aplicativo de servidor e Habilitando [a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).

Definir autenticação significa coisas diferentes, dependendo se o tipo de aplicativo é um aplicativo de servidor ou biblioteca.

## <a name="setting-authentication-for-com-server-applications"></a>Configurando a autenticação para aplicativos de servidor COM+

Para um aplicativo de servidor COM+, você define um nível de autenticação que determina como a autenticação será executada quando os clientes chamarem em componentes dentro do aplicativo. Você pode escolher entre vários níveis de autenticação que fornecem graus variados de segurança, variando de nenhuma autenticação a criptografia de cada pacote e todos os parâmetros de chamada de método. Para obter mais informações, consulte [Definindo um nível de autenticação para um aplicativo de servidor](setting-an-authentication-level-for-a-server-application.md).

A segurança mais alta vem com algum custo de desempenho, no entanto, que você deve levar em consideração ao configurar seu aplicativo. O COM+ negociará entre o nível de autenticação especificado pelo cliente e pelo servidor. A maneira como essa negociação é executada tem o benefício de permitir que você controle administrativamente a autenticação somente do lado do servidor. Para obter detalhes, consulte [Negociação do nível de autenticação](negotiation-of-authentication-level.md).

> [!Note]  
> Você nunca deve especificar um nível de autenticação programaticamente usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) em um aplicativo COM+. COM+ chama **CoInitializeSecurity para** você e isso pode ser chamado apenas uma vez por processo.

 

Os serviços de autenticação subjacentes são fornecidos por COM e Microsoft Windows. Em um serviço de autenticação, um terceiro fornece um certificado para um usuário, atestando a autenticidade da identidade do usuário. Essa certificação é tão confiável quanto a autoridade de certificação e, da mesma forma que uma licença de motorista ou um passaporte, serve como um documento de certificação, depende da autoridade do emissor. Para obter informações mais detalhadas sobre os serviços de autenticação, consulte [PACOTES COM e segurança](/windows/desktop/com/com-and-security-packages) na documentação do COM.

## <a name="setting-authentication-for-com-library-applications"></a>Configurando a autenticação para aplicativos de biblioteca COM+

Para um aplicativo de biblioteca COM+, você habilita ou desabilita a autenticação para determinar se o aplicativo estará sujeito à autenticação executada pelo processo de hospedagem. Embora a autenticação para um aplicativo de biblioteca COM+ seja amplamente controlada pelo processo de hospedagem, você pode configurar o aplicativo de biblioteca para que ele não participe da autenticação. Ou seja, as chamadas para o aplicativo podem ser autenticadas ou não autenticadas e, no último caso, a "autenticação" de clientes sempre é bem-sucedida. Para obter mais informações, consulte [Habilitando a autenticação para um aplicativo de biblioteca.](enabling-authentication-for-a-library-application.md)

Além disso, talvez você queira ou seja necessário autenticar o cliente no banco de dados ou em algum aplicativo downstream, a autenticação de clientes somente no aplicativo COM+ pode não ser suficiente. Se esse for o caso, você precisará representar o cliente para que a identidade do cliente seja propagada downstream. Para obter informações detalhadas sobre representação, consulte [Representação e delegação do cliente.](client-impersonation-and-delegation.md) Para ver uma discussão sobre os problemas envolvidos na decisão de fazer a autenticação na camada de dados, consulte Segurança de aplicativo [de várias camadas.](multi-tier-application-security.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Representação e delegação do cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Segurança do aplicativo de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programático](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em função](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software em COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
