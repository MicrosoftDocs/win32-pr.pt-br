---
description: Declara um objeto para ser uma constante de seleção, para evitar recargas redundantes desse objeto se ele for usado (e declarado) em vários locais na biblioteca DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Macro XMGLOBALCONST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782567"
---
# <a name="xmglobalconst-macro"></a><span data-ttu-id="e0263-103">Macro XMGLOBALCONST</span><span class="sxs-lookup"><span data-stu-id="e0263-103">XMGLOBALCONST macro</span></span>

<span data-ttu-id="e0263-104">Declara um objeto para ser uma constante de *seleção* , para evitar recargas redundantes desse objeto se ele for usado (e declarado) em vários locais na biblioteca DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="e0263-104">Declares an object to be a *pick-any* constant, to avoid redundant reloads of that object if it is used (and declared) in multiple places in the DirectXMath Library.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0263-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0263-105">Syntax</span></span>

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a><span data-ttu-id="e0263-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0263-106">Remarks</span></span>

<span data-ttu-id="e0263-107">O uso de XMGLOBALCONST permite a especificação de constantes globais.</span><span class="sxs-lookup"><span data-stu-id="e0263-107">Using XMGLOBALCONST permits the specification of global constants.</span></span> <span data-ttu-id="e0263-108">Isso ajuda a reduzir o tamanho do segmento de dados de um aplicativo, evitar a criação e destruição de objetos redundantes e reduzir as operações de carga e armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e0263-108">This helps to reduce the size of an application's data segment, avoid redundant object creation and destruction, and reduce load and store operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0263-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0263-109">Requirements</span></span>

<span data-ttu-id="e0263-110">**Cabeçalho:** Declarado em DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="e0263-110">**Header:** Declared in DirectXMath.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0263-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0263-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0263-112">Macros da biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="e0263-112">DirectXMath Library Macros</span></span>](ovw-xnamath-reference-macros.md)
</dt> <dt>

[<span data-ttu-id="e0263-113">Constantes globais na biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="e0263-113">Global Constants in the DirectXMath Library</span></span>](pg-xnamath-internals.md)
</dt> <dt>

<span data-ttu-id="e0263-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="e0263-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span></span>
</dt> <dt>

<span data-ttu-id="e0263-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="e0263-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span></span>
</dt> </dl>

 

 
