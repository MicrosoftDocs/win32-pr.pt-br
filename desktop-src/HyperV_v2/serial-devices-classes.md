---
description: Os dispositivos seriais em uma máquina virtual consistem em controladores seriais e portas seriais. Cada máquina virtual tem exatamente um controlador serial e cada controlador serial tem exatamente duas portas seriais.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classes de dispositivos seriais
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785445"
---
# <a name="serial-devices-classes"></a><span data-ttu-id="3d5dc-104">Classes de dispositivos seriais</span><span class="sxs-lookup"><span data-stu-id="3d5dc-104">Serial devices classes</span></span>

<span data-ttu-id="3d5dc-105">Os dispositivos seriais em uma máquina virtual consistem em controladores seriais e portas seriais.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-105">The serial devices in a virtual machine consist of serial controllers and serial ports.</span></span> <span data-ttu-id="3d5dc-106">Cada máquina virtual tem exatamente um controlador serial e cada controlador serial tem exatamente duas portas seriais.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-106">Each virtual machine has exactly one serial controller, and each serial controller has exactly two serial ports.</span></span>

<span data-ttu-id="3d5dc-107">As configurações para o controlador serial não são configuráveis; Portanto, não há nenhuma instância de dados de configuração associada a ela.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-107">The settings for the serial controller are not configurable; therefore, there is no setting data instance associated with it.</span></span> <span data-ttu-id="3d5dc-108">Além disso, você não pode adicionar ou remover controladores seriais ou portas seriais de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-108">Also, you cannot add or remove serial controllers or serial ports from a virtual machine.</span></span> <span data-ttu-id="3d5dc-109">Portanto, não há nenhuma instância do pool de recursos para dispositivos seriais.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-109">Therefore, there are no resource pool instances for serial devices.</span></span>

<span data-ttu-id="3d5dc-110">Veja a seguir as classes WMI de virtualização relacionadas a dispositivos seriais.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-110">The following are virtualization WMI classes related to serial devices.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3d5dc-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3d5dc-111">In this section</span></span>



| <span data-ttu-id="3d5dc-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="3d5dc-112">Topic</span></span>                                                                                      | <span data-ttu-id="3d5dc-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d5dc-113">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="3d5dc-114">**Msvm \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="3d5dc-114">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)<br/>                         | <span data-ttu-id="3d5dc-115">Representa os recursos e o gerenciamento do controlador serial.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-115">Represents the capabilities and management of the serial controller.</span></span><br/> |
| [<span data-ttu-id="3d5dc-116">**\_SerialPort Msvm**</span><span class="sxs-lookup"><span data-stu-id="3d5dc-116">**Msvm\_SerialPort**</span></span>](msvm-serialport.md)<br/>                                     | <span data-ttu-id="3d5dc-117">Representa uma porta serial associada ao controlador serial.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-117">Represents a serial port associated with the serial controller.</span></span><br/>      |
| [<span data-ttu-id="3d5dc-118">**Msvm \_ SerialPortOnSerialController**</span><span class="sxs-lookup"><span data-stu-id="3d5dc-118">**Msvm\_SerialPortOnSerialController**</span></span>](msvm-serialportonserialcontroller.md)<br/> | <span data-ttu-id="3d5dc-119">Associa uma porta serial a um controlador serial.</span><span class="sxs-lookup"><span data-stu-id="3d5dc-119">Associates a serial port with a serial controller.</span></span><br/>                   |



 

 

 




