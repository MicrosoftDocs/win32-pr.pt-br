---
description: Uma função do instalador pode exibir uma caixa de diálogo de mensagem de erro retornando qualquer um dos erros a seguir. Uma caixa de erro será exibida somente se o nível da interface do usuário estiver no nível completo, reduzido ou básico. Para obter mais informações, consulte níveis de interface do usuário.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Mensagens de erro exibidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748163"
---
# <a name="displayed-error-messages"></a><span data-ttu-id="dfa38-105">Mensagens de erro exibidas</span><span class="sxs-lookup"><span data-stu-id="dfa38-105">Displayed Error Messages</span></span>

<span data-ttu-id="dfa38-106">Uma [função do instalador](installer-function-reference.md) pode exibir uma caixa de diálogo de mensagem de erro retornando qualquer um dos erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="dfa38-106">An [installer function](installer-function-reference.md) may display an error message dialog box returning any of the following errors.</span></span> <span data-ttu-id="dfa38-107">Uma caixa de erro será exibida somente se o nível da interface do usuário estiver no nível completo, reduzido ou básico.</span><span class="sxs-lookup"><span data-stu-id="dfa38-107">An error box is displayed only if the user interface level is at the full, reduced, or basic level.</span></span> <span data-ttu-id="dfa38-108">Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="dfa38-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="dfa38-109">As funções do instalador exibem apenas mensagens de erro que estão na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dfa38-109">The installer functions only display error messages that are in the following table.</span></span> <span data-ttu-id="dfa38-110">Para erros que não estão nessa lista, o chamador da função é responsável por manipular a exibição de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="dfa38-110">For errors not in this list, the caller of the function is responsible for handling the display of error messages.</span></span>



| <span data-ttu-id="dfa38-111">Código do erro</span><span class="sxs-lookup"><span data-stu-id="dfa38-111">Error code</span></span>               | <span data-ttu-id="dfa38-112">Erro</span><span class="sxs-lookup"><span data-stu-id="dfa38-112">Error</span></span>                        |
|--------------------------|------------------------------|
| <span data-ttu-id="dfa38-113">ERRO ao \_ instalar \_ suspensão</span><span class="sxs-lookup"><span data-stu-id="dfa38-113">ERROR\_INSTALL\_SUSPEND</span></span>  | <span data-ttu-id="dfa38-114">A instalação foi suspensa.</span><span class="sxs-lookup"><span data-stu-id="dfa38-114">The install was suspended.</span></span>   |
| <span data-ttu-id="dfa38-115">ERRO ao \_ instalar o \_ UserExit</span><span class="sxs-lookup"><span data-stu-id="dfa38-115">ERROR\_INSTALL\_USEREXIT</span></span> | <span data-ttu-id="dfa38-116">O usuário saiu da instalação.</span><span class="sxs-lookup"><span data-stu-id="dfa38-116">The user exited the install.</span></span> |
| <span data-ttu-id="dfa38-117">\_falha na instalação do erro \_</span><span class="sxs-lookup"><span data-stu-id="dfa38-117">ERROR\_INSTALL\_FAILURE</span></span>  | <span data-ttu-id="dfa38-118">Falha na instalação.</span><span class="sxs-lookup"><span data-stu-id="dfa38-118">Install failed.</span></span>              |



 

 

 



