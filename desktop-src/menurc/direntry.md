---
title: Estrutura de conalugação
description: Contém um ordinal exclusivo que identifica uma fonte individual no grupo de recursos de fonte. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menus de estrutura de dialuguel e outros recursos
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644782"
---
# <a name="direntry-structure"></a><span data-ttu-id="a7c12-105">Estrutura de conalugação</span><span class="sxs-lookup"><span data-stu-id="a7c12-105">DIRENTRY structure</span></span>

<span data-ttu-id="a7c12-106">Contém um ordinal exclusivo que identifica uma fonte individual no grupo de recursos de fonte.</span><span class="sxs-lookup"><span data-stu-id="a7c12-106">Contains a unique ordinal that identifies an individual font in the font resource group.</span></span> <span data-ttu-id="a7c12-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="a7c12-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c12-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7c12-108">Syntax</span></span>


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a><span data-ttu-id="a7c12-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a7c12-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a7c12-110">**fontOrdinal**</span><span class="sxs-lookup"><span data-stu-id="a7c12-110">**fontOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="a7c12-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="a7c12-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a7c12-112">Um identificador ordinal exclusivo para uma fonte individual em um grupo de recursos de fonte.</span><span class="sxs-lookup"><span data-stu-id="a7c12-112">A unique ordinal identifier for an individual font in a font resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7c12-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7c12-113">Remarks</span></span>

<span data-ttu-id="a7c12-114">A estrutura [**FONTDIRENTRY**](fontdirentry.md) para a fonte especificada segue diretamente a estrutura de **dialuguel** para essa fonte.</span><span class="sxs-lookup"><span data-stu-id="a7c12-114">The [**FONTDIRENTRY**](fontdirentry.md) structure for the specified font directly follows the **DIRENTRY** structure for that font.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c12-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7c12-115">Requirements</span></span>



| <span data-ttu-id="a7c12-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c12-116">Requirement</span></span> | <span data-ttu-id="a7c12-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a7c12-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a7c12-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7c12-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7c12-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a7c12-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a7c12-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7c12-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7c12-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a7c12-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a7c12-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a7c12-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7c12-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a7c12-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a7c12-124">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="a7c12-124">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

[<span data-ttu-id="a7c12-125">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="a7c12-125">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="a7c12-126">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a7c12-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7c12-127">Recursos</span><span class="sxs-lookup"><span data-stu-id="a7c12-127">Resources</span></span>](resources.md)
</dt> </dl>

 

 





