---
title: Sobre controles SysLink
description: Um controle SysLink é uma janela que renderiza o texto marcado para cima e notifica o aplicativo quando os usuários clicam em seus hiperlinks inseridos. Esse controle fornece uma alternativa conveniente ao uso do botão link de comando. Para obter mais informações, consulte tipos de botão.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008429"
---
# <a name="about-syslink-controls"></a><span data-ttu-id="ec509-105">Sobre controles SysLink</span><span class="sxs-lookup"><span data-stu-id="ec509-105">About SysLink Controls</span></span>

<span data-ttu-id="ec509-106">Um controle SysLink é uma janela que renderiza o texto marcado para cima e notifica o aplicativo quando os usuários clicam em seus hiperlinks inseridos.</span><span class="sxs-lookup"><span data-stu-id="ec509-106">A SysLink control is a window that renders marked-up text, and notifies the application when users click its embedded hyperlinks.</span></span> <span data-ttu-id="ec509-107">Esse controle fornece uma alternativa conveniente ao uso do [**botão link de comando**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="ec509-107">This control provides a convenient alternative to using the [**Command link button**](button-styles.md).</span></span> <span data-ttu-id="ec509-108">Para obter mais informações, consulte [tipos de botão](button-types-and-styles.md).</span><span class="sxs-lookup"><span data-stu-id="ec509-108">For more information, see [Button Types](button-types-and-styles.md).</span></span>

<span data-ttu-id="ec509-109">Cada controle SysLink pode dar suporte a vários hiperlinks e você pode acessar cada hiperlink por meio de um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="ec509-109">Each SysLink control can support multiple hyperlinks, and you can access each hyperlink through a zero-based index.</span></span> <span data-ttu-id="ec509-110">O controle SysLink é definido no ComCtl32.dll versão 6 e requer um manifesto ou diretiva que especifica que a versão 6 da DLL deve ser usada se estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="ec509-110">The SysLink control is defined in the ComCtl32.dll version 6, and it requires a manifest or directive that specifies that version 6 of the DLL should be used if it is available.</span></span> <span data-ttu-id="ec509-111">Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ec509-111">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="ec509-112">Este artigo inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec509-112">This article contains the following sections.</span></span>

-   [<span data-ttu-id="ec509-113">Marcação SysLink</span><span class="sxs-lookup"><span data-stu-id="ec509-113">SysLink Markup</span></span>](#syslink-markup)
-   [<span data-ttu-id="ec509-114">Atributos de link</span><span class="sxs-lookup"><span data-stu-id="ec509-114">Link Attributes</span></span>](#link-attributes)
-   [<span data-ttu-id="ec509-115">Estados de link</span><span class="sxs-lookup"><span data-stu-id="ec509-115">Link States</span></span>](#link-states)
-   [<span data-ttu-id="ec509-116">Limitações na exibição de texto bidirecional</span><span class="sxs-lookup"><span data-stu-id="ec509-116">Limitations on Bidirectional Text Display</span></span>](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a><span data-ttu-id="ec509-117">Marcação SysLink</span><span class="sxs-lookup"><span data-stu-id="ec509-117">SysLink Markup</span></span>

<span data-ttu-id="ec509-118">O controle SysLink dá suporte à marca de âncora ( &lt; a &gt; ) junto com os atributos **href** e **ID**.</span><span class="sxs-lookup"><span data-stu-id="ec509-118">The SysLink control supports the anchor tag(&lt;a&gt;) along with the attributes **HREF** and **ID**.</span></span> <span data-ttu-id="ec509-119">Um **href** pode ser qualquer protocolo, como http, FTP e mailto.</span><span class="sxs-lookup"><span data-stu-id="ec509-119">An **HREF** can be any protocol, such as http, ftp, and mailto.</span></span> <span data-ttu-id="ec509-120">Uma **ID** é um nome opcional, exclusivo dentro de um controle Syslink e está associado a um link individual.</span><span class="sxs-lookup"><span data-stu-id="ec509-120">An **ID** is an optional name, unique within a SysLink control, and it is associated with an individual link.</span></span> <span data-ttu-id="ec509-121">Os links também são atribuídos a um índice de base zero de acordo com sua posição dentro da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ec509-121">Links are also assigned a zero-based index according to their position within the string.</span></span> <span data-ttu-id="ec509-122">Esse índice é usado para acessar um link.</span><span class="sxs-lookup"><span data-stu-id="ec509-122">This index is used to access a link.</span></span>

## <a name="link-attributes"></a><span data-ttu-id="ec509-123">Atributos de link</span><span class="sxs-lookup"><span data-stu-id="ec509-123">Link Attributes</span></span>

<span data-ttu-id="ec509-124">Os atributos de cada link podem ser definidos dentro da marca de âncora para cada link ou enviando a [**mensagem \_ SETITEM do LM**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ec509-124">Each link's attributes can be set either within the anchor tag for each link or by sending the [**LM\_SETITEM**](lm-setitem.md) message.</span></span> <span data-ttu-id="ec509-125">Definir um atributo especificando-o dentro da cadeia de inicialização simplesmente inicializa o valor.</span><span class="sxs-lookup"><span data-stu-id="ec509-125">Setting an attribute by specifying it within the initialization string merely initializes the value.</span></span> <span data-ttu-id="ec509-126">Você pode alterar o valor de um atributo por meio do uso subsequente da mensagem **\_ SETITEM do LM** .</span><span class="sxs-lookup"><span data-stu-id="ec509-126">You can change the value of an attribute through subsequent use of the **LM\_SETITEM** message.</span></span>

## <a name="link-states"></a><span data-ttu-id="ec509-127">Estados de link</span><span class="sxs-lookup"><span data-stu-id="ec509-127">Link States</span></span>

<span data-ttu-id="ec509-128">Os itens de link podem estar em qualquer um dos três Estados, representados pelos sinalizadores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec509-128">Link items can be in any one of three states, represented by the flags in the following table.</span></span>



| <span data-ttu-id="ec509-129">Sinalizador de estado</span><span class="sxs-lookup"><span data-stu-id="ec509-129">State flag</span></span>   | <span data-ttu-id="ec509-130">Aparência e significado</span><span class="sxs-lookup"><span data-stu-id="ec509-130">Appearance and meaning</span></span>                                            |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="ec509-131">LIS \_ focado</span><span class="sxs-lookup"><span data-stu-id="ec509-131">LIS\_FOCUSED</span></span> | <span data-ttu-id="ec509-132">O link tem o foco do teclado e pressionar Enter o ativa.</span><span class="sxs-lookup"><span data-stu-id="ec509-132">The link has the keyboard focus, and pressing Enter activates it.</span></span> |
| <span data-ttu-id="ec509-133">LIS \_ habilitado</span><span class="sxs-lookup"><span data-stu-id="ec509-133">LIS\_ENABLED</span></span> | <span data-ttu-id="ec509-134">O link está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ec509-134">The link is enabled.</span></span>                                              |
| <span data-ttu-id="ec509-135">LIS \_ visitado</span><span class="sxs-lookup"><span data-stu-id="ec509-135">LIS\_VISITED</span></span> | <span data-ttu-id="ec509-136">O usuário já visitou a URL representada pelo link.</span><span class="sxs-lookup"><span data-stu-id="ec509-136">The user has already visited the URL represented by the link.</span></span>     |



 

## <a name="limitations-on-bidirectional-text-display"></a><span data-ttu-id="ec509-137">Limitações na exibição de texto bidirecional</span><span class="sxs-lookup"><span data-stu-id="ec509-137">Limitations on Bidirectional Text Display</span></span>

<span data-ttu-id="ec509-138">Algumas linguagens, como árabe ou Hebraico, são escritas da direita para a esquerda (RTL); O inglês é escrito da esquerda para a direita (EPD).</span><span class="sxs-lookup"><span data-stu-id="ec509-138">Some languages, such as Arabic or Hebrew, are written right-to-left (RTL); English is written left-to-right (LTR).</span></span> <span data-ttu-id="ec509-139">A combinação de DPE com EPD é chamada de texto bidirecional.</span><span class="sxs-lookup"><span data-stu-id="ec509-139">Combining RTL with LTR is called bidirectional text.</span></span> <span data-ttu-id="ec509-140">Misturar construções de marcação direcional e Unicode EPD e RTL em cadeias de caracteres de recurso, como marcadores de fluxo bidirecionais para controlar o fluxo de cadeias de caracteres, pode não produzir o resultado esperado ao usar um controle SysLink.</span><span class="sxs-lookup"><span data-stu-id="ec509-140">Mixing LTR and RTL Unicode or HTML directional markup constructs in resource strings, as bidirectional flow markers to control the flow of strings, may not produce the expected result when using a SysLink control.</span></span> <span data-ttu-id="ec509-141">Por exemplo, uma sentença marcada como EPD pode não ser exibida corretamente no contexto RTL.</span><span class="sxs-lookup"><span data-stu-id="ec509-141">For instance, an LTR-marked sentence may not display correctly in RTL context.</span></span>

> [!Note]  
> <span data-ttu-id="ec509-142">Os controles SysLink não dão suporte à exibição bidirecional em todos os cenários.</span><span class="sxs-lookup"><span data-stu-id="ec509-142">SysLink controls do not support bidirectional display under all scenarios.</span></span> <span data-ttu-id="ec509-143">Use um controle SysLink somente se você souber que um layout simples EPD ou RTL é adequado.</span><span class="sxs-lookup"><span data-stu-id="ec509-143">Use a SysLink control only if you know that a simple LTR or RTL layout is adequate.</span></span> <span data-ttu-id="ec509-144">Caso contrário, considere o uso de uma tecnologia mais avançada, como [mshtml](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ec509-144">Otherwise, consider using a more advanced technology such as [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span></span>

 

 

 