---
title: Visão geral do cenário do SSO EAPHost
description: Contém dois cenários que demonstram as vantagens de um suplicante habilitado para SSO (logon único).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104084285"
---
# <a name="sso-eaphost-scenario-overview"></a><span data-ttu-id="9a5b7-103">Visão geral do cenário do SSO EAPHost</span><span class="sxs-lookup"><span data-stu-id="9a5b7-103">SSO EAPHost Scenario Overview</span></span>

<span data-ttu-id="9a5b7-104">O tópico a seguir contém dois cenários que demonstram as vantagens de um suplicante habilitado para SSO (logon único).</span><span class="sxs-lookup"><span data-stu-id="9a5b7-104">The following topic contains two scenarios that demonstrate the advantages of a Single-Sign-On (SSO) enabled supplicant.</span></span>

## <a name="about-the-scenarios"></a><span data-ttu-id="9a5b7-105">Sobre os cenários</span><span class="sxs-lookup"><span data-stu-id="9a5b7-105">About the Scenarios</span></span>

<span data-ttu-id="9a5b7-106">O SSO fornece a funcionalidade para reter informações de credenciais de usuário adicionais do que é tradicionalmente armazenado no BLOB de usuário EAP.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-106">SSO provides functionality to retain additional user credential information than is traditionally stored in the EAP user BLOB.</span></span> <span data-ttu-id="9a5b7-107">Ao contrário de outros processos de credenciais, os suplicantes habilitados para SSO podem resolver situações de logon como roaming de AP e alteração de senha sem intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-107">Unlike other credential processes, SSO-enabled supplicants can resolve login situations like AP roaming, and password change without user intervention.</span></span>

## <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="9a5b7-108">Comportamento do cache de PIN do SSO EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="9a5b7-108">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="9a5b7-109">Um suplicante pode tentar a autenticação de rede usando um método EAP baseado em cartão inteligente, como EAP-TLS (Extensible Authentication Protocol Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="9a5b7-109">A supplicant can attempt network authentication using a smartcard-based EAP method such as Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span></span> <span data-ttu-id="9a5b7-110">Nesse e em cenários semelhantes, o suplicante Obtém o PIN do cartão inteligente do usuário e recupera um certificado de usuário para autenticação de rede seguido de uma chamada para WinLogin no computador local.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-110">In this and similar scenarios, the supplicant obtains the smartcard PIN from the user and retrieves a user certificate for network authentication followed by a call to WinLogin on the local computer.</span></span> <span data-ttu-id="9a5b7-111">Após a autenticação bem-sucedida, o suplicante armazena em cache o BLOB do usuário e não armazena informações de PIN do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-111">After successful authentication the supplicant caches the user BLOB, and does not store user PIN information.</span></span>

<span data-ttu-id="9a5b7-112">Quando o usuário faz roaming em uma sessão de local diferente, a retomada e a nova autenticação devem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-112">When the user roams to a different location session resumption and re-authentication must occur.</span></span> <span data-ttu-id="9a5b7-113">Como o certificado não pode ser armazenado antes do logon, a autenticação do usuário falhará e o suplicante liberará o BLOB do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-113">Since the certificate cannot be stored pre-logon, the user authentication will fail and the supplicant flushes the user BLOB.</span></span> <span data-ttu-id="9a5b7-114">Neste ponto, o PIN do usuário é necessário para recuperar o certificado do usuário do cartão inteligente para autenticação de rede.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-114">At this point the user PIN is required to retrieve the user certificate from the smartcard for network authentication.</span></span> <span data-ttu-id="9a5b7-115">Como o SSO armazena em cache o PIN, o certificado pode ser recuperado sem a intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-115">Because SSO caches the PIN, the certificate can be retrieved without user intervention.</span></span> <span data-ttu-id="9a5b7-116">Sem o SSO, o EAP-TLS teria que gerar uma interface do usuário de coleção de PIN novamente.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-116">Without SSO, EAP-TLS would have to raise a PIN collection UI again.</span></span>

<span data-ttu-id="9a5b7-117">Para obter uma abordagem passo a passo, consulte [comportamento de caching de PIN do SSO EAP-TLS](sso-eap-tls-pin-caching-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="9a5b7-117">For a step-by-step approach, see [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span></span>

## <a name="sso-password-change-behavior"></a><span data-ttu-id="9a5b7-118">Comportamento de alteração de senha de SSO</span><span class="sxs-lookup"><span data-stu-id="9a5b7-118">SSO Password Change Behavior</span></span>

<span data-ttu-id="9a5b7-119">Um suplicante pode tentar a autenticação de rede usando um método EAP baseado em senha, como o Microsoft Challenge Handshake Authentication Protocol versão 2,0 (MS-CHAPv2), configurado para usar as credenciais do WinLogin.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-119">A supplicant can attempt network authentication using a password-based EAP method such as Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2), configured to use WinLogin credentials.</span></span> <span data-ttu-id="9a5b7-120">Nesse cenário, o suplicante coleta as credenciais do usuário uma vez e as fornece para o EAPHost para a autenticação de rede.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-120">In this scenario, the supplicant collects user credentials once and provides them to EAPHost for network authentication.</span></span> <span data-ttu-id="9a5b7-121">Após a autenticação de rede bem-sucedida, o suplicante usa o mesmo conjunto de credenciais para WinLogin.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-121">After successful network authentication the supplicant uses the same set of credentials for WinLogin.</span></span>

<span data-ttu-id="9a5b7-122">No entanto, se as credenciais, como a senha do usuário, forem alteradas durante a autenticação de rede sem um suplicante habilitado para SSO, a chamada WinLogin subsequente resultará em falha.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-122">However, if credentials such as the user password were changed during network authentication without an SSO-enabled supplicant, the subsequent WinLogin call will result in failure.</span></span> <span data-ttu-id="9a5b7-123">O SSO retém as novas credenciais e permite um WinLogin bem-sucedido sem intervenção adicional do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a5b7-123">SSO retains the new credentials and allows a successful WinLogin without additional user intervention.</span></span>

<span data-ttu-id="9a5b7-124">Para obter uma abordagem passo a passo, consulte [comportamento de alteração de senha de SSO](sso-password-change-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="9a5b7-124">For a step-by-step approach, see [SSO Password Change Behavior](sso-password-change-behavior-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a5b7-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a5b7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a5b7-126">SSO e PLAP</span><span class="sxs-lookup"><span data-stu-id="9a5b7-126">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




