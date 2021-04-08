---
description: Autenticação de origem da rede
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticação de origem da rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010665"
---
# <a name="network-source-authentication"></a><span data-ttu-id="34920-103">Autenticação de origem da rede</span><span class="sxs-lookup"><span data-stu-id="34920-103">Network Source Authentication</span></span>

<span data-ttu-id="34920-104">Alguns hosts de mídia podem exigir credenciais de usuário de aplicativos cliente antes de permitir o acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="34920-104">Certain media hosts may require user credentials from client applications before allowing access to the media.</span></span> <span data-ttu-id="34920-105">As credenciais do usuário incluem identificação e prova de identificação, como nome de usuário e senha, que são usados pelo servidor de mídia para conceder acesso à fonte de rede que hospeda.</span><span class="sxs-lookup"><span data-stu-id="34920-105">User credentials include identification and proof of identification, such as user name and password, which are used by the media server to grant access to the network source it hosts.</span></span> <span data-ttu-id="34920-106">A fonte de rede pode fornecer autenticação NTLM, Digest ou básica.</span><span class="sxs-lookup"><span data-stu-id="34920-106">The network source can provide NTLM, Digest, or Basic authentication.</span></span>

<span data-ttu-id="34920-107">Aplicativos baseados em Media Foundation podem armazenar credenciais de usuário para uma URL específica em um objeto de *credencial* que expõe a interface [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="34920-107">Applications based on Media Foundation can store user credentials for a specific URL in a *credential* object that exposes the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) interface.</span></span> <span data-ttu-id="34920-108">O objeto Credential armazena credenciais criptografadas e fornece métodos para retornar informações como nome de usuário, senha e domínio.</span><span class="sxs-lookup"><span data-stu-id="34920-108">The credential object stores encrypted credentials and provides methods to return information such as user name, password, and domain.</span></span>

<span data-ttu-id="34920-109">Os objetos de credencial são criados e mantidos em um cache.</span><span class="sxs-lookup"><span data-stu-id="34920-109">The credential objects are created and maintained in a cache.</span></span> <span data-ttu-id="34920-110">O objeto de *cache de credencial* , exposto pela interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , fornece métodos para recuperar os objetos de credencial do cache de credenciais.</span><span class="sxs-lookup"><span data-stu-id="34920-110">The *credential cache* object, exposed by the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface provides methods for retrieving the credential objects from the credential cache.</span></span>

<span data-ttu-id="34920-111">Um aplicativo que dá suporte à autenticação deve implementar a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="34920-111">An application that supports authentication must implement the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="34920-112">Media Foundation não fornece uma implementação padrão dessa interface.</span><span class="sxs-lookup"><span data-stu-id="34920-112">Media Foundation does not provide a default implementation of this interface.</span></span> <span data-ttu-id="34920-113">O Gerenciador de credenciais é responsável por coletar as credenciais necessárias para uma URL da entrada do usuário ou leitura do armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="34920-113">The credential manager is responsible for gathering the required credentials for a URL from user input or reading from persisted storage.</span></span>

<span data-ttu-id="34920-114">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="34920-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="34920-115">Configurando um Gerenciador de credenciais</span><span class="sxs-lookup"><span data-stu-id="34920-115">Setting a Credential Manager</span></span>](setting-a-credential-manager.md)
-   [<span data-ttu-id="34920-116">Usando o cache de credenciais</span><span class="sxs-lookup"><span data-stu-id="34920-116">Using the Credential Cache</span></span>](using-the-credential-cache.md)
-   [<span data-ttu-id="34920-117">Implementando IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="34920-117">Implementing IMFNetCredentialManager</span></span>](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a><span data-ttu-id="34920-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34920-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34920-119">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34920-119">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



