---
title: Estrutura NORMALMENUITEM
description: Contém informações sobre cada item em um recurso de menu que não abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- Menus de estrutura NORMALMENUITEM e outros recursos
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294787"
---
# <a name="normalmenuitem-structure"></a><span data-ttu-id="112ac-105">Estrutura NORMALMENUITEM</span><span class="sxs-lookup"><span data-stu-id="112ac-105">NORMALMENUITEM structure</span></span>

<span data-ttu-id="112ac-106">Contém informações sobre cada item em um recurso de menu que não abre um menu ou um submenu.</span><span class="sxs-lookup"><span data-stu-id="112ac-106">Contains information about each item in a menu resource that does not open a menu or a submenu.</span></span> <span data-ttu-id="112ac-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="112ac-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="112ac-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="112ac-108">Syntax</span></span>


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a><span data-ttu-id="112ac-109">Membros</span><span class="sxs-lookup"><span data-stu-id="112ac-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="112ac-110">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="112ac-110">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="112ac-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="112ac-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="112ac-112">O tipo de item de menu.</span><span class="sxs-lookup"><span data-stu-id="112ac-112">The type of menu item.</span></span> <span data-ttu-id="112ac-113">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="112ac-113">This member can be one of the following values.</span></span>



| <span data-ttu-id="112ac-114">Valor</span><span class="sxs-lookup"><span data-stu-id="112ac-114">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="112ac-115">Significado</span><span class="sxs-lookup"><span data-stu-id="112ac-115">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="112ac-116"><dt>**Mfr \_ ENCERRAR**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="112ac-116"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="112ac-117">O item de menu é o último neste submenu ou recurso de menu; Esse sinalizador é usado internamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="112ac-117">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="112ac-118"><dt>**Mfr \_ POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="112ac-118"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="112ac-119">O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="112ac-119">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/>                    |



 

</dd> <dt>

<span data-ttu-id="112ac-120">**menuText**</span><span class="sxs-lookup"><span data-stu-id="112ac-120">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="112ac-121">Tipo: **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="112ac-121">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="112ac-122">Uma cadeia de caracteres Unicode terminada em nulo que contém o texto para este item de menu.</span><span class="sxs-lookup"><span data-stu-id="112ac-122">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="112ac-123">Não há nenhum limite fixo para o tamanho dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="112ac-123">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="112ac-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="112ac-124">Remarks</span></span>

<span data-ttu-id="112ac-125">Há uma estrutura **NORMALMENUITEM** para cada item de menu que não abre um menu ou um submenu.</span><span class="sxs-lookup"><span data-stu-id="112ac-125">There is one **NORMALMENUITEM** structure for each menu item that does not open a menu or a submenu.</span></span> <span data-ttu-id="112ac-126">Indique o último item de menu em um menu definindo o membro **resInfo** como **mfr \_ end**.</span><span class="sxs-lookup"><span data-stu-id="112ac-126">Indicate the last menu item on a menu by setting the **resInfo** member to **MFR\_END**.</span></span>

<span data-ttu-id="112ac-127">Um separador de menu é um tipo especial de item de menu que está inativo, mas aparece como uma barra de divisão entre dois itens de menu ativos.</span><span class="sxs-lookup"><span data-stu-id="112ac-127">A menu separator is a special type of menu item that is inactive but appears as a dividing bar between two active menu items.</span></span> <span data-ttu-id="112ac-128">Indique um separador de menu deixando o membro **menuText** vazio.</span><span class="sxs-lookup"><span data-stu-id="112ac-128">Indicate a menu separator by leaving the **menuText** member empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="112ac-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="112ac-129">Requirements</span></span>



| <span data-ttu-id="112ac-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="112ac-130">Requirement</span></span> | <span data-ttu-id="112ac-131">Valor</span><span class="sxs-lookup"><span data-stu-id="112ac-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="112ac-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="112ac-132">Minimum supported client</span></span><br/> | <span data-ttu-id="112ac-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="112ac-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="112ac-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="112ac-134">Minimum supported server</span></span><br/> | <span data-ttu-id="112ac-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="112ac-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="112ac-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="112ac-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="112ac-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="112ac-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="112ac-138">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="112ac-138">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="112ac-139">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="112ac-139">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="112ac-140">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="112ac-140">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="112ac-141">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="112ac-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="112ac-142">Recursos</span><span class="sxs-lookup"><span data-stu-id="112ac-142">Resources</span></span>](resources.md)
</dt> </dl>

 

 





