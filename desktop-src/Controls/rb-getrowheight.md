---
title: Mensagem de RB_GETROWHEIGHT (commctrl. h)
description: Recupera a altura de uma linha especificada em um controle rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- Controles de RB_GETROWHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824564"
---
# <a name="rb_getrowheight-message"></a><span data-ttu-id="edc19-104">\_Mensagem RB GETalturadalinha</span><span class="sxs-lookup"><span data-stu-id="edc19-104">RB\_GETROWHEIGHT message</span></span>

<span data-ttu-id="edc19-105">Recupera a altura de uma linha especificada em um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="edc19-105">Retrieves the height of a specified row in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="edc19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edc19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc19-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edc19-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edc19-108">Índice de base zero de uma banda.</span><span class="sxs-lookup"><span data-stu-id="edc19-108">Zero-based index of a band.</span></span> <span data-ttu-id="edc19-109">A altura da linha que contém a faixa especificada será recuperada.</span><span class="sxs-lookup"><span data-stu-id="edc19-109">The height of the row that contains the specified band will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="edc19-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edc19-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="edc19-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="edc19-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc19-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edc19-112">Return value</span></span>

<span data-ttu-id="edc19-113">Retorna um valor **uint** que representa a altura da linha, em pixels.</span><span class="sxs-lookup"><span data-stu-id="edc19-113">Returns a **UINT** value that represents the row height, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="edc19-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="edc19-114">Remarks</span></span>

<span data-ttu-id="edc19-115">Para recuperar o número de linhas em um controle rebar, use a mensagem [**RB \_ GetRowCount**](rb-getrowcount.md) .</span><span class="sxs-lookup"><span data-stu-id="edc19-115">To retrieve the number of rows in a rebar control, use the [**RB\_GETROWCOUNT**](rb-getrowcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc19-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edc19-116">Requirements</span></span>



| <span data-ttu-id="edc19-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc19-117">Requirement</span></span> | <span data-ttu-id="edc19-118">Valor</span><span class="sxs-lookup"><span data-stu-id="edc19-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edc19-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edc19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="edc19-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edc19-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="edc19-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edc19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="edc19-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="edc19-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="edc19-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="edc19-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="edc19-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="edc19-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





