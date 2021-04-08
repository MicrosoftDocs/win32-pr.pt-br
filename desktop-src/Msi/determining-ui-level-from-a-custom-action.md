---
description: Uma ação personalizada em uma tabela de sequência de interface do usuário ou um arquivo executável externo pode precisar do nível de interface do usuário atual da instalação.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Determinando o nível da interface do usuário de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922041"
---
# <a name="determining-ui-level-from-a-custom-action"></a><span data-ttu-id="88a60-103">Determinando o nível da interface do usuário de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="88a60-103">Determining UI Level from a Custom Action</span></span>

<span data-ttu-id="88a60-104">Uma ação personalizada em uma tabela de sequência de interface do usuário ou um arquivo executável externo pode precisar do nível de interface do usuário atual da instalação.</span><span class="sxs-lookup"><span data-stu-id="88a60-104">A custom action in a UI sequence table or an external executable file may need the current user interface level of the installation.</span></span> <span data-ttu-id="88a60-105">Por exemplo, uma ação personalizada que tem uma caixa de diálogo deve exibir apenas o diálogo quando o nível da interface do usuário for interface de usuários completa ou reduzida, ele não deverá exibir a caixa de diálogo se o nível da interface do usuário for Basic UI ou None.</span><span class="sxs-lookup"><span data-stu-id="88a60-105">For example, a custom action that has a dialog box should only display the dialog when the user interface level is Full UI or Reduced UI, it should not display the dialog if the user interface level is Basic UI or None.</span></span> <span data-ttu-id="88a60-106">Você deve usar a propriedade [**UILevel**](uilevel.md) para determinar o nível da interface do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="88a60-106">You should use the [**UILevel**](uilevel.md) property to determine the current user interface level.</span></span> <span data-ttu-id="88a60-107">Você não pode chamar [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) de uma ação personalizada e não é possível alterar a propriedade de nível da interface do usuário de dentro de uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="88a60-107">You cannot call [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) from a custom action and it is not possible to change the UI level property from within a custom action.</span></span>

<span data-ttu-id="88a60-108">É recomendável que as ações personalizadas não usem o nível da interface do usuário como uma condição para enviar mensagens de erro ao instalador, pois isso pode interferir no registro em log e mensagens externas.</span><span class="sxs-lookup"><span data-stu-id="88a60-108">It is recommended that custom actions not use the UI level as a condition for sending error messages to the installer because this can interfere with logging and external messages.</span></span>

 

 



