---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46359821dd1f7741f6038ddb2f33cec591aacdf1bf9fc7fd3e6004e9d7601e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034864"
---
# <a name="saferelease"></a>SafeRelease


Muitos dos exemplos de código nesta documentação usam a função a seguir para liberar ponteiros de interface COM.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> Essa função não está definida em um cabeçalho do SDK. Para usar essa função, você deve defini-la em seu próprio código.

 

Essa função libera o ponteiro *ppt* e o define como **nulo**.

Outra opção é usar uma classe de ponteiro inteligente, como **CComPtr**, que é definida no Active Template Library (ATL).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown:: versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
