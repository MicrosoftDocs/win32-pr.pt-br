---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: L (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a568ed662019cbc0f3c0a242faf884df72acb015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164495"
---
# <a name="l-volume-shadow-copy-service"></a><span data-ttu-id="c8ca7-103">L (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="c8ca7-103">L (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="c8ca7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="c8ca7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c8ca7-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**caminho lógico**</span><span class="sxs-lookup"><span data-stu-id="c8ca7-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**logical path**</span></span>
</dt> <dd>

<span data-ttu-id="c8ca7-106">Um mecanismo para descrever os componentes de um gravador.</span><span class="sxs-lookup"><span data-stu-id="c8ca7-106">A mechanism for describing a writer's components.</span></span> <span data-ttu-id="c8ca7-107">Ele é usado para expressar relações entre componentes, especialmente em sua hierarquia.</span><span class="sxs-lookup"><span data-stu-id="c8ca7-107">It is used to express relationships between components, in particularly their hierarchy.</span></span> <span data-ttu-id="c8ca7-108">Por exemplo, se um gravador gerenciasse vários livros eletrônicos, ele poderá atribuir caminhos lógicos de " \\ ebook \\ book1" e " \\ ebook \\ book2" aos componentes do grupo de arquivos que contêm cada livro.</span><span class="sxs-lookup"><span data-stu-id="c8ca7-108">For instance, if a writer managed several electronic books, it might assign logical paths of "\\ebook\\book1" and "\\ebook\\book2" to file group components containing each book.</span></span> <span data-ttu-id="c8ca7-109">Caminhos lógicos são necessários ao especificar subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c8ca7-109">Logical paths are required when specifying subcomponents.</span></span>

<span data-ttu-id="c8ca7-110">Por convenção, a barra invertida " \\ " é usada para separar elementos de um caminho lógico.</span><span class="sxs-lookup"><span data-stu-id="c8ca7-110">By convention the backslash "\\" is used to separate elements of a logical path.</span></span> <span data-ttu-id="c8ca7-111">Além disso, não há restrições nos caracteres que podem aparecer em um caminho lógico não **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c8ca7-111">Beyond that, there are no restrictions on the characters that can appear in a non-**NULL** logical path.</span></span>

<span data-ttu-id="c8ca7-112">Um caminho lógico pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c8ca7-112">A logical path can be **NULL**.</span></span> <span data-ttu-id="c8ca7-113">Por convenção, os componentes com caminhos lógicos **nulos** são considerados no nível superior da hierarquia de caminho lógico de um gravador.</span><span class="sxs-lookup"><span data-stu-id="c8ca7-113">By convention, components with **NULL** logical paths are said to be at the top level of a writer's logical path hierarchy.</span></span>

<span data-ttu-id="c8ca7-114">Consulte também [*componente*](vssgloss-c.md), [*subcomponente*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="c8ca7-114">See also [*component*](vssgloss-c.md), [*subcomponent*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



