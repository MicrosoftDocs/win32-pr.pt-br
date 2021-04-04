---
title: Cancelar registro do IAgent
description: Cancelar registro do IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823761"
---
# <a name="iagentunregister"></a><span data-ttu-id="db6a7-103">IAgent:: cancelar registro</span><span class="sxs-lookup"><span data-stu-id="db6a7-103">IAgent::Unregister</span></span>

<span data-ttu-id="db6a7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db6a7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

<span data-ttu-id="db6a7-105">Descarrega os dados de caractere do caractere especificado da coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="db6a7-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="db6a7-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="db6a7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="db6a7-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span><span class="sxs-lookup"><span data-stu-id="db6a7-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="db6a7-108">A ID do coletor de notificação.</span><span class="sxs-lookup"><span data-stu-id="db6a7-108">The notification sink ID.</span></span>

</dd> </dl>

<span data-ttu-id="db6a7-109">Use esse método quando não precisar mais dos serviços do Microsoft Agent, como quando o aplicativo for desligado.</span><span class="sxs-lookup"><span data-stu-id="db6a7-109">Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.</span></span>

## <a name="see-also"></a><span data-ttu-id="db6a7-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="db6a7-110">See Also</span></span>

[<span data-ttu-id="db6a7-111">**IAgent:: Register**</span><span class="sxs-lookup"><span data-stu-id="db6a7-111">**IAgent::Register**</span></span>](iagent--register.md)


 

 