---
title: Objetos de dados do servidor
description: A API de SDO (objetos de dados do servidor) possibilita a configuração e a administração programaticamente de um sistema que executa o NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779597"
---
# <a name="server-data-objects"></a><span data-ttu-id="1bede-103">Objetos de dados do servidor</span><span class="sxs-lookup"><span data-stu-id="1bede-103">Server Data Objects</span></span>

> [!Note]  
> <span data-ttu-id="1bede-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1bede-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1bede-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="1bede-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1bede-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="1bede-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1bede-107">A API de SDO (objetos de dados do servidor) possibilita a configuração e a administração programaticamente de um sistema que executa o NPS.</span><span class="sxs-lookup"><span data-stu-id="1bede-107">The Server Data Objects (SDO) API makes it possible to programmatically configure and administer a system running NPS.</span></span> <span data-ttu-id="1bede-108">Usando o SDO, um desenvolvedor também pode escrever aplicativos que administrem perfis e políticas de acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="1bede-108">Using SDO, a developer can also write applications that administer remote access policies and profiles.</span></span> <span data-ttu-id="1bede-109">As políticas de acesso remoto e os perfis são usados pelo RRAS (serviço de roteamento e acesso remoto), bem como pelo NPS, para determinar se um cliente remoto tem permissão para se conectar a um NAS (servidor de acesso à rede).</span><span class="sxs-lookup"><span data-stu-id="1bede-109">The remote access policies and profiles are used by the Routing and Remote Access Service (RRAS) as well as NPS to determine whether a remote client is allowed to connect to a network access server (NAS).</span></span>

<span data-ttu-id="1bede-110">A API de SDO é aplicável em qualquer ambiente que usa políticas de acesso remoto ou NPS.</span><span class="sxs-lookup"><span data-stu-id="1bede-110">The SDO API is applicable in any environment that uses NPS or Remote Access Policies.</span></span>

<span data-ttu-id="1bede-111">Com a API de SDO, um desenvolvedor pode manipular qualquer elemento da configuração do NPS acessível por meio da interface do usuário do NPS.</span><span class="sxs-lookup"><span data-stu-id="1bede-111">With the SDO API, a developer can manipulate any element of the NPS configuration that is accessible through the NPS user interface.</span></span>

<span data-ttu-id="1bede-112">A API SDO também torna possível definir ou recuperar qualquer um dos valores acessíveis por meio da página de propriedades configurações de discagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bede-112">The SDO API also makes it possible to set or retrieve any of the values accessible through the user dial-in settings property page.</span></span>

<span data-ttu-id="1bede-113">A API de SDO é composta por interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="1bede-113">The SDO API is composed of COM interfaces.</span></span> <span data-ttu-id="1bede-114">Cada uma das interfaces na API de SDO herda da interface COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1bede-114">Each of the interfaces in the SDO API inherits from the COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1bede-115">A interface **IDispatch** permite que os desenvolvedores chamem os métodos de interface SDO de Visual Basic ou de qualquer cliente de automação, bem como do C/C++.</span><span class="sxs-lookup"><span data-stu-id="1bede-115">The **IDispatch** interface enables developers to call the SDO interface methods from Visual Basic or any Automation client, as well as from C/C++.</span></span>

<span data-ttu-id="1bede-116">Os desenvolvedores também podem chamar a API de SDO de linguagens de script, como o VBScript.</span><span class="sxs-lookup"><span data-stu-id="1bede-116">Developers can also call the SDO API from scripting languages such as VBScript.</span></span> <span data-ttu-id="1bede-117">No entanto, como o VBScript é limitado ao uso apenas de parâmetros de tipo VARIANT, nem toda a funcionalidade de SDO está disponível.</span><span class="sxs-lookup"><span data-stu-id="1bede-117">However, because VBScript is limited to using VARIANT-type parameters only, not all the functionality of SDO is available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1bede-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1bede-118">In This Section</span></span>

[<span data-ttu-id="1bede-119">Visão geral</span><span class="sxs-lookup"><span data-stu-id="1bede-119">Overview</span></span>](/windows/desktop/Nps/sdo-about-server-data-objects)

<span data-ttu-id="1bede-120">Informações gerais sobre a API de objetos de dados do servidor.</span><span class="sxs-lookup"><span data-stu-id="1bede-120">General information about the Server Data Objects API.</span></span>

[<span data-ttu-id="1bede-121">Usando</span><span class="sxs-lookup"><span data-stu-id="1bede-121">Using</span></span>](/windows/desktop/Nps/sdo-using-server-data-objects)

<span data-ttu-id="1bede-122">Código de exemplo que demonstra como usar a API de objetos de dados do servidor.</span><span class="sxs-lookup"><span data-stu-id="1bede-122">Sample code that demonstrates how to use the Server Data Objects API.</span></span>

[<span data-ttu-id="1bede-123">Referência</span><span class="sxs-lookup"><span data-stu-id="1bede-123">Reference</span></span>](/windows/desktop/Nps/sdo-server-data-objects-reference)

<span data-ttu-id="1bede-124">Documentação dos tipos enumerados e interfaces que compõem a API de objetos de dados do servidor.</span><span class="sxs-lookup"><span data-stu-id="1bede-124">Documentation of the enumerated types and interfaces that compose the Server Data Objects API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bede-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bede-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bede-126">Servidor de políticas de rede (serviço de autenticação da Internet)</span><span class="sxs-lookup"><span data-stu-id="1bede-126">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="1bede-127">Serviço de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="1bede-127">Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 