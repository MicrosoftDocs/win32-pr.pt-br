---
title: Contas de logon de serviço
description: Um serviço, como qualquer processo, tem uma identidade de segurança primária que determina os direitos de acesso e privilégios concedidos para recursos locais e de rede.
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, logon de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822251"
---
# <a name="service-logon-accounts"></a><span data-ttu-id="c5e35-104">Contas de logon de serviço</span><span class="sxs-lookup"><span data-stu-id="c5e35-104">Service Logon Accounts</span></span>

<span data-ttu-id="c5e35-105">Um serviço, como qualquer processo, tem uma identidade de segurança primária que determina os direitos de acesso e privilégios concedidos para recursos locais e de rede.</span><span class="sxs-lookup"><span data-stu-id="c5e35-105">A service, like any process, has a primary security identity that determines the granted access rights and privileges for local and network resources.</span></span> <span data-ttu-id="c5e35-106">Essa identidade de segurança, ou contexto de segurança, também determina o potencial que o serviço tem para danificar recursos locais e de rede.</span><span class="sxs-lookup"><span data-stu-id="c5e35-106">This security identity, or security context, also determines the potential the service has for damaging local and network resources.</span></span>

<span data-ttu-id="c5e35-107">O contexto de segurança para um serviço Microsoft Win32 é determinado pela conta de logon que é usada para iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c5e35-107">The security context for a Microsoft Win32 service is determined by the logon account that is used to start the service.</span></span> <span data-ttu-id="c5e35-108">Esta seção discute problemas de programação e práticas recomendadas relacionadas à conta de logon de serviço usada pelos serviços do Win32, com foco em serviços habilitados para diretório.</span><span class="sxs-lookup"><span data-stu-id="c5e35-108">This section discusses programming issues and best practices relating to the service logon account used by Win32 services, with a focus on directory-enabled services.</span></span> <span data-ttu-id="c5e35-109">Esta seção inclui os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="c5e35-109">This section includes the following topics:</span></span>

-   <span data-ttu-id="c5e35-110">[Sobre as contas de logon de serviço](about-service-logon-accounts.md)— uma visão geral das contas de logon de serviço e problemas de programação de contexto de segurança para um serviço Win32.</span><span class="sxs-lookup"><span data-stu-id="c5e35-110">[About Service Logon Accounts](about-service-logon-accounts.md)—An overview of service logon accounts and security context programming issues for a Win32 service.</span></span>
-   <span data-ttu-id="c5e35-111">[Diretrizes para selecionar uma conta de logon de serviço](guidelines-for-selecting-a-service-logon-account.md) para um serviço Win32.</span><span class="sxs-lookup"><span data-stu-id="c5e35-111">[Guidelines for Selecting a Service Logon Account](guidelines-for-selecting-a-service-logon-account.md) for a Win32 service.</span></span>
-   <span data-ttu-id="c5e35-112">[Configuração da conta de usuário de um serviço](setting-up-a-serviceampaposs-user-account.md).</span><span class="sxs-lookup"><span data-stu-id="c5e35-112">[Setting up a Service's User Account](setting-up-a-serviceampaposs-user-account.md).</span></span>
-   <span data-ttu-id="c5e35-113">[Instalar um serviço em um computador host](installing-a-service-on-a-host-computer.md) e especificar a conta de logon do serviço.</span><span class="sxs-lookup"><span data-stu-id="c5e35-113">[Installing a Service on a Host Computer](installing-a-service-on-a-host-computer.md) and specifying the service logon account.</span></span>
-   <span data-ttu-id="c5e35-114">[Concedendo logon como serviço diretamente no computador host](granting-logon-as-service-right-on-the-host-computer.md), concedendo à conta de usuário do serviço o direito de logon como um serviço no computador host.</span><span class="sxs-lookup"><span data-stu-id="c5e35-114">[Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md)—Granting the service's user account the logon as a service right on the host computer.</span></span>
-   <span data-ttu-id="c5e35-115">[Testando se em execução em um controlador de domínio](testing-whether-running-on-a-domain-controller.md)— detectando no momento da instalação se a instância do serviço está sendo instalada em um controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c5e35-115">[Testing Whether Running on a Domain Controller](testing-whether-running-on-a-domain-controller.md)—Detecting at installation time whether the service instance is being installed on a domain controller.</span></span>
-   <span data-ttu-id="c5e35-116">[Concessão de direitos de acesso à conta de logon do serviço](granting-access-rights-to-the-service-logon-account.md)— definindo e mantendo ACEs e associações de grupo para garantir que o sistema conceda acesso ao serviço em execução aos recursos locais e de rede necessários.</span><span class="sxs-lookup"><span data-stu-id="c5e35-116">[Granting Access Rights to the Service Logon Account](granting-access-rights-to-the-service-logon-account.md)—Setting and maintaining ACEs and group memberships to ensure that the system will grant the running service access to the necessary local and network resources.</span></span>
-   <span data-ttu-id="c5e35-117">[Alterar a senha na conta de usuário de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md)— alterar a senha na conta de usuário de um serviço e, ao mesmo tempo, atualizar a senha registrada com o Gerenciador de controle de serviço em cada servidor host no qual o serviço está instalado.</span><span class="sxs-lookup"><span data-stu-id="c5e35-117">[Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md)—Changing the password on a service's user account, and at the same time updating the password registered with the service control manager on each host server on which the service is installed.</span></span>
-   <span data-ttu-id="c5e35-118">[Autenticação mútua usando Kerberos](mutual-authentication-using-kerberos.md)— mantendo o registro SPN (nome da entidade de serviço) no objeto de diretório associado à conta de logon de cada instância do serviço.</span><span class="sxs-lookup"><span data-stu-id="c5e35-118">[Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md)—Maintaining service principal name (SPN) registration on the directory object associated with the logon account of each instance of your service.</span></span> <span data-ttu-id="c5e35-119">Os SPNs permitem que os clientes autentiquem um serviço usando a autenticação mútua do Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c5e35-119">SPNs enable clients to authenticate a service using Kerberos mutual authentication.</span></span>
-   <span data-ttu-id="c5e35-120">[Convertendo formatos de nome de conta de domínio](converting-domain-account-name-formats.md)— por exemplo, convertendo um nome diferenciado em formato de nome de \*\*\*\*\\*\*\* usuário de domínio\* e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="c5e35-120">[Converting Domain Account Name Formats](converting-domain-account-name-formats.md)—For example, converting a distinguished name to *Domain ***\\*** UserName* format, and vice versa.</span></span>

 

 




