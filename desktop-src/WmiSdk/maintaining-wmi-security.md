---
description: A segurança do WMI se concentra na proteção do acesso aos dados do namespace. O WMI primeiro concede acesso a grupos de usuários conforme especificado pelo controle WMI e pelas configurações do DCOM e, em seguida, os provedores determinam se o usuário deve ter acesso aos dados do namespace.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Mantendo a segurança do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25cbf4a29567b263d6bd279aac9e2e6e21c523e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764027"
---
# <a name="maintaining-wmi-security"></a>Mantendo a segurança do WMI

A segurança do WMI se concentra na proteção do acesso aos dados do namespace. O WMI primeiro concede acesso a grupos de usuários conforme especificado pelo [*controle WMI*](gloss-w.md) e pelas configurações do DCOM e, em seguida, os provedores determinam se o usuário deve ter acesso aos dados do namespace.

As seções a seguir são discutidas neste tópico:

-   [Segurança do namespace](#namespace-security)
-   [Configurações de segurança do DCOM (Component Object Model distribuído).](#distributed-component-object-model-dcom-security-settings)
-   [WMI, hosts de serviço compartilhado e autenticação](#wmi-shared-service-hosts-and-authentication)
-   [Segurança para aplicativos e scripts de cliente do WMI](#security-for-wmi-client-scripts-and-applications)
-   [Tópicos relacionados](#related-topics)

## <a name="namespace-security"></a>Segurança do namespace

A segurança do namespace depende dos [*identificadores de segurança do usuário (SID)*](gloss-s.md) padrão do Windows e do [*descritor de segurança*](gloss-s.md) para o namespace do WMI.

Você pode definir a segurança do namespace executando as seguintes ações:

-   Conceda ou negue direitos de acesso a namespaces para usuários que usam o controle WMI ou quando o namespace é criado. Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md) e [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).
-   Use a guia Segurança do controle WMI para estabelecer a auditoria de segurança. A auditoria de segurança resulta em entradas de log de eventos quando um usuário falha ou é bem sucedido em uma ação auditada, como gravar dados em um objeto WMI ou ler o descritor de segurança. Para obter mais informações, consulte [Access to WMI namespaces](access-to-wmi-namespaces.md).
-   Use o arquivo MOF que define o namespace para exigir que um usuário faça uma conexão criptografada. Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>Configurações de segurança do DCOM (Component Object Model distribuído).

A segurança DCOM requer uma configuração de autenticação e uma configuração de representação. Autenticação significa que um processo se identifica para outro. A representação identifica a autoridade que um cliente concede a um servidor para chamar diferentes processos. Durante uma verificação de segurança, o servidor representa o cliente. Para obter mais informações, consulte [Securing C++ clients and Providers](securing-c---clients-and-providers.md) or [Securing scripting clients](securing-scripting-clients.md).

Os scripts e os aplicativos C/C++/C # estabelecem um nível de autenticação e representação quando se conectam a um namespace WMI ou usam as configurações padrão. As conexões com computadores remotos exigem configurações diferentes dos namespaces do WMI no computador local. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, hosts de serviço compartilhado e autenticação

O WMI reside em um host de serviço compartilhado com vários outros serviços em execução na conta NetworkService. Em um processo Svchost, o WMI compartilha a mesma autenticação que os outros processos no host.

As DLLs do provedor são carregadas em processos de host de serviço separados do WMI. A propriedade **HostingModel** na classe do sistema [**\_ \_ Win32Provider**](--win32provider.md) que representa um provedor especifica a conta do sistema sob a qual o provedor é executado. Definir essa propriedade faz com que o provedor seja carregado em um processo de host compartilhado que tenha um nível de privilégio especificado. Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).

## <a name="security-for-wmi-client-scripts-and-applications"></a>Segurança para aplicativos e scripts de cliente do WMI

Scripts e aplicativos devem estabelecer a segurança correta para se conectar a namespaces WMI em computadores locais e remotos. Para obter mais informações, consulte [protegendo clientes e provedores do C++](securing-c---clients-and-providers.md), [protegendo clientes de script](securing-scripting-clients.md)e [protegendo eventos WMI](securing-wmi-events.md).

A tabela a seguir lista os tópicos sobre como manter a segurança do WMI.



| Tópico                                                                                              | Descrição                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Protegendo namespaces WMI](securing-wmi-namespaces.md)                                             | Você pode limitar o acesso a dados de namespace a usuários autorizados por meio do controle WMI.                                                                                      |
| [Protegendo seu provedor](securing-your-provider.md)                                               | Informações sobre como escrever provedores seguros.                                                                                                                           |
| [Protegendo clientes e provedores do C++](securing-c---clients-and-providers.md)                       | Tanto os provedores de C++ quanto os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.                                                         |
| [Protegendo clientes de script](securing-scripting-clients.md)                                       | Scripts e aplicativos de Visual Basic (clientes de automação) devem definir a segurança apropriada para obter acesso a dados e eventos do WMI.                                        |
| [Protegendo eventos WMI](securing-wmi-events.md)                                                     | Os eventos WMI são entregues pelo provedor de eventos a um consumidor temporário ou permanente. Os eventos são entregues na forma de uma instância de uma classe de evento.               |
| [Alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md) | Com as permissões apropriadas, você pode chamar métodos nos objetos WMI que representam objetos protegíveis que lêem ou alteram descritores de segurança em objetos protegíveis. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 



