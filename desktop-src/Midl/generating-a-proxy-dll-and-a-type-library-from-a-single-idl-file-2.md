---
title: Gerando uma DLL de proxy e uma biblioteca de tipos de um único arquivo IDL
description: Você pode usar um único arquivo IDL para gerar os stubs de proxy e os arquivos de header para marshaling de código e uma biblioteca de tipos.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- linguagem IDL da Microsoft MIDL , tarefas, gerando uma DLL de proxy e uma biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e7bf2694b791007b0f1da303525217cf55d75d574e083c6d1756bc2784d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384232"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Gerando uma DLL de proxy e uma biblioteca de tipos de um único arquivo IDL

Você pode usar um único arquivo IDL para gerar os stubs de proxy e os arquivos de header para marshaling de código e uma biblioteca de tipos. Faça isso definindo uma interface fora do bloco de biblioteca e, em seguida, referenciando essa interface de dentro do bloco de biblioteca, conforme mostrado neste exemplo:

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

Para obter mais informações, consulte [Marshaling de tipos de dados OLE](marshaling-ole-data-types.md) e [arquivos adicionais necessários para gerar uma biblioteca de tipos](additional-files-required-to-generate-a-type-library-2.md).

 

 




