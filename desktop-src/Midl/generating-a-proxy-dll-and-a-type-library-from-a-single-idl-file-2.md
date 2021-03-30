---
title: Gerando uma DLL de proxy e uma biblioteca de tipos de um único arquivo IDL
description: Você pode usar um único arquivo IDL para gerar os stubs de proxy e os arquivos de cabeçalho para o código de marshaling e uma biblioteca de tipos.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Linguagem IDL da Microsoft MIDL, tarefas, gerando uma DLL de proxy e uma biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005892"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a><span data-ttu-id="e8631-104">Gerando uma DLL de proxy e uma biblioteca de tipos de um único arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="e8631-104">Generating a Proxy DLL and a Type Library from a Single IDL File</span></span>

<span data-ttu-id="e8631-105">Você pode usar um único arquivo IDL para gerar os stubs de proxy e os arquivos de cabeçalho para o código de marshaling e uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="e8631-105">You can use a single IDL file to generate both the proxy stubs and header files for marshaling code, and a type library.</span></span> <span data-ttu-id="e8631-106">Você faz isso definindo uma interface fora do bloco de biblioteca e, em seguida, referenciando essa interface de dentro do bloco de biblioteca, conforme mostrado neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="e8631-106">You do this by defining an interface outside the library block and then referencing that interface from inside the library block, as shown in this example:</span></span>

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

<span data-ttu-id="e8631-107">Para obter mais informações, consulte [empacotamento de tipos de dados OLE](marshaling-ole-data-types.md) e [arquivos adicionais necessários para gerar uma biblioteca de tipos](additional-files-required-to-generate-a-type-library-2.md).</span><span class="sxs-lookup"><span data-stu-id="e8631-107">For more information, see [Marshaling OLE Data Types](marshaling-ole-data-types.md) and [Additional Files Required To Generate a Type Library](additional-files-required-to-generate-a-type-library-2.md).</span></span>

 

 




