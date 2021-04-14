---
title: Interpolação
description: Esta seção discute os Cursors que são linhas de intermitência, blocos ou bitmaps na área do cliente de uma janela.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- recursos, Cursors
- Cursors, sobre
- linhas piscando
- blocos piscando
- bitmaps piscando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104370804"
---
# <a name="carets"></a><span data-ttu-id="0dbf2-108">Interpolação</span><span class="sxs-lookup"><span data-stu-id="0dbf2-108">Carets</span></span>

<span data-ttu-id="0dbf2-109">Um *cursor* é uma linha, bloco ou bitmap piscando na área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-109">A *caret* is a blinking line, block, or bitmap in the client area of a window.</span></span> <span data-ttu-id="0dbf2-110">O cursor normalmente indica o local no qual o texto ou os gráficos serão inseridos.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-110">The caret typically indicates the place at which text or graphics will be inserted.</span></span>

<span data-ttu-id="0dbf2-111">A ilustração a seguir mostra algumas variações comuns na aparência do cursor.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-111">The following illustration shows some common variations in the appearance of the caret.</span></span>

![Mostra 5 maneiras diferentes que um cursor pode exibir.](images/cscrt-01.png)

<span data-ttu-id="0dbf2-113">Os aplicativos podem criar um cursor, alterar o tempo de intermitência e exibir, ocultar ou realocar o cursor.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-113">Applications can create a caret, change its blink time, and display, hide, or relocate the caret.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="0dbf2-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0dbf2-114">In This Section</span></span>



| <span data-ttu-id="0dbf2-115">Nome</span><span class="sxs-lookup"><span data-stu-id="0dbf2-115">Name</span></span>                                   | <span data-ttu-id="0dbf2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dbf2-116">Description</span></span>                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="0dbf2-117">Sobre os Cursors</span><span class="sxs-lookup"><span data-stu-id="0dbf2-117">About Carets</span></span>](about-carets.md)       | <span data-ttu-id="0dbf2-118">Discute os acentos.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-118">Discusses carets.</span></span><br/>                                              |
| [<span data-ttu-id="0dbf2-119">Usando os Cursors</span><span class="sxs-lookup"><span data-stu-id="0dbf2-119">Using Carets</span></span>](using-carets.md)       | <span data-ttu-id="0dbf2-120">Exemplos de código que mostram como executar tarefas relacionadas a Cursors.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-120">Code samples that show how to perform tasks related to carets.</span></span><br/> |
| [<span data-ttu-id="0dbf2-121">Referência de cursor</span><span class="sxs-lookup"><span data-stu-id="0dbf2-121">Caret Reference</span></span>](caret-reference.md) | <span data-ttu-id="0dbf2-122">Contém a referência de API.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-122">Contains the API reference.</span></span><br/>                                    |



 

### <a name="caret-functions"></a><span data-ttu-id="0dbf2-123">Funções de cursor</span><span class="sxs-lookup"><span data-stu-id="0dbf2-123">Caret Functions</span></span>



| <span data-ttu-id="0dbf2-124">Nome</span><span class="sxs-lookup"><span data-stu-id="0dbf2-124">Name</span></span>                                           | <span data-ttu-id="0dbf2-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dbf2-125">Description</span></span>                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0dbf2-126">**Não importa**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-126">**CreateCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | <span data-ttu-id="0dbf2-127">Cria uma nova forma para o cursor do sistema e atribui a propriedade do cursor à janela especificada.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-127">Creates a new shape for the system caret and assigns ownership of the caret to the specified window.</span></span> <span data-ttu-id="0dbf2-128">A forma do cursor pode ser uma linha, um bloco ou um bitmap.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-128">The caret shape can be a line, a block, or a bitmap.</span></span> <br/>                                                                                         |
| [<span data-ttu-id="0dbf2-129">**DestroyCaret**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-129">**DestroyCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | <span data-ttu-id="0dbf2-130">Destrói a forma atual do cursor, libera o cursor da janela e remove o cursor da tela.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-130">Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.</span></span> <br/>                                                                                                                                       |
| [<span data-ttu-id="0dbf2-131">**GetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-131">**GetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | <span data-ttu-id="0dbf2-132">Recupera o tempo necessário para inverter os pixels do cursor.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-132">Retrieves the time required to invert the caret's pixels.</span></span> <span data-ttu-id="0dbf2-133">O usuário pode definir esse valor.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-133">The user can set this value.</span></span> <br/>                                                                                                                                                            |
| [<span data-ttu-id="0dbf2-134">**GetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-134">**GetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | <span data-ttu-id="0dbf2-135">Copia a posição do cursor para a estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) especificada.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-135">Copies the caret's position to the specified [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <br/>                                                                                                                                                                    |
| [<span data-ttu-id="0dbf2-136">**HideCaret**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-136">**HideCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | <span data-ttu-id="0dbf2-137">Remove o cursor da tela.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-137">Removes the caret from the screen.</span></span> <span data-ttu-id="0dbf2-138">Ocultar um cursor não destrói sua forma atual ou invalidar o ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-138">Hiding a caret does not destroy its current shape or invalidate the insertion point.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="0dbf2-139">**SetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-139">**SetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | <span data-ttu-id="0dbf2-140">Define o tempo de intermitência do cursor para o número especificado de milissegundos.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-140">Sets the caret blink time to the specified number of milliseconds.</span></span> <span data-ttu-id="0dbf2-141">O tempo de intermitência é o tempo decorrido, em milissegundos, necessário para inverter os pixels do cursor.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-141">The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="0dbf2-142">**SetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-142">**SetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | <span data-ttu-id="0dbf2-143">Move o cursor para as coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-143">Moves the caret to the specified coordinates.</span></span> <span data-ttu-id="0dbf2-144">Se a janela que possui o cursor tiver sido criada com o estilo de classe **cs \_ OWNDC** , as coordenadas especificadas estarão sujeitas ao modo de mapeamento do contexto do dispositivo associado a essa janela.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-144">If the window that owns the caret was created with the **CS\_OWNDC** class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.</span></span> <br/> |
| [<span data-ttu-id="0dbf2-145">**Não importa**</span><span class="sxs-lookup"><span data-stu-id="0dbf2-145">**ShowCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | <span data-ttu-id="0dbf2-146">Torna o cursor visível na tela na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-146">Makes the caret visible on the screen at the caret's current position.</span></span> <span data-ttu-id="0dbf2-147">Quando o cursor se torna visível, ele começa a piscar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0dbf2-147">When the caret becomes visible, it begins flashing automatically.</span></span> <br/>                                                                                                          |



 

 

