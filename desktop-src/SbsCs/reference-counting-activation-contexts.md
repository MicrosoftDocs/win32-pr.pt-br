---
description: Os contextos de ativação são objetos contados como referência. Seu aplicativo deve ter uma referência em um contexto de ativação para poder usá-lo.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Contextos de ativação de contagem de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f7806a452dc8b98f824069be0cd584c39f45ad9807a97a11f6f3d7c4929f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141929"
---
# <a name="reference-counting-activation-contexts"></a>Contextos de ativação de contagem de referência

Os contextos de ativação são objetos contados como referência. Seu aplicativo deve ter uma referência em um contexto de ativação para poder usá-lo. As funções da API de contexto de ativação que usam um contexto de ativação podem executar sua própria contagem de referência. Por exemplo, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) aumenta e [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) diminui a contagem de referência. Se, no entanto, o aplicativo passar um contexto de ativação sem usar essas funções, o aplicativo deverá fornecer seu próprio método de contagem de referência.

Quando um aplicativo chama [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), o identificador retornado terá uma contagem de referência de um. Após a conclusão do aplicativo com o contexto de ativação, o identificador deve ser liberado e a contagem de referência diminuiu com a chamada de [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx). Não tente usar [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)ou qualquer outra função de gerenciamento de memória no identificador de contexto de ativação.

O exemplo a seguir mostra um método para manipular a contagem de referência durante o tempo de vida de um contexto de ativação. A função funct cria um contexto de ativação, que, em seguida, passa para o destino do objeto, que incrementa a contagem de referência para 2. O funct libera sua referência no contexto de ativação e diminui a contagem de referência de volta para 1. Em seguida, o destino tem de liberar sua própria referência quando SetActCtx é chamado novamente ou quando o objeto é destruído.


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



 

 
