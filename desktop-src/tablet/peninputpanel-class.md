---
description: O objeto PenInputPanel permite que você adicione facilmente entrada de caneta in-loco aos seus aplicativos.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Classe PenInputPanel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781428"
---
# <a name="peninputpanel-class"></a><span data-ttu-id="61ba8-103">Classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="61ba8-103">PenInputPanel class</span></span>

<span data-ttu-id="61ba8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="61ba8-104">\[Deprecated.</span></span> <span data-ttu-id="61ba8-105">**PenInputPanel** foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).\]</span><span class="sxs-lookup"><span data-stu-id="61ba8-105">**PenInputPanel** has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).\]</span></span>

<span data-ttu-id="61ba8-106">O objeto **PenInputPanel** permite que você adicione facilmente entrada de caneta in-loco aos seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="61ba8-106">The **PenInputPanel** object enables you to easily add in-place pen input to your applications.</span></span>

<span data-ttu-id="61ba8-107">O objeto **PenInputPanel** está disponível como um objeto anexável que permite adicionar funcionalidade do painel de entrada do Tablet PC a controles existentes.</span><span class="sxs-lookup"><span data-stu-id="61ba8-107">The **PenInputPanel** object is available as an attachable object that allows you to add Tablet PC Input Panel functionality to existing controls.</span></span> <span data-ttu-id="61ba8-108">A interface do usuário é amplamente exigida pelo idioma de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="61ba8-108">The user interface is largely mandated by the current input language.</span></span> <span data-ttu-id="61ba8-109">Você tem a opção de escolher o método de entrada padrão para o objeto **PenInputPanel** , um manuscrito ou um teclado.</span><span class="sxs-lookup"><span data-stu-id="61ba8-109">You have the option of choosing the default input method for the **PenInputPanel** object, either handwriting or keyboard.</span></span> <span data-ttu-id="61ba8-110">O usuário final pode alternar entre os métodos de entrada usando os botões na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="61ba8-110">The end user can switch between input methods using buttons on the user interface.</span></span>

<span data-ttu-id="61ba8-111">**PenInputPanel** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="61ba8-111">**PenInputPanel** has these types of members:</span></span>

-   [<span data-ttu-id="61ba8-112">Enumerações</span><span class="sxs-lookup"><span data-stu-id="61ba8-112">Enumerations</span></span>](#enumerations)
-   [<span data-ttu-id="61ba8-113">Eventos</span><span class="sxs-lookup"><span data-stu-id="61ba8-113">Events</span></span>](#events)
-   [<span data-ttu-id="61ba8-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="61ba8-114">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="61ba8-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="61ba8-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="61ba8-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61ba8-116">Properties</span></span>](#properties)

### <a name="enumerations"></a><span data-ttu-id="61ba8-117">Enumerações</span><span class="sxs-lookup"><span data-stu-id="61ba8-117">Enumerations</span></span>

<span data-ttu-id="61ba8-118">A classe **PenInputPanel** tem essas enumerações.</span><span class="sxs-lookup"><span data-stu-id="61ba8-118">The **PenInputPanel** class has these enumerations.</span></span>



| <span data-ttu-id="61ba8-119">Enumeração</span><span class="sxs-lookup"><span data-stu-id="61ba8-119">Enumeration</span></span>                    | <span data-ttu-id="61ba8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ba8-120">Description</span></span>                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61ba8-121">**PanelType**</span><span class="sxs-lookup"><span data-stu-id="61ba8-121">**PanelType**</span></span>](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | <span data-ttu-id="61ba8-122">Define o tipo de entrada disponível no momento no objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="61ba8-122">Defines the type of input currently available in the **PenInputPanel** object.</span></span><br/> |



 

### <a name="events"></a><span data-ttu-id="61ba8-123">Eventos</span><span class="sxs-lookup"><span data-stu-id="61ba8-123">Events</span></span>

<span data-ttu-id="61ba8-124">A classe **PenInputPanel** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="61ba8-124">The **PenInputPanel** class has these events.</span></span>



| <span data-ttu-id="61ba8-125">Evento</span><span class="sxs-lookup"><span data-stu-id="61ba8-125">Event</span></span>                                                  | <span data-ttu-id="61ba8-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ba8-126">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61ba8-127">**InputFailed**</span><span class="sxs-lookup"><span data-stu-id="61ba8-127">**InputFailed**</span></span>](peninputpanel-inputfailed.md)       | <span data-ttu-id="61ba8-128">Ocorre quando o foco de entrada é alterado antes que o objeto **PenInputPanel** pudesse inserir a entrada do usuário no controle anexado.</span><span class="sxs-lookup"><span data-stu-id="61ba8-128">Occurs when input focus changes before the **PenInputPanel** object was able to insert user input into the attached control.</span></span><br/> |
| [<span data-ttu-id="61ba8-129">**Painelchanged**</span><span class="sxs-lookup"><span data-stu-id="61ba8-129">**PanelChanged**</span></span>](peninputpanel-panelchanged.md)     | <span data-ttu-id="61ba8-130">Ocorre quando o objeto **PenInputPanel** é alterado entre layouts.</span><span class="sxs-lookup"><span data-stu-id="61ba8-130">Occurs when the **PenInputPanel** object changes between layouts.</span></span><br/>                                                            |
| [<span data-ttu-id="61ba8-131">**PanelMoving**</span><span class="sxs-lookup"><span data-stu-id="61ba8-131">**PanelMoving**</span></span>](peninputpanel-panelmoving.md)       | <span data-ttu-id="61ba8-132">Ocorre quando o objeto **PenInputPanel** está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="61ba8-132">Occurs when the **PenInputPanel** object is moving.</span></span><br/>                                                                          |
| [<span data-ttu-id="61ba8-133">**VisibleChanged**</span><span class="sxs-lookup"><span data-stu-id="61ba8-133">**VisibleChanged**</span></span>](peninputpanel-visiblechanged.md) | <span data-ttu-id="61ba8-134">Ocorre quando o objeto **PenInputPanel** é exibido ou oculto.</span><span class="sxs-lookup"><span data-stu-id="61ba8-134">Occurs when the **PenInputPanel** object has shown or hidden itself.</span></span><br/>                                                         |



 

### <a name="interfaces"></a><span data-ttu-id="61ba8-135">Interfaces</span><span class="sxs-lookup"><span data-stu-id="61ba8-135">Interfaces</span></span>

<span data-ttu-id="61ba8-136">A classe **PenInputPanel** define essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="61ba8-136">The **PenInputPanel** class defines these interfaces.</span></span>



| <span data-ttu-id="61ba8-137">Interface</span><span class="sxs-lookup"><span data-stu-id="61ba8-137">Interface</span></span>          | <span data-ttu-id="61ba8-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ba8-138">Description</span></span>                                                             |
|:-------------------|:------------------------------------------------------------------------|
| <span data-ttu-id="61ba8-139">**IPenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="61ba8-139">**IPenInputPanel**</span></span> | <span data-ttu-id="61ba8-140">Esse objeto implementa a interface com do **IPenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="61ba8-140">This object implements the **IPenInputPanel** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="61ba8-141">Métodos</span><span class="sxs-lookup"><span data-stu-id="61ba8-141">Methods</span></span>

<span data-ttu-id="61ba8-142">A classe **PenInputPanel** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="61ba8-142">The **PenInputPanel** class has these methods.</span></span>



| <span data-ttu-id="61ba8-143">Método</span><span class="sxs-lookup"><span data-stu-id="61ba8-143">Method</span></span>                                                         | <span data-ttu-id="61ba8-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ba8-144">Description</span></span>                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61ba8-145">**CommitPendingInput**</span><span class="sxs-lookup"><span data-stu-id="61ba8-145">**CommitPendingInput**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | <span data-ttu-id="61ba8-146">Envia a tinta coletada para o reconhecedor e posta o resultado do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="61ba8-146">Sends collected ink to the recognizer and posts the recognition result.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="61ba8-147">**EnableTsf**</span><span class="sxs-lookup"><span data-stu-id="61ba8-147">**EnableTsf**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | <span data-ttu-id="61ba8-148">Quando passado como **true**, o **PenInputPanel** tenta enviar texto ao controle anexado por meio da estrutura de serviços de texto (TSF) e habilita o uso da interface do usuário de correção.</span><span class="sxs-lookup"><span data-stu-id="61ba8-148">When passed **TRUE**, the **PenInputPanel** attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.</span></span><br/>    |
| [<span data-ttu-id="61ba8-149">**Mover**</span><span class="sxs-lookup"><span data-stu-id="61ba8-149">**MoveTo**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | <span data-ttu-id="61ba8-150">Define a posição do objeto **PenInputPanel** como uma posição de tela estática.</span><span class="sxs-lookup"><span data-stu-id="61ba8-150">Sets the position of the **PenInputPanel** object to a static screen position.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="61ba8-151">**Atualizar**</span><span class="sxs-lookup"><span data-stu-id="61ba8-151">**Refresh**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | <span data-ttu-id="61ba8-152">Atualiza e restaura as propriedades **PenInputPanel** com base nas configurações do painel de entrada do Tablet PC, posiciona automaticamente o painel de entrada da caneta e define a interface do usuário para o painel padrão.</span><span class="sxs-lookup"><span data-stu-id="61ba8-152">Updates and restores the **PenInputPanel** properties based on Tablet PC Input Panel settings, automatically positions the pen input panel and sets the user interface to the default panel.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="61ba8-153">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61ba8-153">Properties</span></span>

<span data-ttu-id="61ba8-154">A classe **PenInputPanel** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="61ba8-154">The **PenInputPanel** class has these properties.</span></span>



| <span data-ttu-id="61ba8-155">Propriedade</span><span class="sxs-lookup"><span data-stu-id="61ba8-155">Property</span></span>                                                                  | <span data-ttu-id="61ba8-156">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="61ba8-156">Access type</span></span>           | <span data-ttu-id="61ba8-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="61ba8-157">Description</span></span>                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61ba8-158">**AttachedEditWindow**</span><span class="sxs-lookup"><span data-stu-id="61ba8-158">**AttachedEditWindow**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | <span data-ttu-id="61ba8-159">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-159">Read/write</span></span><br/> | <span data-ttu-id="61ba8-160">Obtém ou define o identificador de janela do controle ao qual o objeto **PenInputPanel** está anexado.</span><span class="sxs-lookup"><span data-stu-id="61ba8-160">Gets or sets the window handle of the control that the **PenInputPanel** object is attached to.</span></span><br/>                                                                     |
| [<span data-ttu-id="61ba8-161">**Mostrar automostrações**</span><span class="sxs-lookup"><span data-stu-id="61ba8-161">**AutoShow**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | <span data-ttu-id="61ba8-162">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-162">Read/write</span></span><br/> | <span data-ttu-id="61ba8-163">Obtém ou define um valor booliano que especifica se o objeto **PenInputPanel** aparece quando o foco é definido usando a caneta.</span><span class="sxs-lookup"><span data-stu-id="61ba8-163">Gets or sets a Boolean value that specifies whether the **PenInputPanel** object appears when focus is set using the pen.</span></span><br/>                                           |
| [<span data-ttu-id="61ba8-164">**Carregado**</span><span class="sxs-lookup"><span data-stu-id="61ba8-164">**Busy**</span></span>](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | <span data-ttu-id="61ba8-165">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ba8-165">Read-only</span></span><br/>  | <span data-ttu-id="61ba8-166">Obtém um valor booliano que especifica se o objeto **PenInputPanel** está processando a tinta no momento.</span><span class="sxs-lookup"><span data-stu-id="61ba8-166">Gets a Boolean value that specifies whether the **PenInputPanel** object is currently processing ink.</span></span><br/>                                                               |
| [<span data-ttu-id="61ba8-167">**CurrentPanel**</span><span class="sxs-lookup"><span data-stu-id="61ba8-167">**CurrentPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | <span data-ttu-id="61ba8-168">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-168">Read/write</span></span><br/> | <span data-ttu-id="61ba8-169">Obtém ou define qual tipo de painel está sendo usado no momento para entrada dentro do objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="61ba8-169">Gets or sets which panel type is currently being used for input within the **PenInputPanel** object.</span></span><br/>                                                                |
| [<span data-ttu-id="61ba8-170">**DefaultPanel**</span><span class="sxs-lookup"><span data-stu-id="61ba8-170">**DefaultPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | <span data-ttu-id="61ba8-171">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-171">Read/write</span></span><br/> | <span data-ttu-id="61ba8-172">Obtém ou define qual tipo de painel é o tipo de painel padrão usado para entrada dentro do objeto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="61ba8-172">Gets or sets which panel type is the default panel type used for input within the **PenInputPanel** object.</span></span><br/>                                                         |
| [<span data-ttu-id="61ba8-173">**Facto**</span><span class="sxs-lookup"><span data-stu-id="61ba8-173">**Factoid**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | <span data-ttu-id="61ba8-174">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-174">Read/write</span></span><br/> | <span data-ttu-id="61ba8-175">Obtém ou define o nome da cadeia de caracteres do factor usado no reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="61ba8-175">Gets or sets the string name of the factoid used in recognition.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="61ba8-176">**Altura**</span><span class="sxs-lookup"><span data-stu-id="61ba8-176">**Height**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | <span data-ttu-id="61ba8-177">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ba8-177">Read-only</span></span><br/>  | <span data-ttu-id="61ba8-178">Obtém a altura do objeto **PenInputPanel** nas coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="61ba8-178">Gets the height of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                              |
| [<span data-ttu-id="61ba8-179">**As**</span><span class="sxs-lookup"><span data-stu-id="61ba8-179">**HorizontalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | <span data-ttu-id="61ba8-180">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-180">Read/write</span></span><br/> | <span data-ttu-id="61ba8-181">Obtém ou define o deslocamento entre a borda esquerda do objeto **PenInputPanel** e a borda esquerda do controle ao qual ele está anexado.</span><span class="sxs-lookup"><span data-stu-id="61ba8-181">Gets or sets the offset between the left edge of the **PenInputPanel** object and the left edge of the control to which it is attached.</span></span><br/>                             |
| [<span data-ttu-id="61ba8-182">**Mantida**</span><span class="sxs-lookup"><span data-stu-id="61ba8-182">**Left**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | <span data-ttu-id="61ba8-183">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ba8-183">Read-only</span></span><br/>  | <span data-ttu-id="61ba8-184">Obtém o local horizontal, ou eixo x, da borda esquerda do objeto **PenInputPanel** , em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="61ba8-184">Gets the horizontal, or x-axis, location of the left edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                   |
| [<span data-ttu-id="61ba8-185">**Início**</span><span class="sxs-lookup"><span data-stu-id="61ba8-185">**Top**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | <span data-ttu-id="61ba8-186">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ba8-186">Read-only</span></span><br/>  | <span data-ttu-id="61ba8-187">Obtém o local vertical, ou eixo y, da borda superior do objeto **PenInputPanel** , em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="61ba8-187">Gets the vertical, or y-axis, location of the top edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                      |
| [<span data-ttu-id="61ba8-188">**VerticalOffset**</span><span class="sxs-lookup"><span data-stu-id="61ba8-188">**VerticalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | <span data-ttu-id="61ba8-189">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-189">Read/write</span></span><br/> | <span data-ttu-id="61ba8-190">Obtém ou define o deslocamento entre a borda horizontal mais próxima do objeto **PenInputPanel** e a borda horizontal mais próxima do controle ao qual ele está anexado.</span><span class="sxs-lookup"><span data-stu-id="61ba8-190">Gets or sets the offset between the closest horizontal edge of the **PenInputPanel** object and the closest horizontal edge of the control to which it is attached.</span></span><br/> |
| [<span data-ttu-id="61ba8-191">**Visible**</span><span class="sxs-lookup"><span data-stu-id="61ba8-191">**Visible**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | <span data-ttu-id="61ba8-192">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="61ba8-192">Read/write</span></span><br/> | <span data-ttu-id="61ba8-193">Obtém ou define um valor que indica se o objeto **PenInputPanel** está visível.</span><span class="sxs-lookup"><span data-stu-id="61ba8-193">Gets or sets a value that indicates whether the **PenInputPanel** object is visible.</span></span><br/>                                                                                |
| [<span data-ttu-id="61ba8-194">**Largura**</span><span class="sxs-lookup"><span data-stu-id="61ba8-194">**Width**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | <span data-ttu-id="61ba8-195">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61ba8-195">Read-only</span></span><br/>  | <span data-ttu-id="61ba8-196">Obtém a largura do objeto **PenInputPanel** nas coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="61ba8-196">Gets the width of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="61ba8-197">Comentários</span><span class="sxs-lookup"><span data-stu-id="61ba8-197">Remarks</span></span>

<span data-ttu-id="61ba8-198">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="61ba8-198">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="61ba8-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61ba8-199">Requirements</span></span>



| <span data-ttu-id="61ba8-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="61ba8-200">Requirement</span></span> | <span data-ttu-id="61ba8-201">Valor</span><span class="sxs-lookup"><span data-stu-id="61ba8-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ba8-202">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61ba8-202">Minimum supported client</span></span><br/> | <span data-ttu-id="61ba8-203">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="61ba8-203">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="61ba8-204">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61ba8-204">Minimum supported server</span></span><br/> | <span data-ttu-id="61ba8-205">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61ba8-205">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="61ba8-206">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61ba8-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="61ba8-207"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="61ba8-207"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="61ba8-208">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61ba8-208">Library</span></span><br/>                  | <dl> <span data-ttu-id="61ba8-209"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61ba8-209"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="61ba8-210">Confira também</span><span class="sxs-lookup"><span data-stu-id="61ba8-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ba8-211">Programando o painel de entrada usando a classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="61ba8-211">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
