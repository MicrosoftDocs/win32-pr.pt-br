---
title: IAgentSpeechInputProperties getabilited
description: IAgentSpeechInputProperties getabilited
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634737"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a><span data-ttu-id="1e1cf-103">IAgentSpeechInputProperties:: getabilited</span><span class="sxs-lookup"><span data-stu-id="1e1cf-103">IAgentSpeechInputProperties::GetEnabled</span></span>

<span data-ttu-id="1e1cf-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1e1cf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

<span data-ttu-id="1e1cf-105">Recupera um valor que indica se o mecanismo de reconhecimento de fala instalado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-105">Retrieves a value indicating whether the installed speech recognition engine is enabled.</span></span>

-   <span data-ttu-id="1e1cf-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1e1cf-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="1e1cf-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="1e1cf-108">Endereço de uma variável que recebe **true** se o mecanismo de fala estiver habilitado no momento e **false** se estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1e1cf-108">Address of a variable that receives **True** if the speech engine is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

 

 




