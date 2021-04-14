---
title: Estrutura de MENUEX_TEMPLATE_ITEM
description: Define um item de menu em um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM de menus de estrutura e outros recursos
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499681"
---
# <a name="menuex_template_item-structure"></a><span data-ttu-id="0c3d7-105">Estrutura de item de \_ modelo MENUEX \_</span><span class="sxs-lookup"><span data-stu-id="0c3d7-105">MENUEX\_TEMPLATE\_ITEM structure</span></span>

<span data-ttu-id="0c3d7-106">Define um item de menu em um modelo de menu estendido.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-106">Defines a menu item in an extended menu template.</span></span> <span data-ttu-id="0c3d7-107">Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c3d7-108">Syntax</span></span>

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a><span data-ttu-id="0c3d7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="0c3d7-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c3d7-110">**dwType**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-110">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="0c3d7-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0c3d7-112">O tipo de item de menu.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-112">The menu item type.</span></span> <span data-ttu-id="0c3d7-113">Esse membro pode ser uma combinação dos valores de tipo (começando com MFT) listados com a estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="0c3d7-113">This member can be a combination of the type (beginning with MFT) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d7-114">**dwState**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-114">**dwState**</span></span>
</dt> <dd>

<span data-ttu-id="0c3d7-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0c3d7-116">O estado do item de menu.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-116">The menu item state.</span></span> <span data-ttu-id="0c3d7-117">Esse membro pode ser uma combinação dos valores de estado (começando com MFS) listados com a estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="0c3d7-117">This member can be a combination of the state (beginning with MFS) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d7-118">**uId**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-118">**uId**</span></span>
</dt> <dd>

<span data-ttu-id="0c3d7-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="0c3d7-120">O identificador do item de menu.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-120">The menu item identifier.</span></span> <span data-ttu-id="0c3d7-121">Esse é um valor definido pelo aplicativo que identifica o item de menu.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-121">This is an application-defined value that identifies the menu item.</span></span> <span data-ttu-id="0c3d7-122">Em um recurso de menu estendido, os itens que abrem menus ou submenus suspensos, bem como itens de comando, podem ter identificadores.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-122">In an extended menu resource, items that open drop-down menus or submenus as well as command items can have identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d7-123">**wFlags**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-123">**wFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0c3d7-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0c3d7-125">Especifica se o item de menu é o último item na barra de menus, no menu suspenso, no submenu ou no menu de atalho e se é um item que abre um menu suspenso ou submenu.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-125">Specifies whether the menu item is the last item in the menu bar, drop-down menu, submenu, or shortcut menu and whether it is an item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="0c3d7-126">Esse membro pode ser zero ou mais desses valores.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-126">This member can be zero or more of these values.</span></span> <span data-ttu-id="0c3d7-127">Para aplicativos de 32 bits, esse membro é uma palavra; para aplicativos de 16 bits, é um byte.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-127">For 32-bit applications, this member is a word; for 16-bit applications, it is a byte.</span></span>

<dt>

<span data-ttu-id="0c3d7-128">0x80</span><span class="sxs-lookup"><span data-stu-id="0c3d7-128">0x80</span></span>
</dt> <dd>

<span data-ttu-id="0c3d7-129">A estrutura define o último item de menu na barra de menus, no menu suspenso, no submenu ou no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-129">The structure defines the last menu item in the menu bar, drop-down menu, submenu, or shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d7-130">0x01</span><span class="sxs-lookup"><span data-stu-id="0c3d7-130">0x01</span></span>
</dt> <dd>

<span data-ttu-id="0c3d7-131">A estrutura define um item que abre um menu suspenso ou submenu.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-131">The structure defines a item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="0c3d7-132">As estruturas subsequentes definem itens de menu no menu suspenso ou submenu suspenso correspondente.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-132">Subsequent structures define menu items in the corresponding drop-down menu or submenu.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0c3d7-133">**szText**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-133">**szText**</span></span>
</dt> <dd>

<span data-ttu-id="0c3d7-134">Tipo: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-134">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="0c3d7-135">O texto do item de menu.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-135">The menu item text.</span></span> <span data-ttu-id="0c3d7-136">Este membro é uma cadeia de caracteres Unicode terminada em nulo, alinhada em um limite de palavra.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-136">This member is a null-terminated Unicode string, aligned on a word boundary.</span></span> <span data-ttu-id="0c3d7-137">O tamanho da definição do item de menu varia dependendo do comprimento dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-137">The size of the menu item definition varies depending on the length of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c3d7-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c3d7-138">Remarks</span></span>

<span data-ttu-id="0c3d7-139">Um modelo de menu estendido consiste em uma estrutura de [**\_ \_ cabeçalho de modelo MENUEX**](menuex-template-header.md) seguida por uma ou mais estruturas de **\_ \_ item de modelo MENUEX** contíguas.</span><span class="sxs-lookup"><span data-stu-id="0c3d7-139">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one or more contiguous **MENUEX\_TEMPLATE\_ITEM** structures.</span></span> <span data-ttu-id="0c3d7-140">As estruturas de **\_ \_ item de modelo MENUEX** , que são variáveis de comprimento, são alinhadas nos limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0c3d7-140">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="0c3d7-141">Para criar um menu a partir de um modelo de menu estendido na memória, use a função [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) .</span><span class="sxs-lookup"><span data-stu-id="0c3d7-141">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c3d7-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c3d7-142">Requirements</span></span>



| <span data-ttu-id="0c3d7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c3d7-143">Requirement</span></span> | <span data-ttu-id="0c3d7-144">Valor</span><span class="sxs-lookup"><span data-stu-id="0c3d7-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0c3d7-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c3d7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3d7-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0c3d7-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c3d7-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c3d7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3d7-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0c3d7-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0c3d7-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c3d7-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c3d7-150">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0c3d7-151">**LoadMenuIndirect**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-151">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="0c3d7-152">**\_cabeçalho do modelo MENUEX \_**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-152">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="0c3d7-153">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-153">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

<span data-ttu-id="0c3d7-154">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0c3d7-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c3d7-155">Menus</span><span class="sxs-lookup"><span data-stu-id="0c3d7-155">Menus</span></span>](menus.md)
</dt> </dl>

 

 





