---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160157"
---
# <a name="iagentnotifysinkactivateinputstate"></a><span data-ttu-id="3ddb4-103">IAgentNotifySink::ActivateInputState</span><span class="sxs-lookup"><span data-stu-id="3ddb4-103">IAgentNotifySink::ActivateInputState</span></span>

<span data-ttu-id="3ddb4-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3ddb4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

<span data-ttu-id="3ddb4-105">Notifica um aplicativo cliente de que o estado ativo de entrada de um caractere foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3ddb4-105">Notifies a client application that a character's input active state changed.</span></span>

-   <span data-ttu-id="3ddb4-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3ddb4-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="3ddb4-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="3ddb4-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="3ddb4-108">Identificador do caractere cujo estado de ativação de entrada foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3ddb4-108">Identifier of the character whose input activation state changed.</span></span>

</dd> <dt>

<span data-ttu-id="3ddb4-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span><span class="sxs-lookup"><span data-stu-id="3ddb4-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span></span>
</dt> <dd>

<span data-ttu-id="3ddb4-110">Sinalizador de entrada ativa.</span><span class="sxs-lookup"><span data-stu-id="3ddb4-110">Input active flag.</span></span> <span data-ttu-id="3ddb4-111">Esse valor booliano é **true** se o caractere referido por *dwCharID* ficou ativo de entrada; e **false** se o caractere perdeu seu estado ativo de entrada.</span><span class="sxs-lookup"><span data-stu-id="3ddb4-111">This Boolean value is **True** if the character referred to by *dwCharID* became input active; and **False** if the character lost its input active state.</span></span>

</dd> </dl>

 

 




