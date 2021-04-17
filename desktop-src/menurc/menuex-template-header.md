---
title: Estrutura de MENUEX_TEMPLATE_HEADER
description: Define o cabeçalho de um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER de menus de estrutura e outros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105798539"
---
# <a name="menuex_template_header-structure"></a><span data-ttu-id="792af-105">Estrutura de cabeçalho do \_ modelo MENUEX \_</span><span class="sxs-lookup"><span data-stu-id="792af-105">MENUEX\_TEMPLATE\_HEADER structure</span></span>

<span data-ttu-id="792af-106">Define o cabeçalho de um modelo de menu estendido.</span><span class="sxs-lookup"><span data-stu-id="792af-106">Defines the header for an extended menu template.</span></span> <span data-ttu-id="792af-107">Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="792af-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="792af-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="792af-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a><span data-ttu-id="792af-109">Membros</span><span class="sxs-lookup"><span data-stu-id="792af-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="792af-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="792af-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="792af-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="792af-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="792af-112">O número de versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="792af-112">The template version number.</span></span> <span data-ttu-id="792af-113">Esse membro deve ser 1 para modelos de menu estendidos.</span><span class="sxs-lookup"><span data-stu-id="792af-113">This member must be 1 for extended menu templates.</span></span>

</dd> <dt>

<span data-ttu-id="792af-114">**wOffset**</span><span class="sxs-lookup"><span data-stu-id="792af-114">**wOffset**</span></span>
</dt> <dd>

<span data-ttu-id="792af-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="792af-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="792af-116">O deslocamento para a primeira estrutura de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) , em relação ao final deste membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="792af-116">The offset to the first [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structure, relative to the end of this structure member.</span></span> <span data-ttu-id="792af-117">Se a primeira definição de item imediatamente seguir o membro **dwHelpId** , esse membro deverá ser 4.</span><span class="sxs-lookup"><span data-stu-id="792af-117">If the first item definition immediately follows the **dwHelpId** member, this member should be 4.</span></span>

</dd> <dt>

<span data-ttu-id="792af-118">**dwHelpId**</span><span class="sxs-lookup"><span data-stu-id="792af-118">**dwHelpId**</span></span>
</dt> <dd>

<span data-ttu-id="792af-119">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="792af-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="792af-120">O identificador da ajuda da barra de menus.</span><span class="sxs-lookup"><span data-stu-id="792af-120">The help identifier of menu bar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="792af-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="792af-121">Remarks</span></span>

<span data-ttu-id="792af-122">Um modelo de menu estendido consiste em uma estrutura de **\_ \_ cabeçalho de modelo MENUEX** seguida por uma ou mais estruturas de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) contíguas.</span><span class="sxs-lookup"><span data-stu-id="792af-122">An extended menu template consists of a **MENUEX\_TEMPLATE\_HEADER** structure followed by one or more contiguous [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) structures.</span></span> <span data-ttu-id="792af-123">As estruturas de **\_ \_ item de modelo MENUEX** , que são variáveis de comprimento, são alinhadas nos limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="792af-123">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="792af-124">Para criar um menu a partir de um modelo de menu estendido na memória, use a função [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="792af-124">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="792af-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="792af-125">Requirements</span></span>



| <span data-ttu-id="792af-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="792af-126">Requirement</span></span> | <span data-ttu-id="792af-127">Valor</span><span class="sxs-lookup"><span data-stu-id="792af-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="792af-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="792af-128">Minimum supported client</span></span><br/> | <span data-ttu-id="792af-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="792af-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="792af-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="792af-130">Minimum supported server</span></span><br/> | <span data-ttu-id="792af-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="792af-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="792af-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="792af-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="792af-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="792af-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="792af-134">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="792af-134">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="792af-135">**\_item de modelo MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="792af-135">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

<span data-ttu-id="792af-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="792af-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="792af-137">Menus</span><span class="sxs-lookup"><span data-stu-id="792af-137">Menus</span></span>](menus.md)
</dt> </dl>

 

 





