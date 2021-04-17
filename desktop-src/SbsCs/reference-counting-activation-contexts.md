---
description: Os contextos de ativação são objetos contados como referência. Seu aplicativo deve ter uma referência em um contexto de ativação para poder usá-lo.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Contextos de ativação de contagem de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff00afa0dd3a347e14ff9723c06d54af4520ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752542"
---
# <a name="reference-counting-activation-contexts"></a><span data-ttu-id="729b5-104">Contextos de ativação de contagem de referência</span><span class="sxs-lookup"><span data-stu-id="729b5-104">Reference Counting Activation Contexts</span></span>

<span data-ttu-id="729b5-105">Os contextos de ativação são objetos contados como referência.</span><span class="sxs-lookup"><span data-stu-id="729b5-105">Activation contexts are reference-counted objects.</span></span> <span data-ttu-id="729b5-106">Seu aplicativo deve ter uma referência em um contexto de ativação para poder usá-lo.</span><span class="sxs-lookup"><span data-stu-id="729b5-106">Your application must have a reference on an activation context in order to use it.</span></span> <span data-ttu-id="729b5-107">As funções da API de contexto de ativação que usam um contexto de ativação podem executar sua própria contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="729b5-107">The functions of the Activation Context API that take an activation context can perform their own reference counting.</span></span> <span data-ttu-id="729b5-108">Por exemplo, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aumenta e [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) diminui a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="729b5-108">For example, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) increases and [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) decreases the reference count.</span></span> <span data-ttu-id="729b5-109">Se, no entanto, o aplicativo passar um contexto de ativação sem usar essas funções, o aplicativo deverá fornecer seu próprio método de contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="729b5-109">If however your application passes an activation context without using these functions, the application should provide its own method of reference counting.</span></span>

<span data-ttu-id="729b5-110">Quando um aplicativo chama [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), o identificador retornado terá uma contagem de referência de um.</span><span class="sxs-lookup"><span data-stu-id="729b5-110">When an application calls [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), the handle returned will have a reference count of one.</span></span> <span data-ttu-id="729b5-111">Após a conclusão do aplicativo com o contexto de ativação, o identificador deve ser liberado e a contagem de referência diminuiu com a chamada de [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span><span class="sxs-lookup"><span data-stu-id="729b5-111">After the application finishes with the activation context, the handle should be released and the reference count decreased by calling [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span></span> <span data-ttu-id="729b5-112">Não tente usar [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)ou qualquer outra função de gerenciamento de memória no identificador de contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="729b5-112">Do not attempt to use [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree), or any other memory-management functions on the activation context handle.</span></span>

<span data-ttu-id="729b5-113">O exemplo a seguir mostra um método para manipular a contagem de referência durante o tempo de vida de um contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="729b5-113">The following example shows a method for handling reference counting over the lifetime of an activation context.</span></span> <span data-ttu-id="729b5-114">A função funct cria um contexto de ativação, que, em seguida, passa para o destino do objeto, que incrementa a contagem de referência para 2.</span><span class="sxs-lookup"><span data-stu-id="729b5-114">The function Funct creates an activation context, which it then passes to the object Target, which increments the reference count to 2.</span></span> <span data-ttu-id="729b5-115">O funct libera sua referência no contexto de ativação e diminui a contagem de referência de volta para 1.</span><span class="sxs-lookup"><span data-stu-id="729b5-115">Funct then releases its reference on the activation context and decreases the reference count back to 1.</span></span> <span data-ttu-id="729b5-116">Em seguida, o destino tem de liberar sua própria referência quando SetActCtx é chamado novamente ou quando o objeto é destruído.</span><span class="sxs-lookup"><span data-stu-id="729b5-116">Target then owns releasing its own reference when SetActCtx is called again or when the object is destroyed.</span></span>


```C++
#include <windows.h>

class CMyObject 
{
private:
    HANDLE m_hActCtx;
public:
    CMyObject() : m_hActCtx(INVALID_HANDLE_VALUE) { }
    ~CMyObject() 
    { 
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
            m_hActCtx = INVALID_HANDLE_VALUE;
        }
    }
    void SetActCtx(HANDLE hActCtx) 
    {
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
        }
        m_hActCtx = hActCtx;
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            AddRefActCtx(m_hActCtx);
        }
    }
    void DoWorkWithActCtx();
};

void Funct(CMyObject &Target) 
{
    HANDLE hActCtx;
    ACTCTX actctx = { sizeof(ACTCTX) };
    hActCtx = CreateActCtx(&actctx);  //create activation context  
    Target.SetActCtx(hActCtx);    //pass activation context to Target; 
    // actctx now has 1 more reference
    ReleaseActCtx(hActCtx);
}
```



 

 
