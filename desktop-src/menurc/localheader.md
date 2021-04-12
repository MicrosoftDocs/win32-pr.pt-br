---
title: Estrutura LOCALHEADER
description: Contém as coordenadas x e y de um hotspot associado ao cursor identificado por uma estrutura RESDIR. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menus de estrutura LOCALHEADER e outros recursos
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369711"
---
# <a name="localheader-structure"></a><span data-ttu-id="c09ad-105">Estrutura LOCALHEADER</span><span class="sxs-lookup"><span data-stu-id="c09ad-105">LOCALHEADER structure</span></span>

<span data-ttu-id="c09ad-106">Contém as coordenadas x e y de um hotspot associado ao cursor identificado por uma estrutura [**RESDIR**](resdir.md) .</span><span class="sxs-lookup"><span data-stu-id="c09ad-106">Contains the x- and y-coordinates of a hotspot associated with the cursor identified by a [**RESDIR**](resdir.md) structure.</span></span> <span data-ttu-id="c09ad-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="c09ad-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c09ad-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c09ad-108">Syntax</span></span>


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a><span data-ttu-id="c09ad-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c09ad-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c09ad-110">**xHotSpot**</span><span class="sxs-lookup"><span data-stu-id="c09ad-110">**xHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="c09ad-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c09ad-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c09ad-112">A coordenada x do ponto de acesso do cursor, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c09ad-112">The x-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c09ad-113">**yHotSpot**</span><span class="sxs-lookup"><span data-stu-id="c09ad-113">**yHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="c09ad-114">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="c09ad-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c09ad-115">A coordenada y do ponto de acesso do cursor, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c09ad-115">The y-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c09ad-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c09ad-116">Remarks</span></span>

<span data-ttu-id="c09ad-117">A estrutura **LOCALHEADER** é o primeiro dado gravado no recurso [de \_ cursor de RT](/windows/desktop/menurc/resource-types) se uma estrutura [**RESDIR**](resdir.md) contém informações sobre um cursor.</span><span class="sxs-lookup"><span data-stu-id="c09ad-117">The **LOCALHEADER** structure is the first data written to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource if a [**RESDIR**](resdir.md) structure contains information about a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="c09ad-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c09ad-118">Requirements</span></span>



| <span data-ttu-id="c09ad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c09ad-119">Requirement</span></span> | <span data-ttu-id="c09ad-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c09ad-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c09ad-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c09ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c09ad-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c09ad-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c09ad-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c09ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c09ad-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c09ad-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c09ad-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c09ad-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c09ad-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c09ad-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c09ad-127">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="c09ad-127">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="c09ad-128">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="c09ad-128">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="c09ad-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c09ad-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c09ad-130">Recursos</span><span class="sxs-lookup"><span data-stu-id="c09ad-130">Resources</span></span>](resources.md)
</dt> </dl>

 

