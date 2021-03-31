---
title: GetCount IAgentUserInput
description: GetCount IAgentUserInput
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159240"
---
# <a name="iagentuserinputgetcount"></a><span data-ttu-id="698a0-103">IAgentUserInput:: GetCount</span><span class="sxs-lookup"><span data-stu-id="698a0-103">IAgentUserInput::GetCount</span></span>

<span data-ttu-id="698a0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="698a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="698a0-105">Recupera o número de alternativas de [**comando**](command-event.md) passadas para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="698a0-105">Retrieves the number of [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="698a0-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="698a0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="698a0-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span><span class="sxs-lookup"><span data-stu-id="698a0-107"><span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*</span></span>
</dt> <dd>

<span data-ttu-id="698a0-108">Endereço de uma variável que recebe a contagem de alternativas de [**comandos**](command-event.md) identificadas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="698a0-108">Address of a variable that receives the count of [**Commands**](command-event.md) alternatives identified by the server.</span></span>

</dd> </dl>

<span data-ttu-id="698a0-109">Se a entrada de voz não foi a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, **GetCount** retornará 1.</span><span class="sxs-lookup"><span data-stu-id="698a0-109">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, **GetCount** returns 1.</span></span> <span data-ttu-id="698a0-110">Se **GetCount** retornar zero (0), o mecanismo de reconhecimento de fala detectou uma entrada falada, mas determinou que não havia nenhum comando correspondente.</span><span class="sxs-lookup"><span data-stu-id="698a0-110">If **GetCount** returns zero (0), the speech recognition engine detected spoken input but determined that there was no matching command.</span></span>

 

 




