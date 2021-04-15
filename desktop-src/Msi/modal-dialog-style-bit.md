---
description: Se esse bit for definido, a caixa de diálogo será modal, outras caixas de diálogo do mesmo aplicativo não poderão ser colocadas sobre ele, e o diálogo manterá o controle enquanto estiver em execução.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit de estilo de caixa de diálogo modal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506093"
---
# <a name="modal-dialog-style-bit"></a><span data-ttu-id="3f604-103">Bit de estilo de caixa de diálogo modal</span><span class="sxs-lookup"><span data-stu-id="3f604-103">Modal Dialog Style Bit</span></span>

<span data-ttu-id="3f604-104">Se esse bit for definido, a caixa de diálogo será modal, outras caixas de diálogo do mesmo aplicativo não poderão ser colocadas sobre ele, e o diálogo manterá o controle enquanto estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="3f604-104">If this bit is set, the dialog box is modal, other dialogs of the same application cannot be put on top of it, and the dialog keeps the control while it is running.</span></span> <span data-ttu-id="3f604-105">Se esse bit não for definido, a caixa de diálogo será sem janela restrita, outras caixas de diálogo do mesmo aplicativo poderão ser movidas sobre ele.</span><span class="sxs-lookup"><span data-stu-id="3f604-105">If this bit is not set, the dialog is modeless, other dialogs of the same application may be moved on top of it.</span></span> <span data-ttu-id="3f604-106">Depois que uma caixa de diálogo sem janela restrita é criada e exibida, a interface do usuário retorna o controle ao instalador.</span><span class="sxs-lookup"><span data-stu-id="3f604-106">After a modeless dialog is created and displayed, the user interface returns control to the installer.</span></span> <span data-ttu-id="3f604-107">Em seguida, o instalador chama a interface do usuário periodicamente para atualizar a caixa de diálogo e dar a ela a oportunidade de processar as mensagens.</span><span class="sxs-lookup"><span data-stu-id="3f604-107">The installer then calls the user interface periodically to update the dialog and to give it a chance to process the messages.</span></span> <span data-ttu-id="3f604-108">Assim que isso for feito, o controle será retornado para o instalador.</span><span class="sxs-lookup"><span data-stu-id="3f604-108">As soon as this is done, the control is returned to the installer.</span></span>

> [!Note]  
> <span data-ttu-id="3f604-109">Não deve haver caixas de diálogo sem janela restrita em uma sequência de assistente, pois isso retornará o controle ao instalador, encerrando a sequência do assistente prematuramente.</span><span class="sxs-lookup"><span data-stu-id="3f604-109">There should be no modeless dialogs in a wizard sequence, since this would return control to the installer, ending the wizard sequence prematurely.</span></span>

 

## <a name="value"></a><span data-ttu-id="3f604-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3f604-110">Value</span></span>



| <span data-ttu-id="3f604-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="3f604-111">Decimal</span></span> | <span data-ttu-id="3f604-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="3f604-112">Hexadecimal</span></span> | <span data-ttu-id="3f604-113">Constante</span><span class="sxs-lookup"><span data-stu-id="3f604-113">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="3f604-114">2</span><span class="sxs-lookup"><span data-stu-id="3f604-114">2</span></span>       | <span data-ttu-id="3f604-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3f604-115">0x00000002</span></span>  | <span data-ttu-id="3f604-116">**msidbDialogAttributesSysModal**</span><span class="sxs-lookup"><span data-stu-id="3f604-116">**msidbDialogAttributesSysModal**</span></span> |



 

 

 



