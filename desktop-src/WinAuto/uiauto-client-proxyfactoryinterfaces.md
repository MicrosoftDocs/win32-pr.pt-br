---
title: Interfaces de fábrica de proxy para clientes
description: Esta seção descreve as interfaces de fábrica de proxy para aplicativos cliente de automação de interface do usuário não gerenciado.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006014"
---
# <a name="proxy-factory-interfaces-for-clients"></a><span data-ttu-id="fecbf-103">Interfaces de fábrica de proxy para clientes</span><span class="sxs-lookup"><span data-stu-id="fecbf-103">Proxy Factory Interfaces for Clients</span></span>

<span data-ttu-id="fecbf-104">Esta seção descreve as interfaces de fábrica de proxy para aplicativos cliente de automação de interface do usuário não gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fecbf-104">This section describes the proxy factory interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fecbf-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fecbf-105">In this section</span></span>



| <span data-ttu-id="fecbf-106">Interface</span><span class="sxs-lookup"><span data-stu-id="fecbf-106">Interface</span></span>                                                                                      | <span data-ttu-id="fecbf-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fecbf-107">Description</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fecbf-108">**IUIAutomationProxyFactory**</span><span class="sxs-lookup"><span data-stu-id="fecbf-108">**IUIAutomationProxyFactory**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | <span data-ttu-id="fecbf-109">Expõe propriedades e métodos de um objeto que cria um provedor de automação de interface do usuário da Microsoft para elementos de interface do usuário que não têm suporte nativo para automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fecbf-109">Exposes properties and methods of an object that creates a Microsoft UI Automation provider for UI elements that do not have native support for UI Automation.</span></span> <span data-ttu-id="fecbf-110">Essa interface é implementada por proxies.</span><span class="sxs-lookup"><span data-stu-id="fecbf-110">This interface is implemented by proxies.</span></span><br/>                                                                          |
| [<span data-ttu-id="fecbf-111">**IUIAutomationProxyFactoryEntry**</span><span class="sxs-lookup"><span data-stu-id="fecbf-111">**IUIAutomationProxyFactoryEntry**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | <span data-ttu-id="fecbf-112">Representa uma fábrica de proxy na tabela mantida pela automação da interface do usuário e expõe propriedades e métodos que podem ser usados por aplicativos cliente para interagir com objetos [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .</span><span class="sxs-lookup"><span data-stu-id="fecbf-112">Represents a proxy factory in the table maintained by UI Automation, and exposes properties and methods that can be used by client applications to interact with [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) objects.</span></span><br/>                                   |
| [<span data-ttu-id="fecbf-113">**IUIAutomationProxyFactoryMapping**</span><span class="sxs-lookup"><span data-stu-id="fecbf-113">**IUIAutomationProxyFactoryMapping**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | <span data-ttu-id="fecbf-114">Expõe propriedades e métodos para uma tabela de fábricas de proxy.</span><span class="sxs-lookup"><span data-stu-id="fecbf-114">Exposes properties and methods for a table of proxy factories.</span></span> <span data-ttu-id="fecbf-115">Cada entrada de tabela é representada por uma interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) .</span><span class="sxs-lookup"><span data-stu-id="fecbf-115">Each table entry is represented by an [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) interface.</span></span> <span data-ttu-id="fecbf-116">As entradas estão na ordem em que o sistema tentará usar os proxies.</span><span class="sxs-lookup"><span data-stu-id="fecbf-116">The entries are in the order in which the system will attempt to use the proxies.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fecbf-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fecbf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fecbf-118">Clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="fecbf-118">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





