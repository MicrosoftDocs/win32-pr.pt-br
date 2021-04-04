---
title: Extensões do servidor de políticas de rede
description: A API de extensões do NPS permite que os desenvolvedores de software gravem DLLs de extensão que podem ser usadas para autenticação, autorização e contabilidade. A API de extensões do NPS dá suporte ao protocolo RADIUS (serviço RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917531"
---
# <a name="network-policy-server-extensions"></a><span data-ttu-id="7d8fc-104">Extensões do servidor de políticas de rede</span><span class="sxs-lookup"><span data-stu-id="7d8fc-104">Network Policy Server Extensions</span></span>

> [!Note]  
> <span data-ttu-id="7d8fc-105">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="7d8fc-106">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="7d8fc-107">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="7d8fc-108">A API de extensões do NPS permite que os desenvolvedores de software gravem DLLs de extensão que podem ser usadas para autenticação, autorização e contabilidade.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-108">The NPS Extensions API enables software developers to write extension DLLs that can be used for authentication, authorization, and accounting.</span></span> <span data-ttu-id="7d8fc-109">A API de extensões do NPS dá suporte ao protocolo RADIUS (serviço RADIUS).</span><span class="sxs-lookup"><span data-stu-id="7d8fc-109">NPS Extensions API supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span>

<span data-ttu-id="7d8fc-110">As DLLs de extensão implementadas usando a API de extensões do NPS podem fornecer controle de sessão e contabilidade avançados.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-110">The extension DLLs implemented using the NPS Extensions API can provide enhanced session control and accounting.</span></span> <span data-ttu-id="7d8fc-111">Essas DLLs podem ser usadas para cenários como controlar o número de sessões de rede do usuário final, usar um servidor de estado e conectar-se a bancos de dados de autenticação de domínio e serviços de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-111">These DLLs can be used for scenarios such as controlling the number of end-user network sessions, using a state server, and connecting to domain authentication databases and Active Directory services.</span></span> <span data-ttu-id="7d8fc-112">As DLLs de extensão podem expandir as autorizações de acesso remoto fornecidas pelo NPS adicionando suas próprias autorizações ao enviar uma resposta de aceitação de volta a um cliente de autenticação.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-112">The extension DLLs can expand the remote access authorizations provided by NPS by adding their own authorizations when sending an Accept response back to an authenticating client.</span></span>

<span data-ttu-id="7d8fc-113">A API de extensões do NPS é aplicável em qualquer ambiente computacional em que a eficiência seria aprimorada para autenticar usuários de discagem por meio de um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-113">NPS Extensions API is applicable in any computing environment where it would improve efficiency to authenticate dial-in users through a remote server.</span></span> <span data-ttu-id="7d8fc-114">Essa tecnologia é especialmente útil para provedores de serviços de Internet (ISPs).</span><span class="sxs-lookup"><span data-stu-id="7d8fc-114">This technology is especially useful for Internet Service Providers (ISPs).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7d8fc-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7d8fc-115">In This Section</span></span>

[<span data-ttu-id="7d8fc-116">Visão geral</span><span class="sxs-lookup"><span data-stu-id="7d8fc-116">Overview</span></span>](/windows/desktop/Nps/ias-about-internet-authentication-service)

<span data-ttu-id="7d8fc-117">Informações gerais sobre o RADIUS e a API de extensões do NPS.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-117">General information about RADIUS and the NPS Extensions API.</span></span>

[<span data-ttu-id="7d8fc-118">Usando</span><span class="sxs-lookup"><span data-stu-id="7d8fc-118">Using</span></span>](/windows/desktop/Nps/ias-using-internet-authentication-service)

<span data-ttu-id="7d8fc-119">Código de exemplo que demonstra como usar a API de extensões do NPS.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-119">Sample code that demonstrates how to use the NPS Extensions API.</span></span>

[<span data-ttu-id="7d8fc-120">Referência</span><span class="sxs-lookup"><span data-stu-id="7d8fc-120">Reference</span></span>](/windows/desktop/Nps/ias-internet-authentication-service-reference)

<span data-ttu-id="7d8fc-121">Documentação de tipos enumerados, funções e estruturas que compõem a API de extensões do NPS.</span><span class="sxs-lookup"><span data-stu-id="7d8fc-121">Documentation of enumerated types, functions, and structures that compose the NPS Extensions API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d8fc-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d8fc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d8fc-123">Servidor de políticas de rede (serviço de autenticação da Internet)</span><span class="sxs-lookup"><span data-stu-id="7d8fc-123">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="7d8fc-124">Protocolo EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="7d8fc-124">Extensible Authentication Protocol (EAP)</span></span>](../eap/eap-start-page.md)
</dt> </dl>

 

 