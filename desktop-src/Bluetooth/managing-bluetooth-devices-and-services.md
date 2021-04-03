---
title: Gerenciando dispositivos e serviços Bluetooth
description: Duas abordagens de programação Bluetooth primárias para programação do Windows com a interface do Windows Sockets e gerenciamento de dispositivos diretamente com interfaces Bluetooth sem soquete.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Gerenciando dispositivos e serviços Bluetooth
- Dispositivos e serviços Bluetooth, gerenciando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084572"
---
# <a name="managing-bluetooth-devices-and-services"></a><span data-ttu-id="92e74-105">Gerenciando dispositivos e serviços Bluetooth</span><span class="sxs-lookup"><span data-stu-id="92e74-105">Managing Bluetooth Devices and Services</span></span>

<span data-ttu-id="92e74-106">Esta seção descreve como usar a API do Bluetooth para controlar diretamente os dispositivos e serviços Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="92e74-106">This section describes how to use the Bluetooth API to directly control Bluetooth devices and services.</span></span>

<span data-ttu-id="92e74-107">Para obter informações sobre como usar a interface do Windows Sockets para programar Bluetooth no Windows, consulte [suporte do Windows Sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="92e74-107">For information about using the Windows Sockets interface to program Bluetooth on Windows, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>

> [!Note]  
> <span data-ttu-id="92e74-108">O Bluetooth não impede que os recursos de gerenciamento de energia interrompam as transmissões de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="92e74-108">Bluetooth does not prevent power management features from interrupting Bluetooth transmissions.</span></span> <span data-ttu-id="92e74-109">Os aplicativos habilitados para Bluetooth podem monitorar mensagens de energia para evitar tal interrupção.</span><span class="sxs-lookup"><span data-stu-id="92e74-109">Bluetooth-enabled applications can monitor power messages to prevent such interruption.</span></span> <span data-ttu-id="92e74-110">Para obter mais informações, consulte [usando o gerenciamento de energia](/windows/desktop/Power/using-power-management).</span><span class="sxs-lookup"><span data-stu-id="92e74-110">For more information, see [Using Power Management](/windows/desktop/Power/using-power-management).</span></span>

 

<span data-ttu-id="92e74-111">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="92e74-111">This section contains the following topics.</span></span>

| <span data-ttu-id="92e74-112">Seção</span><span class="sxs-lookup"><span data-stu-id="92e74-112">Section</span></span>                                                                               | <span data-ttu-id="92e74-113">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="92e74-113">Content</span></span>                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="92e74-114">Selecionando um dispositivo Bluetooth</span><span class="sxs-lookup"><span data-stu-id="92e74-114">Selecting a Bluetooth Device</span></span>](selecting-a-bluetooth-device.md)                      | <span data-ttu-id="92e74-115">Descreve como selecionar um dispositivo Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="92e74-115">Describes how to select a Bluetooth device.</span></span>                                   |
| [<span data-ttu-id="92e74-116">Mensagens DEVICECHANGE do Bluetooth e do WM \_</span><span class="sxs-lookup"><span data-stu-id="92e74-116">Bluetooth and WM\_DEVICECHANGE Messages</span></span>](bluetooth-and-wm-devicechange-messages.md) | <span data-ttu-id="92e74-117">Explica a interação entre as mensagens do Bluetooth e do **WM \_ DEVICECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="92e74-117">Explains the interaction between Bluetooth and **WM\_DEVICECHANGE** messages.</span></span> |



 

 

 