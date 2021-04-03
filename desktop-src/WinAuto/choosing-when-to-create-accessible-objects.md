---
title: Escolhendo quando criar objetos acessíveis
description: Os desenvolvedores de servidor podem criar todos os objetos acessíveis dentro de um contêiner quando o contêiner é criado ou podem criar objetos acessíveis dinamicamente.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005810"
---
# <a name="choosing-when-to-create-accessible-objects"></a><span data-ttu-id="850f6-103">Escolhendo quando criar objetos acessíveis</span><span class="sxs-lookup"><span data-stu-id="850f6-103">Choosing When to Create Accessible Objects</span></span>

<span data-ttu-id="850f6-104">Os desenvolvedores de servidor podem criar todos os objetos acessíveis dentro de um contêiner quando o contêiner é criado ou podem criar objetos acessíveis dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="850f6-104">Server developers can create all the accessible objects within a container when the container is created, or they can create the accessible objects dynamically.</span></span>

<span data-ttu-id="850f6-105">Por exemplo, imagine uma caixa de diálogo com vários controles personalizados.</span><span class="sxs-lookup"><span data-stu-id="850f6-105">For example, imagine a dialog box with several custom controls.</span></span> <span data-ttu-id="850f6-106">Um servidor cria objetos acessíveis para todos os controles personalizados quando a caixa de diálogo é exibida.</span><span class="sxs-lookup"><span data-stu-id="850f6-106">A server creates accessible objects for all of the custom controls when the dialog box is displayed.</span></span> <span data-ttu-id="850f6-107">No entanto, se um dos controles for uma caixa de combinação personalizada, o servidor aguardará até que um usuário o Selecione para criar objetos acessíveis para os itens que a caixa de combinação contém.</span><span class="sxs-lookup"><span data-stu-id="850f6-107">However, if one of the controls is a custom combo box, the server waits until a user selects it to create accessible objects for the items that the combo box contains.</span></span>

<span data-ttu-id="850f6-108">Ao fazer com que o pai Crie objetos acessíveis dinamicamente, os aplicativos usam menos memória do que se todos os objetos acessíveis possíveis foram criados antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="850f6-108">By having the parent create accessible objects dynamically, applications use less memory than if all the possible accessible objects were created ahead of time.</span></span>

 

 




