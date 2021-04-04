---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007423"
---
# <a name="iagentcharactermoveto"></a><span data-ttu-id="66e4d-103">IAgentCharacter:: MoveTo</span><span class="sxs-lookup"><span data-stu-id="66e4d-103">IAgentCharacter::MoveTo</span></span>

<span data-ttu-id="66e4d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="66e4d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="66e4d-105">Reproduz a animação de estado de **movimentação** associada e move o quadro de caracteres para o local especificado.</span><span class="sxs-lookup"><span data-stu-id="66e4d-105">Plays the associated **Moving** state animation and moves the character frame to the specified location.</span></span>

-   <span data-ttu-id="66e4d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="66e4d-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="66e4d-107">Quando a função retorna, essa variável contém a ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="66e4d-107">When the function returns, this variable contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="66e4d-108"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="66e4d-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="66e4d-109">A coordenada x da nova posição em pixels, relativa à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="66e4d-109">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="66e4d-110">O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.</span><span class="sxs-lookup"><span data-stu-id="66e4d-110">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="66e4d-111"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="66e4d-111"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="66e4d-112">A coordenada y da nova posição em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="66e4d-112">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="66e4d-113">O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.</span><span class="sxs-lookup"><span data-stu-id="66e4d-113">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="66e4d-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span><span class="sxs-lookup"><span data-stu-id="66e4d-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="66e4d-115">Um parâmetro que especifica em milissegundos a velocidade com que o quadro do caractere se move.</span><span class="sxs-lookup"><span data-stu-id="66e4d-115">A parameter specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="66e4d-116">O valor recomendado é 1000.</span><span class="sxs-lookup"><span data-stu-id="66e4d-116">The recommended value is 1000.</span></span> <span data-ttu-id="66e4d-117">A especificação de zero (0) move o quadro sem reproduzir uma animação.</span><span class="sxs-lookup"><span data-stu-id="66e4d-117">Specifying zero (0) moves the frame without playing an animation.</span></span>

</dd> <dt>

<span data-ttu-id="66e4d-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="66e4d-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="66e4d-119">Endereço de uma variável que recebe a ID da solicitação [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .</span><span class="sxs-lookup"><span data-stu-id="66e4d-119">Address of a variable that receives the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="66e4d-120">Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade das animações de estado de **movimentação** antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="66e4d-120">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Moving** state animations before calling this method.</span></span> <span data-ttu-id="66e4d-121">Mesmo que a animação não seja carregada, o servidor ainda moverá o quadro.</span><span class="sxs-lookup"><span data-stu-id="66e4d-121">Even if the animation is not loaded, the server still moves the frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="66e4d-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="66e4d-122">See Also</span></span>

[<span data-ttu-id="66e4d-123">**IAgentCharacter:: SETPOSITION**</span><span class="sxs-lookup"><span data-stu-id="66e4d-123">**IAgentCharacter::SetPosition**</span></span>](iagentcharacter--setposition.md)


 

 