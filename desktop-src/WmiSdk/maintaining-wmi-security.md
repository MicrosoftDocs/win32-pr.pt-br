---
description: A segurança do WMI se concentra na proteção do acesso aos dados do namespace. O WMI primeiro concede acesso a grupos de usuários conforme especificado pelas configurações de Controle WMI e DCOM e, em seguida, os provedores determinam se o usuário deve ter acesso aos dados do namespace.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Mantendo a segurança WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79467b3baffd030cae1022f65bc0b8a97242c5e8bbe2f870753a3d3794b8705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818414"
---
# <a name="maintaining-wmi-security"></a>Mantendo a segurança WMI

A segurança do WMI se concentra na proteção do acesso aos dados do namespace. O WMI primeiro concede acesso a grupos de usuários conforme especificado pelas configurações de [*Controle WMI*](gloss-w.md) e DCOM e, em seguida, os provedores determinam se o usuário deve ter acesso aos dados do namespace.

As seções a seguir são discutidas neste tópico:

-   [Segurança do namespace](#namespace-security)
-   [Segurança Component Object Model (DCOM) distribuída Configurações.](#distributed-component-object-model-dcom-security-settings)
-   [WMI, hosts de serviço compartilhado e autenticação](#wmi-shared-service-hosts-and-authentication)
-   [Segurança para aplicativos e scripts de cliente WMI](#security-for-wmi-client-scripts-and-applications)
-   [Tópicos relacionados](#related-topics)

## <a name="namespace-security"></a>Segurança do namespace

A segurança do namespace depende Windows SID (identificadores de segurança do [*usuário)*](gloss-s.md) padrão e do [*descritor de*](gloss-s.md) segurança para o namespace WMI.

Você pode definir a segurança do namespace executando as seguintes ações:

-   Conceda ou negue direitos de acesso a namespaces para usuários que usam o controle WMI ou quando o namespace é criado. Para obter mais informações, consulte [Configurando a segurança do namespace com o](setting-namespace-security-with-the-wmi-control.md) controle WMI e Configurando a segurança do [namespace quando o namespace é criado.](setting-namespace-security-when-the-namespace-is-created.md)
-   Use o controle WMI guia Segurança estabelecer a auditoria de segurança. A auditoria de segurança resulta em entradas de log de eventos quando um usuário falha ou é bem-sucedido em uma ação auditada, como escrever dados em um objeto WMI ou ler o descritor de segurança. Para obter mais informações, [consulte Acesso a namespaces WMI](access-to-wmi-namespaces.md).
-   Use o arquivo MOF que define o namespace para exigir que um usuário faça uma conexão criptografada. Para obter mais informações, consulte [Exigindo uma conexão criptografada com um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>Segurança Component Object Model (DCOM) distribuída Configurações.

A segurança do DCOM requer uma configuração de autenticação e uma configuração de representação. Autenticação significa que um processo se identifica com outro. A representação identifica a autoridade que um cliente concede a um servidor para chamar processos diferentes. Durante uma verificação de segurança, o servidor representa o cliente. Para obter mais informações, consulte Proteger clientes e provedores [C++](securing-c---clients-and-providers.md) ou [Proteger clientes de script.](securing-scripting-clients.md)

Scripts e aplicativos C/C++/C# estabelecem níveis de autenticação e representação quando se conectam a um namespace WMI ou usam as configurações padrão. As conexões com computadores remotos exigem configurações diferentes dos namespaces WMI no computador local. Para obter mais informações, [consulte Conectando-se ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md)

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, hosts de serviço compartilhado e autenticação

O WMI reside em um host de serviço compartilhado com vários outros serviços em execução na conta NetworkService. Em um processo Svchost, o WMI compartilha a mesma autenticação que os outros processos no host.

As DLLs do provedor são carregadas em processos de host de serviço separados do WMI. A **propriedade HostingModel** na classe do sistema [**\_ \_ Win32Provider**](--win32provider.md) que representa um provedor especifica a conta do sistema na qual o provedor é executado. Definir essa propriedade faz com que o provedor seja carregado em um processo de host compartilhado que tem um nível de privilégio especificado. Para obter mais informações, consulte [Hospedagem e segurança do provedor.](provider-hosting-and-security.md)

## <a name="security-for-wmi-client-scripts-and-applications"></a>Segurança para aplicativos e scripts de cliente WMI

Scripts e aplicativos devem estabelecer a segurança correta para se conectar a namespaces WMI em computadores locais e remotos. Para obter mais informações, consulte Proteger clientes e provedores [do C++,](securing-c---clients-and-providers.md)Proteger [clientes de script](securing-scripting-clients.md)e Proteger eventos [WMI](securing-wmi-events.md).

A tabela a seguir lista os tópicos sobre como manter a segurança do WMI.



| Tópico                                                                                              | Descrição                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Proteger namespaces WMI](securing-wmi-namespaces.md)                                             | Você pode limitar o acesso a dados de namespace para usuários autorizados por meio do Controle WMI.                                                                                      |
| [Proteger seu provedor](securing-your-provider.md)                                               | Informações sobre como escrever provedores seguros.                                                                                                                           |
| [Proteger clientes e provedores C++](securing-c---clients-and-providers.md)                       | Os provedores C++ e os aplicativos cliente devem executar muitas das mesmas operações para manter a segurança do WMI.                                                         |
| [Proteger clientes de script](securing-scripting-clients.md)                                       | Scripts e aplicativos Visual Basic (clientes de automação) devem definir a segurança apropriada para obter acesso a dados e eventos WMI.                                        |
| [Proteger eventos WMI](securing-wmi-events.md)                                                     | Os eventos WMI são entregues pelo provedor de eventos a um consumidor temporário ou permanente. Os eventos são entregues na forma de uma instância de uma classe de evento.               |
| [Alterando a segurança de acesso em objetos securáveis](changing-access-security-on-securable-objects.md) | Com as permissões apropriadas, você pode chamar métodos nos objetos WMI que representam objetos que leem ou alteram descritores de segurança em objetos que podem sercuráveis. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 



