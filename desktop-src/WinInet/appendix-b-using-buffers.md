---
title: Usando buffers de cadeia de caracteres
description: As funções que retornam cadeias de caracteres contêm um parâmetro de entrada, lpszBuffer e um parâmetro de tamanho, lpdwBufferLength. Embora lpszBuffer possa ser nulo, lpdwBufferLength deve ser um ponteiro válido para uma variável DWORD.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641465"
---
# <a name="using-string-buffers"></a><span data-ttu-id="6d912-104">Usando buffers de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="6d912-104">Using String Buffers</span></span>

<span data-ttu-id="6d912-105">As funções que retornam cadeias de caracteres contêm um parâmetro de entrada, *lpszBuffer* e um parâmetro de tamanho, *lpdwBufferLength*.</span><span class="sxs-lookup"><span data-stu-id="6d912-105">Functions that return strings contain an input parameter, *lpszBuffer*, and a size parameter, *lpdwBufferLength*.</span></span> <span data-ttu-id="6d912-106">Embora *lpszBuffer* possa ser **nulo**, *lpdwBufferLength* deve ser um ponteiro válido para uma variável **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6d912-106">Although *lpszBuffer* can be **NULL**, *lpdwBufferLength* must be a valid pointer to a **DWORD** variable.</span></span> <span data-ttu-id="6d912-107">Se o buffer de entrada apontado por *lpszBuffer* for **nulo** ou muito pequeno para manter a cadeia de caracteres de saída, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **erro de \_ \_ buffer insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="6d912-107">If the input buffer pointed to by *lpszBuffer* is **NULL** or too small to hold the output string, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="6d912-108">A variável apontada por *lpdwBufferLength* contém um número que representa o número de bytes que a função requer para retornar a cadeia de caracteres solicitada, incluindo o terminador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6d912-108">The variable pointed to by *lpdwBufferLength* contains a number that represents the number of bytes the function requires to return the requested string, including the **null** terminator.</span></span> <span data-ttu-id="6d912-109">O aplicativo deve alocar um buffer desse tamanho, definir a variável apontada por *lpdwBufferLength* para esse valor e reenviar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6d912-109">The application should allocate a buffer of this size, set the variable pointed to by *lpdwBufferLength* to this value, and resubmit the request.</span></span> <span data-ttu-id="6d912-110">Se o tamanho do buffer for suficiente para receber a cadeia de caracteres solicitada, a cadeia de caracteres será copiada para o buffer de saída com um terminador **nulo** e a função retornará uma indicação de êxito.</span><span class="sxs-lookup"><span data-stu-id="6d912-110">If the buffer size is sufficient to receive the requested string, the string is copied to the output buffer with a **null** terminator and the function returns a success indication.</span></span> <span data-ttu-id="6d912-111">A variável apontada por *lpdwBufferLength* agora contém o número de caracteres armazenados no buffer, excluindo o terminador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6d912-111">The variable pointed to by *lpdwBufferLength* now contains the number of characters stored in the buffer, excluding the **null** terminator.</span></span>

> [!Note]  
> <span data-ttu-id="6d912-112">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="6d912-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="6d912-113">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="6d912-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="6d912-114">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="6d912-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 