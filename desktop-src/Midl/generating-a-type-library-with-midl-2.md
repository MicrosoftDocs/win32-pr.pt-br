---
title: Gerando uma biblioteca de tipos com MIDL
description: O elemento de nível superior da sintaxe ODL é a instrução de biblioteca (bloco de biblioteca).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Linguagem IDL da Microsoft MIDL, tarefas, gerando uma biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752061"
---
# <a name="generating-a-type-library-with-midl"></a>Gerando uma biblioteca de tipos com MIDL

O elemento de nível superior da sintaxe ODL é a instrução de biblioteca (bloco de biblioteca). Todas as outras instruções ODL, com exceção dos atributos aplicados à instrução da biblioteca, devem ser definidas dentro do bloco de biblioteca. Quando o compilador MIDL vê um bloco de biblioteca, ele gera uma biblioteca de tipos praticamente da mesma forma que o MkTypLib. Com algumas exceções, descritas em [diferenças entre MIDL e MkTypLib](differences-between-midl-and-mktyplib.md), as instruções dentro do bloco de biblioteca devem seguir a mesma sintaxe do idioma ODL e MkTypLib.

> [!Note]  
> A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL.

 

Você pode aplicar atributos ODL a elementos que são definidos dentro ou fora do bloco de biblioteca. Esses atributos não têm efeito fora do bloco de biblioteca, a menos que o elemento ao qual eles são aplicados seja referenciado dentro do bloco de biblioteca. As instruções dentro do bloco de biblioteca podem fazer referência a um elemento externo usando-o como um tipo base, herdando dele ou referenciando-o em uma linha, conforme mostrado:

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

Se um elemento definido fora do bloco de biblioteca for referenciado dentro do bloco de biblioteca, sua definição será colocada na biblioteca de tipos gerada. O compilador MIDL trata as instruções fora de um bloco de biblioteca como um arquivo IDL típico e analisa essas instruções, como sempre foi feito. Normalmente, isso significa gerar stubs de linguagem C para um aplicativo RPC.

Para obter mais informações sobre a sintaxe geral de um arquivo ODL, consulte [sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax).

 

 