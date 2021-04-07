---
title: Estrutura NEWHEADER
description: Contém o número de componentes de ícone ou cursor em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menus de estrutura NEWHEADER e outros recursos
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918125"
---
# <a name="newheader-structure"></a><span data-ttu-id="55ee2-105">Estrutura NEWHEADER</span><span class="sxs-lookup"><span data-stu-id="55ee2-105">NEWHEADER structure</span></span>

<span data-ttu-id="55ee2-106">Contém o número de componentes de ícone ou cursor em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55ee2-106">Contains the number of icon or cursor components in a resource group.</span></span> <span data-ttu-id="55ee2-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="55ee2-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ee2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55ee2-108">Syntax</span></span>


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a><span data-ttu-id="55ee2-109">Membros</span><span class="sxs-lookup"><span data-stu-id="55ee2-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="55ee2-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="55ee2-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="55ee2-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="55ee2-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="55ee2-112">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="55ee2-112">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="55ee2-113">**ResType**</span><span class="sxs-lookup"><span data-stu-id="55ee2-113">**ResType**</span></span>
</dt> <dd>

<span data-ttu-id="55ee2-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="55ee2-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="55ee2-115">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="55ee2-115">The resource type.</span></span> <span data-ttu-id="55ee2-116">Esse membro deve ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="55ee2-116">This member must have one of the following values.</span></span>



| <span data-ttu-id="55ee2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="55ee2-117">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="55ee2-118">Significado</span><span class="sxs-lookup"><span data-stu-id="55ee2-118">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <span data-ttu-id="55ee2-119"><dt>**Res \_ CURSOR**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="55ee2-119"><dt>**RES\_CURSOR**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="55ee2-120">Tipo de recurso de cursor.</span><span class="sxs-lookup"><span data-stu-id="55ee2-120">Cursor resource type.</span></span><br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <span data-ttu-id="55ee2-121"><dt>**Res \_ ÍCONE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="55ee2-121"><dt>**RES\_ICON**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="55ee2-122">Tipo de recurso de ícone.</span><span class="sxs-lookup"><span data-stu-id="55ee2-122">Icon resource type.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="55ee2-123">**ResCount**</span><span class="sxs-lookup"><span data-stu-id="55ee2-123">**ResCount**</span></span>
</dt> <dd>

<span data-ttu-id="55ee2-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="55ee2-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="55ee2-125">O número de componentes de ícone ou cursor no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55ee2-125">The number of icon or cursor components in the resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55ee2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="55ee2-126">Remarks</span></span>

<span data-ttu-id="55ee2-127">Uma ou mais estruturas [**RESDIR**](resdir.md) seguem imediatamente a estrutura **NEWHEADER** no arquivo. res.</span><span class="sxs-lookup"><span data-stu-id="55ee2-127">One or more [**RESDIR**](resdir.md) structures immediately follow the **NEWHEADER** structure in the .res file.</span></span> <span data-ttu-id="55ee2-128">O membro **ResCount** especifica o número de estruturas **RESDIR** .</span><span class="sxs-lookup"><span data-stu-id="55ee2-128">The **ResCount** member specifies the number of **RESDIR** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ee2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55ee2-129">Requirements</span></span>



| <span data-ttu-id="55ee2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ee2-130">Requirement</span></span> | <span data-ttu-id="55ee2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="55ee2-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="55ee2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55ee2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="55ee2-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55ee2-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="55ee2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55ee2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="55ee2-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="55ee2-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="55ee2-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="55ee2-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="55ee2-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="55ee2-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55ee2-138">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="55ee2-138">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="55ee2-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="55ee2-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55ee2-140">Recursos</span><span class="sxs-lookup"><span data-stu-id="55ee2-140">Resources</span></span>](resources.md)
</dt> </dl>

 

 





