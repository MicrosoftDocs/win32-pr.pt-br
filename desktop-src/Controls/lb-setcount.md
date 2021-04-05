---
title: Mensagem de LB_SETCOUNT (WinUser. h)
description: Define a contagem de itens em uma caixa de listagem criada com o \_ estilo NOdata de lbs e não é criada com o \_ estilo lbs HASSTRINGS.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- Controles de LB_SETCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009653"
---
# <a name="lb_setcount-message"></a><span data-ttu-id="2e5ed-104">\_Mensagem do número de contagem lb</span><span class="sxs-lookup"><span data-stu-id="2e5ed-104">LB\_SETCOUNT message</span></span>

<span data-ttu-id="2e5ed-105">Define a contagem de itens em uma caixa de listagem criada com o estilo [**\_ NODATA de lbs**](list-box-styles.md) e não é criada com o estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5ed-105">Sets the count of items in a list box created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e5ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e5ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e5ed-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e5ed-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e5ed-108">Especifica a nova contagem de itens na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-108">Specifies the new count of items in the list box.</span></span>

<span data-ttu-id="2e5ed-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="2e5ed-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="2e5ed-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="2e5ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e5ed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e5ed-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e5ed-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e5ed-114">Return value</span></span>

<span data-ttu-id="2e5ed-115">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="2e5ed-115">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="2e5ed-116">Se não houver memória suficiente para armazenar os itens, o valor de retorno será LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-116">If there is insufficient memory to store the items, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e5ed-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e5ed-117">Remarks</span></span>

<span data-ttu-id="2e5ed-118">Há suporte para a mensagem de **\_ número de lb** somente por caixas de listagem criadas com o estilo do [**lbs \_ NODATA**](list-box-styles.md) e não criadas com o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5ed-118">The **LB\_SETCOUNT** message is supported only by list boxes created with the [**LBS\_NODATA**](list-box-styles.md) style and not created with the [**LBS\_HASSTRINGS**](list-box-styles.md) style.</span></span> <span data-ttu-id="2e5ed-119">Todas as outras caixas de listagem retornam o \_ erro lb.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-119">All other list boxes return LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5ed-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e5ed-120">Requirements</span></span>



| <span data-ttu-id="2e5ed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5ed-121">Requirement</span></span> | <span data-ttu-id="2e5ed-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2e5ed-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5ed-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e5ed-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5ed-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e5ed-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e5ed-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e5ed-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5ed-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e5ed-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e5ed-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e5ed-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e5ed-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e5ed-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e5ed-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e5ed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5ed-130">**GetCount de LB \_**</span><span class="sxs-lookup"><span data-stu-id="2e5ed-130">**LB\_GETCOUNT**</span></span>](lb-getcount.md)
</dt> </dl>

 

 





