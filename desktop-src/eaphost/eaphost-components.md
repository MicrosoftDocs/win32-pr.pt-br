---
title: Componentes do EAPHost
description: Saiba mais sobre os três componentes da autenticação do EAPHost. Exiba recursos adicionais disponíveis para usar a autenticação EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454351"
---
# <a name="components-of-eaphost"></a><span data-ttu-id="6abea-104">Componentes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="6abea-104">Components of EAPHost</span></span>

<span data-ttu-id="6abea-105">Este tópico descreve os três componentes da autenticação do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="6abea-105">This topic describes the three components of EAPHost authentication.</span></span>

## <a name="eaphost-components"></a><span data-ttu-id="6abea-106">Componentes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="6abea-106">EAPHost Components</span></span>

<span data-ttu-id="6abea-107">A autenticação EAPHost tem os três componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="6abea-107">EAPHost authentication has the following three components.</span></span>

-   <span data-ttu-id="6abea-108">O suplicante, que faz as solicitações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="6abea-108">The supplicant, which makes the authentication requests.</span></span>
-   <span data-ttu-id="6abea-109">Os métodos EAP de par (ou cliente), que implementam os métodos de EAP específicos e gerenciam a sessão de autenticação no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="6abea-109">The peer (or client) EAP methods, which implement the specific EAP methods and manage the authentication session on the client side.</span></span>
-   <span data-ttu-id="6abea-110">Os métodos EAP do autenticador (ou servidor), que implementam o lado do servidor do protocolo EAP.</span><span class="sxs-lookup"><span data-stu-id="6abea-110">The authenticator (or server) EAP methods, which implement the server side of the EAP protocol.</span></span>

<span data-ttu-id="6abea-111">As APIs suplicantes são chamadas diretamente de um aplicativo que deseja autenticar via EAPHost.</span><span class="sxs-lookup"><span data-stu-id="6abea-111">The supplicant APIs are called directly from an application that wants to authenticate via EAPHost.</span></span> <span data-ttu-id="6abea-112">O método par e as APIs do método autenticador, no entanto, são protótipos de função que devem ser implementados para um tipo de método de autenticação EAP específico, como o protocolo de autenticação handshake de desafio da Microsoft versão 2,0 (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="6abea-112">The peer method and authenticator method APIs, however, are function prototypes that must be implemented for a specific EAP authentication method type - such as the Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2).</span></span>

<span data-ttu-id="6abea-113">Se você estiver criando um aplicativo que usará o EAPHost para autenticação, consulte a referência da [API suplicante do EAPHost](eap-host-supplicant-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6abea-113">If you are authoring an application that will use EAPHost for authentication, please refer to the [EAPHost Supplicant API Reference](eap-host-supplicant-api-reference.md).</span></span>

<span data-ttu-id="6abea-114">Se você estiver criando um novo método de autenticação EAP a ser gerenciado pelo EAPHost, consulte a referência da [API do método par do EAPHost](eap-host-peer-method-api-reference.md) e as [APIs do método de autenticador EAPHost](eaphost-authenticator-method-apis.md).</span><span class="sxs-lookup"><span data-stu-id="6abea-114">If you are authoring a new EAP authentication method to be managed by EAPHost, please refer to the [EAPHost Peer Method API Reference](eap-host-peer-method-api-reference.md) and the [EAPHost Authenticator Method APIs](eaphost-authenticator-method-apis.md).</span></span> <span data-ttu-id="6abea-115">Observe que você estará criando implementações dessas APIs expostas em uma nova DLL que o EAPHost carrega, em vez de chamá-las diretamente.</span><span class="sxs-lookup"><span data-stu-id="6abea-115">Note that you will be creating implementations of these APIs exposed in a new DLL that EAPHost loads, rather than calling them directly.</span></span>

 

 




