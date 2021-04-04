---
title: GetGUID IAgentCharacterEx
description: GetGUID IAgentCharacterEx
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916475"
---
# <a name="iagentcharacterexgetguid"></a><span data-ttu-id="e05ec-103">IAgentCharacterEx:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="e05ec-103">IAgentCharacterEx::GetGUID</span></span>

<span data-ttu-id="e05ec-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e05ec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

<span data-ttu-id="e05ec-105">Recupera a ID exclusiva para o caractere.</span><span class="sxs-lookup"><span data-stu-id="e05ec-105">Retrieves the unique ID for the character.</span></span>

-   <span data-ttu-id="e05ec-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e05ec-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e05ec-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span><span class="sxs-lookup"><span data-stu-id="e05ec-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="e05ec-108">Endereço de um BSTR que recebe a ID para o caractere.</span><span class="sxs-lookup"><span data-stu-id="e05ec-108">Address of a BSTR that receives the ID for the character.</span></span>

</dd> </dl>

<span data-ttu-id="e05ec-109">A propriedade retorna uma representação de cadeia de caracteres do GUID (formatado com chaves e traços) que o servidor usa para identificar exclusivamente o caractere.</span><span class="sxs-lookup"><span data-stu-id="e05ec-109">The property returns a string representation of the GUID (formatted with braces and dashes) that the server uses to uniquely identify the character.</span></span> <span data-ttu-id="e05ec-110">Um identificador de caractere é definido quando é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e05ec-110">A character identifier is set when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e05ec-111">a propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e05ec-111">The property is read-only.</span></span>

 

 




