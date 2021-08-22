---
description: O IMM inclui verificação de identificação de thread que determina se um thread de chamada é o criador de um identificador de contexto do método de entrada especificado (tipo HIMC) ou identificador de janela (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Desenvolvendo IME-Aware aplicativos de vários threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf495922d347119db3b8b517af13c850f2f19dfc558609f93f24953f0a3386a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949591"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a>Desenvolvendo IME-Aware aplicativos de vários threads

O IMM inclui verificação de identificação de thread que determina se um thread de chamada é o criador de um identificador de contexto do método de entrada especificado (tipo HIMC) ou identificador de janela (tipo HWND). Se o thread não for o criador do handle, a função chamada IMM falhará e uma chamada subsequente para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará ERROR \_ INVALID \_ ACCESS.

> [!Note]  
> A arquitetura atual do IMM não fornece um recurso de sincronização para acesso a alças do IMM.

 

Para usar a verificação de identificação de thread, seus aplicativos devem seguir as seguintes diretrizes:

-   Um thread não deve acessar o contexto de entrada criado por outro thread.
-   Um thread não deve associar um contexto de entrada a uma janela criada por outro thread e vice-versa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Gerenciador de Métodos de Entrada](using-input-method-manager.md)
</dt> </dl>

 

 
