---
title: Carregando e registrando uma biblioteca de tipos
description: A biblioteca de vínculo dinâmico de automação, Oleaut32.dll, fornece várias funções que você pode chamar para carregar e registrar uma biblioteca de tipos. Chamar LoadTypeLibEx, conforme mostrado no exemplo a seguir, carrega a biblioteca e cria as entradas do registro.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d533225913d6bcfbb74df3ac42bd00b18b00e4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008480"
---
# <a name="loading-and-registering-a-type-library"></a><span data-ttu-id="78516-104">Carregando e registrando uma biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="78516-104">Loading and Registering a Type Library</span></span>

<span data-ttu-id="78516-105">A biblioteca de vínculo dinâmico de automação, Oleaut32.dll, fornece várias funções que você pode chamar para carregar e registrar uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="78516-105">The Automation dynamic link library, Oleaut32.dll, provides several functions that you can call to load and register a type library.</span></span> <span data-ttu-id="78516-106">Chamar [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), conforme mostrado no exemplo a seguir, carrega a biblioteca e cria as entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="78516-106">Calling [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), as shown in the following example, both loads the library and creates the registry entries.</span></span>

## <a name="example"></a><span data-ttu-id="78516-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="78516-107">Example</span></span>

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

 

 