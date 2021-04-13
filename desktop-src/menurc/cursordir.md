---
title: Estrutura CURSORDIR
description: Contém as dimensões de uma imagem de cursor individual em um grupo de recursos. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menus de estrutura CURSORDIR e outros recursos
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369850"
---
# <a name="cursordir-structure"></a><span data-ttu-id="eb968-105">Estrutura CURSORDIR</span><span class="sxs-lookup"><span data-stu-id="eb968-105">CURSORDIR structure</span></span>

<span data-ttu-id="eb968-106">Contém as dimensões de uma imagem de cursor individual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb968-106">Contains the dimensions of an individual cursor image in a resource group.</span></span> <span data-ttu-id="eb968-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="eb968-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb968-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb968-108">Syntax</span></span>


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a><span data-ttu-id="eb968-109">Membros</span><span class="sxs-lookup"><span data-stu-id="eb968-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb968-110">**Largura**</span><span class="sxs-lookup"><span data-stu-id="eb968-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="eb968-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="eb968-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="eb968-112">A largura do cursor, em pixels.</span><span class="sxs-lookup"><span data-stu-id="eb968-112">The width of the cursor, in pixels.</span></span> <span data-ttu-id="eb968-113">Os valores aceitáveis são 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="eb968-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="eb968-114">**Altura**</span><span class="sxs-lookup"><span data-stu-id="eb968-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="eb968-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="eb968-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="eb968-116">A altura do cursor, em pixels.</span><span class="sxs-lookup"><span data-stu-id="eb968-116">The height of the cursor, in pixels.</span></span> <span data-ttu-id="eb968-117">Os valores aceitáveis são 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="eb968-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb968-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb968-118">Remarks</span></span>

<span data-ttu-id="eb968-119">A estrutura **CURSORDIR** é passada na estrutura [**RESDIR**](resdir.md) se a estrutura **RESDIR** descreve um cursor.</span><span class="sxs-lookup"><span data-stu-id="eb968-119">The **CURSORDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb968-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb968-120">Requirements</span></span>



| <span data-ttu-id="eb968-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb968-121">Requirement</span></span> | <span data-ttu-id="eb968-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eb968-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="eb968-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb968-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eb968-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb968-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="eb968-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb968-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eb968-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb968-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="eb968-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb968-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb968-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="eb968-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eb968-129">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="eb968-129">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="eb968-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="eb968-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eb968-131">Recursos</span><span class="sxs-lookup"><span data-stu-id="eb968-131">Resources</span></span>](resources.md)
</dt> </dl>

 

 





