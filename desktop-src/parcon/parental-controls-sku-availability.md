---
description: Controle dos pais disponibilidade de SKU
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Controle dos pais disponibilidade de SKU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761221"
---
# <a name="parental-controls-sku-availability"></a><span data-ttu-id="9ef3b-103">Controle dos pais disponibilidade de SKU</span><span class="sxs-lookup"><span data-stu-id="9ef3b-103">Parental Controls SKU Availability</span></span>

<span data-ttu-id="9ef3b-104">Os pais controlam as interfaces do usuário, os recursos e as APIs descritas nesta seção estão atualmente planejados para estar disponíveis somente em SKUs com foco no consumidor, como:</span><span class="sxs-lookup"><span data-stu-id="9ef3b-104">The Parental Controls user interfaces, features, and APIs described in this section are currently planned to be available only on consumer-focused SKUs such as:</span></span>

-   <span data-ttu-id="9ef3b-105">Windows Vista Starter</span><span class="sxs-lookup"><span data-stu-id="9ef3b-105">Windows Vista Starter</span></span>
-   <span data-ttu-id="9ef3b-106">Windows Vista Home Basic</span><span class="sxs-lookup"><span data-stu-id="9ef3b-106">Windows Vista Home Basic</span></span>
-   <span data-ttu-id="9ef3b-107">Windows Vista Home Premium</span><span class="sxs-lookup"><span data-stu-id="9ef3b-107">Windows Vista Home Premium</span></span>
-   <span data-ttu-id="9ef3b-108">Windows Vista Ultimate</span><span class="sxs-lookup"><span data-stu-id="9ef3b-108">Windows Vista Ultimate</span></span>

<span data-ttu-id="9ef3b-109">Os controles dos pais são instalados apenas nessas SKUs.</span><span class="sxs-lookup"><span data-stu-id="9ef3b-109">Parental Controls only installs on these SKUs.</span></span> <span data-ttu-id="9ef3b-110">As soluções que têm um requisito para implantar em SKUs de negócios precisarão:</span><span class="sxs-lookup"><span data-stu-id="9ef3b-110">Solutions having a requirement to deploy onto business SKUs will need to either:</span></span>

-   <span data-ttu-id="9ef3b-111">Detectar e não fornecer a funcionalidade de controles dos pais em SKUs de negócios.</span><span class="sxs-lookup"><span data-stu-id="9ef3b-111">Detect and not provide parental controls functionality on business SKUs.</span></span>
-   <span data-ttu-id="9ef3b-112">Detecte e forneça um meio alternativo de configuração, registro em log e restrições.</span><span class="sxs-lookup"><span data-stu-id="9ef3b-112">Detect and provide an alternative means of configuration, logging, and restrictions.</span></span>

<span data-ttu-id="9ef3b-113">É recomendável que as soluções detectem a disponibilidade da infraestrutura de controles dos pais verificando o êxito de COM CoCreateInstance na API de conformidade.</span><span class="sxs-lookup"><span data-stu-id="9ef3b-113">It is recommended that solutions detect availability of the Parental Controls Infrastructure by checking for success of COM CoCreateInstance on the Compliance API.</span></span>

<span data-ttu-id="9ef3b-114">Os aplicativos com reconhecimento de controles pelos pais, dependendo da infraestrutura do Windows Vista, também podem querer suprimir qualquer uma de suas próprias configurações de exposição da interface do usuário ou outras funcionalidades quando a interface do usuário de controles dos pais for suprimida em uma SKU com suporte.</span><span class="sxs-lookup"><span data-stu-id="9ef3b-114">Parental Controls-aware applications depending on the Windows Vista infrastructure may also want to suppress any of their own UI exposing settings or other functionality when Parental Controls UI is suppressed on a supported SKU.</span></span> <span data-ttu-id="9ef3b-115">Uma função é fornecida para determinação de visibilidade que abrange casos como supressão ingressada no domínio.</span><span class="sxs-lookup"><span data-stu-id="9ef3b-115">A function is provided for visibility determination that covers cases such as domain-joined suppression.</span></span>

 

 



