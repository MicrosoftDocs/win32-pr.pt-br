---
title: Escutando eventos da faixa de das
description: O Windows Ribbon Framework usa a infraestrutura ETW (rastreamento de eventos para Windows) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de faixas do aplicativo.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Faixa de, eventos do Windows
- Faixa de, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294553"
---
# <a name="listening-for-ribbon-events"></a><span data-ttu-id="4f546-105">Escutando eventos da faixa de das</span><span class="sxs-lookup"><span data-stu-id="4f546-105">Listening for Ribbon Events</span></span>

<span data-ttu-id="4f546-106">O Windows Ribbon Framework usa a infraestrutura [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para permitir que os desenvolvedores aprendam como os usuários estão interagindo com a faixa de faixas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f546-106">The Windows Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="introduction"></a><span data-ttu-id="4f546-107">Introdução</span><span class="sxs-lookup"><span data-stu-id="4f546-107">Introduction</span></span>

<span data-ttu-id="4f546-108">O mecanismo de eventos da estrutura da faixa de faixas foi projetado de modo que a estrutura relate eventos da interface do usuário da faixa de da forma para que você possa monitorar a atividade do usuário, aprender seus padrões de interação e avaliar tendências de uso.</span><span class="sxs-lookup"><span data-stu-id="4f546-108">The Ribbon framework event mechanism is designed such that the framework reports ribbon UI events to the application so you can monitor user activity, learn their interaction patterns, and assess usage trends.</span></span> <span data-ttu-id="4f546-109">Essas informações podem ser usadas para refinar a experiência do usuário para iterações futuras do seu aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="4f546-109">This information can be used to refine the user experience for future iterations of your ribbon app.</span></span>

<span data-ttu-id="4f546-110">O uso dos eventos da estrutura da faixa de opções envolve o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4f546-110">Using the Ribbon framework events involves the following:</span></span>

1.  <span data-ttu-id="4f546-111">O aplicativo da faixa de faixas deve registrar um ouvinte [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) para receber notificações de eventos da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="4f546-111">The ribbon application must register an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener to receive ribbon event notifications from the Ribbon framework.</span></span>
2.  <span data-ttu-id="4f546-112">A estrutura da faixa de chamadas dispara retornos de chamada de evento da interface do usuário em tempo de execução, se o aplicativo tiver registrado um ouvinte [ETW (rastreamento de eventos para Windows)](../etw/event-tracing-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4f546-112">The Ribbon framework fires ribbon UI event callbacks at run time, if the application has registered an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener.</span></span>

## <a name="supported-events"></a><span data-ttu-id="4f546-113">Eventos com suporte</span><span class="sxs-lookup"><span data-stu-id="4f546-113">Supported events</span></span>

<span data-ttu-id="4f546-114">Os eventos expostos aos aplicativos da faixa de opções são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f546-114">The events exposed to ribbon applications are described in the following table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f546-115">Evento</span><span class="sxs-lookup"><span data-stu-id="4f546-115">Event</span></span></th>
<th><span data-ttu-id="4f546-116">Relatório de eventos</span><span class="sxs-lookup"><span data-stu-id="4f546-116">Event report</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4f546-117">Guia ativada</span><span class="sxs-lookup"><span data-stu-id="4f546-117">Tab activated</span></span></td>
<td><span data-ttu-id="4f546-118">ID do comando</span><span class="sxs-lookup"><span data-stu-id="4f546-118">Command ID</span></span><br/> <span data-ttu-id="4f546-119">Nome de comando</span><span class="sxs-lookup"><span data-stu-id="4f546-119">Command name</span></span><br/> <span data-ttu-id="4f546-120">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-120">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f546-121">Guia contextual ativada</span><span class="sxs-lookup"><span data-stu-id="4f546-121">Contextual tab activated</span></span></td>
<td><span data-ttu-id="4f546-122">ID do comando</span><span class="sxs-lookup"><span data-stu-id="4f546-122">Command ID</span></span><br/> <span data-ttu-id="4f546-123">Nome de comando</span><span class="sxs-lookup"><span data-stu-id="4f546-123">Command name</span></span><br/> <span data-ttu-id="4f546-124">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-124">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f546-125">Menu do aplicativo aberto</span><span class="sxs-lookup"><span data-stu-id="4f546-125">Application Menu opened</span></span></td>
<td><span data-ttu-id="4f546-126">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-126">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f546-127">Menu do aplicativo fechado</span><span class="sxs-lookup"><span data-stu-id="4f546-127">Application Menu closed</span></span></td>
<td><span data-ttu-id="4f546-128">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-128">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f546-129">Menu (regular ou galeria) aberto</span><span class="sxs-lookup"><span data-stu-id="4f546-129">Menu (regular or gallery) opened</span></span></td>
<td><span data-ttu-id="4f546-130">ID do comando</span><span class="sxs-lookup"><span data-stu-id="4f546-130">Command ID</span></span><br/> <span data-ttu-id="4f546-131">Nome de comando</span><span class="sxs-lookup"><span data-stu-id="4f546-131">Command name</span></span><br/> <span data-ttu-id="4f546-132">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-132">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4f546-133">Os eventos do menu QAT não são expostos.</span><span class="sxs-lookup"><span data-stu-id="4f546-133">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f546-134">Menu (regular ou galeria) fechado</span><span class="sxs-lookup"><span data-stu-id="4f546-134">Menu (regular or gallery) closed</span></span></td>
<td><span data-ttu-id="4f546-135">ID do comando</span><span class="sxs-lookup"><span data-stu-id="4f546-135">Command ID</span></span><br/> <span data-ttu-id="4f546-136">Nome de comando</span><span class="sxs-lookup"><span data-stu-id="4f546-136">Command name</span></span><br/> <span data-ttu-id="4f546-137">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-137">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4f546-138">Os eventos do menu QAT não são expostos.</span><span class="sxs-lookup"><span data-stu-id="4f546-138">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f546-139">Comando</span><span class="sxs-lookup"><span data-stu-id="4f546-139">Command</span></span></td>
<td><span data-ttu-id="4f546-140">ID do comando</span><span class="sxs-lookup"><span data-stu-id="4f546-140">Command ID</span></span><br/> <span data-ttu-id="4f546-141">Nome de comando</span><span class="sxs-lookup"><span data-stu-id="4f546-141">Command name</span></span><br/> <span data-ttu-id="4f546-142">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-142">Event verb</span></span><br/> <span data-ttu-id="4f546-143">Um dos seguintes locais de evento:</span><span class="sxs-lookup"><span data-stu-id="4f546-143">One of the following event locations:</span></span>
<ul>
<li><span data-ttu-id="4f546-144">3D</span><span class="sxs-lookup"><span data-stu-id="4f546-144">RIBBON</span></span></li>
<li><span data-ttu-id="4f546-145">QUICKACCESSTOOLBAR</span><span class="sxs-lookup"><span data-stu-id="4f546-145">QUICKACCESSTOOLBAR</span></span></li>
<li><span data-ttu-id="4f546-146">APPLICATIONMENU</span><span class="sxs-lookup"><span data-stu-id="4f546-146">APPLICATIONMENU</span></span></li>
<li><span data-ttu-id="4f546-147">CONTEXTPOPUP</span><span class="sxs-lookup"><span data-stu-id="4f546-147">CONTEXTPOPUP</span></span></li>
</ul>
<br/> <span data-ttu-id="4f546-148">ID do comando pai</span><span class="sxs-lookup"><span data-stu-id="4f546-148">Parent Command ID</span></span><br/> <span data-ttu-id="4f546-149">Nome do comando pai</span><span class="sxs-lookup"><span data-stu-id="4f546-149">Parent Command name</span></span><br/> <span data-ttu-id="4f546-150">Um dos seguintes métodos Invoke:</span><span class="sxs-lookup"><span data-stu-id="4f546-150">One of the following invoke methods:</span></span>
<ul>
<li><span data-ttu-id="4f546-151">Selecione</span><span class="sxs-lookup"><span data-stu-id="4f546-151">CLICK</span></span></li>
<li><span data-ttu-id="4f546-152">KEYTIP</span><span class="sxs-lookup"><span data-stu-id="4f546-152">KEYTIP</span></span></li>
<li><span data-ttu-id="4f546-153">TECLADO</span><span class="sxs-lookup"><span data-stu-id="4f546-153">KEYBOARD</span></span></li>
<li><span data-ttu-id="4f546-154">Tom</span><span class="sxs-lookup"><span data-stu-id="4f546-154">TOUCH</span></span></li>
</ul>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4f546-155">As galerias de itens e as caixas de combinação incluem o índice de item selecionado, mas não incluem valores de cadeia de caracteres e inteiros.</span><span class="sxs-lookup"><span data-stu-id="4f546-155">Item galleries and combo boxes include the selected item index but do not include string and integer values.</span></span> <span data-ttu-id="4f546-156">Os eninteriors não incluem o valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="4f546-156">Spinners do not include the integer value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f546-157">Faixa de faixas minimizada</span><span class="sxs-lookup"><span data-stu-id="4f546-157">Ribbon minimized</span></span></td>
<td><span data-ttu-id="4f546-158">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-158">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f546-159">Faixa de faixas expandida (botão de expansão clicado ou toque fixado)</span><span class="sxs-lookup"><span data-stu-id="4f546-159">Ribbon expanded (expand button clicked or tap pinned)</span></span></td>
<td><span data-ttu-id="4f546-160">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-160">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f546-161">Modo de aplicativo alternado</span><span class="sxs-lookup"><span data-stu-id="4f546-161">Application mode switched</span></span></td>
<td><span data-ttu-id="4f546-162">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-162">Event verb</span></span><br/> <span data-ttu-id="4f546-163">ID do modo (valor definido por meio de <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>modos</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="4f546-163">Mode ID (value set through <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4f546-164">O aplicativo é responsável por desempacotar esse inteiro para determinar quais modos foram definidos.</span><span class="sxs-lookup"><span data-stu-id="4f546-164">The application is responsible for unpacking this integer to determine which modes were set.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f546-165">Dica de ferramenta exibida</span><span class="sxs-lookup"><span data-stu-id="4f546-165">Tooltip displayed</span></span></td>
<td><span data-ttu-id="4f546-166">Verbo de evento</span><span class="sxs-lookup"><span data-stu-id="4f546-166">Event verb</span></span><br/> <span data-ttu-id="4f546-167">ID do comando pai</span><span class="sxs-lookup"><span data-stu-id="4f546-167">Parent Command ID</span></span><br/> <span data-ttu-id="4f546-168">Nome do comando pai</span><span class="sxs-lookup"><span data-stu-id="4f546-168">Parent Command name</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4f546-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f546-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f546-170">Guias de desenvolvedor do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="4f546-170">Windows Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)
</dt> <dt>

[<span data-ttu-id="4f546-171">Declarando comandos e controles com marcação de faixa de medida</span><span class="sxs-lookup"><span data-stu-id="4f546-171">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="4f546-172">Diretrizes de experiência do usuário da faixa de das</span><span class="sxs-lookup"><span data-stu-id="4f546-172">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="4f546-173">Processo de design da faixa de das</span><span class="sxs-lookup"><span data-stu-id="4f546-173">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

