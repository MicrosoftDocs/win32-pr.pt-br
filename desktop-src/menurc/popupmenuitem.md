---
title: Estrutura POPUPMENUITEM
description: Contém informações sobre os itens de menu em um recurso de menu que abre um menu ou um submenu. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- Menus de estrutura POPUPMENUITEM e outros recursos
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faa755c2ec7a2b9eeb2f123d7fd3e169b2df1be1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918123"
---
# <a name="popupmenuitem-structure"></a><span data-ttu-id="cefd1-105">Estrutura POPUPMENUITEM</span><span class="sxs-lookup"><span data-stu-id="cefd1-105">POPUPMENUITEM structure</span></span>

<span data-ttu-id="cefd1-106">Contém informações sobre os itens de menu em um recurso de menu que abre um menu ou um submenu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-106">Contains information about the menu items in a menu resource that open a menu or a submenu.</span></span> <span data-ttu-id="cefd1-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="cefd1-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cefd1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cefd1-108">Syntax</span></span>


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a><span data-ttu-id="cefd1-109">Membros</span><span class="sxs-lookup"><span data-stu-id="cefd1-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="cefd1-110">**tipo**</span><span class="sxs-lookup"><span data-stu-id="cefd1-110">**type**</span></span>
</dt> <dd>

<span data-ttu-id="cefd1-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cefd1-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cefd1-112">Descreve o item de menu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-112">Describes the menu item.</span></span> <span data-ttu-id="cefd1-113">Alguns dos valores que esse membro pode ter incluem os mostrados na lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="cefd1-113">Some of the values this member can have include those shown in the list below.</span></span>

<span data-ttu-id="cefd1-114">Além dos valores mostrados, esse membro também pode ser uma combinação dos valores de tipo listados com o membro **ftype** da estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="cefd1-114">In addition to the values shown, this member can also be a combination of the type values listed with the **fType** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="cefd1-115">Os valores de tipo são aqueles que começam com MFT \_ .</span><span class="sxs-lookup"><span data-stu-id="cefd1-115">The type values are those that begin with MFT\_.</span></span> <span data-ttu-id="cefd1-116">Para usar esses valores de tipo de MFT predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:</span><span class="sxs-lookup"><span data-stu-id="cefd1-116">To use these predefined MFT\_\* type values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`



| <span data-ttu-id="cefd1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cefd1-117">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="cefd1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="cefd1-118">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <span data-ttu-id="cefd1-119"><dt>**MF \_ ENCERRAR**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="cefd1-119"><dt>**MF\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="cefd1-120">O item de menu é o último no menu; o sinalizador é usado internamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="cefd1-120">The menu item is the last on the menu; the flag is used internally by the system.</span></span> <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="cefd1-121"><dt>**MF \_ POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="cefd1-121"><dt>**MF\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="cefd1-122">O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="cefd1-122">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="cefd1-123">**state**</span><span class="sxs-lookup"><span data-stu-id="cefd1-123">**state**</span></span>
</dt> <dd>

<span data-ttu-id="cefd1-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cefd1-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cefd1-125">Descreve o item de menu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-125">Describes the menu item.</span></span> <span data-ttu-id="cefd1-126">Esse membro pode ser uma combinação dos valores de estado listados com o membro **dwState** da estrutura [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="cefd1-126">This member can be a combination of the state values listed with the **dwState** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="cefd1-127">Os valores de estado são aqueles que começam com MFS \_ .</span><span class="sxs-lookup"><span data-stu-id="cefd1-127">The state values are those that begin with MFS\_.</span></span> <span data-ttu-id="cefd1-128">Para usar esses valores de estado de MFS predefinidos \_ \* , inclua a seguinte instrução no arquivo. rc:</span><span class="sxs-lookup"><span data-stu-id="cefd1-128">To use these predefined MFS\_\* state values, include the following statement in your .rc file:</span></span>

`#include "winuser.h"`

</dd> <dt>

<span data-ttu-id="cefd1-129">**id**</span><span class="sxs-lookup"><span data-stu-id="cefd1-129">**id**</span></span>
</dt> <dd>

<span data-ttu-id="cefd1-130">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cefd1-130">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cefd1-131">Uma expressão numérica que identifica o item de menu que é passado na mensagem de [**\_ comando do WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="cefd1-131">A numeric expression that identifies the menu item that is passed in the [**WM\_COMMAND**](wm-command.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="cefd1-132">**resInfo**</span><span class="sxs-lookup"><span data-stu-id="cefd1-132">**resInfo**</span></span>
</dt> <dd>

<span data-ttu-id="cefd1-133">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="cefd1-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="cefd1-134">Um conjunto de sinalizadores de bits que especificam o tipo de item de menu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-134">A set of bit flags that specify the type of menu item.</span></span> <span data-ttu-id="cefd1-135">Esse membro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cefd1-135">This member can be one of the following values.</span></span>



| <span data-ttu-id="cefd1-136">Valor</span><span class="sxs-lookup"><span data-stu-id="cefd1-136">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="cefd1-137">Significado</span><span class="sxs-lookup"><span data-stu-id="cefd1-137">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <span data-ttu-id="cefd1-138"><dt>**Mfr \_ ENCERRAR**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="cefd1-138"><dt>**MFR\_END**</dt> <dt>0x80</dt></span></span> </dl>       | <span data-ttu-id="cefd1-139">O item de menu é o último neste submenu ou recurso de menu; Esse sinalizador é usado internamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="cefd1-139">The menu item is the last in this submenu or menu resource; this flag is used internally by the system.</span></span><br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <span data-ttu-id="cefd1-140"><dt>**Mfr \_ POPUP**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="cefd1-140"><dt>**MFR\_POPUP**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="cefd1-141">O item de menu abre um menu ou um submenu; o sinalizador é usado internamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="cefd1-141">The menu item opens a menu or a submenu; the flag is used internally by the system.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="cefd1-142">**menuText**</span><span class="sxs-lookup"><span data-stu-id="cefd1-142">**menuText**</span></span>
</dt> <dd>

<span data-ttu-id="cefd1-143">Tipo: **szOrOrd**</span><span class="sxs-lookup"><span data-stu-id="cefd1-143">Type: **szOrOrd**</span></span>

</dd> <dd>

<span data-ttu-id="cefd1-144">Uma cadeia de caracteres Unicode terminada em nulo que contém o texto para este item de menu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-144">A null-terminated Unicode string that contains the text for this menu item.</span></span> <span data-ttu-id="cefd1-145">Não há nenhum limite fixo para o tamanho dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cefd1-145">There is no fixed limit on the size of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cefd1-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="cefd1-146">Remarks</span></span>

<span data-ttu-id="cefd1-147">Há uma estrutura **POPUPMENUITEM** para cada item de menu que abre um menu ou um submenu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-147">There is one **POPUPMENUITEM** structure for each menu item that opens a menu or a submenu.</span></span> <span data-ttu-id="cefd1-148">Identifique esse tipo de item de menu definindo o membro de **tipo** como **\_ Popup MF** e definindo o bit de **\_ Popup mfr** no membro **resInfo** como 0x0001.</span><span class="sxs-lookup"><span data-stu-id="cefd1-148">Identify this type of menu item by setting the **type** member to **MF\_POPUP** and by setting the **MFR\_POPUP** bit in the **resInfo** member to 0x0001.</span></span> <span data-ttu-id="cefd1-149">Nesse caso, os dados finais gravados no recurso [**de \_ menu RT**](/windows/desktop/menurc/resource-types) para o menu ou submenu é a estrutura [**MENUHELPID**](menuhelpid.md) .</span><span class="sxs-lookup"><span data-stu-id="cefd1-149">In this case, the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for the menu or submenu is the [**MENUHELPID**](menuhelpid.md) structure.</span></span> <span data-ttu-id="cefd1-150">**MENUHELPID** contém uma expressão numérica que identifica o menu durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .</span><span class="sxs-lookup"><span data-stu-id="cefd1-150">**MENUHELPID** contains a numeric expression that identifies the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

<span data-ttu-id="cefd1-151">Além disso, toda estrutura **POPUPMENUITEM** que tem o bit de **\_ Popup mfr** definido no membro **ResInfo** será seguida por uma estrutura [**MENUHELPID**](menuhelpid.md) mais um número adicional de estruturas **POPUPMENUITEM** , uma para cada item de menu nesse submenu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-151">Additionally, every **POPUPMENUITEM** structure that has the **MFR\_POPUP** bit set in the **resInfo** member will be followed by a [**MENUHELPID**](menuhelpid.md) structure plus an additional number of **POPUPMENUITEM** structures, one for each menu item in that submenu.</span></span> <span data-ttu-id="cefd1-152">A última estrutura **POPUPMENUITEM** no submenu terá o bit de **\_ término mfr** definido no membro **resInfo** .</span><span class="sxs-lookup"><span data-stu-id="cefd1-152">The last **POPUPMENUITEM** structure in the submenu will have the **MFR\_END** bit set in the **resInfo** member.</span></span> <span data-ttu-id="cefd1-153">Para localizar o fim do recurso, procure uma **\_ extremidade mfr** correspondente para cada **\_ pop-up mfr** , além de **uma \_ extremidade** adicional de Mfr que corresponda ao conjunto mais externo de itens de menu.</span><span class="sxs-lookup"><span data-stu-id="cefd1-153">To find the end of the resource, look for a matching **MFR\_END** for every **MFR\_POPUP** plus one additional **MFR\_END** that matches the outermost set of menu items.</span></span>

<span data-ttu-id="cefd1-154">Indique o último item de menu definindo o membro de **tipo** para o **\_ fim de MF**.</span><span class="sxs-lookup"><span data-stu-id="cefd1-154">Indicate the last menu item by setting the **type** member to **MF\_END**.</span></span> <span data-ttu-id="cefd1-155">Como você pode aninhar submenus, pode haver vários níveis de **\_ fim de MF**.</span><span class="sxs-lookup"><span data-stu-id="cefd1-155">Because you can nest submenus, there can be multiple levels of **MF\_END**.</span></span> <span data-ttu-id="cefd1-156">Nesses casos, os itens de menu são sequenciais.</span><span class="sxs-lookup"><span data-stu-id="cefd1-156">In these instances, the menu items are sequential.</span></span>

## <a name="requirements"></a><span data-ttu-id="cefd1-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cefd1-157">Requirements</span></span>



| <span data-ttu-id="cefd1-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="cefd1-158">Requirement</span></span> | <span data-ttu-id="cefd1-159">Valor</span><span class="sxs-lookup"><span data-stu-id="cefd1-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cefd1-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cefd1-160">Minimum supported client</span></span><br/> | <span data-ttu-id="cefd1-161">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cefd1-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cefd1-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cefd1-162">Minimum supported server</span></span><br/> | <span data-ttu-id="cefd1-163">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cefd1-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cefd1-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="cefd1-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="cefd1-165">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cefd1-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cefd1-166">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="cefd1-166">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="cefd1-167">**MENUHELPID**</span><span class="sxs-lookup"><span data-stu-id="cefd1-167">**MENUHELPID**</span></span>](menuhelpid.md)
</dt> <dt>

[<span data-ttu-id="cefd1-168">**MENUITEMINFO**</span><span class="sxs-lookup"><span data-stu-id="cefd1-168">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[<span data-ttu-id="cefd1-169">**NORMALMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="cefd1-169">**NORMALMENUITEM**</span></span>](normalmenuitem.md)
</dt> <dt>

<span data-ttu-id="cefd1-170">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cefd1-170">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cefd1-171">Recursos</span><span class="sxs-lookup"><span data-stu-id="cefd1-171">Resources</span></span>](resources.md)
</dt> </dl>

 

