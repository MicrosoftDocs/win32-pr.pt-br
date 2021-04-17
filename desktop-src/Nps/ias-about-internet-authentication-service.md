---
title: Sobre as extensões do NPS
description: Esta seção descreve como implementar DLLs para estender a funcionalidade do NPS. Ele descreve a interação entre o NPS e as DLLs e apresenta algumas considerações de design sobre as DLLs.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754144"
---
# <a name="about-nps-extensions"></a><span data-ttu-id="3d777-104">Sobre as extensões do NPS</span><span class="sxs-lookup"><span data-stu-id="3d777-104">About NPS Extensions</span></span>

> [!Note]  
> <span data-ttu-id="3d777-105">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3d777-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="3d777-106">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="3d777-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="3d777-107">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="3d777-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="3d777-108">Esta seção descreve como implementar DLLs para estender a funcionalidade do NPS.</span><span class="sxs-lookup"><span data-stu-id="3d777-108">This section describes how to implement DLLs to extend the functionality of NPS.</span></span> <span data-ttu-id="3d777-109">Ele descreve a interação entre o NPS e as DLLs e apresenta algumas considerações de design sobre as DLLs.</span><span class="sxs-lookup"><span data-stu-id="3d777-109">It describes the interaction between NPS and the DLLs, and presents some design considerations regarding the DLLs.</span></span>

<span data-ttu-id="3d777-110">O NPS fornece dois pontos de extensão, um para autenticação e o outro para autorização.</span><span class="sxs-lookup"><span data-stu-id="3d777-110">NPS provides two extension points, one for authentication and the other for authorization.</span></span> <span data-ttu-id="3d777-111">Autenticação refere-se à verificação da identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="3d777-111">Authentication refers to verifying the identity of the user.</span></span> <span data-ttu-id="3d777-112">A autorização refere-se à determinação de quais serviços a rede deve fornecer ao usuário.</span><span class="sxs-lookup"><span data-stu-id="3d777-112">Authorization refers to determining what services the network should provide to the user.</span></span> <span data-ttu-id="3d777-113">Os dois pontos de extensão correspondem a DLLs de extensão de autenticação e DLLs de extensão de autorização.</span><span class="sxs-lookup"><span data-stu-id="3d777-113">The two extension points correspond to Authentication Extension DLLs and Authorization Extension DLLs.</span></span> <span data-ttu-id="3d777-114">Cada ponto de extensão pode dar suporte a várias DLLs.</span><span class="sxs-lookup"><span data-stu-id="3d777-114">Each extension point can support multiple DLLs.</span></span>

<span data-ttu-id="3d777-115">O NPS fornece serviços de autenticação e autorização.</span><span class="sxs-lookup"><span data-stu-id="3d777-115">NPS provides both authentication and authorization services.</span></span> <span data-ttu-id="3d777-116">As DLLs de extensão de autenticação são chamadas pelo NPS antes da autenticação e autorização internas do NPS.</span><span class="sxs-lookup"><span data-stu-id="3d777-116">Authentication Extension DLLs are called by NPS prior to the built-in NPS authentication and authorization.</span></span> <span data-ttu-id="3d777-117">As DLLs de extensão de autorização são chamadas após a autenticação e autorização do NPS.</span><span class="sxs-lookup"><span data-stu-id="3d777-117">Authorization Extension DLLs are called after NPS authentication and authorization.</span></span>

<span data-ttu-id="3d777-118">O diagrama a seguir ilustra o fluxo de pacotes por meio de um servidor RADIUS NPS que é expandido usando DLLs de extensão.</span><span class="sxs-lookup"><span data-stu-id="3d777-118">The following diagram illustrates the flow of packets through an NPS RADIUS server that is expanded using Extension DLLs.</span></span>

![processo de autenticação e autorização do NPS](images/ias03.png)

<span data-ttu-id="3d777-120">Se um DLL de extensão de autenticação retornar ACCEPT, o pacote ignorará a autenticação NPS e vai diretamente para a autorização do NPS.</span><span class="sxs-lookup"><span data-stu-id="3d777-120">If an Authentication Extension DLL returns ACCEPT, the packet skips the NPS authentication and goes directly to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="3d777-121">Quando várias DLLs de extensão de autenticação estão presentes, o restante das DLLs de extensão também pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="3d777-121">When multiple Authentication Extension DLLs are present, the rest of the Extension DLLs might be skipped as well.</span></span> <span data-ttu-id="3d777-122">Consulte [configurando as DLLs de extensão](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3d777-122">See [Setting Up the Extension DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) for more information.</span></span>

 

<span data-ttu-id="3d777-123">Se uma DLL de extensão de autenticação retornar continuar, o pacote vai para a autenticação do NPS e, em seguida, para a autorização do NPS.</span><span class="sxs-lookup"><span data-stu-id="3d777-123">If an Authentication Extension DLL returns CONTINUE, the packet goes to NPS authentication, and then to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="3d777-124">Quando várias DLLs de extensão de autenticação estão presentes, o restante das DLLs de extensão de autenticação são invocadas antes da autenticação NPS.</span><span class="sxs-lookup"><span data-stu-id="3d777-124">When multiple Authentication Extension DLLs are present, the rest of the Authentication Extension DLLs are invoked before NPS authentication.</span></span>

 

<span data-ttu-id="3d777-125">Os tópicos a seguir descrevem as DLLs de extensão com mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="3d777-125">The following topics describe the Extension DLLs in more detail:</span></span>

-   [<span data-ttu-id="3d777-126">Configurando as DLLs de extensão</span><span class="sxs-lookup"><span data-stu-id="3d777-126">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [<span data-ttu-id="3d777-127">Invocando as DLLs de extensão</span><span class="sxs-lookup"><span data-stu-id="3d777-127">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [<span data-ttu-id="3d777-128">Atributos de identificação de usuário</span><span class="sxs-lookup"><span data-stu-id="3d777-128">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)

 

 