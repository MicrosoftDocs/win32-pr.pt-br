---
title: Expondo informações adicionais não cobertas pela interface IAccessible
description: Dependendo de seus produtos, os desenvolvedores de servidores talvez precisem expor informações ou funcionalidades além do suporte ao Microsoft Acessibilidade Ativa.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294357"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a><span data-ttu-id="250c9-103">Expondo informações adicionais não cobertas pela interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="250c9-103">Exposing Additional Information Not Covered by IAccessible Interface</span></span>

<span data-ttu-id="250c9-104">Dependendo de seus produtos, os desenvolvedores de servidores talvez precisem expor informações ou funcionalidades além do suporte ao Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="250c9-104">Depending on their products, server developers might need to expose information or functionality in addition to Microsoft Active Accessibility support.</span></span> <span data-ttu-id="250c9-105">Se esse for o caso, trabalhe com fornecedores de tecnologia assistencial (clientes) para garantir que eles adicionem suporte para os recursos.</span><span class="sxs-lookup"><span data-stu-id="250c9-105">If this is the case, work with assistive technology vendors (clients) to ensure that they add support for the features.</span></span>

<span data-ttu-id="250c9-106">Não tente estender a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="250c9-106">Do not attempt to extend the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="250c9-107">As interfaces não podem ser alteradas depois de serem publicadas.</span><span class="sxs-lookup"><span data-stu-id="250c9-107">Interfaces cannot be changed once they are published.</span></span> <span data-ttu-id="250c9-108">Para expor informações adicionais, use uma interface personalizada e exporte-a usando uma das seguintes técnicas:</span><span class="sxs-lookup"><span data-stu-id="250c9-108">To expose additional information, use a custom interface and expose it by using one of the following techniques:</span></span>

-   [<span data-ttu-id="250c9-109">Usando OBJID \_ NATIVEOM para expor uma interface de modelo de objeto nativo para uma janela</span><span class="sxs-lookup"><span data-stu-id="250c9-109">Using OBJID\_NATIVEOM to expose a native object model interface for a window</span></span>](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [<span data-ttu-id="250c9-110">Usando o QueryService para expor uma interface de modelo de objeto nativo para um objeto IAccessible</span><span class="sxs-lookup"><span data-stu-id="250c9-110">Using QueryService to expose a native object model interface for an IAccessible object</span></span>](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

<span data-ttu-id="250c9-111">Observe que o objetivo da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) é ter uma interface bem definida que é usada por servidores e clientes.</span><span class="sxs-lookup"><span data-stu-id="250c9-111">Note that the goal of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is to have a well-defined interface that is used by servers and clients.</span></span> <span data-ttu-id="250c9-112">Antes de expor interfaces personalizadas, não se esqueça de expor o máximo possível de informações por meio do **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="250c9-112">Before exposing custom interfaces, be sure to expose as much information as possible through **IAccessible**.</span></span>

<span data-ttu-id="250c9-113">Você não pode usar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para expor interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="250c9-113">You cannot use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to expose custom interfaces.</span></span> <span data-ttu-id="250c9-114">Use **IServiceProvider:: QueryService** conforme descrito nos procedimentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="250c9-114">Use **IServiceProvider::QueryService** as outlined in the following procedures.</span></span>

 

 