---
description: Se esse bit for definido, a caixa de diálogo chamará periodicamente o instalador.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Bit de estilo de caixa de diálogo TrackDiskSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089851"
---
# <a name="trackdiskspace-dialog-style-bit"></a><span data-ttu-id="e5421-103">Bit de estilo de caixa de diálogo TrackDiskSpace</span><span class="sxs-lookup"><span data-stu-id="e5421-103">TrackDiskSpace Dialog Style Bit</span></span>

<span data-ttu-id="e5421-104">Se esse bit for definido, a caixa de diálogo chamará periodicamente o instalador.</span><span class="sxs-lookup"><span data-stu-id="e5421-104">If this bit is set, the dialog box periodically calls the installer.</span></span> <span data-ttu-id="e5421-105">Se a propriedade for alterada, ela notificará os controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e5421-105">If the property changes, it notifies the controls on the dialog.</span></span> <span data-ttu-id="e5421-106">Esse estilo pode ser usado se houver um controle na caixa de diálogo que indique espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="e5421-106">This style can be used if there is a control on the dialog indicating disk space.</span></span> <span data-ttu-id="e5421-107">Se o usuário alternar para outro aplicativo, adicionar ou remover arquivos ou, de outra forma, modificar o espaço em disco disponível, você poderá implementar rapidamente a alteração usando esse estilo.</span><span class="sxs-lookup"><span data-stu-id="e5421-107">If the user switches to another application, adds or removes files, or otherwise modifies available disk space, you can quickly implement the change using this style.</span></span>

<span data-ttu-id="e5421-108">Qualquer caixa de diálogo que dependa da propriedade [**OutOfDiskSpace**](outofdiskspace.md) para determinar se um diálogo deve ser definido por um bit de estilo de caixa de diálogo TrackDiskSpace para a caixa de diálogo para atualizar dinamicamente o espaço nos volumes de destino.</span><span class="sxs-lookup"><span data-stu-id="e5421-108">Any dialog box relying on the [**OutOfDiskSpace**](outofdiskspace.md) property to determine whether to bring up a dialog must set the TrackDiskSpace Dialog Style Bit for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="value"></a><span data-ttu-id="e5421-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e5421-109">Value</span></span>



| <span data-ttu-id="e5421-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="e5421-110">Decimal</span></span> | <span data-ttu-id="e5421-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="e5421-111">Hexadecimal</span></span> | <span data-ttu-id="e5421-112">Constante</span><span class="sxs-lookup"><span data-stu-id="e5421-112">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="e5421-113">32</span><span class="sxs-lookup"><span data-stu-id="e5421-113">32</span></span>      | <span data-ttu-id="e5421-114">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e5421-114">0x00000020</span></span>  | <span data-ttu-id="e5421-115">**msidbDialogAttributesTrackDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="e5421-115">**msidbDialogAttributesTrackDiskSpace**</span></span> |



 

 

 



