---
title: Estrutura MENUHEADER
description: Contém informações de versão para o recurso de menu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- Menus de estrutura MENUHEADER e outros recursos
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749346"
---
# <a name="menuheader-structure"></a><span data-ttu-id="405ec-105">Estrutura MENUHEADER</span><span class="sxs-lookup"><span data-stu-id="405ec-105">MENUHEADER structure</span></span>

<span data-ttu-id="405ec-106">Contém informações de versão para o recurso de menu.</span><span class="sxs-lookup"><span data-stu-id="405ec-106">Contains version information for the menu resource.</span></span> <span data-ttu-id="405ec-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="405ec-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="405ec-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="405ec-108">Syntax</span></span>


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a><span data-ttu-id="405ec-109">Membros</span><span class="sxs-lookup"><span data-stu-id="405ec-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="405ec-110">**wVersion**</span><span class="sxs-lookup"><span data-stu-id="405ec-110">**wVersion**</span></span>
</dt> <dd>

<span data-ttu-id="405ec-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="405ec-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="405ec-112">O número de versão do modelo de menu.</span><span class="sxs-lookup"><span data-stu-id="405ec-112">The version number of the menu template.</span></span> <span data-ttu-id="405ec-113">Esse membro deve ser igual a zero para indicar que este é um [**\_ menu de RT**](/windows/desktop/menurc/resource-types) criado com um modelo de menu padrão.</span><span class="sxs-lookup"><span data-stu-id="405ec-113">This member must be equal to zero to indicate that this is an [**RT\_MENU**](/windows/desktop/menurc/resource-types) created with a standard menu template.</span></span>

</dd> <dt>

<span data-ttu-id="405ec-114">**cbHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="405ec-114">**cbHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="405ec-115">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="405ec-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="405ec-116">O tamanho do cabeçalho do modelo de menu.</span><span class="sxs-lookup"><span data-stu-id="405ec-116">The size of the menu template header.</span></span> <span data-ttu-id="405ec-117">Esse valor é zero para os menus que você criar com um modelo de menu padrão.</span><span class="sxs-lookup"><span data-stu-id="405ec-117">This value is zero for menus you create with a standard menu template.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="405ec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="405ec-118">Requirements</span></span>



| <span data-ttu-id="405ec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="405ec-119">Requirement</span></span> | <span data-ttu-id="405ec-120">Valor</span><span class="sxs-lookup"><span data-stu-id="405ec-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="405ec-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="405ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="405ec-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="405ec-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="405ec-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="405ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="405ec-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="405ec-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="405ec-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="405ec-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="405ec-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="405ec-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="405ec-127">**\_cabeçalho do modelo MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="405ec-127">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="405ec-128">**\_item de modelo MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="405ec-128">**MENUEX\_TEMPLATE\_ITEM**</span></span>](menuex-template-item.md)
</dt> <dt>

[<span data-ttu-id="405ec-129">**MENUITEMTEMPLATE**</span><span class="sxs-lookup"><span data-stu-id="405ec-129">**MENUITEMTEMPLATE**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[<span data-ttu-id="405ec-130">**MENUITEMTEMPLATEHEADER**</span><span class="sxs-lookup"><span data-stu-id="405ec-130">**MENUITEMTEMPLATEHEADER**</span></span>](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[<span data-ttu-id="405ec-131">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="405ec-131">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

[<span data-ttu-id="405ec-132">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="405ec-132">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="405ec-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="405ec-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="405ec-134">Recursos</span><span class="sxs-lookup"><span data-stu-id="405ec-134">Resources</span></span>](resources.md)
</dt> </dl>

 

