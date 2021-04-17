---
description: Os dispositivos de entrada do usuário são representados por essas classes. Uma máquina virtual sempre tem uma instância de cada classe associada a ela.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Classes de entrada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812947"
---
# <a name="input-classes"></a><span data-ttu-id="5784b-104">Classes de entrada</span><span class="sxs-lookup"><span data-stu-id="5784b-104">Input classes</span></span>

<span data-ttu-id="5784b-105">Os dispositivos de entrada do usuário são representados por essas classes.</span><span class="sxs-lookup"><span data-stu-id="5784b-105">The user input devices are represented by these classes.</span></span> <span data-ttu-id="5784b-106">Uma máquina virtual sempre tem uma instância de cada classe associada a ela.</span><span class="sxs-lookup"><span data-stu-id="5784b-106">A virtual machine always has one instance of each class associated with it.</span></span> <span data-ttu-id="5784b-107">Esses dispositivos podem não ser adicionados ou removidos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5784b-107">These devices may not be added or removed from the virtual machine.</span></span> <span data-ttu-id="5784b-108">Portanto, não há nenhuma instância do pool de recursos para dispositivos de teclado ou mouse.</span><span class="sxs-lookup"><span data-stu-id="5784b-108">Therefore, there are no resource pool instances for keyboard or mouse devices.</span></span>

<span data-ttu-id="5784b-109">Os dispositivos de teclado e mouse são vinculados à máquina virtual por meio da Associação [**Msvm \_ SystemDevice**](msvm-systemdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="5784b-109">The keyboard and mouse devices are linked to the virtual machine through the [**Msvm\_SystemDevice**](msvm-systemdevice.md) association.</span></span> <span data-ttu-id="5784b-110">Uma máquina virtual contém um dispositivo de mouse PS2 e sintético.</span><span class="sxs-lookup"><span data-stu-id="5784b-110">A virtual machine contains both a PS2 and a synthetic mouse device.</span></span> <span data-ttu-id="5784b-111">Somente um dispositivo apontador está ativo por vez.</span><span class="sxs-lookup"><span data-stu-id="5784b-111">Only one pointing device is active at a time.</span></span>

<span data-ttu-id="5784b-112">Veja a seguir as classes WMI de virtualização relacionadas à entrada.</span><span class="sxs-lookup"><span data-stu-id="5784b-112">The following are virtualization WMI classes related to input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5784b-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5784b-113">In this section</span></span>



| <span data-ttu-id="5784b-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="5784b-114">Topic</span></span>                                                          | <span data-ttu-id="5784b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5784b-115">Description</span></span>                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="5784b-116">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="5784b-116">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)<br/>             | <span data-ttu-id="5784b-117">Representa um dispositivo de teclado.</span><span class="sxs-lookup"><span data-stu-id="5784b-117">Represents a keyboard device.</span></span><br/>        |
| [<span data-ttu-id="5784b-118">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="5784b-118">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)<br/>             | <span data-ttu-id="5784b-119">Representa um dispositivo de mouse PS2.</span><span class="sxs-lookup"><span data-stu-id="5784b-119">Represents a PS2 mouse device.</span></span><br/>       |
| [<span data-ttu-id="5784b-120">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="5784b-120">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)<br/> | <span data-ttu-id="5784b-121">Representa um dispositivo de mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="5784b-121">Represents a synthetic mouse device.</span></span><br/> |



 

 

 




