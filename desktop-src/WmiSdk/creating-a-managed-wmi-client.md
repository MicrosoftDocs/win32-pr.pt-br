---
description: Atualmente, o WMI não oferece suporte a código gerenciado no WMI, mas tem suporte em MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Criando um cliente WMI gerenciado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782418"
---
# <a name="creating-a-managed-wmi-client"></a><span data-ttu-id="d15c9-103">Criando um cliente WMI gerenciado</span><span class="sxs-lookup"><span data-stu-id="d15c9-103">Creating a Managed WMI Client</span></span>

<span data-ttu-id="d15c9-104">A versão atual do WMI contém o namespace System. Management, que expõe uma série de APIs que interagem com o WMI.</span><span class="sxs-lookup"><span data-stu-id="d15c9-104">The current release of WMI does contain the System.Management namespace, which exposes a number of API's that interact with WMI.</span></span> <span data-ttu-id="d15c9-105">No entanto, não é recomendável que você use esse namespace.</span><span class="sxs-lookup"><span data-stu-id="d15c9-105">However, it is not recommended that you use this namespace.</span></span>

<span data-ttu-id="d15c9-106">Se você quiser criar um cliente WMI gerenciado, é recomendável usar o MI (infraestrutura de gerenciamento do Windows).</span><span class="sxs-lookup"><span data-stu-id="d15c9-106">If you wish to create a managed WMI client, it is recommended that you use the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="d15c9-107">MI é a versão de última geração do WMI e contém suporte completo para código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d15c9-107">MI is the next-generation version of WMI, and contains full support for managed code.</span></span> <span data-ttu-id="d15c9-108">Para obter mais informações, consulte [como implementar um cliente mi gerenciado](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span><span class="sxs-lookup"><span data-stu-id="d15c9-108">For more information, see [How to Implement a Managed MI Client](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span></span>

 

 
