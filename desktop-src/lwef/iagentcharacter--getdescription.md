---
title: Getdescrição do IAgentCharacter
description: Getdescrição do IAgentCharacter
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364505"
---
# <a name="iagentcharactergetdescription"></a><span data-ttu-id="de9ca-103">IAgentCharacter:: GetDescription</span><span class="sxs-lookup"><span data-stu-id="de9ca-103">IAgentCharacter::GetDescription</span></span>

<span data-ttu-id="de9ca-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de9ca-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

<span data-ttu-id="de9ca-105">Recupera a descrição do caractere.</span><span class="sxs-lookup"><span data-stu-id="de9ca-105">Retrieves the description of the character.</span></span>

-   <span data-ttu-id="de9ca-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="de9ca-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="de9ca-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span><span class="sxs-lookup"><span data-stu-id="de9ca-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="de9ca-108">O endereço de um BSTR que recebe o valor da descrição para o caractere.</span><span class="sxs-lookup"><span data-stu-id="de9ca-108">The address of a BSTR that receives the value of the description for the character.</span></span> <span data-ttu-id="de9ca-109">A descrição de um caractere é definida quando é compilada com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="de9ca-109">A character's description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="de9ca-110">A configuração descrição é opcional e pode não ser fornecida para todos os caracteres.</span><span class="sxs-lookup"><span data-stu-id="de9ca-110">The description setting is optional and may not be supplied for all characters.</span></span>

</dd> </dl>

 

 




