---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006206"
---
# <a name="iagentcharacterplay"></a><span data-ttu-id="0a10e-103">IAgentCharacter::P deite</span><span class="sxs-lookup"><span data-stu-id="0a10e-103">IAgentCharacter::Play</span></span>

<span data-ttu-id="0a10e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a10e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

<span data-ttu-id="0a10e-105">Reproduz a animação especificada.</span><span class="sxs-lookup"><span data-stu-id="0a10e-105">Plays the specified animation.</span></span>

-   <span data-ttu-id="0a10e-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0a10e-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="0a10e-107">Quando a função retorna, *pdwReqID* contém a ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="0a10e-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="0a10e-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span><span class="sxs-lookup"><span data-stu-id="0a10e-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span></span>
</dt> <dd>

<span data-ttu-id="0a10e-109">O nome de uma animação.</span><span class="sxs-lookup"><span data-stu-id="0a10e-109">The name of an animation.</span></span>

</dd> <dt>

<span data-ttu-id="0a10e-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="0a10e-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="0a10e-111">Endereço de uma variável que recebe a ID de solicitação de:P de direcionamento de **IAgentCharacter:** .</span><span class="sxs-lookup"><span data-stu-id="0a10e-111">Address of a variable that receives the **IAgentCharacter::Play** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="0a10e-112">O nome de uma animação é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0a10e-112">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0a10e-113">Antes de reproduzir a animação especificada, o servidor tenta reproduzir a animação de **retorno** para a animação anterior (se uma tiver sido atribuída).</span><span class="sxs-lookup"><span data-stu-id="0a10e-113">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation (if one has been assigned).</span></span>

<span data-ttu-id="0a10e-114">Quando os dados de animação de um caractere são armazenados no computador local do usuário, você pode usar o método **IAgentCharacter::P deite** e especificar o nome da animação.</span><span class="sxs-lookup"><span data-stu-id="0a10e-114">When a character's animation data is stored on the user's local machine, you can use the **IAgentCharacter::Play** method and specify the name of the animation.</span></span> <span data-ttu-id="0a10e-115">Ao usar o protocolo HTTP para acessar dados de animação, use o método [**Prepare**](iagentcharacter--prepare.md) para garantir a disponibilidade da animação antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="0a10e-115">When using the HTTP protocol to access animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure the availability of the animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a10e-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0a10e-116">See Also</span></span>

[<span data-ttu-id="0a10e-117">**IAgentCharacter::P reparênteses**</span><span class="sxs-lookup"><span data-stu-id="0a10e-117">**IAgentCharacter::Prepare**</span></span>](iagentcharacter--prepare.md)


 

 




