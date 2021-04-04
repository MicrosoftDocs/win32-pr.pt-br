---
title: Tipos de ponteiro padrão
description: Não é necessário que os ponteiros tenham uma descrição explícita do atributo. Quando um atributo explícito não é fornecido, o compilador MIDL usa um atributo de ponteiro padrão.
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007863"
---
# <a name="default-pointer-types"></a>Tipos de ponteiro padrão

Não é necessário que os ponteiros tenham uma descrição explícita do atributo. Quando um atributo explícito não é fornecido, o compilador MIDL usa um atributo de ponteiro padrão.

Os casos padrão para ponteiros não atributo são os seguintes:

-   Ponteiros de nível superior que aparecem em listas de parâmetros padrão para \[ [](/windows/desktop/Midl/ref) \] ponteiros de referência.
-   Todos os outros ponteiros assumem como padrão o tipo especificado pelo \[ atributo [**\_ padrão do ponteiro**](/windows/desktop/Midl/pointer-default) \] . Quando nenhum \[ **atributo \_ padrão de ponteiro** \] é fornecido, esses ponteiros assumem como padrão o \[ atributo [**exclusivo**](/windows/desktop/Midl/unique) \] quando o compilador MIDL estiver no modo extensões da [Microsoft](microsoft-rpc-binding-handle-extensions.md) ou no \[ atributo [**PTR**](/windows/desktop/Midl/ptr) \] quando o compilador MIDL estiver no modo compatível com DCE.

Quando um procedimento remoto retorna um ponteiro, o valor de retorno deve ser um \[ ponteiro [**exclusivo**](/windows/desktop/Midl/unique) \] ou completo ( \[ [**PTR**](/windows/desktop/Midl/ptr) \] ).

``` syntax
/* IDL file compiled without /osf */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0),
  pointer_default(ptr)
]
interface MyInterface
{
    typedef long *PLONG;
  
    struct MyCircularList {
        struct MyCircularList *pRight;
        struct MyCircularList *pLeft;
        long Data;
    };

    void Foo1( [in] PLONG p );                   // p is ref
 
    void Foo2( [in] struct MyCircularList *p );  // p is ref, p->pRight and p->pLeft is ptr

    struct MyCircularList *Foo3( void );         // returned pointer is ptr.    
}

[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea46),
  version(1.0)
]
interface MyInterface2
{
    struct MySingleList
       {
       struct MySingleList *pNext;
       long Data;
       };
    void Foo4( [in] struct MySingleList *p );  // p is ref, p->pNext is unique

    struct MySingleList *Foo5( void );         // returned pointer is unique.    
}
```

### <a name="remarks"></a>Comentários

Para garantir um comportamento de atributo de ponteiro não ambíguo, sempre use atributos de ponteiro explícitos ao definir um ponteiro.

É recomendável que **\[** PTR **\]** seja usado somente quando o alias do ponteiro for necessário.

 

 