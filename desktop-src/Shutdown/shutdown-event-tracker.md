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
# <a name="shutdown-event-tracker"></a>Controlador de eventos de desligamento

O *controlador de eventos de desligamento* permite que o usuário ou aplicativo documente o motivo para desligar ou reiniciar o sistema. O usuário é solicitado a preencher informações ao selecionar **desligar** no menu **Iniciar** ou ao usar Shutdown.exe. Os desenvolvedores podem incluir um código de motivo ao chamar as funções [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) . As informações são armazenadas no log de eventos.

**Windows XP:** Embora esse recurso esteja habilitado por padrão a partir do Windows Server 2003, você deve habilitá-lo no Windows XP. Para obter mais informações, consulte a documentação do controlador de eventos de desligamento incluído no sistema ou no TechNet.

As funções [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) foram atualizadas para dar suporte a códigos de motivo de desligamento no parâmetro *dwReason* . Use os valores definidos em Reason. h para construir um código de motivo de desligamento ou defina um código de motivo personalizado. Um código de motivo de desligamento é construído a partir de um sinalizador principal, um sinalizador secundário e dois sinalizadores opcionais. Para obter mais informações, consulte [códigos de motivo de desligamento do sistema](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlador de eventos de desligamento (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
