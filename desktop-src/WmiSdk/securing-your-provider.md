---
description: Escrever um provedor seguro requer considerar como o provedor é hospedado, como o provedor lida com a representação e garantindo que os usuários sejam verificados quanto aos direitos de acesso aos dados.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Protegendo seu provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782751"
---
# <a name="securing-your-provider"></a><span data-ttu-id="8666d-103">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="8666d-103">Securing Your Provider</span></span>

<span data-ttu-id="8666d-104">Escrever um provedor seguro requer considerar como o provedor é hospedado, como o provedor lida com a representação e garantindo que os usuários sejam verificados quanto aos direitos de acesso aos dados.</span><span class="sxs-lookup"><span data-stu-id="8666d-104">Writing a secure provider requires considering how the provider is hosted, how the provider handles impersonation, and ensuring that users are checked for access rights to data.</span></span> <span data-ttu-id="8666d-105">Você pode proteger os dados no namespace do provedor exigindo que os dados sejam autenticados antes de enviá-los por uma rede.</span><span class="sxs-lookup"><span data-stu-id="8666d-105">You can secure the data in your provider namespace by requiring that data be encrypted authentication before sending it over a network.</span></span> <span data-ttu-id="8666d-106">Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="8666d-106">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="8666d-107">Se um usuário tiver acesso de **\_ gravação total** em qualquer namespace, o usuário poderá criar assinaturas de namespace cruzado para dados em um namespace no qual o usuário é restrito.</span><span class="sxs-lookup"><span data-stu-id="8666d-107">If a user has **FULL\_WRITE** access in any namespace, then the user can create cross-namespace subscriptions for data in a namespace in which the user is restricted.</span></span> <span data-ttu-id="8666d-108">Como um provedor pode ser carregado em qualquer namespace e ser executado em qualquer contexto de segurança, o provedor deve executar suas próprias verificações de acesso para garantir que somente usuários autorizados tenham permissão de acesso a dados ou executem métodos.</span><span class="sxs-lookup"><span data-stu-id="8666d-108">Because a provider can be loaded into any namespace and be executing in any security context, the provider should perform its own access checks to ensure that only authorized users are allowed access to data or to execute methods.</span></span> <span data-ttu-id="8666d-109">Para obter mais informações, consulte [executando verificações de acesso](performing-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="8666d-109">For more information, see [Performing Access Checks](performing-access-checks.md).</span></span>

<span data-ttu-id="8666d-110">Os tópicos a seguir abordam a segurança do provedor:</span><span class="sxs-lookup"><span data-stu-id="8666d-110">The following topics discuss provider security:</span></span>

-   [<span data-ttu-id="8666d-111">Hospedagem e segurança de provedor</span><span class="sxs-lookup"><span data-stu-id="8666d-111">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
-   [<span data-ttu-id="8666d-112">Executando verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="8666d-112">Performing Access Checks</span></span>](performing-access-checks.md)
-   [<span data-ttu-id="8666d-113">Chaves do registro para controlar a segurança do provedor</span><span class="sxs-lookup"><span data-stu-id="8666d-113">Registry Keys for Controlling Provider Security</span></span>](registry-keys-for-controlling-provider-security-.md)
-   [<span data-ttu-id="8666d-114">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="8666d-114">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
-   [<span data-ttu-id="8666d-115">Representando um cliente</span><span class="sxs-lookup"><span data-stu-id="8666d-115">Impersonating a Client</span></span>](impersonating-a-client.md)

<span data-ttu-id="8666d-116">Os tópicos a seguir discutem como os clientes e scripts interagem com a segurança do provedor:</span><span class="sxs-lookup"><span data-stu-id="8666d-116">The following topics discuss how clients and scripts interact with provider security:</span></span>

-   [<span data-ttu-id="8666d-117">Configurando a autenticação no WMI</span><span class="sxs-lookup"><span data-stu-id="8666d-117">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
-   [<span data-ttu-id="8666d-118">Conectando entre diferentes sistemas operacionais</span><span class="sxs-lookup"><span data-stu-id="8666d-118">Connecting Between Different Operating Systems</span></span>](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [<span data-ttu-id="8666d-119">Definindo o nível de segurança do processo padrão usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="8666d-119">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)
-   [<span data-ttu-id="8666d-120">Definindo a segurança do processo do aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="8666d-120">Setting Client Application Process Security</span></span>](setting-client-application-process-security.md)

## <a name="related-topics"></a><span data-ttu-id="8666d-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8666d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8666d-122">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8666d-122">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="8666d-123">Usando o WMI</span><span class="sxs-lookup"><span data-stu-id="8666d-123">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
