---
title: Intervalos
description: Intervalos
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- TSF (estrutura de serviços de texto), intervalos
- TSF (estrutura de serviços de texto), intervalos
- serviços de texto, intervalos
- Aplicativos habilitados para TSF, intervalos
- ranges
- TSF (estrutura de serviços de texto), âncoras
- TSF (estrutura de serviços de texto), âncoras
- serviços de texto, âncoras
- Aplicativos habilitados para TSF, âncoras
- âncoras
- TSF (estrutura de serviços de texto), clones
- TSF (estrutura de serviços de texto), clones
- serviços de texto, clones
- Aplicativos habilitados para TSF, clones
- clones
- TSF (estrutura de serviços de texto), backups
- TSF (estrutura de serviços de texto), backups
- serviços de texto, backups
- Aplicativos habilitados para TSF, backups
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916612"
---
# <a name="ranges"></a><span data-ttu-id="89791-123">Intervalos</span><span class="sxs-lookup"><span data-stu-id="89791-123">Ranges</span></span>

## <a name="anchors"></a><span data-ttu-id="89791-124">Âncoras</span><span class="sxs-lookup"><span data-stu-id="89791-124">Anchors</span></span>

<span data-ttu-id="89791-125">Um intervalo é delimitado por duas *âncoras*, uma âncora inicial e uma âncora final.</span><span class="sxs-lookup"><span data-stu-id="89791-125">A range is delimited by two *anchors*, a start anchor and an end anchor.</span></span> <span data-ttu-id="89791-126">Existe uma âncora em um slot imaginário entre dois caracteres.</span><span class="sxs-lookup"><span data-stu-id="89791-126">An anchor exists in an imaginary slot between two characters.</span></span> <span data-ttu-id="89791-127">A âncora inicial está relacionada ao texto que segue a âncora e a âncora final está relacionada ao texto que precede a âncora.</span><span class="sxs-lookup"><span data-stu-id="89791-127">The start anchor relates to text that follows the anchor and the end anchor relates to text that precedes the anchor.</span></span> <span data-ttu-id="89791-128">As âncoras de início e de término podem existir no mesmo local.</span><span class="sxs-lookup"><span data-stu-id="89791-128">Both the start and end anchors can exist in the same location.</span></span> <span data-ttu-id="89791-129">Nesse caso, o intervalo tem comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="89791-129">In this case, the range has zero length.</span></span>

<span data-ttu-id="89791-130">Por exemplo, comece com o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="89791-130">For example, start with the following text:</span></span>


```C++
This is text.
```



<span data-ttu-id="89791-131">Agora, aplique um intervalo a esse texto com as âncoras início e término na posição 0.</span><span class="sxs-lookup"><span data-stu-id="89791-131">Now apply a range to this text with both the start and end anchors at position 0.</span></span> <span data-ttu-id="89791-132">Ele é visualmente representado como:</span><span class="sxs-lookup"><span data-stu-id="89791-132">It is visually represented as:</span></span>


```C++
<anchor></anchor>This is text.
```



<span data-ttu-id="89791-133">As âncoras não ocupam nenhum espaço no próprio texto.</span><span class="sxs-lookup"><span data-stu-id="89791-133">The anchors do not take up any space within the text itself.</span></span> <span data-ttu-id="89791-134">Este é um intervalo de comprimento zero e seu texto está vazio.</span><span class="sxs-lookup"><span data-stu-id="89791-134">This is a zero-length range and its text is empty.</span></span>

<span data-ttu-id="89791-135">Agora, mude a âncora final + 3 posições.</span><span class="sxs-lookup"><span data-stu-id="89791-135">Now shift the end anchor +3 positions.</span></span> <span data-ttu-id="89791-136">Ele é visualmente representado como:</span><span class="sxs-lookup"><span data-stu-id="89791-136">It is visually represented as:</span></span>


```C++
<anchor>Thi</anchor>s is text.
```



<span data-ttu-id="89791-137">A âncora inicial é posicionada logo antes do caractere na posição 0 e a âncora final é posicionada logo após o caractere na posição 3 porque a âncora final foi movida para os três locais certos.</span><span class="sxs-lookup"><span data-stu-id="89791-137">The start anchor is positioned just before the character in position 0 and the end anchor is positioned just after the character in position 3 because the end anchor moved to the right 3 places.</span></span> <span data-ttu-id="89791-138">O intervalo de texto agora é "Thi".</span><span class="sxs-lookup"><span data-stu-id="89791-138">The range of text is now "Thi".</span></span>

<span data-ttu-id="89791-139">Além disso, a âncora inicial não pode ser feita para seguir a âncora final e a âncora final não pode ser feita para preceder a âncora inicial.</span><span class="sxs-lookup"><span data-stu-id="89791-139">Additionally, the start anchor cannot be made to follow the end anchor and the end anchor cannot be made to precede the start anchor.</span></span>

## <a name="anchor-gravity"></a><span data-ttu-id="89791-140">Gravidade da âncora</span><span class="sxs-lookup"><span data-stu-id="89791-140">Anchor Gravity</span></span>

<span data-ttu-id="89791-141">Cada âncora tem uma configuração de *gravidade* que determina como a âncora responde quando o texto é inserido no fluxo de texto na posição da âncora.</span><span class="sxs-lookup"><span data-stu-id="89791-141">Each anchor has a *gravity* setting that determines how the anchor responds when text is inserted into the text stream at the anchor position.</span></span> <span data-ttu-id="89791-142">Quando uma inserção é feita na posição de uma âncora, um ajuste deve ser feito na posição da âncora.</span><span class="sxs-lookup"><span data-stu-id="89791-142">When an insertion is made at the position of an anchor, an adjustment must be made in the position of the anchor.</span></span> <span data-ttu-id="89791-143">A gravidade determina como esse ajuste de posição de ancoragem é feito.</span><span class="sxs-lookup"><span data-stu-id="89791-143">The gravity determines how this anchor position adjustment is made.</span></span>

<span data-ttu-id="89791-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="89791-144">For example:</span></span>


```C++
It is <anchor></anchor>cold today.
```



<span data-ttu-id="89791-145">Se a palavra "muito" for inserida na posição do intervalo, a âncora de início poderá ser posicionada antes ou depois da palavra inserida:</span><span class="sxs-lookup"><span data-stu-id="89791-145">If the word "very " is inserted at the range position, the start anchor can be positioned either before or after the inserted word:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="89791-146">\- Ou –</span><span class="sxs-lookup"><span data-stu-id="89791-146">\- Or -</span></span>


```C++
It is very <anchor></anchor>cold today.
```



<span data-ttu-id="89791-147">A gravidade da âncora especifica como a âncora é reposicionada quando uma inserção é feita em sua posição.</span><span class="sxs-lookup"><span data-stu-id="89791-147">The anchor gravity specifies how the anchor is repositioned when an insertion is made at its position.</span></span> <span data-ttu-id="89791-148">A gravidade pode ser *retroativa* ou *posterior*.</span><span class="sxs-lookup"><span data-stu-id="89791-148">The gravity can be either *backward* or *forward*.</span></span>

<span data-ttu-id="89791-149">Se a âncora tiver gravidade regressiva, a âncora retrocederá, em relação ao ponto de inserção, na inserção para que o texto inserido siga a âncora:</span><span class="sxs-lookup"><span data-stu-id="89791-149">If the anchor has backward gravity, the anchor moves backward, relative to the insertion point, on insertion so that the inserted text follows the anchor:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="89791-150">Se a âncora tiver gravidade progressiva, a âncora avançará (em relação ao ponto de inserção) na inserção para que o texto inserido preceda a âncora:</span><span class="sxs-lookup"><span data-stu-id="89791-150">If the anchor has forward gravity, the anchor moves forward (relative to the insertion point) on insertion so that the inserted text precedes the anchor:</span></span>


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a><span data-ttu-id="89791-151">Clones e backups</span><span class="sxs-lookup"><span data-stu-id="89791-151">Clones and Backups</span></span>

<span data-ttu-id="89791-152">Há duas maneiras de fazer uma "cópia" de um objeto Range.</span><span class="sxs-lookup"><span data-stu-id="89791-152">There are two ways to make a "copy" of a range object.</span></span> <span data-ttu-id="89791-153">A primeira é fazer um *clone* do intervalo usando [ITfRange:: clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span><span class="sxs-lookup"><span data-stu-id="89791-153">The first is to make a *clone* of the range using [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span></span> <span data-ttu-id="89791-154">A segunda é fazer um *backup* do intervalo usando [ITfContext:: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span><span class="sxs-lookup"><span data-stu-id="89791-154">The second is to make a *backup* of the range using [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span></span>

<span data-ttu-id="89791-155">Um clone é uma cópia de um intervalo que não inclui dados estáticos.</span><span class="sxs-lookup"><span data-stu-id="89791-155">A clone is a copy of a range that does not include static data.</span></span> <span data-ttu-id="89791-156">As âncoras do intervalo são copiadas, mas o clone ainda cobre um intervalo de texto dentro do contexto.</span><span class="sxs-lookup"><span data-stu-id="89791-156">The anchors of the range are copied, but the clone still covers a range of text within the context.</span></span> <span data-ttu-id="89791-157">Um clone é um objeto de intervalo em todos os aspectos.</span><span class="sxs-lookup"><span data-stu-id="89791-157">A clone is a range object in all respects.</span></span> <span data-ttu-id="89791-158">Isso significa que o texto e as propriedades de um intervalo clonado são dinâmicos e serão alterados se o texto e/ou as propriedades do intervalo cobertos pelo clone forem alterados.</span><span class="sxs-lookup"><span data-stu-id="89791-158">This means that the text and properties for a cloned range are dynamic and will change if the text and/or properties of the range covered by the clone changes.</span></span>

<span data-ttu-id="89791-159">Um backup armazena o texto e as propriedades de um intervalo no momento em que o backup é feito como dados estáticos.</span><span class="sxs-lookup"><span data-stu-id="89791-159">A backup stores the text and properties of a range at the time the backup is made as static data.</span></span> <span data-ttu-id="89791-160">Um backup também clona o intervalo original para que as alterações no tamanho e na posição do intervalo original possam ser rastreadas.</span><span class="sxs-lookup"><span data-stu-id="89791-160">A backup also clones the original range so that changes to the size and position of the original range can be tracked.</span></span> <span data-ttu-id="89791-161">Isso significa que o texto e as propriedades de um intervalo de backup são estáticos e não são alterados se o texto e/ou as propriedades do intervalo cobertos pelo backup forem alterados.</span><span class="sxs-lookup"><span data-stu-id="89791-161">This means that the text and properties for a backed up range are static and do not change if the text and/or properties of the range covered by the backup changes.</span></span>

<span data-ttu-id="89791-162">Por exemplo, o seguinte intervalo (pRange) no contexto:</span><span class="sxs-lookup"><span data-stu-id="89791-162">For example, the following range (pRange) within the context:</span></span>


```C++
"This is some <pRange>text</pRange>."
```



<span data-ttu-id="89791-163">Agora faça um clone e um backup desse intervalo:</span><span class="sxs-lookup"><span data-stu-id="89791-163">Now make a clone and a backup of this range:</span></span>


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



<span data-ttu-id="89791-164">Agora, os objetos contêm o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89791-164">Now, the objects contain the following:</span></span>


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="89791-165">Agora, altere o texto de pRange:</span><span class="sxs-lookup"><span data-stu-id="89791-165">Now change the text of pRange:</span></span>


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



<span data-ttu-id="89791-166">Agora, os objetos contêm o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89791-166">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="89791-167">Definir o texto fez com que o texto dentro do contexto fosse alterado.</span><span class="sxs-lookup"><span data-stu-id="89791-167">Setting the text caused the text within the context to change.</span></span> <span data-ttu-id="89791-168">Ele também fez com que a âncora final de pRange e pClone fosse alterada.</span><span class="sxs-lookup"><span data-stu-id="89791-168">It also caused the end anchor of pRange and pClone to change.</span></span> <span data-ttu-id="89791-169">pClone agora contém "outras palavras" porque o texto foi alterado dentro do intervalo e essas alterações são controladas por todos os intervalos.</span><span class="sxs-lookup"><span data-stu-id="89791-169">pClone now contains "other words" because the text changed within the range and these changes are tracked by all ranges.</span></span> <span data-ttu-id="89791-170">Quando o texto coberto por pRange e pClone alterado, o texto de pClone também mudou.</span><span class="sxs-lookup"><span data-stu-id="89791-170">When the text covered by both pRange and pClone changed, the text of pClone changed as well.</span></span>

<span data-ttu-id="89791-171">O texto em pBackup não foi alterado do pRange original porque os dados (texto e propriedades) no backup não estão relacionados ao contexto e são armazenados separadamente.</span><span class="sxs-lookup"><span data-stu-id="89791-171">The text in pBackup has not changed from the original pRange because the data (text and properties) in the backup is unrelated to the context and is stored separately.</span></span> <span data-ttu-id="89791-172">O clone contido no backup realmente muda, mas os dados são estáticos.</span><span class="sxs-lookup"><span data-stu-id="89791-172">The clone contained within the backup does actually change, but the data is static.</span></span>

<span data-ttu-id="89791-173">Ao restaurar um backup, o backup pode ser aplicado ao clone dentro do backup ou a um intervalo diferente inteiramente.</span><span class="sxs-lookup"><span data-stu-id="89791-173">When restoring a backup, the backup can be applied to the clone within the backup or to a different range entirely.</span></span> <span data-ttu-id="89791-174">Para aplicar o backup ao clone no backup, passe **NULL** para [ITfRangeBackup:: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , conforme mostrado no exemplo de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="89791-174">To apply the backup to the clone within the backup, pass **NULL** to [ITfRangeBackup::Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) as shown in the following code example:</span></span>


```C++
pBackup->Restore(ec, NULL);
```



<span data-ttu-id="89791-175">Agora, os objetos contêm o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89791-175">Now, the objects contain the following:</span></span>


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="89791-176">Para restaurar o backup em um intervalo diferente, passe um ponteiro para o objeto Range ao chamar **ITfRangeBackup:: Restore**.</span><span class="sxs-lookup"><span data-stu-id="89791-176">To restore the backup to a different range, pass a pointer to the range object when calling **ITfRangeBackup::Restore**.</span></span> <span data-ttu-id="89791-177">O texto e as propriedades de backup serão aplicados ao novo intervalo.</span><span class="sxs-lookup"><span data-stu-id="89791-177">The backed up text and properties will be applied to the new range.</span></span> <span data-ttu-id="89791-178">Por exemplo, usando o exemplo acima antes da chamada de **restauração** , pRange será modificado para demonstrar isso:</span><span class="sxs-lookup"><span data-stu-id="89791-178">For example, using the example above prior to the **Restore** call, pRange will be modified to demonstrate this:</span></span>


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



<span data-ttu-id="89791-179">Agora, os objetos contêm o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89791-179">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="89791-180">Quando a âncora final de pRange foi deslocada para os dois locais à esquerda, a âncora final de pClone não foi alterada.</span><span class="sxs-lookup"><span data-stu-id="89791-180">When the end anchor of pRange was shifted to the left two places, the end anchor of pClone did not change.</span></span>

<span data-ttu-id="89791-181">Agora, restaure o backup usando pRange com o seguinte exemplo de código:</span><span class="sxs-lookup"><span data-stu-id="89791-181">Now restore the backup using pRange with the following code example:</span></span>


```C++
pBackup->Restore(ec, pRange);
```



<span data-ttu-id="89791-182">Agora, os objetos contêm o seguinte:</span><span class="sxs-lookup"><span data-stu-id="89791-182">Now, the objects contain the following:</span></span>


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



<span data-ttu-id="89791-183">O texto coberto por pRange foi substituído por "text", uma parte do texto coberta por pClone foi alterada e pBackup muda para corresponder a pRange.</span><span class="sxs-lookup"><span data-stu-id="89791-183">The text covered by pRange has been replaced with "text", a portion of the text covered by pClone has changed, and pBackup changes to match pRange.</span></span>

 

 




