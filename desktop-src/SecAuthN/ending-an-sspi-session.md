---
description: Quando o cliente tiver terminado de se comunicar com qualquer servidor ou tiver terminado de usar as credenciais adicionais passadas para a função falha AcquireCredentialsHandle, o cliente deverá chamar a função FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Encerrando uma sessão SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1fdc51ba1c31ae4ac8abb52c6d4c4372a9d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647007"
---
# <a name="ending-an-sspi-session"></a><span data-ttu-id="9f269-103">Encerrando uma sessão SSPI</span><span class="sxs-lookup"><span data-stu-id="9f269-103">Ending an SSPI Session</span></span>

<span data-ttu-id="9f269-104">Depois que o cliente e o servidor tiverem terminado a comunicação, ambos os lados chamarão a função [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) com seus respectivos identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="9f269-104">After the client and server have finished communicating, both sides call the [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) function with their respective context handles.</span></span> <span data-ttu-id="9f269-105">Quando o cliente tiver terminado de se comunicar com qualquer servidor ou tiver terminado de usar as credenciais adicionais passadas para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , o cliente deverá chamar a função [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="9f269-105">When the client has finished communicating with any server or has finished using the additional credentials passed to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, the client must call the [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) function.</span></span> <span data-ttu-id="9f269-106">Quando o servidor estiver pronto para desligar e antes de descarregar a DLL, o servidor deverá chamar **DeleteSecurityContext**.</span><span class="sxs-lookup"><span data-stu-id="9f269-106">When the server is ready to shut down and before unloading the DLL, the server must call **DeleteSecurityContext**.</span></span>

 

 
