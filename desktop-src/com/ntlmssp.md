---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105788922"
---
# <a name="ntlmssp"></a><span data-ttu-id="4ec8e-103">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="4ec8e-103">NTLMSSP</span></span>

<span data-ttu-id="4ec8e-104">NTLMSSP, cujo identificador de serviço de autenticação é RPC \_ C \_ Authn \_ WinNT, é um provedor de suporte de segurança que está disponível em todas as versões do DCOM.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-104">NTLMSSP, whose authentication service identifier is RPC\_C\_AUTHN\_WINNT, is a security support provider that is available on all versions of DCOM.</span></span> <span data-ttu-id="4ec8e-105">Ele usa o protocolo NTLM para autenticação.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-105">It uses the NTLM protocol for authentication.</span></span> <span data-ttu-id="4ec8e-106">O NTLM nunca transmite realmente a senha do usuário para o servidor durante a autenticação.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-106">NTLM never actually transmits the user's password to the server during authentication.</span></span> <span data-ttu-id="4ec8e-107">Portanto, o servidor não pode usar a senha durante a representação para acessar os recursos de rede aos quais o usuário teria acesso.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-107">Therefore, the server cannot use the password during impersonation to access network resources that the user would have access to.</span></span> <span data-ttu-id="4ec8e-108">Somente recursos locais podem ser acessados.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-108">Only local resources can be accessed.</span></span>

<span data-ttu-id="4ec8e-109">O NTLM funciona tanto localmente quanto entre computadores.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-109">NTLM works both locally and across computers.</span></span> <span data-ttu-id="4ec8e-110">Ou seja, se o cliente e o servidor estiverem em computadores diferentes, o NTLM ainda poderá garantir que o cliente seja quem alega ser.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-110">That is, if the client and server are on different computers, NTLM can still make sure the client is who it claims to be.</span></span>

<span data-ttu-id="4ec8e-111">Com o NTLM, a identidade do cliente é representada por um nome de domínio, nome de usuário e senha ou token.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-111">With NTLM, the client's identity is represented by a domain name, user name, and a password or token.</span></span> <span data-ttu-id="4ec8e-112">Quando um servidor chama [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), o nome de domínio e o nome de usuário do cliente são retornados.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-112">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), the client's domain name and user name are returned.</span></span> <span data-ttu-id="4ec8e-113">No entanto, quando um servidor chama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), o token do cliente é retornado.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-113">However, when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="4ec8e-114">Se não houver nenhuma relação de confiança entre o cliente e o servidor e se o servidor tiver uma conta local com o mesmo nome e senha que o cliente, essa conta será usada para representar o cliente.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-114">If there is no trust relationship between client and server and if the server has a local account with the same name and password as the client, that account will be used to represent the client.</span></span>

<span data-ttu-id="4ec8e-115">O NTLM dá suporte à autenticação mútua entre threads e processos cruzados (somente localmente).</span><span class="sxs-lookup"><span data-stu-id="4ec8e-115">NTLM supports mutual authentication cross-thread and cross-process (locally only).</span></span> <span data-ttu-id="4ec8e-116">Se o cliente especificar o nome da entidade de segurança do servidor no formato \\ usuário do domínio em uma chamada para [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), a identidade do servidor deverá corresponder ao nome principal ou a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-116">If the client specifies the principal name of the server in the form domain\\user in a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), the server's identity must match that principal name or the call will fail.</span></span> <span data-ttu-id="4ec8e-117">Se o cliente especificar **NULL**, a identidade do servidor não será verificada.</span><span class="sxs-lookup"><span data-stu-id="4ec8e-117">If the client specifies **NULL**, the server's identity will not be checked.</span></span>

<span data-ttu-id="4ec8e-118">O NTLM adicionalmente dá suporte ao nível de representação entre threads e processos cruzados (somente localmente).</span><span class="sxs-lookup"><span data-stu-id="4ec8e-118">NTLM additionally supports the delegate impersonation level cross-thread and cross-process (locally only).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ec8e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ec8e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ec8e-120">Pacotes de segurança e COM</span><span class="sxs-lookup"><span data-stu-id="4ec8e-120">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 