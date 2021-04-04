---
title: Atributo pointer_default
description: O atributo \ padrão \ pointername \_ especifica o atributo de ponteiro padrão para todos os ponteiros, exceto os ponteiros de nível superior que aparecem nas listas de parâmetros.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default do atributo MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007402"
---
# <a name="pointer_default-attribute"></a><span data-ttu-id="aa2f3-104">\_atributo padrão de ponteiro</span><span class="sxs-lookup"><span data-stu-id="aa2f3-104">pointer\_default attribute</span></span>

<span data-ttu-id="aa2f3-105">O atributo **\[ \_ padrão \] de ponteiro** especifica o atributo de ponteiro padrão para todos os ponteiros, exceto para os ponteiros de nível superior que aparecem nas listas de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aa2f3-105">The **\[pointer\_default\]** attribute specifies the default pointer attribute for all pointers except top-level pointers that appear in parameter lists.</span></span>

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a><span data-ttu-id="aa2f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa2f3-106">Parameters</span></span>

<span data-ttu-id="aa2f3-107">Este atributo não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aa2f3-107">This attribute has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="aa2f3-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa2f3-108">Examples</span></span>

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="aa2f3-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa2f3-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa2f3-110">**interface**</span><span class="sxs-lookup"><span data-stu-id="aa2f3-110">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="aa2f3-111">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="aa2f3-111">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="aa2f3-112">**Storage**</span><span class="sxs-lookup"><span data-stu-id="aa2f3-112">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="aa2f3-113">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="aa2f3-113">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="aa2f3-114">**ptr**</span><span class="sxs-lookup"><span data-stu-id="aa2f3-114">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="aa2f3-115">**ref**</span><span class="sxs-lookup"><span data-stu-id="aa2f3-115">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="aa2f3-116">**diferente**</span><span class="sxs-lookup"><span data-stu-id="aa2f3-116">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="aa2f3-117">Tipos de ponteiro padrão</span><span class="sxs-lookup"><span data-stu-id="aa2f3-117">Default Pointer Types</span></span>](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 