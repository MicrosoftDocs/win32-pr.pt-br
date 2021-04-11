---
title: Propriedade KeyboardShortcut
description: A Propriedade KeyboardShortcut descreve uma combinação de chave ou chave que ativa um objeto acessível especificado.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159840"
---
# <a name="keyboardshortcut-property"></a><span data-ttu-id="2d88c-103">Propriedade KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="2d88c-103">KeyboardShortcut Property</span></span>

<span data-ttu-id="2d88c-104">A propriedade **KeyboardShortcut** descreve uma combinação de chave ou chave que ativa um objeto acessível especificado.</span><span class="sxs-lookup"><span data-stu-id="2d88c-104">The **KeyboardShortcut** property describes a key or key combination that activates a specified accessible object.</span></span>

<span data-ttu-id="2d88c-105">A propriedade **KeyboardShortcut** é recuperada chamando [**IAccessible:: get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span><span class="sxs-lookup"><span data-stu-id="2d88c-105">The **KeyboardShortcut** property is retrieved by calling [**IAccessible::get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span></span>

<span data-ttu-id="2d88c-106">A cadeia de caracteres recuperada descreve uma *tecla de atalho* (também chamada de *acelerador de teclado*) ou uma chave de *acesso* (também chamada de *mnemônico*).</span><span class="sxs-lookup"><span data-stu-id="2d88c-106">The retrieved string describes a *shortcut key* (also called a *keyboard accelerator*) or an *access key* (also called a *mnemonic*).</span></span> <span data-ttu-id="2d88c-107">Uma tecla de acesso é um caractere sublinhado no texto de um menu, item de menu ou rótulo de um controle, como um botão de ação.</span><span class="sxs-lookup"><span data-stu-id="2d88c-107">An access key is an underlined character in the text of a menu, menu item, or label of a control such as a push button.</span></span>

<span data-ttu-id="2d88c-108">A cadeia de caracteres recuperada deve conter o nome da chave junto com as chaves ou teclas de modificador.</span><span class="sxs-lookup"><span data-stu-id="2d88c-108">The retrieved string must contain the name of the key along with the modifier key or keys.</span></span> <span data-ttu-id="2d88c-109">A cadeia de caracteres deve estar no seguinte formato para que os clientes possam analisá-lo facilmente: \[ \[ chave de modificador \] + \[ ... \] + \] nome da chave.</span><span class="sxs-lookup"><span data-stu-id="2d88c-109">The string must be in the following format so that clients can easily parse it: \[\[modifier key\]+\[...\]+\] key name.</span></span>

<span data-ttu-id="2d88c-110">Os exemplos incluem ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + SHIFT + BACKSPACE ou simplesmente Backspace.</span><span class="sxs-lookup"><span data-stu-id="2d88c-110">Examples include ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+SHIFT+BACKSPACE, or simply BACKSPACE.</span></span>

<span data-ttu-id="2d88c-111">A tabela a seguir lista as teclas modificadoras.</span><span class="sxs-lookup"><span data-stu-id="2d88c-111">The following table lists modifier keys.</span></span>



| <span data-ttu-id="2d88c-112">Tecla modificadora</span><span class="sxs-lookup"><span data-stu-id="2d88c-112">Modifier key</span></span> | <span data-ttu-id="2d88c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d88c-113">Description</span></span>                        |
|--------------|------------------------------------|
| <span data-ttu-id="2d88c-114">ALT</span><span class="sxs-lookup"><span data-stu-id="2d88c-114">ALT</span></span>          | <span data-ttu-id="2d88c-115">Tecla modificador alternativo</span><span class="sxs-lookup"><span data-stu-id="2d88c-115">Alternate modifier key</span></span>             |
| <span data-ttu-id="2d88c-116">CTRL</span><span class="sxs-lookup"><span data-stu-id="2d88c-116">CTRL</span></span>         | <span data-ttu-id="2d88c-117">Tecla de modificador de controle</span><span class="sxs-lookup"><span data-stu-id="2d88c-117">Control modifier key</span></span>               |
| <span data-ttu-id="2d88c-118">ALTERNÂNCIA</span><span class="sxs-lookup"><span data-stu-id="2d88c-118">SHIFT</span></span>        | <span data-ttu-id="2d88c-119">Tecla modificador de deslocamento</span><span class="sxs-lookup"><span data-stu-id="2d88c-119">Shift modifier key</span></span>                 |
| <span data-ttu-id="2d88c-120">VENCEU</span><span class="sxs-lookup"><span data-stu-id="2d88c-120">WIN</span></span>          | <span data-ttu-id="2d88c-121">Tecla de logotipo do Windows</span><span class="sxs-lookup"><span data-stu-id="2d88c-121">Windows logo key</span></span>                   |
| <span data-ttu-id="2d88c-122">FN</span><span class="sxs-lookup"><span data-stu-id="2d88c-122">FN</span></span>           | <span data-ttu-id="2d88c-123">Chave de função em computadores portáteis</span><span class="sxs-lookup"><span data-stu-id="2d88c-123">Function key on portable computers</span></span> |



 

<span data-ttu-id="2d88c-124">Não Localize cadeias de caracteres de atalho de teclado.</span><span class="sxs-lookup"><span data-stu-id="2d88c-124">Do not localize keyboard shortcut strings.</span></span>

## <a name="handling-objects-that-have-both-key-types"></a><span data-ttu-id="2d88c-125">Manipulando objetos que têm os dois tipos de chave</span><span class="sxs-lookup"><span data-stu-id="2d88c-125">Handling Objects That Have Both Key Types</span></span>

<span data-ttu-id="2d88c-126">Se um objeto tiver uma tecla de atalho e uma tecla de acesso, a propriedade **KeyboardShortcut** retornará a tecla de acesso.</span><span class="sxs-lookup"><span data-stu-id="2d88c-126">If an object has both a shortcut key and an access key, the **KeyboardShortcut** property returns the access key.</span></span> <span data-ttu-id="2d88c-127">A chave de acesso é aquela que um usuário deve pressionar quando o objeto ou o pai do objeto tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="2d88c-127">The access key is the one a user would press when the object or the object's parent has the keyboard focus.</span></span> <span data-ttu-id="2d88c-128">Por exemplo, o item de menu **Imprimir** pode ter uma tecla de atalho (Ctrl + P) e uma tecla de acesso (P).</span><span class="sxs-lookup"><span data-stu-id="2d88c-128">For example, the **Print** menu item might have both a shortcut key (CTRL+P) and an access key (P).</span></span> <span data-ttu-id="2d88c-129">Se um usuário pressionar CTRL + P enquanto o menu estiver ativo, nada acontecerá.</span><span class="sxs-lookup"><span data-stu-id="2d88c-129">If a user presses CTRL+P while the menu is active, nothing happens.</span></span> <span data-ttu-id="2d88c-130">Mas se um usuário pressionar P enquanto o menu estiver ativo, ele invocará a caixa de diálogo **Imprimir** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d88c-130">But if a user presses P while the menu is active, it invokes the application's **Print** dialog box.</span></span> <span data-ttu-id="2d88c-131">Nesse caso, a propriedade **KeyboardShortcut** é "P" para refletir o que o usuário deve pressionar quando o menu tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="2d88c-131">In this case, the **KeyboardShortcut** property is "P" to reflect what the user must press when the menu has the keyboard focus.</span></span>

 

 




