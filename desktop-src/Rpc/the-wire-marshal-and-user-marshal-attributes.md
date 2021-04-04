---
title: Os atributos wire_marshal e user_marshal
description: Esta seção discute a implementação da conversão de tipo de dados do programador usando os atributos MIDL \ Wire \_ Marshal \ e \ user \_ Marshal \.
ms.assetid: 0ee2ce86-cd14-4659-a69f-6336145359da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a789f11fa15a20eab0fcd468cc410bb5a7200717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007962"
---
# <a name="the-wire_marshal-and-user_marshal-attributes"></a><span data-ttu-id="7d000-103">Os \_ atributos de marshaling e \_ Marshal do usuário de transmissão</span><span class="sxs-lookup"><span data-stu-id="7d000-103">The wire\_marshal and user\_marshal Attributes</span></span>

<span data-ttu-id="7d000-104">Esta seção discute a implementação da conversão de tipo de dados do programador usando os \[ atributos [ \_ Marshal Wire Marshall](/windows/desktop/Midl/wire-marshal) \] e \[ [ \_ Marshal do usuário](/windows/desktop/Midl/user-marshal) \] .</span><span class="sxs-lookup"><span data-stu-id="7d000-104">This section discusses the implementation of programmer data type conversion using the MIDL \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="7d000-105">As informações são apresentadas nas seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="7d000-105">The information is presented in the following sections:</span></span>

-   [<span data-ttu-id="7d000-106">O \_ atributo de marshaling de fio</span><span class="sxs-lookup"><span data-stu-id="7d000-106">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
-   [<span data-ttu-id="7d000-107">O \_ atributo de marshaling do usuário</span><span class="sxs-lookup"><span data-stu-id="7d000-107">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
-   [<span data-ttu-id="7d000-108">A \_ função de Usersize do tipo</span><span class="sxs-lookup"><span data-stu-id="7d000-108">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
-   [<span data-ttu-id="7d000-109">A \_ função de Usermarshal do tipo</span><span class="sxs-lookup"><span data-stu-id="7d000-109">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
-   [<span data-ttu-id="7d000-110">A \_ função Type UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="7d000-110">The type\_UserUnmarshal Function</span></span>](the-type-userunmarshal-function.md)
-   [<span data-ttu-id="7d000-111">O tipo \_ função Userfree</span><span class="sxs-lookup"><span data-stu-id="7d000-111">The type\_UserFree Function</span></span>](the-type-userfree-function.md)
-   [<span data-ttu-id="7d000-112">Regras de marshaling para marshaling de usuário \_ e \_ marshaling de conexão</span><span class="sxs-lookup"><span data-stu-id="7d000-112">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)

 

 