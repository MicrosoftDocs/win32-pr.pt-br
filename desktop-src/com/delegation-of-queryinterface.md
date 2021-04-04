---
title: Delegação de QueryInterface
description: Delegação de QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084923"
---
# <a name="delegation-of-queryinterface"></a><span data-ttu-id="3d35b-103">Delegação de QueryInterface</span><span class="sxs-lookup"><span data-stu-id="3d35b-103">Delegation of QueryInterface</span></span>

<span data-ttu-id="3d35b-104">Os manipuladores que exigem acesso a algumas interfaces internas no Gerenciador de proxy precisam passar pela interface [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) .</span><span class="sxs-lookup"><span data-stu-id="3d35b-104">Handlers that require access to some of the internal interfaces on the proxy manager have to go through the [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) interface.</span></span> <span data-ttu-id="3d35b-105">Isso impede que os manipuladores delegom e exponham indistintamente as interfaces internas do agregado fora da agregação.</span><span class="sxs-lookup"><span data-stu-id="3d35b-105">This prevents handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate.</span></span> <span data-ttu-id="3d35b-106">Essas interfaces incluem [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span><span class="sxs-lookup"><span data-stu-id="3d35b-106">These interfaces include [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span></span> <span data-ttu-id="3d35b-107">Se o manipulador quiser expor **IClientSecurity** ou **IMultiQI**, ele deverá implementá-lo por conta própria.</span><span class="sxs-lookup"><span data-stu-id="3d35b-107">If the handler wants to expose **IClientSecurity** or **IMultiQI**, it should implement them itself.</span></span>

<span data-ttu-id="3d35b-108">No caso do [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), se o cliente tentar definir a segurança em uma interface que o manipulador tenha exposto, o manipulador deverá definir a segurança no proxy de interface de rede subjacente.</span><span class="sxs-lookup"><span data-stu-id="3d35b-108">In the case of [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.</span></span>

<span data-ttu-id="3d35b-109">No caso do [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), o manipulador deve preencher as interfaces que ele conhece e, em seguida, encaminhar a chamada para o Gerenciador de proxy para obter o restante das interfaces preenchidas.</span><span class="sxs-lookup"><span data-stu-id="3d35b-109">In the case of [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to get the rest of the interfaces filled in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d35b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d35b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d35b-111">O manipulador de Client-Side leve</span><span class="sxs-lookup"><span data-stu-id="3d35b-111">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 