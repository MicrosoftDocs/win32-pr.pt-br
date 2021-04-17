---
description: Ocorre quando a seleção atual de texto no controle InkEdit é alterada ou o ponto de inserção foi movido.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit. SelChange (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748697"
---
# <a name="inkeditselchange-event"></a><span data-ttu-id="08447-103">Evento InkEdit. SelChange</span><span class="sxs-lookup"><span data-stu-id="08447-103">InkEdit.SelChange event</span></span>

<span data-ttu-id="08447-104">Ocorre quando a seleção atual de texto no controle [InkEdit](inkedit-control-reference.md) é alterada ou o ponto de inserção foi movido.</span><span class="sxs-lookup"><span data-stu-id="08447-104">Occurs when the current selection of text in the [InkEdit](inkedit-control-reference.md) control has changed or the insertion point has moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="08447-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08447-105">Syntax</span></span>


```C++
void SelChange();
```



## <a name="parameters"></a><span data-ttu-id="08447-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08447-106">Parameters</span></span>

<span data-ttu-id="08447-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="08447-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08447-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08447-108">Return value</span></span>

<span data-ttu-id="08447-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="08447-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08447-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="08447-110">Remarks</span></span>

<span data-ttu-id="08447-111">Você pode usar o evento **SelChange** para verificar as várias propriedades que fornecem informações sobre a seleção atual (como [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) para que você possa atualizar botões em uma barra de ferramentas, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="08447-111">You can use the **SelChange** event to check the various properties that give information about the current selection (such as [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) so you can update buttons in a toolbar, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="08447-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08447-112">Requirements</span></span>



| <span data-ttu-id="08447-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="08447-113">Requirement</span></span> | <span data-ttu-id="08447-114">Valor</span><span class="sxs-lookup"><span data-stu-id="08447-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08447-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08447-115">Minimum supported client</span></span><br/> | <span data-ttu-id="08447-116">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="08447-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="08447-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08447-117">Minimum supported server</span></span><br/> | <span data-ttu-id="08447-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="08447-118">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="08447-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08447-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="08447-120"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="08447-120"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="08447-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08447-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="08447-122"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08447-122"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="08447-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="08447-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08447-124">InkEdit</span><span class="sxs-lookup"><span data-stu-id="08447-124">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




