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
# <a name="using-string-buffers"></a>Usando buffers de cadeia de caracteres

As funções que retornam cadeias de caracteres contêm um parâmetro de entrada, *lpszBuffer* e um parâmetro de tamanho, *lpdwBufferLength*. Embora *lpszBuffer* possa ser **nulo**, *lpdwBufferLength* deve ser um ponteiro válido para uma variável **DWORD** . Se o buffer de entrada apontado por *lpszBuffer* for **nulo** ou muito pequeno para manter a cadeia de caracteres de saída, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um **erro de \_ \_ buffer insuficiente**. A variável apontada por *lpdwBufferLength* contém um número que representa o número de bytes que a função requer para retornar a cadeia de caracteres solicitada, incluindo o terminador **nulo** . O aplicativo deve alocar um buffer desse tamanho, definir a variável apontada por *lpdwBufferLength* para esse valor e reenviar a solicitação. Se o tamanho do buffer for suficiente para receber a cadeia de caracteres solicitada, a cadeia de caracteres será copiada para o buffer de saída com um terminador **nulo** e a função retornará uma indicação de êxito. A variável apontada por *lpdwBufferLength* agora contém o número de caracteres armazenados no buffer, excluindo o terminador **nulo** .

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 