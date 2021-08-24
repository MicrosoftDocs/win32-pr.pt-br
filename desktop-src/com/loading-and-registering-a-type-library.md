---
title: Carregando e registrando uma biblioteca de tipos
description: A biblioteca de vínculo dinâmico de automação, Oleaut32.dll, fornece várias funções que você pode chamar para carregar e registrar uma biblioteca de tipos. Chamar LoadTypeLibEx, conforme mostrado no exemplo a seguir, carrega a biblioteca e cria as entradas do registro.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98ea3a28f3884cbd6a377e45f1b537d169f510fdc4ce9a433dff6e976d9c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854226"
---
# <a name="loading-and-registering-a-type-library"></a>Carregando e registrando uma biblioteca de tipos

A biblioteca de vínculo dinâmico de automação, Oleaut32.dll, fornece várias funções que você pode chamar para carregar e registrar uma biblioteca de tipos. Chamar [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), conforme mostrado no exemplo a seguir, carrega a biblioteca e cria as entradas do registro.

## <a name="example"></a>Exemplo

``` syntax
ITypeLib *pTypeLib;
HRESULT hr;
hr = LoadTypeLibEx("example.tlb", REGKIND_REGISTER, &pTypeLib);
if(SUCCEEDED(hr))
{
    pTypeLib->Release();
} else {
    exit(0); // Handle errors here.
}
```

 

 