---
description: O aplicativo pode solicitar um dos dois modos de operação ao abrir um dispositivo de telefone.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modos de operação e privilégios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661786"
---
# <a name="operating-modes-and-privileges"></a><span data-ttu-id="53a1c-103">Modos de operação e privilégios</span><span class="sxs-lookup"><span data-stu-id="53a1c-103">Operating Modes and Privileges</span></span>

<span data-ttu-id="53a1c-104">O aplicativo pode solicitar um dos dois modos de operação ao abrir um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="53a1c-104">The application can request one of two operating modes when opening a phone device.</span></span> <span data-ttu-id="53a1c-105">Esses modos refletem os privilégios que o aplicativo solicita para o dispositivo:</span><span class="sxs-lookup"><span data-stu-id="53a1c-105">These modes reflect the privileges the application requests for the device:</span></span>

-   <span data-ttu-id="53a1c-106">Abrir um telefone para monitorar privilégios permite que o aplicativo determine o status do dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="53a1c-106">Opening a phone for monitor privileges lets the application determine the status of the phone device.</span></span> <span data-ttu-id="53a1c-107">As mensagens são enviadas ao aplicativo quando o status é alterado no dispositivo de telefone é detectado.</span><span class="sxs-lookup"><span data-stu-id="53a1c-107">Messages are sent to the application when status changes on the phone device are detected.</span></span>
-   <span data-ttu-id="53a1c-108">Um aplicativo que abre um dispositivo de telefone para privilégios de proprietário pode usar operações que modificam o estado do dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="53a1c-108">An application that opens a phone device for owner privileges can use operations that modify the state of the phone device.</span></span> <span data-ttu-id="53a1c-109">O privilégio de proprietário também inclui automaticamente privilégios de monitor completo.</span><span class="sxs-lookup"><span data-stu-id="53a1c-109">Owner privilege automatically includes full monitor privileges as well.</span></span> <span data-ttu-id="53a1c-110">A qualquer momento, um determinado dispositivo de telefone pode ser aberto apenas uma vez para privilégios de proprietário, mas várias vezes para os privilégios de monitor.</span><span class="sxs-lookup"><span data-stu-id="53a1c-110">At any time, a given phone device can be open only once for owner privileges, but multiple times for monitor privileges.</span></span> <span data-ttu-id="53a1c-111">Todas as operações de **phoneset** exigem privilégios de proprietário, enquanto todas as operações de **phoneGet** exigem apenas o monitoramento de privilégios.</span><span class="sxs-lookup"><span data-stu-id="53a1c-111">All **phoneSet** operations require owner privileges, while all **phoneGet** operations require only monitor privileges.</span></span>

 

 



