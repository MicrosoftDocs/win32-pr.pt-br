---
title: Escolhendo um nível de autenticação
description: Ao escolher um nível de autenticação, use a seguinte diretriz.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453573"
---
# <a name="choosing-an-authentication-level"></a><span data-ttu-id="acfc6-103">Escolhendo um nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="acfc6-103">Choosing an Authentication Level</span></span>

<span data-ttu-id="acfc6-104">Ao escolher um nível de autenticação, use a seguinte diretriz.</span><span class="sxs-lookup"><span data-stu-id="acfc6-104">When choosing an authentication level, use the following guideline.</span></span> <span data-ttu-id="acfc6-105">Se não importa se os dados enviados podem ser interceptados e modificados e os dados recebidos podem ser interceptados ou modificados, use RPC \_ C \_ Authn \_ nível \_ None, que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="acfc6-105">If it does not matter whether the data being sent can be intercepted and modified, and the data received can be intercepted or modified, use RPC\_C\_AUTHN\_LEVEL\_NONE, which is the default.</span></span> <span data-ttu-id="acfc6-106">Se os dados não devem ser modificados e os dados privados não estão sendo enviados ou recebidos, use \_ a \_ integridade do pkt do nível de autenticação RPC C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="acfc6-106">If the data should not be modified, and private data is not being sent or received, use RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY.</span></span> <span data-ttu-id="acfc6-107">Em todos os outros casos, use \_ a \_ privacidade do PCT do nível de autenticação RPC C \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="acfc6-107">In all other cases, use RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

<span data-ttu-id="acfc6-108">Não use o \_ \_ \_ padrão de nível de autenticação RPC c \_ , o RPC \_ c \_ Authn \_ \_ Connect, a \_ chamada de nível RPC c \_ Authn \_ ou o PCT do \_ \_ nível de autenticação RPC c \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="acfc6-108">Do not use RPC\_C\_AUTHN\_LEVEL\_DEFAULT, RPC\_C\_AUTHN\_LEVEL\_CONNECT, RPC\_C\_AUTHN\_LEVEL\_CALL or RPC\_C\_AUTHN\_LEVEL\_PKT.</span></span> <span data-ttu-id="acfc6-109">Um invasor sofisticado pode interromper esses níveis de autenticação e renderizá-los ineficazes.</span><span class="sxs-lookup"><span data-stu-id="acfc6-109">A sophisticated attacker can break these authentication levels and render them ineffective.</span></span> <span data-ttu-id="acfc6-110">Cada um desses níveis torna um pouco mais difícil para um invasor interceptar e modificar dados, e para representar, mas a segurança não é realmente alcançada.</span><span class="sxs-lookup"><span data-stu-id="acfc6-110">Each of these levels does make it slightly more difficult for an attacker to intercept and modify data, and to impersonate, but security is not really achieved.</span></span> <span data-ttu-id="acfc6-111">Como o nível de sofisticação de um invasor raramente é conhecido, essas não são opções inteligentes.</span><span class="sxs-lookup"><span data-stu-id="acfc6-111">Since the sophistication level of an attacker is rarely known, these are not wise choices.</span></span>

 

 




