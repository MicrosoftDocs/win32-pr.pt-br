---
description: A API de energia do dispositivo facilita a determinação de quais dispositivos são capazes de ativar o sistema de um estado de suspensão e quais Estados de suspensão os dispositivos dão suporte à ativação do. Para obter mais informações sobre os Estados de suspensão, consulte Estados de energia do sistema.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Gerenciamento de energia do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921727"
---
# <a name="device-power-management"></a><span data-ttu-id="cf28a-104">Gerenciamento de energia do dispositivo</span><span class="sxs-lookup"><span data-stu-id="cf28a-104">Device Power Management</span></span>

<span data-ttu-id="cf28a-105">A API de energia do dispositivo facilita a determinação de quais dispositivos são capazes de ativar o sistema de um estado de suspensão e quais Estados de suspensão os dispositivos dão suporte à ativação do.</span><span class="sxs-lookup"><span data-stu-id="cf28a-105">The Device Power API makes it easy to determine which devices are able to wake the system from a sleep state, and which sleep states those devices support waking from.</span></span> <span data-ttu-id="cf28a-106">Para obter mais informações sobre os Estados de suspensão, consulte [Estados de energia do sistema](system-power-states.md).</span><span class="sxs-lookup"><span data-stu-id="cf28a-106">For more information about sleep states, see [System Power States](system-power-states.md).</span></span>

<span data-ttu-id="cf28a-107">A função [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) pode ser usada para pesquisar a lista de dispositivos que correspondem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="cf28a-107">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function can be used to search the device list for devices that match specified criteria.</span></span> <span data-ttu-id="cf28a-108">Os critérios podem incluir a capacidade do dispositivo de dar suporte a um estado do sistema ou despertar com base nesse estado.</span><span class="sxs-lookup"><span data-stu-id="cf28a-108">The criteria may include the device's ability to support a system state, or wake from that state.</span></span> <span data-ttu-id="cf28a-109">Os sinalizadores com suporte no momento podem ser encontrados em WinNT. h e DevPower. h.</span><span class="sxs-lookup"><span data-stu-id="cf28a-109">Currently supported flags can be found in WinNT.h and DevPower.h.</span></span>

<span data-ttu-id="cf28a-110">A função [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) habilita ou desabilita um dispositivo especificado de ativar o sistema de um estado de suspensão.</span><span class="sxs-lookup"><span data-stu-id="cf28a-110">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function enables or disables a specified device from waking the system from a sleep state.</span></span>

<span data-ttu-id="cf28a-111">A API de energia do dispositivo permite aos desenvolvedores criar uma melhor experiência do usuário, fornecendo ao usuário mais informações sobre o que o sistema está fazendo e mais controle sobre os dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="cf28a-111">The Device Power API allows developers to create a better user experience by giving the user more information about what the system is doing, and more control over the devices in the system.</span></span> <span data-ttu-id="cf28a-112">A energia do dispositivo é útil em situações em que o consumo de energia é crítico, como em dispositivos portáteis em execução em baterias.</span><span class="sxs-lookup"><span data-stu-id="cf28a-112">Device Power is useful in situations where power consumption is critical, such as in portable devices running on batteries.</span></span> <span data-ttu-id="cf28a-113">Por exemplo, o esquema de gerenciamento de energia usado em um computador desktop pode não ser o esquema ideal para um computador laptop, de modo que o usuário talvez queira desabilitar a ativação de determinados dispositivos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="cf28a-113">For example, the power management scheme used in a desktop computer may not be the optimal scheme for a laptop computer, so the user may want to disable certain devices from waking the system.</span></span> <span data-ttu-id="cf28a-114">Isso pode conservar energia porque os dispositivos desabilitados não desenharão energia enquanto o sistema estiver no modo de suspensão.</span><span class="sxs-lookup"><span data-stu-id="cf28a-114">This can conserve energy because the disabled devices will not draw power while the system is in sleep mode.</span></span>

<span data-ttu-id="cf28a-115">Para obter um exemplo, consulte [usando a API de energia do dispositivo](using-the-device-power-api.md).</span><span class="sxs-lookup"><span data-stu-id="cf28a-115">For an example, see [Using the Device Power API](using-the-device-power-api.md).</span></span>

 

 



