---
title: Mensagem de LB_GETITEMDATA (WinUser. h)
description: Obtém o valor definido pelo aplicativo associado ao item da caixa de listagem especificado.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- Controles de LB_GETITEMDATA de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086326"
---
# <a name="lb_getitemdata-message"></a><span data-ttu-id="3fcb5-104">GETITEMDATA de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="3fcb5-104">LB\_GETITEMDATA message</span></span>

<span data-ttu-id="3fcb5-105">Obtém o valor definido pelo aplicativo associado ao item da caixa de listagem especificado.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-105">Gets the application-defined value associated with the specified list box item.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fcb5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fcb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fcb5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fcb5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcb5-108">O índice do item.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-108">The index of the item.</span></span>

<span data-ttu-id="3fcb5-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="3fcb5-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="3fcb5-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="3fcb5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fcb5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcb5-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fcb5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3fcb5-114">Return value</span></span>

<span data-ttu-id="3fcb5-115">O valor de retorno é o valor associado ao item, ou erro de LB \_ se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-115">The return value is the value associated with the item, or LB\_ERR if an error occurs.</span></span> <span data-ttu-id="3fcb5-116">Se o item estiver em uma caixa de listagem desenhada pelo proprietário e tiver sido criado sem o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , esse valor estará no parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lb \_ InsertString**](lb-insertstring.md) que adicionou o item à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="3fcb5-116">If the item is in an owner-drawn list box and was created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this value was in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span> <span data-ttu-id="3fcb5-117">Caso contrário, é o valor no *lParam* da mensagem [**\_ SETITEMDATA de lb**](lb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3fcb5-117">Otherwise, it is the value in the *lParam* of the [**LB\_SETITEMDATA**](lb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fcb5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fcb5-118">Requirements</span></span>



| <span data-ttu-id="3fcb5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fcb5-119">Requirement</span></span> | <span data-ttu-id="3fcb5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3fcb5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fcb5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fcb5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3fcb5-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fcb5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3fcb5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fcb5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3fcb5-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fcb5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3fcb5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fcb5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fcb5-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fcb5-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fcb5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fcb5-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3fcb5-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3fcb5-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3fcb5-129">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="3fcb5-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="3fcb5-130">**KG \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="3fcb5-130">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="3fcb5-131">**\_SETITEMDATA lb**</span><span class="sxs-lookup"><span data-stu-id="3fcb5-131">**LB\_SETITEMDATA**</span></span>](lb-setitemdata.md)
</dt> </dl>

 

 





