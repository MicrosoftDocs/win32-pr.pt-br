---
description: Descrição de conflitos entre os gestos e caracteres e símbolos do aplicativo.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflitos entre gestos de aplicativo e caracteres e símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791256"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a><span data-ttu-id="41ef0-103">Conflitos entre gestos de aplicativo e caracteres e símbolos</span><span class="sxs-lookup"><span data-stu-id="41ef0-103">Conflicts Between Application Gestures and Characters and Symbols</span></span>

<span data-ttu-id="41ef0-104">Alguns gestos de aplicativo podem entrar em conflito com caracteres, combinações de caracteres, símbolos, combinações de caracteres e símbolos ou palavras inteiras escritas em um único traço.</span><span class="sxs-lookup"><span data-stu-id="41ef0-104">Some application gestures may conflict with characters, combinations of characters, symbols, combinations of characters and symbols or whole words written in a single stroke.</span></span> <span data-ttu-id="41ef0-105">A maioria desses conflitos é evitada com uma compreensão detalhada do contexto no qual o gesto do aplicativo é executado.</span><span class="sxs-lookup"><span data-stu-id="41ef0-105">Most of these conflicts are avoided by having a detailed understanding of the context in which the application gesture is performed.</span></span>

<span data-ttu-id="41ef0-106">Por exemplo, para distinguir um gesto direito de um traço (-) ou um sublinhado ( \_ ), um aplicativo pode filtrar por quão próximo o gesto é para os caracteres vizinhos, o tamanho relativo em comparação com os caracteres ou outras informações contidas em um pacote.</span><span class="sxs-lookup"><span data-stu-id="41ef0-106">For example, to distinguish a right gesture from a dash (-) or an underscore (\_), an application may filter for how close the gesture is to neighboring characters, the relative size as compared to characters, or other information contained in a packet.</span></span> <span data-ttu-id="41ef0-107">O tempo do gesto do aplicativo também pode ser um fator determinante para decidir entre gestos e caracteres.</span><span class="sxs-lookup"><span data-stu-id="41ef0-107">The timing of the application gesture may also be a determining factor in deciding between gestures and characters.</span></span> <span data-ttu-id="41ef0-108">Pode haver mais de uma pausa antes de aplicar um gesto de aplicativo do que antes de inserir caracteres.</span><span class="sxs-lookup"><span data-stu-id="41ef0-108">There may be more of a pause before applying an application gesture than before inputting characters.</span></span> <span data-ttu-id="41ef0-109">A menos que um usuário esteja executando uma série de gestos de desfazer ou Backspace, também pode haver mais de uma pausa após um gesto de um caractere.</span><span class="sxs-lookup"><span data-stu-id="41ef0-109">Unless a user is performing a series of undo or backspace gestures, there may also be more of a pause after a gesture than a character.</span></span>

<span data-ttu-id="41ef0-110">Os tópicos a seguir detalham esses conflitos:</span><span class="sxs-lookup"><span data-stu-id="41ef0-110">The following topics detail these conflicts:</span></span>

-   [<span data-ttu-id="41ef0-111">Conflitos com caracteres latinos e símbolos</span><span class="sxs-lookup"><span data-stu-id="41ef0-111">Conflicts with Latin characters and symbols</span></span>](conflicts-with-latin-characters-and-symbols.md)
-   [<span data-ttu-id="41ef0-112">Conflitos com East-Asian caracteres</span><span class="sxs-lookup"><span data-stu-id="41ef0-112">Conflicts with East-Asian Characters</span></span>](conflicts-with-east-asian-characters.md)

 

 



