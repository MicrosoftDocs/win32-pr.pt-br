---
title: CFSTR_DSOP_DS_SELECTION_LIST (Objsel. h)
description: O formato da área de transferência da lista de seleção do CFSTR \_ DSOP \_ DS fornece um \_ \_ HGLOBAL que contém uma estrutura de lista de seleção do DS \_ \_ . A estrutura da lista de seleção do DS \_ \_ contém dados sobre os itens selecionados em uma caixa de diálogo Seletor de objetos de diretório.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918288"
---
# <a name="cfstr_dsop_ds_selection_list"></a><span data-ttu-id="0804b-104">lista de seleção do CFSTR \_ DSOP \_ DS \_ \_</span><span class="sxs-lookup"><span data-stu-id="0804b-104">CFSTR\_DSOP\_DS\_SELECTION\_LIST</span></span>

<dl> <dt>

<span data-ttu-id="0804b-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**lista de seleção do CFSTR \_ DSOP \_ DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0804b-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR\_DSOP\_DS\_SELECTION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0804b-106">"lista de seleção do CFSTR \_ DSOP \_ DS \_ \_ "</span><span class="sxs-lookup"><span data-stu-id="0804b-106">"CFSTR\_DSOP\_DS\_SELECTION\_LIST"</span></span>
</dt> <dt>



<span data-ttu-id="0804b-107">O formato da área de transferência da **lista de seleção do CFSTR \_ DSOP \_ \_ \_ DS** é fornecido pelo [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtido chamando [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span><span class="sxs-lookup"><span data-stu-id="0804b-107">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format is provided by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtained by calling [**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span></span> <span data-ttu-id="0804b-108">O formato da área de transferência da **lista de seleção do CFSTR \_ DSOP \_ \_ \_ DS** fornece um **HGLOBAL** que contém uma estrutura de [**\_ \_ lista de seleção do DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) .</span><span class="sxs-lookup"><span data-stu-id="0804b-108">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format provides an **HGLOBAL** that contains a [**DS\_SELECTION\_LIST**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) structure.</span></span> <span data-ttu-id="0804b-109">A estrutura da **\_ \_ lista de seleção do DS** contém dados sobre os itens selecionados em uma caixa de diálogo [seletor de objetos de diretório](directory-object-picker.md) .</span><span class="sxs-lookup"><span data-stu-id="0804b-109">The **DS\_SELECTION\_LIST** structure contains data about the items selected in a [Directory Object Picker](directory-object-picker.md) dialog box.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0804b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0804b-110">Requirements</span></span>



| <span data-ttu-id="0804b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0804b-111">Requirement</span></span> | <span data-ttu-id="0804b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0804b-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0804b-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0804b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0804b-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0804b-114">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="0804b-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0804b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0804b-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0804b-116">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="0804b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0804b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0804b-118"><dt>Objsel. h</dt></span><span class="sxs-lookup"><span data-stu-id="0804b-118"><dt>Objsel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0804b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0804b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0804b-120">**\_lista de seleção de DS \_**</span><span class="sxs-lookup"><span data-stu-id="0804b-120">**DS\_SELECTION\_LIST**</span></span>](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[<span data-ttu-id="0804b-121">**IDsObjectPicker::InvokeDialog**</span><span class="sxs-lookup"><span data-stu-id="0804b-121">**IDsObjectPicker::InvokeDialog**</span></span>](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[<span data-ttu-id="0804b-122">Seletor de objetos de diretório</span><span class="sxs-lookup"><span data-stu-id="0804b-122">Directory Object Picker</span></span>](directory-object-picker.md)
</dt> </dl>

 

