---
description: A estrutura COMMCONFIG define a configuração de um recurso de comunicação, serial ou de outra forma.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuração de recursos de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089205"
---
# <a name="communications-resource-configuration"></a><span data-ttu-id="55680-103">Configuração de recursos de comunicação</span><span class="sxs-lookup"><span data-stu-id="55680-103">Communications Resource Configuration</span></span>

<span data-ttu-id="55680-104">A estrutura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) define a configuração de um recurso de comunicação, serial ou de outra forma.</span><span class="sxs-lookup"><span data-stu-id="55680-104">The [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure defines the configuration of a communications resource, serial or otherwise.</span></span> <span data-ttu-id="55680-105">O formato da estrutura varia dependendo do tipo de recurso de comunicação (o subtipo do provedor).</span><span class="sxs-lookup"><span data-stu-id="55680-105">The format of the structure varies depending on the type of communications resource (the provider subtype).</span></span> <span data-ttu-id="55680-106">Os primeiros membros da estrutura são comuns a todos os recursos de comunicação; membros adicionais são definidos para subtipos de provedor específicos.</span><span class="sxs-lookup"><span data-stu-id="55680-106">The first few structure members are common to all communications resources; additional members are defined for specific provider subtypes.</span></span> <span data-ttu-id="55680-107">Provedores de serviço específicos também podem estender a estrutura **COMMCONFIG** .</span><span class="sxs-lookup"><span data-stu-id="55680-107">Specific service providers may extend the **COMMCONFIG** structure as well.</span></span>

<span data-ttu-id="55680-108">Um aplicativo pode obter e definir a configuração de um recurso de comunicação usando as funções [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) e [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) .</span><span class="sxs-lookup"><span data-stu-id="55680-108">An application can get and set the configuration of a communications resource by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions.</span></span> <span data-ttu-id="55680-109">Quando aberto, um recurso de comunicação é inicializado usando a configuração padrão para seu subtipo de provedor.</span><span class="sxs-lookup"><span data-stu-id="55680-109">When opened, a communications resource is initialized using the default configuration for its provider subtype.</span></span> <span data-ttu-id="55680-110">Para obter e definir a configuração padrão para um subtipo de provedor, use as funções [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) e [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .</span><span class="sxs-lookup"><span data-stu-id="55680-110">To get and set the default configuration for a provider subtype, use the [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) and [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) functions.</span></span>

<span data-ttu-id="55680-111">Para solicitar informações de configuração ao usuário, use a função [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) .</span><span class="sxs-lookup"><span data-stu-id="55680-111">To prompt the user for configuration information, use the [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) function.</span></span> <span data-ttu-id="55680-112">Essa função exibe uma caixa de diálogo definida pelo provedor de serviços e preenche uma estrutura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) com base na entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="55680-112">This function displays a dialog box defined by the service provider and fills in a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure based on user input.</span></span>

 

 



