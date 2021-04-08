---
description: A autenticação é o processo de determinar que os chamadores são realmente quem dizem que são&\# 8212; verificando a autenticidade de uma declaração de identidade.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Autenticação de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd24edf341fc2033807587b01fd37420d781d5f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920447"
---
# <a name="client-authentication"></a>Autenticação de cliente

A autenticação é o processo de determinar que os chamadores são realmente quem dizem que são: verificando a autenticidade de uma declaração de identidade. Em geral, isso pode ser feito pelo servidor e pelo cliente, cada um Autenticando o outro. Mas é especialmente importante para um aplicativo de servidor que esteja autorizando clientes, como com a segurança baseada em função, também para fazer a autenticação. A autenticação de clientes é um pré-requisito para uma política de autorização significativa. Você pode fazer toda a verificação de função desejada, mas se não souber que a identidade do cliente que você está verificando é autêntica, seu aplicativo está basicamente contando com o sistema honra.

Para aplicativos COM+, a autenticação é algo que você pode ativar e configurar administrativamente, após o qual ele funciona de forma transparente para o aplicativo. Você especifica um nível de autenticação administrativamente usando a ferramenta administrativa serviços de componentes ou as funções administrativas. Para obter detalhes sobre como configurar a autenticação, consulte [definindo um nível de autenticação para um aplicativo de servidor](setting-an-authentication-level-for-a-server-application.md) e [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).

A configuração da autenticação significa coisas diferentes, dependendo se o tipo de aplicativo é um aplicativo de servidor ou de biblioteca.

## <a name="setting-authentication-for-com-server-applications"></a>Configurando a autenticação para aplicativos de servidor COM+

Para um aplicativo de servidor do COM+, você define um nível de autenticação que determina como a autenticação será executada quando os clientes chamam os componentes dentro do aplicativo. Você pode escolher entre vários níveis de autenticação que fornecem diferentes graus de segurança, variando de nenhuma autenticação à criptografia de todos os pacotes e de todos os parâmetros de chamada de método. Para obter mais informações, consulte [definindo um nível de autenticação para um aplicativo de servidor](setting-an-authentication-level-for-a-server-application.md).

A segurança mais alta vem com algum custo de desempenho, no entanto, que você deve levar em consideração ao configurar seu aplicativo. O COM+ negociará entre o nível de autenticação especificado pelo cliente e o servidor. A maneira como essa negociação é realizada tem o benefício de permitir que você controle administrativamente a autenticação do lado do servidor. Para obter detalhes, consulte [negociação de nível de autenticação](negotiation-of-authentication-level.md).

> [!Note]  
> Você nunca deve especificar um nível de autenticação programaticamente usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) em um aplicativo com+. O COM+ chama **CoInitializeSecurity** para você e isso pode ser chamado apenas uma vez por processo.

 

Os serviços de autenticação subjacentes são fornecidos pelo COM e pelo Microsoft Windows. Em um serviço de autenticação, um terceiro fornece um certificado para um usuário, atestando a autenticidade da identidade do usuário. Essa certificação é tão confiável quanto a autoridade de certificação e, praticamente da mesma forma que a licença de um driver ou um passaporte serve como um documento de certificação — depende da autoridade do emissor. Para obter informações mais detalhadas sobre os serviços de autenticação, consulte [com e pacotes de segurança](/windows/desktop/com/com-and-security-packages) na documentação do com.

## <a name="setting-authentication-for-com-library-applications"></a>Configurando a autenticação para aplicativos de biblioteca COM+

Para um aplicativo de biblioteca COM+, você habilita ou desabilita a autenticação para determinar se o aplicativo estará sujeito à autenticação executada pelo processo de hospedagem. Embora a autenticação para um aplicativo de biblioteca COM+ seja basicamente controlada pelo processo de hospedagem, você pode configurar o aplicativo de biblioteca para que ele não participe da autenticação. Ou seja, as chamadas para o aplicativo podem ser autenticadas ou não autenticadas e, no último caso, a "autenticação" dos clientes sempre terá sucesso. Para obter mais informações, consulte [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).

Além disso, talvez você queira ou seja necessário autenticar o cliente no banco de dados ou em algum aplicativo downstream – autenticar clientes no aplicativo COM+ sozinho pode não ser suficiente. Se esse for o caso, você precisará representar o cliente para que a identidade do cliente seja propagada downstream. Para obter informações detalhadas sobre a representação, consulte [representação e delegação do cliente](client-impersonation-and-delegation.md). Para obter uma discussão sobre os problemas envolvidos na decisão de fazer a autenticação na camada de dados, consulte [segurança de aplicativos de várias camadas](multi-tier-application-security.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Segurança de aplicativos de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em funções](role-based-security-administration.md)
</dt> <dt>

[Usando a política de restrição de software no COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
