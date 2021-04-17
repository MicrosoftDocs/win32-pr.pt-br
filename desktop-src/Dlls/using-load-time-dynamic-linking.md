---
description: Depois de criar uma DLL, você pode usar as funções que ele define em um aplicativo. Veja a seguir um aplicativo de console simples que usa a função mycolocar exportada de Myputs.dll (consulte criando uma biblioteca de Dynamic-Link simples).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Usando Load-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783313"
---
# <a name="using-load-time-dynamic-linking"></a>Usando Load-Time vinculação dinâmica

Depois de criar uma DLL, você pode usar as funções que ele define em um aplicativo. Veja a seguir um aplicativo de console simples que usa a função mycolocar exportada de Myputs.dll (consulte [criando uma biblioteca de Dynamic-Link simples](creating-a-simple-dynamic-link-library.md)).

Como este exemplo chama a função DLL explicitamente, o módulo para o aplicativo deve ser vinculado à biblioteca de importação mycoloque. lib. Para obter mais informações sobre como criar DLLs, consulte a documentação incluída com suas ferramentas de desenvolvimento.


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vinculação dinâmica em tempo de carregamento](load-time-dynamic-linking.md)
</dt> </dl>

 

 



