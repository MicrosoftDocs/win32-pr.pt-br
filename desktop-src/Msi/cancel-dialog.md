---
description: Uma caixa de diálogo cancelar confirma que o usuário deseja encerrar a instalação. Essa é uma caixa de diálogo modal.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Cancelar caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749804"
---
# <a name="cancel-dialog"></a><span data-ttu-id="ca022-104">Cancelar caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="ca022-104">Cancel Dialog</span></span>

<span data-ttu-id="ca022-105">Uma caixa de diálogo **Cancelar** confirma que o usuário deseja encerrar a instalação.</span><span class="sxs-lookup"><span data-stu-id="ca022-105">A **Cancel** dialog box confirms that the user wants to terminate the installation.</span></span> <span data-ttu-id="ca022-106">Essa é uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="ca022-106">This is a modal dialog box.</span></span>

<span data-ttu-id="ca022-107">Esse tipo de caixa de diálogo normalmente contém um [controle de texto](text-control.md) e dois [supressãos](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="ca022-107">This type of dialog box commonly contains a [Text control](text-control.md) and two [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="ca022-108">Os dois botões dão ao usuário a opção de retornar à última caixa de diálogo ou confirmar o encerramento da instalação.</span><span class="sxs-lookup"><span data-stu-id="ca022-108">The two buttons give the user the choice of either returning to the last dialog box or confirming the termination of the installation.</span></span>

<span data-ttu-id="ca022-109">O [EndDialog](enddialog-controlevent.md) ControlEvent, está vinculado a esses dois botões na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="ca022-109">The [EndDialog](enddialog-controlevent.md) ControlEvent is linked to these two buttons in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="ca022-110">O parâmetro de *retorno* do ControlEvent, EndDialog é vinculado a um dos botões e faz com que a caixa de diálogo **Cancelar** seja encerrada e o foco retorne à caixa de diálogo anterior.</span><span class="sxs-lookup"><span data-stu-id="ca022-110">The *Return* parameter of the EndDialog ControlEvent is linked to one of the buttons and causes the **Cancel** dialog box to be terminated and the focus to return to the previous dialog box.</span></span> <span data-ttu-id="ca022-111">O parâmetro *Exit* é vinculado ao outro botão e faz com que a interface do usuário retorne o controle para o instalador com o código apropriado indicando que o usuário deseja sair.</span><span class="sxs-lookup"><span data-stu-id="ca022-111">The *Exit* parameter is linked to the other button and causes the user interface to return control to the installer with the appropriate code indicating that the user wants to exit.</span></span> <span data-ttu-id="ca022-112">Em seguida, o instalador desliga e exibe a [caixa de diálogo UserExit](userexit-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="ca022-112">The installer then shuts down and displays the [UserExit Dialog](userexit-dialog.md).</span></span>

 

 



