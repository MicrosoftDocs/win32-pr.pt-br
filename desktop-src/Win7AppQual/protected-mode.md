---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modo protegido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828813"
---
# <a name="protected-mode"></a><span data-ttu-id="da12c-103">Modo protegido</span><span class="sxs-lookup"><span data-stu-id="da12c-103">Protected Mode</span></span>

<span data-ttu-id="da12c-104">A maioria dos recursos de segurança do Windows Internet Explorer 8 está disponível no Internet Explorer 8 para o sistema operacional Windows XP com Service Pack 2 (SP2) e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="da12c-104">Most Windows Internet Explorer 8 security features are available in Internet Explorer 8 for the Windows XP with Service Pack 2 (SP2) operating system and later versions.</span></span> <span data-ttu-id="da12c-105">O modo protegido está disponível apenas para o Windows Vista ou versões posteriores porque ele se baseia nos seguintes recursos de segurança que são novos no Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="da12c-105">Protected Mode is available only for Windows Vista or later versions because it is based on the following security features that are new to Windows Vista:</span></span>

-   <span data-ttu-id="da12c-106">O [UAC (controle de conta de usuário)](https://msdn.microsoft.com/library/aa511445.aspx) facilita a execução sem privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="da12c-106">[User Account Control (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) makes it easy to run without administrator privileges.</span></span> <span data-ttu-id="da12c-107">Quando os usuários executam programas com privilégios de usuário limitados, eles são mais seguros de um ataque do que quando são executados com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="da12c-107">When users run programs with limited user privileges, they are safer from an attack than when they run with administrator privileges.</span></span> <span data-ttu-id="da12c-108">O sistema operacional Windows pode restringir o código mal-intencionado de realizar ações perigosas.</span><span class="sxs-lookup"><span data-stu-id="da12c-108">The Windows operating system can restrict the malicious code from carrying out damaging actions.</span></span>
-   <span data-ttu-id="da12c-109">Um mecanismo de integridade restringe o acesso de gravação a [objetos protegíveis](../secauthz/securable-objects.md) por processos de baixa integridade, da mesma maneira que a associação de grupo de contas de usuário restringe os direitos de usuários para acessar componentes confidenciais do sistema.</span><span class="sxs-lookup"><span data-stu-id="da12c-109">An integrity mechanism restricts write access to [securable objects](../secauthz/securable-objects.md) by lower-integrity processes, in the same way that user account group membership restricts the rights of users to access sensitive system components.</span></span>
-   <span data-ttu-id="da12c-110">O [UIPI (isolamento de privilégios de interface do usuário)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impede que processos enviem mensagens de janela selecionadas e outras APIs de usuário para processos que estão sendo executados com maior integridade.</span><span class="sxs-lookup"><span data-stu-id="da12c-110">[User Interface Privilege Isolation (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) prevents processes from sending selected window messages and other USER APIs to processes that are running with higher integrity.</span></span>

<span data-ttu-id="da12c-111">A infraestrutura de segurança do mecanismo de integridade do Windows permite que o modo protegido forneça ao Windows Internet Explorer os privilégios de que os usuários precisam para navegar na Web, enquanto os privilégios de retenção dos usuários precisam instalar programas silenciosamente ou modificar dados confidenciais do sistema.</span><span class="sxs-lookup"><span data-stu-id="da12c-111">The Windows Integrity Mechanism security infrastructure allows Protected Mode to provide Windows Internet Explorer with the privileges that users need to browse the web, while withholding privileges that users need to install programs silently or modify sensitive system data.</span></span>

<span data-ttu-id="da12c-112">Os usuários podem desabilitar esse recurso por meio de uma caixa de seleção e os administradores podem desabilitá-lo usando Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="da12c-112">Users can disable this feature through a check box, and administrators can disable it by using Group Policy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da12c-113">Você deve desabilitar o recurso somente como uma medida temporária durante a solução de problemas para comparar o comportamento do aplicativo quando o recurso estiver habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="da12c-113">You should disable the feature only as a temporary measure during troubleshooting to compare behavior of the application when the feature is enabled or not.</span></span> <span data-ttu-id="da12c-114">Recomendamos que você mantenha esse recurso permanentemente habilitado.</span><span class="sxs-lookup"><span data-stu-id="da12c-114">We recommended that you keep this feature permanently enabled.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da12c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da12c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da12c-116">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="da12c-116">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
