---
title: Elemento EVENT (SDK do WMP)
description: O elemento EVENT define um comportamento ou uma ação realizada pelo Windows Media Player quando ele recebe um comando de script rotulado como um evento.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Elemento de evento Windows Media Player
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760262"
---
# <a name="event-element"></a><span data-ttu-id="c6e1e-104">Elemento EVENT</span><span class="sxs-lookup"><span data-stu-id="c6e1e-104">EVENT Element</span></span>

<span data-ttu-id="c6e1e-105">O elemento **Event** define um comportamento ou uma ação realizada pelo Windows Media Player quando ele recebe um comando de script rotulado como um evento.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-105">The **EVENT** element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a><span data-ttu-id="c6e1e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c6e1e-106">Attributes</span></span>

<span data-ttu-id="c6e1e-107">**Nome** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="c6e1e-107">**NAME** (required)</span></span>

<span data-ttu-id="c6e1e-108">O nome do evento.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-108">The name of the event.</span></span>

<span data-ttu-id="c6e1e-109">**WHENDONE** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="c6e1e-109">**WHENDONE** (required)</span></span>

<span data-ttu-id="c6e1e-110">Um valor que define o que o Windows Media Player faz depois de reproduzir o conteúdo referenciado.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-110">A value that defines what Windows Media Player does after playing the referenced content.</span></span>

<span data-ttu-id="c6e1e-111">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-111">The following values are possible.</span></span>



| <span data-ttu-id="c6e1e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c6e1e-112">Value</span></span>  | <span data-ttu-id="c6e1e-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6e1e-113">Description</span></span>                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e1e-114">RESUME</span><span class="sxs-lookup"><span data-stu-id="c6e1e-114">RESUME</span></span> | <span data-ttu-id="c6e1e-115">A entrada atual (o clipe interrompido pelo evento) reinicia a reprodução.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-115">The current entry (the clip interrupted by the event) resumes playing.</span></span> <span data-ttu-id="c6e1e-116">Se o conteúdo for armazenado no conteúdo, ele será retomado no mesmo ponto em que foi interrompido; Se o conteúdo for difundido, ele será retomado na posição atual.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-116">If the content is stored content, it resumes at the same point where it stopped; if the content is broadcast, it resumes at the current position.</span></span>        |
| <span data-ttu-id="c6e1e-117">NEXT</span><span class="sxs-lookup"><span data-stu-id="c6e1e-117">NEXT</span></span>   | <span data-ttu-id="c6e1e-118">O próximo elemento de **entrada** é reproduzido como se o evento não tivesse ocorrido e o Windows Media Player atingiu o final do clipe atual.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-118">The next **ENTRY** element plays as if the event had not occurred and Windows Media Player had reached the end of the current clip.</span></span>                                                                                             |
| <span data-ttu-id="c6e1e-119">BREAK</span><span class="sxs-lookup"><span data-stu-id="c6e1e-119">BREAK</span></span>  | <span data-ttu-id="c6e1e-120">Se a entrada atual estiver dentro de um loop de **repetição** , o loop será encerrado como se a contagem de repetição tivesse sido concluída.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-120">If the current entry is within a **REPEAT** loop, the loop terminates as if the repeat count had been completed.</span></span> <span data-ttu-id="c6e1e-121">Caso contrário, o Windows Media Player vai até o final da lista de reprodução como se a entrada final tivesse sido concluída como de costume.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-121">Otherwise, Windows Media Player jumps to the end of the playlist as if the final entry had completed as usual.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="c6e1e-122">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="c6e1e-122">Parent/Child Elements</span></span>



| <span data-ttu-id="c6e1e-123">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="c6e1e-123">Hierarchy</span></span>       | <span data-ttu-id="c6e1e-124">Elementos</span><span class="sxs-lookup"><span data-stu-id="c6e1e-124">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="c6e1e-125">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c6e1e-125">Parent elements</span></span> | <span data-ttu-id="c6e1e-126">**ASX**</span><span class="sxs-lookup"><span data-stu-id="c6e1e-126">**ASX**</span></span>                 |
| <span data-ttu-id="c6e1e-127">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c6e1e-127">Child elements</span></span>  | <span data-ttu-id="c6e1e-128">**entrada**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="c6e1e-128">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c6e1e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6e1e-129">Remarks</span></span>

<span data-ttu-id="c6e1e-130">Esse elemento define um comportamento ou uma ação realizada pelo Windows Media Player quando ele recebe um comando de script rotulado como um evento.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-130">This element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span> <span data-ttu-id="c6e1e-131">Um evento é um tipo específico de comando de script inserido em um fluxo enviado ao Windows Media Player que consiste em uma cadeia de caracteres dupla.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-131">An event is a particular type of script command embedded in a stream sent to Windows Media Player that consists of a double string.</span></span> <span data-ttu-id="c6e1e-132">A primeira cadeia de caracteres é a palavra "Event", e a segunda cadeia de caracteres é o nome do evento.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-132">The first string is the word "event", and the second string is the event name.</span></span> <span data-ttu-id="c6e1e-133">O nome do evento na segunda cadeia de caracteres deve corresponder ao nome do evento definido no metarquivo.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-133">The event name in the second string must match the event name defined in the metafile.</span></span> <span data-ttu-id="c6e1e-134">(A correspondência não diferencia maiúsculas de minúsculas.) Os eventos podem ser enviados para o Windows Media Player recebendo um fluxo em tempo real ou podem ser salvos em um arquivo. ASF,. WMA ou. wmv que é entregue como um fluxo unicast sob demanda.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-134">(The match is not case-sensitive.) Events can be sent to Windows Media Player receiving a real-time stream, or can be saved in an .asf, .wma, or .wmv file that gets delivered as an on-demand unicast stream.</span></span> <span data-ttu-id="c6e1e-135">Quando o Windows Media Player recebe o comando de script, ele processa o evento conforme definido pelo elemento **Event** .</span><span class="sxs-lookup"><span data-stu-id="c6e1e-135">When Windows Media Player receives the script command, it processes the event as defined by the **EVENT** element.</span></span>

<span data-ttu-id="c6e1e-136">Esse elemento define um escopo de elementos **entry** ou **ENTRYREF** que são processados sempre que o Windows Media Player recebe o comando de script com o evento nomeado.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-136">This element defines a scope of **ENTRY** or **ENTRYREF** elements that are processed whenever Windows Media Player receives the script command with the named event.</span></span> <span data-ttu-id="c6e1e-137">O **ENTRYREF** pode ser uma URL que aponta para uma página ASP.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-137">The **ENTRYREF** can be a URL that points to an ASP page.</span></span> <span data-ttu-id="c6e1e-138">Com esse elemento, você pode especificar um comportamento para a alternância de fluxo quase em tempo real, em oposição às alterações de fluxo pré-autorizadas usando referências a outras partes de conteúdo ou os metaarquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-138">With this element, you can specify a behavior for stream switching in near real time, as opposed to pre-authored stream changes using references to other pieces of content or Windows Media metafiles.</span></span>

<span data-ttu-id="c6e1e-139">Ao usar páginas ASP para gerar listas de reprodução, você deve especificar um valor para a *resposta*. Propriedade **ContentType** e a *resposta*. **expira** a propriedade na página ASP devido a problemas de latência com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-139">When you use ASP pages to generate playlists, you must specify a value for the *Response*.**ContentType** property and the *Response*.**expires** property in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="c6e1e-140">A *resposta*. **ContentType** deve ser uma extensão de nome de arquivo válida para os metaarquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-140">The *Response*.**ContentType** must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="c6e1e-141">Os tipos válidos incluem. ASF,. ASX,. WMA,. Wax,. wmv e. wvx.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-141">Valid types include .asf, .asx, .wma, .wax, .wmv, and .wvx.</span></span>

<span data-ttu-id="c6e1e-142">Consulte o SDK da plataforma para obter detalhes sobre como usar o objeto de **resposta** no ASP.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-142">See the Platform SDK for details about using the **Response** object in ASP.</span></span>

<span data-ttu-id="c6e1e-143">Esse elemento pode aparecer em qualquer lugar dentro do elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="c6e1e-143">This element can appear anywhere within the **ASX** element.</span></span> <span data-ttu-id="c6e1e-144">Se vários elementos de **evento** dentro de um elemento **ASX** tiverem valores idênticos para seus atributos de **nome** , o Windows Media Player usará a primeira ocorrência dentro do elemento **ASX** e ignorará todos os outros.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-144">If multiple **EVENT** elements within an **ASX** element have identical values for their **NAME** attributes, Windows Media Player uses the first occurrence within the **ASX** element, and ignores all others.</span></span> <span data-ttu-id="c6e1e-145">Quando elementos de **evento** têm atributos de **nome** distintos, sua ordem dentro do elemento **ASX** não importa.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-145">When **EVENT** elements have distinct **NAME** attributes, their order within the **ASX** element does not matter.</span></span>

<span data-ttu-id="c6e1e-146">O Windows Media Player descarta eventos recebidos durante o processamento de outro evento.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-146">Windows Media Player discards events it receives while processing another event.</span></span> <span data-ttu-id="c6e1e-147">Não há suporte para o aninhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-147">Nesting of events is not supported.</span></span> <span data-ttu-id="c6e1e-148">Quando o Windows Media Player está no modo de visualização, o conteúdo do evento não é restrito pelo elemento **PREVIEWDURATION** ; o comprimento total do conteúdo do evento pode ser reproduzido mesmo se a duração da visualização do elemento de **entrada** ativo expirar antes do final do evento.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-148">When Windows Media Player is in preview mode, event content is not constrained by the **PREVIEWDURATION** element; the full length of event content can play even if the preview duration for the active **ENTRY** element expires prior to the end of the event.</span></span>

## <a name="examples"></a><span data-ttu-id="c6e1e-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6e1e-149">Examples</span></span>

<span data-ttu-id="c6e1e-150">Neste exemplo, quando o Windows Media Player recebe o evento de comando de script e a cadeia de caracteres de comando "Adlink" na mídia de streaming que está renderizando, ele pesquisa na lista de reprodução um **EventName** "Adlink".</span><span class="sxs-lookup"><span data-stu-id="c6e1e-150">In this example, when Windows Media Player receives the script command EVENT and command string "Adlink" in the streaming media it is rendering, it searches the playlist for an **EVENTNAME** "Adlink".</span></span> <span data-ttu-id="c6e1e-151">O Windows Media Player alterna do fluxo que está renderizando e reproduz o conteúdo referenciado no **evento**" https://example.microsoft.com/adlink.htm ".</span><span class="sxs-lookup"><span data-stu-id="c6e1e-151">Windows Media Player switches from the stream it is rendering and plays the content referenced in the **EVENT**, "https://example.microsoft.com/adlink.htm".</span></span>

<span data-ttu-id="c6e1e-152">O atributo de **entrada** **CLIENTSKIP** está definido como não para impedir que o clipe de **evento** seja ignorado.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-152">**ENTRY** attribute **CLIENTSKIP** is set to NO to prevent the **EVENT** clip from being skipped.</span></span> <span data-ttu-id="c6e1e-153">Ele deve ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-153">It must be played.</span></span>

<span data-ttu-id="c6e1e-154">O script `WHENDONE="RESUME"` instrui o Windows Media Player a retomar a reprodução da mídia anterior que ele alternou assim que Adlink. ASF for concluído.</span><span class="sxs-lookup"><span data-stu-id="c6e1e-154">The script `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous media it switched from as soon as Adlink.asf is finished.</span></span>


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="c6e1e-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6e1e-155">Requirements</span></span>



| <span data-ttu-id="c6e1e-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6e1e-156">Requirement</span></span> | <span data-ttu-id="c6e1e-157">Valor</span><span class="sxs-lookup"><span data-stu-id="c6e1e-157">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c6e1e-158">Versão</span><span class="sxs-lookup"><span data-stu-id="c6e1e-158">Version</span></span><br/> | <span data-ttu-id="c6e1e-159">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c6e1e-159">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6e1e-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6e1e-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e1e-161">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c6e1e-161">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="c6e1e-162">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="c6e1e-162">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="c6e1e-163">**Modelo de objeto do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="c6e1e-163">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





