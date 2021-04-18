---
description: Representa informações sobre um quadro na pilha de chamadas.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura CallStackFrame
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105813456"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span data-ttu-id="739de-103"><span id="vspixengine.callstackframe"></span>Estrutura CallStackFrame</span><span class="sxs-lookup"><span data-stu-id="739de-103"><span id="vspixengine.callstackframe"></span>CallStackFrame structure</span></span>

<span data-ttu-id="739de-104">Representa informações sobre um quadro na pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="739de-104">Represents information about a frame on the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="739de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="739de-105">Syntax</span></span>


```C++
} CallStackFrame;
```

## <a name="members"></a><span data-ttu-id="739de-106">Membros</span><span class="sxs-lookup"><span data-stu-id="739de-106">Members</span></span>

<span data-ttu-id="739de-107">**functionName**</span><span class="sxs-lookup"><span data-stu-id="739de-107">**functionName**</span></span>  
<span data-ttu-id="739de-108">Uma cadeia de caracteres COM que contém o nome da função associada.</span><span class="sxs-lookup"><span data-stu-id="739de-108">A COM string containing the name of the associated function.</span></span>

<span data-ttu-id="739de-109">**sourceFile**</span><span class="sxs-lookup"><span data-stu-id="739de-109">**sourceFile**</span></span>  
<span data-ttu-id="739de-110">Uma cadeia de caracteres COM que contém o caminho de arquivo de origem associado.</span><span class="sxs-lookup"><span data-stu-id="739de-110">A COM string containing the filepath of the associated source file.</span></span>

<span data-ttu-id="739de-111">**moduleName**</span><span class="sxs-lookup"><span data-stu-id="739de-111">**moduleName**</span></span>  
<span data-ttu-id="739de-112">Uma cadeia de caracteres COM que contém o nome do módulo de código associado.</span><span class="sxs-lookup"><span data-stu-id="739de-112">A COM string containing the name of the associated code module.</span></span>

<span data-ttu-id="739de-113">**lineNumber**</span><span class="sxs-lookup"><span data-stu-id="739de-113">**lineNumber**</span></span>  
<span data-ttu-id="739de-114">O número da linha associada.</span><span class="sxs-lookup"><span data-stu-id="739de-114">The associated line number.</span></span>

## <a name="requirements"></a><span data-ttu-id="739de-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="739de-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="739de-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="739de-116">Header</span></span></p></td><td><span data-ttu-id="739de-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="739de-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



