---
description: O controlador de eventos de desligamento permite que o usuário ou aplicativo documente o motivo para desligar ou reiniciar o sistema.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Controlador de eventos de desligamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296790"
---
# <a name="shutdown-event-tracker"></a><span data-ttu-id="fa06d-103">Controlador de eventos de desligamento</span><span class="sxs-lookup"><span data-stu-id="fa06d-103">Shutdown Event Tracker</span></span>

<span data-ttu-id="fa06d-104">O *controlador de eventos de desligamento* permite que o usuário ou aplicativo documente o motivo para desligar ou reiniciar o sistema.</span><span class="sxs-lookup"><span data-stu-id="fa06d-104">The *Shutdown Event Tracker* enables the user or application to document the reason for shutting down or restarting the system.</span></span> <span data-ttu-id="fa06d-105">O usuário é solicitado a preencher informações ao selecionar **desligar** no menu **Iniciar** ou ao usar Shutdown.exe.</span><span class="sxs-lookup"><span data-stu-id="fa06d-105">The user is prompted to fill in information when selecting **Shut Down** from the **Start** menu, or when using Shutdown.exe.</span></span> <span data-ttu-id="fa06d-106">Os desenvolvedores podem incluir um código de motivo ao chamar as funções [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .</span><span class="sxs-lookup"><span data-stu-id="fa06d-106">Developers can include a reason code when calling the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions.</span></span> <span data-ttu-id="fa06d-107">As informações são armazenadas no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="fa06d-107">The information is stored in the event log.</span></span>

<span data-ttu-id="fa06d-108">**Windows XP:** Embora esse recurso esteja habilitado por padrão a partir do Windows Server 2003, você deve habilitá-lo no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa06d-108">**Windows XP:** While this feature is enabled by default starting with Windows Server 2003, you must enable it on Windows XP.</span></span> <span data-ttu-id="fa06d-109">Para obter mais informações, consulte a documentação do controlador de eventos de desligamento incluído no sistema ou no TechNet.</span><span class="sxs-lookup"><span data-stu-id="fa06d-109">For more information, see the documentation for the Shutdown Event Tracker included in the system or on TechNet.</span></span>

<span data-ttu-id="fa06d-110">As funções [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) foram atualizadas para dar suporte a códigos de motivo de desligamento no parâmetro *dwReason* .</span><span class="sxs-lookup"><span data-stu-id="fa06d-110">The [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions have been updated to support shutdown reason codes in the *dwReason* parameter.</span></span> <span data-ttu-id="fa06d-111">Use os valores definidos em Reason. h para construir um código de motivo de desligamento ou defina um código de motivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="fa06d-111">Use the values defined in Reason.h to construct a shutdown reason code, or define a custom reason code.</span></span> <span data-ttu-id="fa06d-112">Um código de motivo de desligamento é construído a partir de um sinalizador principal, um sinalizador secundário e dois sinalizadores opcionais.</span><span class="sxs-lookup"><span data-stu-id="fa06d-112">A shutdown reason code is constructed from a major flag, a minor flag, and two optional flags.</span></span> <span data-ttu-id="fa06d-113">Para obter mais informações, consulte [códigos de motivo de desligamento do sistema](system-shutdown-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fa06d-113">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa06d-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa06d-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fa06d-115">[Controlador de eventos de desligamento (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="fa06d-115">[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span></span>
</dt> </dl>

 

 
