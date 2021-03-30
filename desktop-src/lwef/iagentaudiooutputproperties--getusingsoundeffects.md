---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635948"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a><span data-ttu-id="88bd1-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span><span class="sxs-lookup"><span data-stu-id="88bd1-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span></span>

<span data-ttu-id="88bd1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88bd1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

<span data-ttu-id="88bd1-105">Recupera um valor que indica se a saída de efeitos de som está habilitada.</span><span class="sxs-lookup"><span data-stu-id="88bd1-105">Retrieves a value indicating whether sound effects output is enabled.</span></span>

-   <span data-ttu-id="88bd1-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="88bd1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="88bd1-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span><span class="sxs-lookup"><span data-stu-id="88bd1-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span></span>
</dt> <dd>

<span data-ttu-id="88bd1-108">Endereço de uma variável que recebe **true** se a saída de efeitos de som estiver habilitada no momento e **false** se estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="88bd1-108">Address of a variable that receives **True** if the sound effects output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="88bd1-109">Os efeitos de som para a animação de um caractere são atribuídos no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="88bd1-109">Sound effects for a character's animation are assigned in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="88bd1-110">Como essa configuração afeta a saída de efeitos de som para todos os caracteres, somente o usuário pode alterar essa propriedade na folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="88bd1-110">Because this setting affects sound effects output for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




