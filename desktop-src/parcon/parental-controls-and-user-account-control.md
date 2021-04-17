---
description: Controles dos pais e controle de conta de usuário
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Controles dos pais e controle de conta de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771327"
---
# <a name="parental-controls-and-user-account-control"></a><span data-ttu-id="c7970-103">Controles dos pais e controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="c7970-103">Parental Controls and User Account Control</span></span>

<span data-ttu-id="c7970-104">O UAC (controle de conta de usuário) resultará na presença de contas de usuário padrão e de administrador protegido.</span><span class="sxs-lookup"><span data-stu-id="c7970-104">User Account Control (UAC) will result in presence of Protected Administrator and Standard User accounts.</span></span> <span data-ttu-id="c7970-105">Um administrador protegido será executado com os mesmos direitos que um usuário padrão em uso normal.</span><span class="sxs-lookup"><span data-stu-id="c7970-105">A Protected Administrator will run with the same rights as a Standard User under normal usage.</span></span> <span data-ttu-id="c7970-106">Para operações privilegiadas:</span><span class="sxs-lookup"><span data-stu-id="c7970-106">For privileged operations:</span></span>

-   <span data-ttu-id="c7970-107">Um usuário padrão será mostrado na caixa de diálogo credenciais da interface do usuário, que requer a entrada de um nome de usuário e senha para um administrador protegido ou administrador interno.</span><span class="sxs-lookup"><span data-stu-id="c7970-107">A Standard User will be shown the Credentials User Interface dialog box, which requires the input of a user name and password for a Protected Administrator or built-in Administrator.</span></span>
-   <span data-ttu-id="c7970-108">Um administrador protegido será mostrado na caixa de diálogo interface do usuário de consentimento, que requer a seleção de permitir para continuar.</span><span class="sxs-lookup"><span data-stu-id="c7970-108">A Protected Administrator will be shown the Consent User Interface dialog box, which requires selection of Allow to proceed.</span></span>

<span data-ttu-id="c7970-109">É importante observar que o UAC é implementado por processo, de modo que um processo seja executado com privilégios elevados ou não.</span><span class="sxs-lookup"><span data-stu-id="c7970-109">It is important to note that UAC is implemented on a per-process basis, so a process either runs elevated or not.</span></span> <span data-ttu-id="c7970-110">Em geral, ele não é adequado de um ponto de vista de segurança para executar aplicativos grandes como sempre elevado.</span><span class="sxs-lookup"><span data-stu-id="c7970-110">Generally, it is not suitable from a security standpoint to run large applications as always elevated.</span></span> <span data-ttu-id="c7970-111">Para controles dos pais, o código que deve modificar as configurações deve ser isolado por uma das duas opções de implementação:</span><span class="sxs-lookup"><span data-stu-id="c7970-111">For Parental Controls, code that must modify settings should be isolated by one of two implementation options:</span></span>

1.  <span data-ttu-id="c7970-112">Crie um pequeno executável para o gerenciamento de configurações que está marcado em seu manifesto, exigindo direitos administrativos.</span><span class="sxs-lookup"><span data-stu-id="c7970-112">Create a small executable for settings management that is marked in its manifest as requiring administrative rights.</span></span> <span data-ttu-id="c7970-113">A invocação do executável fará com que a interface do usuário de consentimento ou credenciais seja exibida antes de permitir que o processo seja executado.</span><span class="sxs-lookup"><span data-stu-id="c7970-113">Invocation of the executable will cause the Consent or Credentials UI to be shown prior to allowing the process to run.</span></span>
2.  <span data-ttu-id="c7970-114">Forneça interfaces COM em uma DLL de produto que permita invocação por documentação do UAC.</span><span class="sxs-lookup"><span data-stu-id="c7970-114">Provide COM interfaces in a product DLL that allow for invocation per UAC documentation.</span></span> <span data-ttu-id="c7970-115">Isso também fará com que a interface do usuário de credenciais ou consentimento apropriado seja mostrada.</span><span class="sxs-lookup"><span data-stu-id="c7970-115">This will also cause the appropriate Consent or Credentials UI to be shown.</span></span>

 

 



