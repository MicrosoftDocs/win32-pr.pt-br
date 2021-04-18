---
title: Entrada do mouse (introdução ao Win32 e ao C++)
description: Entrada do mouse
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105810161"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a><span data-ttu-id="8bc12-103">Entrada do mouse (introdução ao Win32 e ao C++)</span><span class="sxs-lookup"><span data-stu-id="8bc12-103">Mouse Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="8bc12-104">O Windows dá suporte a mouses com até cinco botões: esquerdo, meio e direito, além de dois botões adicionais chamados XBUTTON1 e XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="8bc12-104">Windows supports mice with up to five buttons: left, middle, and right, plus two additional buttons called XBUTTON1 and XBUTTON2.</span></span>

![uma ilustração que mostra os botões esquerdo (1), direito (2), médio (3) e XButton1 (4).](images/mouse.png)

<span data-ttu-id="8bc12-106">A maioria dos mouses para Windows tem pelo menos os botões esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="8bc12-106">Most mice for Windows have at least the left and right buttons.</span></span> <span data-ttu-id="8bc12-107">O botão esquerdo do mouse é usado para apontar, selecionar, arrastar e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8bc12-107">The left mouse button is used for pointing, selecting, dragging, and so forth.</span></span> <span data-ttu-id="8bc12-108">O botão direito do mouse normalmente exibe um menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="8bc12-108">The right mouse button typically displays a context menu.</span></span> <span data-ttu-id="8bc12-109">Alguns mouses têm uma roda de rolagem localizada entre os botões esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="8bc12-109">Some mice have a scroll wheel located between the left and right buttons.</span></span> <span data-ttu-id="8bc12-110">Dependendo do mouse, a roda de rolagem também pode ser clicável, tornando-o o botão do meio.</span><span class="sxs-lookup"><span data-stu-id="8bc12-110">Depending on the mouse, the scroll wheel might also be clickable, making it the middle button.</span></span>

<span data-ttu-id="8bc12-111">Os botões XBUTTON1 e XBUTTON2 geralmente estão localizados nos lados do mouse, perto da base.</span><span class="sxs-lookup"><span data-stu-id="8bc12-111">The XBUTTON1 and XBUTTON2 buttons are often located on the sides of the mouse, near the base.</span></span> <span data-ttu-id="8bc12-112">Esses botões extras não estão presentes em todos os mouses.</span><span class="sxs-lookup"><span data-stu-id="8bc12-112">These extra buttons are not present on all mice.</span></span> <span data-ttu-id="8bc12-113">Se houver, os botões XBUTTON1 e XBUTTON2 geralmente são mapeados para uma função de aplicativo, como navegação para frente e para trás em um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="8bc12-113">If present, the XBUTTON1 and XBUTTON2 buttons are often mapped to an application function, such as forward and backward navigation in a Web browser.</span></span>

<span data-ttu-id="8bc12-114">Os usuários da mão esquerda geralmente acham mais confortável trocar as funções dos botões esquerdo e direito — usando o botão direito como ponteiro e o botão esquerdo para mostrar o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="8bc12-114">Left-handed users often find it more comfortable to swap the functions of the left and right buttons—using the right button as the pointer, and the left button to show the context menu.</span></span> <span data-ttu-id="8bc12-115">Por esse motivo, a documentação de ajuda do Windows usa o botão de termos *primário* e o *botão secundário*, que se referem à função lógica em vez do posicionamento físico.</span><span class="sxs-lookup"><span data-stu-id="8bc12-115">For this reason, the Windows help documentation uses the terms *primary button* and *secondary button*, which refer to logical function rather than physical placement.</span></span> <span data-ttu-id="8bc12-116">Na configuração padrão (canhoto), o botão esquerdo é o botão principal e a direita é o botão secundário.</span><span class="sxs-lookup"><span data-stu-id="8bc12-116">In the default (right-handed) setting, the left button is the primary button and the right is the secondary button.</span></span> <span data-ttu-id="8bc12-117">No entanto, os termos clique com o *botão direito do mouse* e *esquerdo clique em* consulte ações lógicas.</span><span class="sxs-lookup"><span data-stu-id="8bc12-117">However, the terms *right click* and *left click* refer to logical actions.</span></span> <span data-ttu-id="8bc12-118">*Clicando com o botão direito do mouse* significa clicar no botão primário, se esse botão está fisicamente no lado direito ou esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="8bc12-118">*Right clicking* means clicking the primary button, whether that button is physically on the right or left side of the mouse.</span></span>

<span data-ttu-id="8bc12-119">Independentemente de como o usuário configura o mouse, o Windows converte automaticamente as mensagens do mouse para que elas sejam consistentes.</span><span class="sxs-lookup"><span data-stu-id="8bc12-119">Regardless of how the user configures the mouse, Windows automatically translates mouse messages so they are consistent.</span></span> <span data-ttu-id="8bc12-120">O usuário pode trocar os botões primário e secundário no meio do uso do programa e não afetará a forma como o seu programa se comporta.</span><span class="sxs-lookup"><span data-stu-id="8bc12-120">The user can swap the primary and secondary buttons in the middle of using your program, and it will not affect how your program behaves.</span></span>

<span data-ttu-id="8bc12-121">A documentação do MSDN usa o botão *direito do mouse* e o *botão esquerdo* para significar o botão *primário* e o *secundário* .</span><span class="sxs-lookup"><span data-stu-id="8bc12-121">MSDN documentation uses the terms *right button* and *left button* to mean *primary* and *secondary* button.</span></span> <span data-ttu-id="8bc12-122">Essa terminologia é consistente com os nomes das mensagens de janela para entrada do mouse.</span><span class="sxs-lookup"><span data-stu-id="8bc12-122">This terminology is consistent with the names of the window messages for mouse input.</span></span> <span data-ttu-id="8bc12-123">Apenas lembre-se de que os botões físico esquerdo e direito podem ser trocados.</span><span class="sxs-lookup"><span data-stu-id="8bc12-123">Just remember that the physical left and right buttons might be swapped.</span></span>

## <a name="next"></a><span data-ttu-id="8bc12-124">Avançar</span><span class="sxs-lookup"><span data-stu-id="8bc12-124">Next</span></span>

[<span data-ttu-id="8bc12-125">Respondendo a cliques do mouse</span><span class="sxs-lookup"><span data-stu-id="8bc12-125">Responding to Mouse Clicks</span></span>](mouse-clicks.md)

 

 




