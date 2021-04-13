---
title: Estrutura DLGTEMPLATEEX
description: Um modelo de caixa de diálogo estendido começa com um cabeçalho DLGTEMPLATEEX que descreve a caixa de diálogo e especifica o número de controles na caixa de diálogo.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Caixas de diálogo da estrutura DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499566"
---
# <a name="dlgtemplateex-structure"></a><span data-ttu-id="4c3e3-104">Estrutura DLGTEMPLATEEX</span><span class="sxs-lookup"><span data-stu-id="4c3e3-104">DLGTEMPLATEEX structure</span></span>

<span data-ttu-id="4c3e3-105">Um modelo de caixa de diálogo estendido começa com um cabeçalho **DLGTEMPLATEEX** que descreve a caixa de diálogo e especifica o número de controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-105">An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box.</span></span> <span data-ttu-id="4c3e3-106">Para cada controle em uma caixa de diálogo, um modelo de caixa de diálogo estendida tem um bloco de dados que usa o formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) para descrever o controle.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-106">For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control.</span></span>

<span data-ttu-id="4c3e3-107">A estrutura **DLGTEMPLATEEX** não está definida em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-107">The **DLGTEMPLATEEX** structure is not defined in any standard header file.</span></span> <span data-ttu-id="4c3e3-108">A definição de estrutura é fornecida aqui para explicar o formato de um modelo estendido para uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-108">The structure definition is provided here to explain the format of an extended template for a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3e3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c3e3-109">Syntax</span></span>


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="4c3e3-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4c3e3-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c3e3-111">**dlgVer**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-111">**dlgVer**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-112">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-112">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-113">O número de versão do modelo da caixa de diálogo estendida.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-113">The version number of the extended dialog box template.</span></span> <span data-ttu-id="4c3e3-114">Esse membro deve ser definido como 1.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-114">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-115">**assinatura**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-115">**signature**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-116">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-117">Indica se um modelo é um modelo de caixa de diálogo estendida.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-117">Indicates whether a template is an extended dialog box template.</span></span> <span data-ttu-id="4c3e3-118">Se a **assinatura** for 0xFFFF, esse será um modelo de caixa de diálogo estendido.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-118">If **signature** is 0xFFFF, this is an extended dialog box template.</span></span> <span data-ttu-id="4c3e3-119">Nesse caso, o membro **dlgVer** especifica o número de versão do modelo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-119">In this case, the **dlgVer** member specifies the template version number.</span></span> <span data-ttu-id="4c3e3-120">Se a **assinatura** for qualquer valor diferente de 0xFFFF, esse será um modelo de caixa de diálogo padrão que usa as estruturas [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) e [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-120">If **signature** is any value other than 0xFFFF, this is a standard dialog box template that uses the [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) and [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-121">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-121">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-123">O identificador de contexto da ajuda para a janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-123">The help context identifier for the dialog box window.</span></span> <span data-ttu-id="4c3e3-124">Quando o sistema envia uma mensagem de [**\_ ajuda do WM**](../shell/wm-help.md) , ele passa esse valor no membro **wContextId** da estrutura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-124">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes this value in the **wContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-125">**comstyle**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-125">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-126">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-127">Os estilos estendidos do Windows.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-127">The extended windows styles.</span></span> <span data-ttu-id="4c3e3-128">Esse membro não é usado ao criar caixas de diálogo, mas os aplicativos que usam modelos de caixa de diálogo podem usá-lo para criar outros tipos de janelas.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-128">This member is not used when creating dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="4c3e3-129">Para obter uma lista de valores, consulte [**estilos de janela estendidos**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="4c3e3-129">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-130">**style**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-130">**style**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-131">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-132">O estilo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-132">The style of the dialog box.</span></span> <span data-ttu-id="4c3e3-133">Esse membro pode ser uma combinação de [valores de estilo de janela](/windows/desktop/winmsg/window-styles) e [valores de estilo de caixa de diálogo](dialog-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="4c3e3-133">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) and [dialog box style values](dialog-box-styles.md).</span></span>

<span data-ttu-id="4c3e3-134">Se **o estilo** incluir o estilo de caixa de diálogo **DS \_ SetFont** ou **DS \_ SHELLFONT** , o cabeçalho **DLGTEMPLATEEX** do modelo da caixa de diálogo estendida conterá quatro membros adicionais ( **pontos**, **peso**, **itálico** e **tipo**) que descrevem a fonte a ser usada para o texto na área do cliente e os controles da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-134">If **style** includes the **DS\_SETFONT** or **DS\_SHELLFONT** dialog box style, the **DLGTEMPLATEEX** header of the extended dialog box template contains four additional members ( **pointsize**, **weight**, **italic**, and **typeface**) that describe the font to use for the text in the client area and controls of the dialog box.</span></span> <span data-ttu-id="4c3e3-135">Se possível, o sistema cria uma fonte de acordo com os valores especificados nesses membros.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-135">If possible, the system creates a font according to the values specified in these members.</span></span> <span data-ttu-id="4c3e3-136">Em seguida, o sistema envia uma mensagem do [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) para a caixa de diálogo e para cada controle para fornecer um identificador para a fonte.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-136">Then the system sends a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to the dialog box and to each control to provide a handle to the font.</span></span>

<span data-ttu-id="4c3e3-137">Para obter mais informações, consulte [fontes da caixa de diálogo](about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="4c3e3-137">For more information, see [Dialog Box Fonts](about-dialog-boxes.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-138">**cDlgItems**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-138">**cDlgItems**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-139">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-140">O número de controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-140">The number of controls in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-141">**x**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-141">**x**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-142">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-142">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-143">A coordenada x, nas unidades da caixa de diálogo, do canto superior esquerdo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-143">The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-144">**y**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-144">**y**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-145">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-145">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-146">A coordenada y, nas unidades da caixa de diálogo, do canto superior esquerdo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-146">The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-147">**CX**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-147">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-148">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-148">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-149">A largura, nas unidades da caixa de diálogo, da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-149">The width, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-150">**Cy**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-150">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-151">Tipo: **curto**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-151">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-152">A altura, nas unidades da caixa de diálogo, da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-152">The height, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-153">**AdicionarMenu**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-153">**menu**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-154">Tipo: **sz \_ ou \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-154">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-155">Uma matriz de comprimento variável de elementos de 16 bits que identifica um recurso de menu para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-155">A variable-length array of 16-bit elements that identifies a menu resource for the dialog box.</span></span> <span data-ttu-id="4c3e3-156">Se o primeiro elemento dessa matriz for 0x0000, a caixa de diálogo não terá nenhum menu e a matriz não terá nenhum outro elemento.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-156">If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements.</span></span> <span data-ttu-id="4c3e3-157">Se o primeiro elemento for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de um recurso de menu em um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-157">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file.</span></span> <span data-ttu-id="4c3e3-158">Se o primeiro elemento tiver qualquer outro valor, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de um recurso de menu em um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-158">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-159">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-159">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-160">Tipo: **sz \_ ou \_ Ord**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-160">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-161">Uma matriz de comprimento variável de elementos de 16 bits que identifica a classe de janela da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-161">A variable-length array of 16-bit elements that identifies the window class of the dialog box.</span></span> <span data-ttu-id="4c3e3-162">Se o primeiro elemento da matriz for 0x0000, o sistema usará a classe de caixa de diálogo predefinida para a caixa de diálogo e a matriz não terá outros elementos.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-162">If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements.</span></span> <span data-ttu-id="4c3e3-163">Se o primeiro elemento for 0xFFFF, a matriz terá um elemento adicional que especifica o valor ordinal de uma classe de janela do sistema predefinida.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-163">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class.</span></span> <span data-ttu-id="4c3e3-164">Se o primeiro elemento tiver qualquer outro valor, o sistema tratará a matriz como uma cadeia de caracteres Unicode terminada em nulo que especifica o nome de uma classe de janela registrada.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-164">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-165">**title**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-165">**title**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-166">Tipo: **WCHAR \[ titleLen \]**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-166">Type: **WCHAR\[titleLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-167">O título da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-167">The title of the dialog box.</span></span> <span data-ttu-id="4c3e3-168">Se o primeiro elemento dessa matriz for 0x0000, a caixa de diálogo não terá nenhum título e a matriz não terá nenhum outro elemento.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-168">If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-169">**pontos**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-169">**pointsize**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-170">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-170">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-171">O tamanho do ponto da fonte a ser usado para o texto na caixa de diálogo e seus controles.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-171">The point size of the font to use for the text in the dialog box and its controls.</span></span>

<span data-ttu-id="4c3e3-172">Esse membro estará presente somente se o membro de **estilo** especificar **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-172">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-173">**weight**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-173">**weight**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-174">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-174">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-175">O peso da fonte.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-175">The weight of the font.</span></span> <span data-ttu-id="4c3e3-176">Observe que, embora isso possa ser qualquer um dos valores listados para o membro **lfWeight** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , qualquer valor usado será alterado automaticamente para o **FW \_ normal**.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-176">Note that, although this can be any of the values listed for the **lfWeight** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure, any value that is used will be automatically changed to **FW\_NORMAL**.</span></span>

<span data-ttu-id="4c3e3-177">Esse membro estará presente somente se o membro de **estilo** especificar **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-177">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-178">**italic**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-178">**italic**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-179">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-179">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-180">Indica se a fonte está em itálico.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-180">Indicates whether the font is italic.</span></span> <span data-ttu-id="4c3e3-181">Se esse valor for **true**, a fonte será itálico.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-181">If this value is **TRUE**, the font is italic.</span></span>

<span data-ttu-id="4c3e3-182">Esse membro estará presente somente se o membro de **estilo** especificar **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-182">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-183">**charset**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-183">**charset**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-184">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-184">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-185">O conjunto de caracteres a ser usado.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-185">The character set to be used.</span></span> <span data-ttu-id="4c3e3-186">Para obter mais informações, consulte o membro **lfCharSet** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span><span class="sxs-lookup"><span data-stu-id="4c3e3-186">For more information, see the **lfcharset** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span></span>

<span data-ttu-id="4c3e3-187">Esse membro estará presente somente se o membro de **estilo** especificar **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-187">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="4c3e3-188">**face**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-188">**typeface**</span></span>
</dt> <dd>

<span data-ttu-id="4c3e3-189">Tipo: **WCHAR \[ stringLen \]**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-189">Type: **WCHAR\[stringLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="4c3e3-190">O nome da face de tipos da fonte.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-190">The name of the typeface for the font.</span></span>

<span data-ttu-id="4c3e3-191">Esse membro estará presente somente se o membro de **estilo** especificar **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-191">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c3e3-192">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c3e3-192">Remarks</span></span>

<span data-ttu-id="4c3e3-193">Você pode usar um modelo de caixa de diálogo estendida em vez de um modelo de caixa de diálogo padrão nas funções [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)e [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-193">You can use an extended dialog box template instead of a standard dialog box template in the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta), and [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) functions.</span></span>

<span data-ttu-id="4c3e3-194">Seguir o cabeçalho **DLGTEMPLATEEX** em um modelo de caixa de diálogo estendido é uma ou mais estruturas [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) que descrevem os controles da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-194">Following the **DLGTEMPLATEEX** header in an extended dialog box template is one or more [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structures that describe the controls of the dialog box.</span></span> <span data-ttu-id="4c3e3-195">O membro **cDlgItems** da estrutura **DLGITEMTEMPLATEEX** especifica o número de estruturas **DLGITEMTEMPLATEEX** que seguem no modelo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-195">The **cDlgItems** member of the **DLGITEMTEMPLATEEX** structure specifies the number of **DLGITEMTEMPLATEEX** structures that follow in the template.</span></span>

<span data-ttu-id="4c3e3-196">Cada estrutura [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) no modelo deve ser alinhada em um limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-196">Each [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structure in the template must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="4c3e3-197">Se o membro de **estilo** especificar o estilo **DS \_ SetFont** ou **DS \_ SHELLFONT** , a primeira estrutura **DLGITEMTEMPLATEEX** começará no primeiro limite **DWORD** após a cadeia de caracteres de **tipo** .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-197">If the **style** member specifies the **DS\_SETFONT** or **DS\_SHELLFONT** style, the first **DLGITEMTEMPLATEEX** structure begins on the first **DWORD** boundary after the **typeface** string.</span></span> <span data-ttu-id="4c3e3-198">Se esses estilos não forem especificados, a primeira estrutura começará no primeiro limite **DWORD** após a cadeia de **título** .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-198">If these styles are not specified, the first structure begins on the first **DWORD** boundary after the **title** string.</span></span>

<span data-ttu-id="4c3e3-199">As matrizes **menu**, **WindowClass**, **title** e **face de tipos** devem ser alinhadas em limites de **palavras** .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-199">The **menu**, **windowClass**, **title**, and **typeface** arrays must be aligned on **WORD** boundaries.</span></span>

<span data-ttu-id="4c3e3-200">Se você especificar cadeias de caracteres nas matrizes **menu**, **WindowClass**, **title** e **face** , deverá usar cadeias de caractere Unicode.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-200">If you specify character strings in the **menu**, **windowClass**, **title**, and **typeface** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="4c3e3-201">Use a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para gerar essas cadeias de caracteres Unicode a partir de cadeias de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-201">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="4c3e3-202">Os membros **x**, **y**, **CX** e **CY** especificam valores nas unidades da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-202">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="4c3e3-203">Você pode converter esses valores em unidades de tela (pixels) usando a função [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-203">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3e3-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3e3-204">Requirements</span></span>



| <span data-ttu-id="4c3e3-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c3e3-205">Requirement</span></span> | <span data-ttu-id="4c3e3-206">Valor</span><span class="sxs-lookup"><span data-stu-id="4c3e3-206">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4c3e3-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3e3-207">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3e3-208">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c3e3-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4c3e3-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c3e3-209">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3e3-210">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c3e3-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4c3e3-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c3e3-211">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c3e3-212">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-212">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4c3e3-213">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-213">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="4c3e3-214">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-214">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="4c3e3-215">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-215">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="4c3e3-216">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-216">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="4c3e3-217">**DLGITEMTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-217">**DLGITEMTEMPLATEEX**</span></span>](dlgitemtemplateex.md)
</dt> <dt>

[<span data-ttu-id="4c3e3-218">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-218">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="4c3e3-219">**WM \_ SETfont**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-219">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

<span data-ttu-id="4c3e3-220">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4c3e3-221">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="4c3e3-221">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="4c3e3-222">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-222">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4c3e3-223">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-223">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="4c3e3-224">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-224">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

