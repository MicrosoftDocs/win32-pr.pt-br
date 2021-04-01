---
title: IAgentAudioOutputProperties getabilited
description: IAgentAudioOutputProperties getabilited
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005476"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a><span data-ttu-id="d85d1-103">IAgentAudioOutputProperties:: getabilited</span><span class="sxs-lookup"><span data-stu-id="d85d1-103">IAgentAudioOutputProperties::GetEnabled</span></span>

<span data-ttu-id="d85d1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d85d1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

<span data-ttu-id="d85d1-105">Recupera um valor que indica se a saída de fala de caractere está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d85d1-105">Retrieves a value indicating whether character speech output is enabled.</span></span>

-   <span data-ttu-id="d85d1-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d85d1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d85d1-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="d85d1-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="d85d1-108">Endereço de uma variável que recebe **true** se a saída de fala estiver habilitada no momento e **false** se estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d85d1-108">Address of a variable that receives **True** if the speech output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="d85d1-109">Como essa configuração afeta a saída falada (TTS e arquivo de som) para todos os caracteres, somente o usuário pode alterar essa propriedade na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d85d1-109">Because this setting affects spoken output (TTS and sound file) for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




