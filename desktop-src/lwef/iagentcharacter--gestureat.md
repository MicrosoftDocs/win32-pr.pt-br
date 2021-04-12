---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364506"
---
# <a name="iagentcharactergestureat"></a><span data-ttu-id="b4ae9-103">IAgentCharacter::GestureAt</span><span class="sxs-lookup"><span data-stu-id="b4ae9-103">IAgentCharacter::GestureAt</span></span>

<span data-ttu-id="b4ae9-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b4ae9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="b4ae9-105">Reproduz a animação de estado **gesturing** associada com base no local especificado.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-105">Plays the associated **Gesturing** state animation based on the specified location.</span></span>

-   <span data-ttu-id="b4ae9-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="b4ae9-107">Quando a função retorna, *pdwReqID* contém a ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="b4ae9-108"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="b4ae9-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="b4ae9-109">A coordenada x do local especificado em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="b4ae9-109">The x-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="b4ae9-110"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="b4ae9-110"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="b4ae9-111">A coordenada y do local especificado em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="b4ae9-111">The y-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="b4ae9-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="b4ae9-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="b4ae9-113">Endereço de uma variável que recebe a ID de solicitação **GestureAt** .</span><span class="sxs-lookup"><span data-stu-id="b4ae9-113">Address of a variable that receives the **GestureAt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="b4ae9-114">O servidor determina automaticamente e reproduz a animação gesturing apropriada com base na posição atual do caractere e no local especificado.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-114">The server automatically determines and plays the appropriate gesturing animation based on the character's current position and the specified location.</span></span> <span data-ttu-id="b4ae9-115">Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](iagentcharacter--prepare.md) para garantir que as animações estejam disponíveis antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-115">When using the HTTP protocol to access character and animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure that the animations are available before calling this method.</span></span>

 

 




