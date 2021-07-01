---
title: IAgentCharacter preparar
description: IAgentCharacter preparar
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119871"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="2092e-103">IAgentCharacter::P reparênteses</span><span class="sxs-lookup"><span data-stu-id="2092e-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="2092e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2092e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="2092e-105">Recupera dados de animação para um caractere.</span><span class="sxs-lookup"><span data-stu-id="2092e-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="2092e-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2092e-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="2092e-107">Quando a função retorna, *pdwReqID* contém a ID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="2092e-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="2092e-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="2092e-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="2092e-109">Um valor que indica o tipo de dados de animação a ser carregado que deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="2092e-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="2092e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2092e-110">Value</span></span>                                                           | <span data-ttu-id="2092e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2092e-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2092e-112">animação de **curta preparação não assinada const** **\_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="2092e-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="2092e-113">Dados de animação de um caractere.</span><span class="sxs-lookup"><span data-stu-id="2092e-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="2092e-114">**const estado curto de preparação não assinado** **\_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="2092e-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="2092e-115">Dados de estado de um caractere.</span><span class="sxs-lookup"><span data-stu-id="2092e-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="2092e-116">**const de curto-circuito sem sinal constante** **\_ = 2**</span><span class="sxs-lookup"><span data-stu-id="2092e-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="2092e-117">Um arquivo de som de um caractere (. WAV ou. LWV) para saída falada.</span><span class="sxs-lookup"><span data-stu-id="2092e-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2092e-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="2092e-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="2092e-119">O nome da animação ou do estado.</span><span class="sxs-lookup"><span data-stu-id="2092e-119">The name of the animation or state.</span></span>

<span data-ttu-id="2092e-120">O nome da animação é baseado nessa definição para o caractere quando ele foi salvo usando o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2092e-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="2092e-121">Para Estados, o valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="2092e-121">For states, the value can be one of the following:</span></span>



|                      | <span data-ttu-id="2092e-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="2092e-122">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="2092e-123">**"Gesturing"**</span><span class="sxs-lookup"><span data-stu-id="2092e-123">**"Gesturing"**</span></span>      | <span data-ttu-id="2092e-124">Para recuperar todas as animações de estado **gesturing** .</span><span class="sxs-lookup"><span data-stu-id="2092e-124">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="2092e-125">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="2092e-125">**"GesturingDown"**</span></span>  | <span data-ttu-id="2092e-126">Para recuperar animações **GesturingDown** .</span><span class="sxs-lookup"><span data-stu-id="2092e-126">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="2092e-127">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="2092e-127">**"GesturingLeft"**</span></span>  | <span data-ttu-id="2092e-128">Para recuperar animações **GesturingLeft** .</span><span class="sxs-lookup"><span data-stu-id="2092e-128">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="2092e-129">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="2092e-129">**"GesturingRight"**</span></span> | <span data-ttu-id="2092e-130">Para recuperar animações **GesturingRight** .</span><span class="sxs-lookup"><span data-stu-id="2092e-130">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="2092e-131">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="2092e-131">**"GesturingUp"**</span></span>    | <span data-ttu-id="2092e-132">Para recuperar animações **GesturingUp** .</span><span class="sxs-lookup"><span data-stu-id="2092e-132">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="2092e-133">**Ocultar**</span><span class="sxs-lookup"><span data-stu-id="2092e-133">**"Hiding"**</span></span>         | <span data-ttu-id="2092e-134">Para recuperar as animações de estado **ocultos** .</span><span class="sxs-lookup"><span data-stu-id="2092e-134">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="2092e-135">**Auditiva**</span><span class="sxs-lookup"><span data-stu-id="2092e-135">**"Hearing"**</span></span>        | <span data-ttu-id="2092e-136">Para recuperar as animações de estado **audição** .</span><span class="sxs-lookup"><span data-stu-id="2092e-136">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="2092e-137">**Deixar**</span><span class="sxs-lookup"><span data-stu-id="2092e-137">**"Idling"**</span></span>         | <span data-ttu-id="2092e-138">Para recuperar todas as animações de estado **deixar** .</span><span class="sxs-lookup"><span data-stu-id="2092e-138">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="2092e-139">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="2092e-139">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="2092e-140">Para recuperar todas as animações **IdlingLevel1** .</span><span class="sxs-lookup"><span data-stu-id="2092e-140">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="2092e-141">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="2092e-141">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="2092e-142">Para recuperar todas as animações **IdlingLevel2** .</span><span class="sxs-lookup"><span data-stu-id="2092e-142">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="2092e-143">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="2092e-143">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="2092e-144">Para recuperar todas as animações **IdlingLevel3** .</span><span class="sxs-lookup"><span data-stu-id="2092e-144">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="2092e-145">**Detecta**</span><span class="sxs-lookup"><span data-stu-id="2092e-145">**"Listening"**</span></span>      | <span data-ttu-id="2092e-146">Para recuperar as animações do estado de **escuta** .</span><span class="sxs-lookup"><span data-stu-id="2092e-146">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="2092e-147">**Movimenta**</span><span class="sxs-lookup"><span data-stu-id="2092e-147">**"Moving"**</span></span>         | <span data-ttu-id="2092e-148">Para recuperar todas as animações de estado **móvel** .</span><span class="sxs-lookup"><span data-stu-id="2092e-148">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="2092e-149">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="2092e-149">**"MovingDown"**</span></span>     | <span data-ttu-id="2092e-150">Para recuperar todas as animações em **movimento** .</span><span class="sxs-lookup"><span data-stu-id="2092e-150">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="2092e-151">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="2092e-151">**"MovingLeft"**</span></span>     | <span data-ttu-id="2092e-152">Para recuperar todas as animações **MovingLeft** .</span><span class="sxs-lookup"><span data-stu-id="2092e-152">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="2092e-153">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="2092e-153">**"MovingRight"**</span></span>    | <span data-ttu-id="2092e-154">Para recuperar todas as animações **MovingRight** .</span><span class="sxs-lookup"><span data-stu-id="2092e-154">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="2092e-155">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="2092e-155">**"MovingUp"**</span></span>       | <span data-ttu-id="2092e-156">Para recuperar todas as animações **MovingUp** .</span><span class="sxs-lookup"><span data-stu-id="2092e-156">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="2092e-157">**Mostrando**</span><span class="sxs-lookup"><span data-stu-id="2092e-157">**"Showing"**</span></span>        | <span data-ttu-id="2092e-158">Para recuperar as animações de estado em **exibição** .</span><span class="sxs-lookup"><span data-stu-id="2092e-158">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="2092e-159">**Língua**</span><span class="sxs-lookup"><span data-stu-id="2092e-159">**"Speaking"**</span></span>       | <span data-ttu-id="2092e-160">Para recuperar as animações de estado de **fala** .</span><span class="sxs-lookup"><span data-stu-id="2092e-160">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="2092e-161">Fins. Arquivos WAV, defina *bszName* para a especificação de URL ou arquivo para o. Arquivo WAV.</span><span class="sxs-lookup"><span data-stu-id="2092e-161">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="2092e-162">Se a especificação não for concluída, ela será interpretada como sendo relativa à especificação usada no método [**Load**](https://www.bing.com/search?q=**Load**) .</span><span class="sxs-lookup"><span data-stu-id="2092e-162">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="2092e-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="2092e-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="2092e-164">Um booliano que especifica se o servidor enfileira a solicitação de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="2092e-164">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="2092e-165">**True** enfileira a solicitação e faz com que qualquer solicitação de animação a seguir aguarde até que os dados de animação que ele especifica sejam carregados.</span><span class="sxs-lookup"><span data-stu-id="2092e-165">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="2092e-166">**False** recupera os dados de animação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2092e-166">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="2092e-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="2092e-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="2092e-168">Endereço de uma variável que recebe a ID da solicitação de [**preparação**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="2092e-168">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="2092e-169">Se você carregar um caractere usando o protocolo HTTP (um. Arquivo ACF), você deve usar o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para recuperar dados de animação antes de poder reproduzir a animação.</span><span class="sxs-lookup"><span data-stu-id="2092e-169">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="2092e-170">Você não poderá usar esse método se tiver carregado o caractere usando o protocolo UNC (um. Arquivo ACS).</span><span class="sxs-lookup"><span data-stu-id="2092e-170">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="2092e-171">Você também não pode recuperar dados HTTP para um caractere usando **Prepare** se você carregou esse caractere usando o protocolo UNC (. Arquivo de caracteres do ACS).</span><span class="sxs-lookup"><span data-stu-id="2092e-171">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="2092e-172">Dados de animação ou de som recuperados com o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) são armazenados no cache do navegador.</span><span class="sxs-lookup"><span data-stu-id="2092e-172">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="2092e-173">As chamadas subsequentes verificarão o cache e, se os dados da animação já estiverem lá, o controle carregará os dados diretamente do cache.</span><span class="sxs-lookup"><span data-stu-id="2092e-173">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="2092e-174">Depois de carregados, os dados de animação ou de som podem ser reproduzidos com os métodos [**Play**](/windows/desktop/lwef/iagentcharacter--play) ou [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="2092e-174">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="2092e-175">Você pode especificar várias animações e Estados separando-os com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="2092e-175">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="2092e-176">No entanto, você não pode misturar tipos na mesma instrução [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="2092e-176">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

