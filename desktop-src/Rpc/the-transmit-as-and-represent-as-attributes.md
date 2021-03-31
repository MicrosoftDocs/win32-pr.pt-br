---
title: Os atributos transmit_as e represent_as
description: Esta seção discute a implementação da conversão de tipo de dados do programador usando os atributos MIDL \ Transmit \_ as \ e \ representa as \_ \.
ms.assetid: 2e1af786-f507-453f-bb10-74805ef6b1a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16760091479a306b9dc9c815c7f3a41b25012ca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823822"
---
# <a name="the-transmit_as-and-represent_as-attributes"></a><span data-ttu-id="b7f45-103">A transmissão \_ como e representa \_ como atributos</span><span class="sxs-lookup"><span data-stu-id="b7f45-103">The transmit\_as and represent\_as Attributes</span></span>

<span data-ttu-id="b7f45-104">Esta seção discute a implementação da conversão de tipo de dados do programador usando a **\[** [**transmissão MIDL \_ como**](/windows/desktop/Midl/transmit-as) **\]** e **\[** [**representa \_ como**](/windows/desktop/Midl/represent-as) **\]** atributos.</span><span class="sxs-lookup"><span data-stu-id="b7f45-104">This section discusses the implementation of programmer data type conversion using the MIDL **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** and **\[**[**represent\_as**](/windows/desktop/Midl/represent-as)**\]** attributes.</span></span> <span data-ttu-id="b7f45-105">A discussão é apresentada nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="b7f45-105">The discussion is presented in the following sections:</span></span>

-   [<span data-ttu-id="b7f45-106">O atributo **transmitir \_ como**</span><span class="sxs-lookup"><span data-stu-id="b7f45-106">The **transmit\_as** Attribute</span></span>](the-transmit-as-attribute.md)
-   [<span data-ttu-id="b7f45-107">O **tipo \_ para \_** a função de transmissão</span><span class="sxs-lookup"><span data-stu-id="b7f45-107">The **type\_to\_xmit** Function</span></span>](the-type-to-xmit-function.md)
-   [<span data-ttu-id="b7f45-108">O **tipo \_ da função de \_ transmissão**</span><span class="sxs-lookup"><span data-stu-id="b7f45-108">The **type\_from\_xmit** Function</span></span>](the-type-from-xmit-function.md)
-   [<span data-ttu-id="b7f45-109">A função de **\_ \_ transmissão gratuita de tipo**</span><span class="sxs-lookup"><span data-stu-id="b7f45-109">The **type\_free\_xmit** Function</span></span>](the-type-free-xmit-function.md)
-   [<span data-ttu-id="b7f45-110">A **função \_ \_ Inst sem tipo**</span><span class="sxs-lookup"><span data-stu-id="b7f45-110">The **type\_free\_inst** Function</span></span>](the-type-free-inst-function.md)
-   [<span data-ttu-id="b7f45-111">O atributo de **representar \_ como**</span><span class="sxs-lookup"><span data-stu-id="b7f45-111">The **represent\_as** Attribute</span></span>](the-represent-as-attribute.md)
-   [<span data-ttu-id="b7f45-112">O **\_ tipo nomeado \_ da função \_ local**</span><span class="sxs-lookup"><span data-stu-id="b7f45-112">The **named\_type\_from\_local** Function</span></span>](the-named-type-from-local-function.md)
-   [<span data-ttu-id="b7f45-113">O **\_ tipo nomeado \_ para função \_ local**</span><span class="sxs-lookup"><span data-stu-id="b7f45-113">The **named\_type\_to\_local** Function</span></span>](the-named-type-to-local-function.md)
-   [<span data-ttu-id="b7f45-114">O **\_ tipo nomeado \_ função \_ local gratuita**</span><span class="sxs-lookup"><span data-stu-id="b7f45-114">The **named\_type\_free\_local** Function</span></span>](the-named-type-free-local-function.md)
-   [<span data-ttu-id="b7f45-115">A **função \_ \_ \_ instra gratuita de tipo nomeado**</span><span class="sxs-lookup"><span data-stu-id="b7f45-115">The **named\_type\_free\_inst** Function</span></span>](the-named-type-free-inst-function.md)

 

 