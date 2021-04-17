---
description: As fontes primárias para procedimentos de instalação são o kit de recursos para o sistema operacional de destino, documentação do aplicativo e instruções do provedor de serviços. Para provedores de serviços da Microsoft, o kit de recursos apropriado contém instruções.
ms.assetid: a94023ac-5226-4a51-a08b-c53d08260710
title: Instalação (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446510c3d92431188bcff50842b15c200cc5d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783368"
---
# <a name="installation-telephony-api"></a><span data-ttu-id="4c437-104">Instalação (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="4c437-104">Installation (Telephony API)</span></span>

<span data-ttu-id="4c437-105">As fontes primárias para procedimentos de instalação são o kit de recursos para o sistema operacional de destino, documentação do aplicativo e instruções do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="4c437-105">The primary sources for installation procedures are the Resource Kit for the target operating system, application documentation, and service provider instructions.</span></span> <span data-ttu-id="4c437-106">Para provedores de serviços da Microsoft, o kit de recursos apropriado contém instruções.</span><span class="sxs-lookup"><span data-stu-id="4c437-106">For Microsoft service providers, the appropriate resource kit contains instructions.</span></span>

<span data-ttu-id="4c437-107">O processo de instalação deve incluir a listagem de "serviço de telefonia" como dependência.</span><span class="sxs-lookup"><span data-stu-id="4c437-107">The installation process must include listing "Telephony Service" as dependency.</span></span>

<span data-ttu-id="4c437-108">Se um aplicativo ou provedor de serviços usar o registro para armazenamento de dados privados persistentes, as informações não deverão ser colocadas na seção da TAPI do registro.</span><span class="sxs-lookup"><span data-stu-id="4c437-108">If an application or service provider uses the registry for storage of persistent private data, the information must not be placed in TAPI's section of the registry.</span></span> <span data-ttu-id="4c437-109">Não há garantia de que o formato desta seção seja mantido em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="4c437-109">The format of this section is not guaranteed to be maintained in future versions.</span></span>

 

 



