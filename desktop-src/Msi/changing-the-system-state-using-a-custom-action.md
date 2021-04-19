---
description: Ações personalizadas destinadas a alterar o estado do sistema devem ser ações personalizadas de execução adiada.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Alterando o estado do sistema usando uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756741"
---
# <a name="changing-the-system-state-using-a-custom-action"></a><span data-ttu-id="6d42f-103">Alterando o estado do sistema usando uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="6d42f-103">Changing the System State Using a Custom Action</span></span>

<span data-ttu-id="6d42f-104">Ações personalizadas destinadas a alterar o estado do sistema devem ser ações personalizadas de execução adiada.</span><span class="sxs-lookup"><span data-stu-id="6d42f-104">Custom actions intended to change the system state must be deferred execution custom actions.</span></span> <span data-ttu-id="6d42f-105">As ações personalizadas que definem propriedades, Estados de recursos, Estados de componentes ou diretórios de destino ou agendam operações do sistema inserindo linhas em tabelas de sequência podem usar a execução imediata com segurança.</span><span class="sxs-lookup"><span data-stu-id="6d42f-105">Custom actions that set properties, feature states, component states, or target directories, or schedule system operations by inserting rows into sequence tables can use immediate execution safely.</span></span> <span data-ttu-id="6d42f-106">No entanto, as ações personalizadas que alteram o sistema diretamente ou chamam outro serviço do sistema devem ser adiadas para a hora em que o script de instalação é executado.</span><span class="sxs-lookup"><span data-stu-id="6d42f-106">However, custom actions that change the system directly or call another system service must be deferred to the time when the installation script is executed.</span></span> <span data-ttu-id="6d42f-107">Para obter mais informações, consulte [ações personalizadas de execução adiada](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6d42f-107">For more information, see [Deferred Execution Custom Actions](deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="6d42f-108">Você não deve tentar usar uma ação personalizada de execução imediata para alterar o estado do sistema, pois cada ação personalizada que altera o estado precisa ter uma ação personalizada de reversão correspondente para desfazer a alteração do estado do sistema em uma reversão de instalação.</span><span class="sxs-lookup"><span data-stu-id="6d42f-108">You should not attempt to use an immediate execution custom action to change the system state, because every custom action that changes the state needs to have a corresponding rollback custom action to undo the system state change on an installation rollback.</span></span> <span data-ttu-id="6d42f-109">Todas as ações personalizadas de reversão também são medidas personalizadas adiadas e devem preceder a ação que eles desfazem.</span><span class="sxs-lookup"><span data-stu-id="6d42f-109">All rollback custom actions are also deferred custom actions and must precede the action they undo.</span></span> <span data-ttu-id="6d42f-110">Para obter mais informações, consulte [Rollback Custom Actions](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6d42f-110">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



