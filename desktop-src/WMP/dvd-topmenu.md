---
title: Método DVD. topMenu
description: O método topMenu interrompe a reprodução do título e exibe o menu superior (ou raiz) do título atual.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- método topMenu Windows Media Player
- método topMenu Windows Media Player, classe de DVD
- Classe DVD Windows Media Player, método topMenu
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455367"
---
# <a name="dvdtopmenu-method"></a><span data-ttu-id="9c895-106">Método DVD. topMenu</span><span class="sxs-lookup"><span data-stu-id="9c895-106">DVD.topMenu method</span></span>

<span data-ttu-id="9c895-107">O método **topMenu** interrompe a reprodução do título e exibe o menu superior (ou raiz) do título atual.</span><span class="sxs-lookup"><span data-stu-id="9c895-107">The **topMenu** method stops title playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c895-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c895-108">Syntax</span></span>


```JScript
DVD.topMenu()
```



## <a name="parameters"></a><span data-ttu-id="9c895-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c895-109">Parameters</span></span>

<span data-ttu-id="9c895-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9c895-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c895-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c895-111">Return value</span></span>

<span data-ttu-id="9c895-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9c895-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c895-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c895-113">Remarks</span></span>

<span data-ttu-id="9c895-114">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="9c895-114">Every DVD is authored differently.</span></span> <span data-ttu-id="9c895-115">O DVD deve conter um menu para que esse método funcione.</span><span class="sxs-lookup"><span data-stu-id="9c895-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="9c895-116">Alguns DVDs são criados para que os métodos **topMenu** e **titleMenu** Abram o mesmo menu.</span><span class="sxs-lookup"><span data-stu-id="9c895-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="9c895-117">O método **topMenu** geralmente invoca o menu superior (ou raiz), mas ele pode invocar o menu de título, se não houver nenhum menu raiz disponível.</span><span class="sxs-lookup"><span data-stu-id="9c895-117">The **topMenu** method usually invokes the top (or root) menu but it may invoke the title menu instead, if there is no root menu available.</span></span>

<span data-ttu-id="9c895-118">**Windows Media Player 10 Mobile:** Esse método sempre tem sucesso, mas não executa a operação pretendida.</span><span class="sxs-lookup"><span data-stu-id="9c895-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c895-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c895-119">Requirements</span></span>



| <span data-ttu-id="9c895-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c895-120">Requirement</span></span> | <span data-ttu-id="9c895-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9c895-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c895-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c895-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9c895-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9c895-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c895-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c895-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9c895-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c895-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c895-126">Versão</span><span class="sxs-lookup"><span data-stu-id="9c895-126">Version</span></span><br/>                  | <span data-ttu-id="9c895-127">Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9c895-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="9c895-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9c895-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c895-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c895-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c895-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9c895-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c895-131">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="9c895-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="9c895-132">**DVD. titleMenu**</span><span class="sxs-lookup"><span data-stu-id="9c895-132">**DVD.titleMenu**</span></span>](dvd-titlemenu.md)
</dt> </dl>

 

 





