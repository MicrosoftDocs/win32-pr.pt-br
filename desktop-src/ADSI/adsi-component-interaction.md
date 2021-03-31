---
title: Interação do componente ADSI
description: O componente de roteador Active Directory popula uma tabela de provedor ADSI dos provedores ADSI instalados listados no registro quando ele recebe a primeira solicitação do aplicativo cliente.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641826"
---
# <a name="adsi-component-interaction"></a><span data-ttu-id="a45e0-103">Interação do componente ADSI</span><span class="sxs-lookup"><span data-stu-id="a45e0-103">ADSI Component Interaction</span></span>

<span data-ttu-id="a45e0-104">O componente de roteador Active Directory popula uma tabela de provedor ADSI dos provedores ADSI instalados listados no registro quando ele recebe a primeira solicitação do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="a45e0-104">The Active Directory router component populates an ADSI provider table from the installed ADSI providers listed in the registry when it receives the first request from the client application.</span></span> <span data-ttu-id="a45e0-105">Para obter mais informações sobre o registro, consulte [instalando o componente do provedor de exemplo](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="a45e0-105">For more information about the Registry, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

<span data-ttu-id="a45e0-106">Operações que fazem uma solicitação de um diretório para um ponteiro para uma interface em um Active Directory objeto passam por uma função (**GetObject** em Visual Basic ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) em C ou C++), ou um método de interface ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span><span class="sxs-lookup"><span data-stu-id="a45e0-106">Operations that make a request from a directory for a pointer to an interface on an Active Directory object come through a function (**GetObject** in Visual Basic or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) in C or C++), or an interface method ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)).</span></span> <span data-ttu-id="a45e0-107">Na figura a seguir, o aplicativo cliente ADSI passa tal solicitação de ligação para o componente de roteador ADSI (1).</span><span class="sxs-lookup"><span data-stu-id="a45e0-107">In the following figure, the ADSI client application passes such a bind request to the ADSI router component (1).</span></span> <span data-ttu-id="a45e0-108">O componente roteador identifica o ProgID do provedor a partir da primeira parte do ADsPath e usa [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para localizar o CLSID correspondente no registro (2) e carrega o componente de provedor apropriado (3).</span><span class="sxs-lookup"><span data-stu-id="a45e0-108">The router component identifies the ProgID for the provider from the first part of the ADsPath and uses [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) to find the matching CLSID in the registry (2) and loads the proper provider component (3).</span></span>

![interações de componente ADSI no provedor de exemplo](images/dscspr.png)

<span data-ttu-id="a45e0-110">Na figura anterior, o componente do provedor cria um objeto de Active Directory que representa o elemento de diretório nomeado.</span><span class="sxs-lookup"><span data-stu-id="a45e0-110">In the preceding figure, the provider component creates an Active Directory object representing the named directory element.</span></span> <span data-ttu-id="a45e0-111">O componente de suporte ADSI faz um **QueryInterface** no identificador de interface solicitado.</span><span class="sxs-lookup"><span data-stu-id="a45e0-111">The ADSI support component does a **QueryInterface** on the requested interface identifier.</span></span> <span data-ttu-id="a45e0-112">Quando um ponteiro para essa interface é recuperado (4), assim como acontece com todas as implementações de cliente/servidor COM, ele é passado de volta para o cliente (5) e, a partir de então, no aplicativo cliente funciona diretamente com o componente do provedor (6).</span><span class="sxs-lookup"><span data-stu-id="a45e0-112">When a pointer to that interface is retrieved (4), as with all COM client/server implementations, it is then passed back to the client (5), and from then on the client application works directly with the provider component (6).</span></span>

 

 