---
title: Estilos estendidos de controle ComboBoxEx (CommCtrl. h)
description: Dê suporte aos estilos estendidos listados nesta seção, bem como a maioria dos estilos de controle de caixa de combinação padrão.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750552"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="5f4cb-103">Estilos estendidos do controle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="5f4cb-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="5f4cb-104">Dê suporte aos estilos estendidos listados nesta seção, bem como a maioria dos estilos de controle de caixa de combinação padrão.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="5f4cb-105">Constante</span><span class="sxs-lookup"><span data-stu-id="5f4cb-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="5f4cb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f4cb-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="5f4cb-107"><dt>**CBES \_ ex \_ CASESENSITIVE**</dt></span><span class="sxs-lookup"><span data-stu-id="5f4cb-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="5f4cb-108">As pesquisas **BSTR** na lista serão diferenciadas entre maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="5f4cb-109">Isso inclui pesquisas como resultado de texto que está sendo digitado na caixa de edição e na \_ mensagem CB FINDSTRINGEXACT.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="5f4cb-110"><dt>**CBES \_ ex \_ NOEDITIMAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="5f4cb-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="5f4cb-111">A caixa de edição e a lista suspensa não exibirão imagens de item.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="5f4cb-112"><dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt></span><span class="sxs-lookup"><span data-stu-id="5f4cb-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="5f4cb-113">A caixa de edição e a lista suspensa não exibirão imagens de item.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="5f4cb-114"><dt>**CBES \_ ex \_ NOSIZELIMIT**</dt></span><span class="sxs-lookup"><span data-stu-id="5f4cb-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="5f4cb-115">Permite que o controle ComboBoxEx seja verticalmente dimensionado menor do que seu controle de caixa de combinação contido.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="5f4cb-116">Se o ComboBoxEx for menor que a caixa de combinação, a caixa de combinação será recortada.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="5f4cb-117"><dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt></span><span class="sxs-lookup"><span data-stu-id="5f4cb-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="5f4cb-118">Somente Windows NT.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-118">Windows NT only.</span></span> <span data-ttu-id="5f4cb-119">A caixa de edição usará a barra (/), as barras invertidas ( \) e os caracteres de ponto (.) como delimitadores de palavras.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-119">The edit box will use the slash (/), backslash (\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="5f4cb-120">Isso torna os atalhos de teclado para o movimento de cursor de palavra por palavra efetivo em nomes de caminho e URLs.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="5f4cb-121"><dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="5f4cb-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="5f4cb-122">**Windows Vista e posterior.**</span><span class="sxs-lookup"><span data-stu-id="5f4cb-122">**Windows Vista and later.**</span></span> <span data-ttu-id="5f4cb-123">Faz com que os itens na lista suspensa e na caixa de edição (quando a caixa de edição é somente leitura) sejam truncados com reticências ("...") em vez de apenas recortados pela borda do controle.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="5f4cb-124">Isso é útil quando o controle precisa ser definido com uma largura fixa, mas as entradas na lista podem ser longas.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5f4cb-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f4cb-125">Remarks</span></span>

<span data-ttu-id="5f4cb-126">Você define e recupera os estilos estendidos da ComboBox usando as mensagens [**CBEM \_ Extended**](cbem-setextendedstyle.md) e [**CBEM \_ getextendedattribute**](cbem-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="5f4cb-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="5f4cb-127">Se você tentar definir um estilo estendido para um controle ComboBoxEx criado com o [**estilo \_ simples do CBS**](combo-box-styles.md) , ele poderá não ser redesenhado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="5f4cb-128">O **estilo \_ simples do CBS** também não funciona corretamente com o \_ \_ estilo estendido CBES ex PATHWORDBREAKPROC.</span><span class="sxs-lookup"><span data-stu-id="5f4cb-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f4cb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f4cb-129">Requirements</span></span>



| <span data-ttu-id="5f4cb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f4cb-130">Requirement</span></span> | <span data-ttu-id="5f4cb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5f4cb-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4cb-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f4cb-132">Header</span></span><br/> | <dl> <span data-ttu-id="5f4cb-133"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4cb-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





