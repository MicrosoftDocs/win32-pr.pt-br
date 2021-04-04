---
title: Desabilitando recursos de Serviços de Área de Trabalho Remota
description: Para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/01/2020
ms.locfileid: "103917866"
---
# <a name="disabling-remote-desktop-services-features"></a><span data-ttu-id="fad1b-103">Desabilitando recursos de Serviços de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="fad1b-103">Disabling Remote Desktop Services features</span></span>

<span data-ttu-id="fad1b-104">Para aumentar a segurança, você pode optar por desabilitar Serviços de Área de Trabalho Remota recursos como redirecionamento de área de transferência e redirecionamento de impressora para clientes que se conectam a servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) usando o controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="fad1b-104">For enhanced security, you might choose to disable Remote Desktop Services features such as clipboard redirection and printer redirection for clients that connect to Remote Desktop Session Host (RD Session Host) servers using the Remote Desktop ActiveX Control.</span></span>

<span data-ttu-id="fad1b-105">**Para desabilitar Serviços de Área de Trabalho Remota recursos**</span><span class="sxs-lookup"><span data-stu-id="fad1b-105">**To disable Remote Desktop Services features**</span></span>

1.  <span data-ttu-id="fad1b-106">Edite o registro do computador cliente e adicione as seguintes chaves:</span><span class="sxs-lookup"><span data-stu-id="fad1b-106">Edit the registry of the client computer and add the following keys:</span></span>

    -   <span data-ttu-id="fad1b-107">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**</span><span class="sxs-lookup"><span data-stu-id="fad1b-107">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableClipboardRedirection**</span></span>
    -   <span data-ttu-id="fad1b-108">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**</span><span class="sxs-lookup"><span data-stu-id="fad1b-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableDriveRedirection**</span></span>
    -   <span data-ttu-id="fad1b-109">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**</span><span class="sxs-lookup"><span data-stu-id="fad1b-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisablePrinterRedirection**</span></span>

2.  <span data-ttu-id="fad1b-110">Defina o valor de ambas as chaves para **reg \_ DWORD** 1.</span><span class="sxs-lookup"><span data-stu-id="fad1b-110">Set the value of both keys to **REG\_DWORD** 1.</span></span>

 

 




