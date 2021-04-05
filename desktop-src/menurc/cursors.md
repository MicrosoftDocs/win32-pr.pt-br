---
title: Cursores
description: Esta seção aborda os cursores que são pequenas imagens cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- recursos, cursores
- cursores, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9014befcc41161d7491af97186b33088f508dd8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005599"
---
# <a name="cursors"></a><span data-ttu-id="c2e59-105">Cursores</span><span class="sxs-lookup"><span data-stu-id="c2e59-105">Cursors</span></span>

<span data-ttu-id="c2e59-106">Um cursor é uma pequena imagem cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball.</span><span class="sxs-lookup"><span data-stu-id="c2e59-106">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="c2e59-107">No restante desta visão geral, o termo mouse se refere a qualquer dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="c2e59-107">In the remainder of this overview, the term mouse refers to any pointing device.</span></span>

<span data-ttu-id="c2e59-108">Quando o usuário move o mouse, o sistema move o cursor de acordo.</span><span class="sxs-lookup"><span data-stu-id="c2e59-108">When the user moves the mouse, the system moves the cursor accordingly.</span></span> <span data-ttu-id="c2e59-109">As funções de cursor permitem que os aplicativos criem, carreguem, exibam, animem, movam, confinam e destruam cursores.</span><span class="sxs-lookup"><span data-stu-id="c2e59-109">The cursor functions enable applications to create, load, display, animate, move, confine, and destroy cursors.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="c2e59-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c2e59-110">In This Section</span></span>



| <span data-ttu-id="c2e59-111">Nome</span><span class="sxs-lookup"><span data-stu-id="c2e59-111">Name</span></span>                                     | <span data-ttu-id="c2e59-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2e59-112">Description</span></span>                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="c2e59-113">Sobre cursores</span><span class="sxs-lookup"><span data-stu-id="c2e59-113">About Cursors</span></span>](about-cursors.md)       | <span data-ttu-id="c2e59-114">Discute os cursores padrão.</span><span class="sxs-lookup"><span data-stu-id="c2e59-114">Discusses the standard cursors.</span></span><br/>                    |
| [<span data-ttu-id="c2e59-115">Usando cursores</span><span class="sxs-lookup"><span data-stu-id="c2e59-115">Using Cursors</span></span>](using-cursors.md)       | <span data-ttu-id="c2e59-116">Discute como executar tarefas relacionadas a cursores.</span><span class="sxs-lookup"><span data-stu-id="c2e59-116">Discusses how to perform tasks related to cursors.</span></span><br/> |
| [<span data-ttu-id="c2e59-117">Referência do cursor</span><span class="sxs-lookup"><span data-stu-id="c2e59-117">Cursor Reference</span></span>](cursor-reference.md) | <span data-ttu-id="c2e59-118">Contém a referência de API.</span><span class="sxs-lookup"><span data-stu-id="c2e59-118">Contains the API reference.</span></span><br/>                        |



 

### <a name="cursor-functions"></a><span data-ttu-id="c2e59-119">Funções do cursor</span><span class="sxs-lookup"><span data-stu-id="c2e59-119">Cursor Functions</span></span>



| <span data-ttu-id="c2e59-120">Nome</span><span class="sxs-lookup"><span data-stu-id="c2e59-120">Name</span></span>                                                 | <span data-ttu-id="c2e59-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2e59-121">Description</span></span>                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2e59-122">**ClipCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-122">**ClipCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | <span data-ttu-id="c2e59-123">Ajusta o cursor para uma área retangular na tela.</span><span class="sxs-lookup"><span data-stu-id="c2e59-123">Confines the cursor to a rectangular area on the screen.</span></span> <span data-ttu-id="c2e59-124">Se uma posição de cursor subsequente (definida pela função [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) ou pelo mouse) estiver fora do retângulo, o sistema ajustará automaticamente a posição para manter o cursor dentro da área retangular.</span><span class="sxs-lookup"><span data-stu-id="c2e59-124">If a subsequent cursor position (set by the [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) function or the mouse) lies outside the rectangle, the system automatically adjusts the position to keep the cursor inside the rectangular area.</span></span> <br/> |
| [<span data-ttu-id="c2e59-125">**CopyCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-125">**CopyCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | <span data-ttu-id="c2e59-126">Copia o cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="c2e59-126">Copies the specified cursor.</span></span> <br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c2e59-127">**CreateCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-127">**CreateCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | <span data-ttu-id="c2e59-128">Cria um cursor com o tamanho especificado, os padrões de bits e o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="c2e59-128">Creates a cursor having the specified size, bit patterns, and hot spot.</span></span> <br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="c2e59-129">**DestroyCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-129">**DestroyCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | <span data-ttu-id="c2e59-130">Destrói um cursor e libera qualquer memória do cursor ocupada.</span><span class="sxs-lookup"><span data-stu-id="c2e59-130">Destroys a cursor and frees any memory the cursor occupied.</span></span> <span data-ttu-id="c2e59-131">Não use essa função para destruir um cursor compartilhado.</span><span class="sxs-lookup"><span data-stu-id="c2e59-131">Do not use this function to destroy a shared cursor.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="c2e59-132">**GetClipCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-132">**GetClipCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | <span data-ttu-id="c2e59-133">Recupera as coordenadas de tela da área retangular à qual o cursor está confinado.</span><span class="sxs-lookup"><span data-stu-id="c2e59-133">Retrieves the screen coordinates of the rectangular area to which the cursor is confined.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="c2e59-134">**GetCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-134">**GetCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | <span data-ttu-id="c2e59-135">Recupera um identificador para o cursor atual.</span><span class="sxs-lookup"><span data-stu-id="c2e59-135">Retrieves a handle to the current cursor.</span></span> <br/>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="c2e59-136">**GetCursorInfo**</span><span class="sxs-lookup"><span data-stu-id="c2e59-136">**GetCursorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | <span data-ttu-id="c2e59-137">Recupera informações sobre o cursor global.</span><span class="sxs-lookup"><span data-stu-id="c2e59-137">Retrieves information about the global cursor.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="c2e59-138">**GetCursorPos**</span><span class="sxs-lookup"><span data-stu-id="c2e59-138">**GetCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | <span data-ttu-id="c2e59-139">Recupera a posição do cursor, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="c2e59-139">Retrieves the cursor's position, in screen coordinates.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c2e59-140">**GetPhysicalCursorPos**</span><span class="sxs-lookup"><span data-stu-id="c2e59-140">**GetPhysicalCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | <span data-ttu-id="c2e59-141">Recupera a posição do cursor em coordenadas físicas.</span><span class="sxs-lookup"><span data-stu-id="c2e59-141">Retrieves the position of the cursor in physical coordinates.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="c2e59-142">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-142">**LoadCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | <span data-ttu-id="c2e59-143">Carrega o recurso de cursor especificado do executável (. EXE) associado a uma instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2e59-143">Loads the specified cursor resource from the executable (.EXE) file associated with an application instance.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="c2e59-144">**LoadCursorFromFile**</span><span class="sxs-lookup"><span data-stu-id="c2e59-144">**LoadCursorFromFile**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | <span data-ttu-id="c2e59-145">Cria um cursor com base nos dados contidos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2e59-145">Creates a cursor based on data contained in a file.</span></span> <br/>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="c2e59-146">**SetCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-146">**SetCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | <span data-ttu-id="c2e59-147">Define a forma do cursor.</span><span class="sxs-lookup"><span data-stu-id="c2e59-147">Sets the cursor shape.</span></span> <br/>                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c2e59-148">**SetCursorPos**</span><span class="sxs-lookup"><span data-stu-id="c2e59-148">**SetCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | <span data-ttu-id="c2e59-149">Move o cursor para as coordenadas de tela especificadas.</span><span class="sxs-lookup"><span data-stu-id="c2e59-149">Moves the cursor to the specified screen coordinates.</span></span> <span data-ttu-id="c2e59-150">Se as novas coordenadas não estiverem dentro do retângulo da tela definido pela chamada de função [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) mais recente, o sistema ajustará automaticamente as coordenadas para que o cursor permaneça dentro do retângulo.</span><span class="sxs-lookup"><span data-stu-id="c2e59-150">If the new coordinates are not within the screen rectangle set by the most recent [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) function call, the system automatically adjusts the coordinates so that the cursor stays within the rectangle.</span></span> <br/>    |
| [<span data-ttu-id="c2e59-151">**SetPhysicalCursorPos**</span><span class="sxs-lookup"><span data-stu-id="c2e59-151">**SetPhysicalCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | <span data-ttu-id="c2e59-152">Define a posição do cursor em coordenadas físicas.</span><span class="sxs-lookup"><span data-stu-id="c2e59-152">Sets the position of the cursor in physical coordinates.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c2e59-153">**SetSystemCursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-153">**SetSystemCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | <span data-ttu-id="c2e59-154">Permite que um aplicativo Personalize os cursores do sistema.</span><span class="sxs-lookup"><span data-stu-id="c2e59-154">Enables an application to customize the system cursors.</span></span> <span data-ttu-id="c2e59-155">Ele substitui o conteúdo do cursor do sistema especificado pelo parâmetro *ID* pelo conteúdo do cursor especificado pelo parâmetro *hcur* e, em seguida, destrói *hcur*.</span><span class="sxs-lookup"><span data-stu-id="c2e59-155">It replaces the contents of the system cursor specified by the *id* parameter with the contents of the cursor specified by the *hcur* parameter and then destroys *hcur*.</span></span> <br/>                                                          |
| [<span data-ttu-id="c2e59-156">**Obter cursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-156">**ShowCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | <span data-ttu-id="c2e59-157">Exibe ou oculta o cursor.</span><span class="sxs-lookup"><span data-stu-id="c2e59-157">Displays or hides the cursor.</span></span> <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a><span data-ttu-id="c2e59-158">Notificações do cursor</span><span class="sxs-lookup"><span data-stu-id="c2e59-158">Cursor Notifications</span></span>



| <span data-ttu-id="c2e59-159">Nome</span><span class="sxs-lookup"><span data-stu-id="c2e59-159">Name</span></span>                                  | <span data-ttu-id="c2e59-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2e59-160">Description</span></span>                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2e59-161">**WM \_ SETcursor**</span><span class="sxs-lookup"><span data-stu-id="c2e59-161">**WM\_SETCURSOR**</span></span>](wm-setcursor.md) | <span data-ttu-id="c2e59-162">Enviado a uma janela se o mouse fizer com que o cursor se mova dentro de uma janela e a entrada do mouse não for capturada.</span><span class="sxs-lookup"><span data-stu-id="c2e59-162">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span> <br/> |



 

### <a name="cursor-structures"></a><span data-ttu-id="c2e59-163">Estruturas de cursor</span><span class="sxs-lookup"><span data-stu-id="c2e59-163">Cursor Structures</span></span>



| <span data-ttu-id="c2e59-164">Nome</span><span class="sxs-lookup"><span data-stu-id="c2e59-164">Name</span></span>                             | <span data-ttu-id="c2e59-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2e59-165">Description</span></span>                                    |
|----------------------------------|------------------------------------------------|
| [<span data-ttu-id="c2e59-166">**CURSORINFO**</span><span class="sxs-lookup"><span data-stu-id="c2e59-166">**CURSORINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-cursorinfo) | <span data-ttu-id="c2e59-167">Contém informações de cursor global.</span><span class="sxs-lookup"><span data-stu-id="c2e59-167">Contains global cursor information.</span></span><br/> |



 

 

 





