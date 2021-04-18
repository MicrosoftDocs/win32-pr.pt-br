---
description: O IMM inclui a verificação de identificação de thread que determina se um thread de chamada é o criador de um identificador de contexto de método de entrada especificado (tipo HIMC) ou identificador de janela (tipo HWND).
ms.assetid: da55d6fe-a620-4ea7-9055-91bcd3233267
title: Desenvolvendo IME-Aware aplicativos de vários threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5730fc72ef41a84e01655116f94fc274f60548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782800"
---
# <a name="developing-ime-aware-multiple-thread-applications"></a><span data-ttu-id="bfd6f-103">Desenvolvendo IME-Aware aplicativos de vários threads</span><span class="sxs-lookup"><span data-stu-id="bfd6f-103">Developing IME-Aware Multiple-thread Applications</span></span>

<span data-ttu-id="bfd6f-104">O IMM inclui a verificação de identificação de thread que determina se um thread de chamada é o criador de um identificador de contexto de método de entrada especificado (tipo HIMC) ou identificador de janela (tipo HWND).</span><span class="sxs-lookup"><span data-stu-id="bfd6f-104">The IMM includes thread identification checking that determines if a calling thread is the creator of a specified input method context handle (HIMC type) or window handle (HWND type).</span></span> <span data-ttu-id="bfd6f-105">Se o thread não for o criador do identificador, a função chamada IMM falhará e uma chamada subsequente para [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de \_ \_ acesso inválido.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-105">If the thread is not the creator of the handle, the called IMM function fails and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_ACCESS.</span></span>

> [!Note]  
> <span data-ttu-id="bfd6f-106">A arquitetura atual do IMM não fornece um recurso de sincronização para acesso aos identificadores do IMM.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-106">The current IMM architecture does not provide a synchronization facility for access to IMM handles.</span></span>

 

<span data-ttu-id="bfd6f-107">Para usar a verificação de identificação de thread, seus aplicativos devem aderir às seguintes diretrizes:</span><span class="sxs-lookup"><span data-stu-id="bfd6f-107">To use thread identification checking, your applications must adhere to the following guidelines:</span></span>

-   <span data-ttu-id="bfd6f-108">Um thread não deve acessar o contexto de entrada criado por outro thread.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-108">A thread should not access the input context created by another thread.</span></span>
-   <span data-ttu-id="bfd6f-109">Um thread não deve associar um contexto de entrada a uma janela criada por outro thread, e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="bfd6f-109">A thread should not associate an input context with a window created by another thread, and vice versa.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfd6f-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfd6f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfd6f-111">Usando o Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="bfd6f-111">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
