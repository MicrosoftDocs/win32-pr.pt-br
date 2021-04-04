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
# <a name="default-pointer-types"></a><span data-ttu-id="63510-104">Tipos de ponteiro padrão</span><span class="sxs-lookup"><span data-stu-id="63510-104">Default Pointer Types</span></span>

<span data-ttu-id="63510-105">Não é necessário que os ponteiros tenham uma descrição explícita do atributo.</span><span class="sxs-lookup"><span data-stu-id="63510-105">Pointers are not required to have an explicit attribute description.</span></span> <span data-ttu-id="63510-106">Quando um atributo explícito não é fornecido, o compilador MIDL usa um atributo de ponteiro padrão.</span><span class="sxs-lookup"><span data-stu-id="63510-106">When an explicit attribute is not provided, the MIDL Compiler uses a default pointer attribute.</span></span>

<span data-ttu-id="63510-107">Os casos padrão para ponteiros não atributo são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="63510-107">The default cases for unattributed pointers are the following:</span></span>

-   <span data-ttu-id="63510-108">Ponteiros de nível superior que aparecem em listas de parâmetros padrão para \[ [](/windows/desktop/Midl/ref) \] ponteiros de referência.</span><span class="sxs-lookup"><span data-stu-id="63510-108">Top-level pointers that appear in parameter lists default to \[[**ref**](/windows/desktop/Midl/ref)\] pointers.</span></span>
-   <span data-ttu-id="63510-109">Todos os outros ponteiros assumem como padrão o tipo especificado pelo \[ atributo [**\_ padrão do ponteiro**](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="63510-109">All other pointers default to the type specified by the \[[**pointer\_default**](/windows/desktop/Midl/pointer-default)\] attribute.</span></span> <span data-ttu-id="63510-110">Quando nenhum \[ **atributo \_ padrão de ponteiro** \] é fornecido, esses ponteiros assumem como padrão o \[ atributo [**exclusivo**](/windows/desktop/Midl/unique) \] quando o compilador MIDL estiver no modo extensões da [Microsoft](microsoft-rpc-binding-handle-extensions.md) ou no \[ atributo [**PTR**](/windows/desktop/Midl/ptr) \] quando o compilador MIDL estiver no modo compatível com DCE.</span><span class="sxs-lookup"><span data-stu-id="63510-110">When no \[**pointer\_default**\] attribute is supplied, these pointers default to the \[ [**unique**](/windows/desktop/Midl/unique) \] attribute when the MIDL compiler is in [Microsoft Extensions](microsoft-rpc-binding-handle-extensions.md) mode or the \[[**ptr**](/windows/desktop/Midl/ptr)\] attribute when the MIDL compiler is in DCE-compatible mode.</span></span>

<span data-ttu-id="63510-111">Quando um procedimento remoto retorna um ponteiro, o valor de retorno deve ser um \[ ponteiro [**exclusivo**](/windows/desktop/Midl/unique) \] ou completo ( \[ [**PTR**](/windows/desktop/Midl/ptr) \] ).</span><span class="sxs-lookup"><span data-stu-id="63510-111">When a remote procedure returns a pointer, the return value must be a \[ [**unique**](/windows/desktop/Midl/unique) \] or full (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) pointer.</span></span>

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

### <a name="remarks"></a><span data-ttu-id="63510-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="63510-112">Remarks</span></span>

<span data-ttu-id="63510-113">Para garantir um comportamento de atributo de ponteiro não ambíguo, sempre use atributos de ponteiro explícitos ao definir um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="63510-113">To ensure unambiguous pointer-attribute behavior, always use explicit pointer attributes when defining a pointer.</span></span>

<span data-ttu-id="63510-114">É recomendável que **\[** PTR **\]** seja usado somente quando o alias do ponteiro for necessário.</span><span class="sxs-lookup"><span data-stu-id="63510-114">It is recommended that **\[** ptr **\]** is used only when pointer aliasing is required.</span></span>

 

 