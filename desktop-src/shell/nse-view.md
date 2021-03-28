---
description: A maioria das extensões de namespace são um subconjunto do namespace do Shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Exibindo uma exibição Self-Contained de uma extensão de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968014"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a><span data-ttu-id="3eca4-103">Exibindo uma exibição Self-Contained de uma extensão de namespace</span><span class="sxs-lookup"><span data-stu-id="3eca4-103">Displaying a Self-Contained View of a Namespace Extension</span></span>

<span data-ttu-id="3eca4-104">A maioria das extensões de namespace são um subconjunto do namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="3eca4-104">Most namespace extensions are a subset of the Shell namespace.</span></span> <span data-ttu-id="3eca4-105">Quando você cria um ponto de junção, conforme descrito em [especificando o local de uma extensão de namespace](nse-junction.md), o Windows Explorer permite que os usuários naveguem para dentro e para fora da extensão do namespace, assim como qualquer outra pasta.</span><span class="sxs-lookup"><span data-stu-id="3eca4-105">When you create a junction point, as described in [Specifying a Namespace Extension's Location](nse-junction.md), Windows Explorer allows users to navigate into and out of your namespace extension just like any other folder.</span></span> <span data-ttu-id="3eca4-106">No entanto, também é possível usar o Windows Explorer para exibir apenas o conteúdo da extensão do namespace.</span><span class="sxs-lookup"><span data-stu-id="3eca4-106">However, it is also possible to use Windows Explorer to display only the contents of your namespace extension.</span></span> <span data-ttu-id="3eca4-107">Essa opção de exibição às vezes é chamada de *exibição com raiz*.</span><span class="sxs-lookup"><span data-stu-id="3eca4-107">This display option is sometimes referred to as a *rooted view*.</span></span> <span data-ttu-id="3eca4-108">Embora não seja comumente usado, as exibições com raiz podem ser preferíveis às exibições normais para alguns tipos de extensões.</span><span class="sxs-lookup"><span data-stu-id="3eca4-108">Although not commonly used, rooted views might be preferable to normal views for some types of extensions.</span></span>

<span data-ttu-id="3eca4-109">Com uma exibição com raiz, é criada uma nova instância do Windows Explorer que exibe o conteúdo da extensão como um namespace separado.</span><span class="sxs-lookup"><span data-stu-id="3eca4-109">With a rooted view, a new instance of Windows Explorer is created that displays the contents of the extension as a separate namespace.</span></span> <span data-ttu-id="3eca4-110">O modo de exibição de árvore de uma exibição com raiz mostra apenas as pastas que fazem parte da extensão.</span><span class="sxs-lookup"><span data-stu-id="3eca4-110">The tree view of a rooted view shows only those folders that are part of the extension.</span></span> <span data-ttu-id="3eca4-111">Os usuários não podem navegar de uma exibição com raiz para outras partes do namespace do Shell.</span><span class="sxs-lookup"><span data-stu-id="3eca4-111">Users cannot navigate from a rooted view to other parts of the Shell namespace.</span></span>

<span data-ttu-id="3eca4-112">As extensões são implementadas da mesma maneira para exibições com raiz, como são para exibições normais.</span><span class="sxs-lookup"><span data-stu-id="3eca4-112">Extensions are implemented in the same way for rooted views as they are for normal views.</span></span> <span data-ttu-id="3eca4-113">A única diferença está na maneira como o conteúdo da extensão é exibido pelo Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="3eca4-113">The only difference is in the way the contents of the extension are displayed by Windows Explorer.</span></span> <span data-ttu-id="3eca4-114">É possível até mesmo ter exibições normais e com raiz da mesma extensão.</span><span class="sxs-lookup"><span data-stu-id="3eca4-114">It is even possible to have normal and rooted views of the same extension.</span></span>

<span data-ttu-id="3eca4-115">Para abrir uma exibição de uma extensão, você deve iniciar uma instância do Explorer.exe com um sinalizador/root.</span><span class="sxs-lookup"><span data-stu-id="3eca4-115">To open a view of an extension, you must launch an instance of Explorer.exe with a /root flag.</span></span> <span data-ttu-id="3eca4-116">Há várias maneiras diferentes de iniciar uma exibição com raiz, dependendo da natureza de sua extensão.</span><span class="sxs-lookup"><span data-stu-id="3eca4-116">There are several different ways to launch a rooted view, depending on the nature of your extension.</span></span>

-   [<span data-ttu-id="3eca4-117">Como usar um ponto de junção para abrir uma exibição com raiz</span><span class="sxs-lookup"><span data-stu-id="3eca4-117">How To Use a Junction Point to Open a Rooted View</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [<span data-ttu-id="3eca4-118">Como usar um arquivo de atalho para abrir uma exibição com raiz</span><span class="sxs-lookup"><span data-stu-id="3eca4-118">How To Use a Shortcut File to Open a Rooted View</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [<span data-ttu-id="3eca4-119">Como exibir uma exibição com raiz de um arquivo</span><span class="sxs-lookup"><span data-stu-id="3eca4-119">How To Display a Rooted View of a File</span></span>](how-to-display-a-rooted-view-of-a-file.md)

 

 



