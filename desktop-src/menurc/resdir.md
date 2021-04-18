---
title: Estrutura RESDIR
description: Contém informações sobre um ícone individual ou componente de cursor em um grupo de recursos. Há uma estrutura RESDIR para cada componente de grupo. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menus de estrutura RESDIR e outros recursos
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105785027"
---
# <a name="resdir-structure"></a><span data-ttu-id="adfee-106">Estrutura RESDIR</span><span class="sxs-lookup"><span data-stu-id="adfee-106">RESDIR structure</span></span>

<span data-ttu-id="adfee-107">Contém informações sobre um ícone individual ou componente de cursor em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="adfee-107">Contains information about an individual icon or cursor component in a resource group.</span></span> <span data-ttu-id="adfee-108">Há uma estrutura **RESDIR** para cada componente de grupo.</span><span class="sxs-lookup"><span data-stu-id="adfee-108">There is one **RESDIR** structure for each group component.</span></span> <span data-ttu-id="adfee-109">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="adfee-109">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="adfee-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adfee-110">Syntax</span></span>


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a><span data-ttu-id="adfee-111">Membros</span><span class="sxs-lookup"><span data-stu-id="adfee-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="adfee-112">**Ícone**</span><span class="sxs-lookup"><span data-stu-id="adfee-112">**Icon**</span></span>
</dt> <dd>

<span data-ttu-id="adfee-113">Tipo: **[ **ICONRESDIR**](iconresdir.md)**</span><span class="sxs-lookup"><span data-stu-id="adfee-113">Type: **[**ICONRESDIR**](iconresdir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adfee-114">A largura, a altura e a contagem de cores do ícone indicado.</span><span class="sxs-lookup"><span data-stu-id="adfee-114">The width, height, and color count of the indicated icon.</span></span>

</dd> <dt>

<span data-ttu-id="adfee-115">**Cursor**</span><span class="sxs-lookup"><span data-stu-id="adfee-115">**Cursor**</span></span>
</dt> <dd>

<span data-ttu-id="adfee-116">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="adfee-116">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adfee-117">A largura e a altura do cursor indicado.</span><span class="sxs-lookup"><span data-stu-id="adfee-117">The width and height of the indicated cursor.</span></span>

</dd> <dt>

<span data-ttu-id="adfee-118">**Aviões**</span><span class="sxs-lookup"><span data-stu-id="adfee-118">**Planes**</span></span>
</dt> <dd>

<span data-ttu-id="adfee-119">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="adfee-119">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adfee-120">O número de planos de cores no bitmap do ícone ou do cursor.</span><span class="sxs-lookup"><span data-stu-id="adfee-120">The number of color planes in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="adfee-121">**BitCount**</span><span class="sxs-lookup"><span data-stu-id="adfee-121">**BitCount**</span></span>
</dt> <dd>

<span data-ttu-id="adfee-122">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="adfee-122">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adfee-123">O número de bits por pixel no bitmap do ícone ou do cursor.</span><span class="sxs-lookup"><span data-stu-id="adfee-123">The number of bits per pixel in the icon or cursor bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="adfee-124">**BytesInRes**</span><span class="sxs-lookup"><span data-stu-id="adfee-124">**BytesInRes**</span></span>
</dt> <dd>

<span data-ttu-id="adfee-125">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="adfee-125">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adfee-126">O tamanho do recurso, em bytes.</span><span class="sxs-lookup"><span data-stu-id="adfee-126">The size of the resource, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="adfee-127">**IconCursorId**</span><span class="sxs-lookup"><span data-stu-id="adfee-127">**IconCursorId**</span></span>
</dt> <dd>

<span data-ttu-id="adfee-128">Tipo: **[ **CURSORDIR**](cursordir.md)**</span><span class="sxs-lookup"><span data-stu-id="adfee-128">Type: **[**CURSORDIR**](cursordir.md)**</span></span>

</dd> <dd>

<span data-ttu-id="adfee-129">O ícone ou cursor com um identificador ordinal exclusivo.</span><span class="sxs-lookup"><span data-stu-id="adfee-129">The icon or cursor with a unique ordinal identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adfee-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="adfee-130">Remarks</span></span>

<span data-ttu-id="adfee-131">Uma ou mais estruturas **RESDIR** seguem imediatamente a estrutura [**NEWHEADER**](newheader.md) no arquivo. res.</span><span class="sxs-lookup"><span data-stu-id="adfee-131">One or more **RESDIR** structures immediately follow the [**NEWHEADER**](newheader.md) structure in the .res file.</span></span> <span data-ttu-id="adfee-132">O membro **ResCount** da estrutura **NEWHEADER** especifica o número de estruturas **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="adfee-132">The **ResCount** member of the **NEWHEADER** structure specifies the number of **RESDIR** structures.</span></span> <span data-ttu-id="adfee-133">Observe que a estrutura **RESDIR** consiste em uma estrutura [**ICONRESDIR**](iconresdir.md) ou uma estrutura [**CURSORDIR**](cursordir.md) seguida pelos membros **aviões**, **BitCount**, **BytesInRes** e **IconCursorId** .</span><span class="sxs-lookup"><span data-stu-id="adfee-133">Note that the **RESDIR** structure consists of either an [**ICONRESDIR**](iconresdir.md) structure or a [**CURSORDIR**](cursordir.md) structure followed by the **Planes**, **BitCount**, **BytesInRes**, and **IconCursorId** members.</span></span> <span data-ttu-id="adfee-134">Se a estrutura **RESDIR** contiver informações sobre um cursor, as duas **primeiras palavras** do compilador de recursos gravará no recurso de [ \_ cursor de RT](/windows/desktop/menurc/resource-types) são os membros **xHotSpot** e **yHotSpot** da estrutura [**LOCALHEADER**](localheader.md) .</span><span class="sxs-lookup"><span data-stu-id="adfee-134">If the **RESDIR** structure contains information about a cursor, the first two **WORD** s the resource compiler writes to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource are the **xHotSpot** and **yHotSpot** members of the [**LOCALHEADER**](localheader.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="adfee-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adfee-135">Requirements</span></span>



| <span data-ttu-id="adfee-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="adfee-136">Requirement</span></span> | <span data-ttu-id="adfee-137">Valor</span><span class="sxs-lookup"><span data-stu-id="adfee-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="adfee-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adfee-138">Minimum supported client</span></span><br/> | <span data-ttu-id="adfee-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="adfee-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="adfee-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adfee-140">Minimum supported server</span></span><br/> | <span data-ttu-id="adfee-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="adfee-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="adfee-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="adfee-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="adfee-143">**Referência**</span><span class="sxs-lookup"><span data-stu-id="adfee-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="adfee-144">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="adfee-144">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="adfee-145">**ICONRESDIR**</span><span class="sxs-lookup"><span data-stu-id="adfee-145">**ICONRESDIR**</span></span>](iconresdir.md)
</dt> <dt>

[<span data-ttu-id="adfee-146">**LOCALHEADER**</span><span class="sxs-lookup"><span data-stu-id="adfee-146">**LOCALHEADER**</span></span>](localheader.md)
</dt> <dt>

[<span data-ttu-id="adfee-147">**NEWHEADER**</span><span class="sxs-lookup"><span data-stu-id="adfee-147">**NEWHEADER**</span></span>](newheader.md)
</dt> <dt>

<span data-ttu-id="adfee-148">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="adfee-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="adfee-149">Recursos</span><span class="sxs-lookup"><span data-stu-id="adfee-149">Resources</span></span>](resources.md)
</dt> </dl>

 

