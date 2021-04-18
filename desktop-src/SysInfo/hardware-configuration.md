---
description: As funções de configuração de hardware recuperam informações como processador, perfil de hardware e informações de teclado.
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: Configuração de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee4abe543f0603ab6cf80ef395fe56e4e3300c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756351"
---
# <a name="hardware-configuration"></a><span data-ttu-id="5209f-103">Configuração de hardware</span><span class="sxs-lookup"><span data-stu-id="5209f-103">Hardware Configuration</span></span>

<span data-ttu-id="5209f-104">As funções de configuração de hardware recuperam informações como processador, perfil de hardware e informações de teclado.</span><span class="sxs-lookup"><span data-stu-id="5209f-104">The hardware configuration functions retrieve information such as processor, hardware profile, and keyboard information.</span></span>

<span data-ttu-id="5209f-105">A função [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) recupera informações de processador e memória, como o tamanho da página, o identificador OEM (fabricante original do equipamento), o número e o tipo de processadores, o intervalo de endereços do aplicativo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5209f-105">The [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function retrieves processor and memory information, such as the page size, original equipment manufacturer (OEM) identifier, number and type of processors, application address range, and so on.</span></span> <span data-ttu-id="5209f-106">A função [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) recupera informações sobre as operações de ponto flutuante e os conjuntos de instruções com suporte do processador.</span><span class="sxs-lookup"><span data-stu-id="5209f-106">The [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent) function retrieves information about the floating-point operations and instruction sets supported by the processor.</span></span>

<span data-ttu-id="5209f-107">A função [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) recupera informações sobre o perfil de hardware.</span><span class="sxs-lookup"><span data-stu-id="5209f-107">The [**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea) function retrieves information about the hardware profile.</span></span> <span data-ttu-id="5209f-108">O perfil de hardware inclui informações como o estado de encaixe, o GUID (identificador global exclusivo) e o nome de exibição do perfil.</span><span class="sxs-lookup"><span data-stu-id="5209f-108">The hardware profile includes information such as the docking state, globally unique identifier (GUID), and display name for the profile.</span></span> <span data-ttu-id="5209f-109">A função [**Getkeyboardtype**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) recupera informações como o tipo de teclado e o número de teclas de função no teclado atual.</span><span class="sxs-lookup"><span data-stu-id="5209f-109">The [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype) function retrieves such information as the type of keyboard and the number of function keys on the current keyboard.</span></span>

 

 
