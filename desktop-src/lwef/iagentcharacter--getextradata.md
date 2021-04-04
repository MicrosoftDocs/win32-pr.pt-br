---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084133"
---
# <a name="iagentcharactergetextradata"></a><span data-ttu-id="f8b65-103">IAgentCharacter::GetExtraData</span><span class="sxs-lookup"><span data-stu-id="f8b65-103">IAgentCharacter::GetExtraData</span></span>

<span data-ttu-id="f8b65-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f8b65-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

<span data-ttu-id="f8b65-105">Recupera dados adicionais armazenados como parte do caractere.</span><span class="sxs-lookup"><span data-stu-id="f8b65-105">Retrieves additional data stored as part of the character.</span></span>

-   <span data-ttu-id="f8b65-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f8b65-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f8b65-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span><span class="sxs-lookup"><span data-stu-id="f8b65-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span></span>
</dt> <dd>

<span data-ttu-id="f8b65-108">O endereço de um BSTR que recebe o valor dos dados adicionais para o caractere.</span><span class="sxs-lookup"><span data-stu-id="f8b65-108">The address of a BSTR that receives the value of the additional data for the character.</span></span> <span data-ttu-id="f8b65-109">Os dados adicionais de um caractere são definidos quando compilados com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f8b65-109">A character's additional data is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f8b65-110">Um desenvolvedor de caracteres pode fornecer essa cadeia de caracteres editando o. Arquivo ad para um caractere.</span><span class="sxs-lookup"><span data-stu-id="f8b65-110">A character developer can supply this string by editing the .ACD file for a character.</span></span> <span data-ttu-id="f8b65-111">A configuração é opcional e pode não ser fornecida para todos os caracteres, nem os dados podem ser definidos ou alterados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f8b65-111">The setting is optional and may not be supplied for all characters, nor can the data be defined or changed at run time.</span></span> <span data-ttu-id="f8b65-112">Além disso, o significado dos dados fornecidos é definido pelo desenvolvedor de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f8b65-112">In addition, the meaning of the data supplied is defined by the character developer.</span></span>

</dd> </dl>

 

 




