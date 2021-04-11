---
title: Método DVD. titleMenu
description: O método titleMenu interrompe a reprodução do título e exibe o menu título.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- método titleMenu Windows Media Player
- método titleMenu Windows Media Player, classe de DVD
- Classe DVD Windows Media Player, método titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295766"
---
# <a name="dvdtitlemenu-method"></a><span data-ttu-id="b7c28-106">Método DVD. titleMenu</span><span class="sxs-lookup"><span data-stu-id="b7c28-106">DVD.titleMenu method</span></span>

<span data-ttu-id="b7c28-107">O método **titleMenu** interrompe a reprodução do título e exibe o menu título.</span><span class="sxs-lookup"><span data-stu-id="b7c28-107">The **titleMenu** method stops title playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c28-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7c28-108">Syntax</span></span>


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a><span data-ttu-id="b7c28-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7c28-109">Parameters</span></span>

<span data-ttu-id="b7c28-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b7c28-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7c28-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7c28-111">Return value</span></span>

<span data-ttu-id="b7c28-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b7c28-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7c28-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7c28-113">Remarks</span></span>

<span data-ttu-id="b7c28-114">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="b7c28-114">Every DVD is authored differently.</span></span> <span data-ttu-id="b7c28-115">O DVD deve conter um menu para que esse método funcione.</span><span class="sxs-lookup"><span data-stu-id="b7c28-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="b7c28-116">Alguns DVDs são criados para que os métodos **topMenu** e **titleMenu** Abram o mesmo menu.</span><span class="sxs-lookup"><span data-stu-id="b7c28-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="b7c28-117">O método **titleMenu** geralmente invoca o menu de título, mas ele pode invocar o menu superior, se não houver nenhum menu de título disponível.</span><span class="sxs-lookup"><span data-stu-id="b7c28-117">The **titleMenu** method usually invokes the title menu but it may invoke the top menu instead, if there is no title menu available.</span></span>

<span data-ttu-id="b7c28-118">**Windows Media Player 10 Mobile:** Esse método sempre tem sucesso, mas não executa a operação pretendida.</span><span class="sxs-lookup"><span data-stu-id="b7c28-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c28-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7c28-119">Requirements</span></span>



| <span data-ttu-id="b7c28-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7c28-120">Requirement</span></span> | <span data-ttu-id="b7c28-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b7c28-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c28-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7c28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c28-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b7c28-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7c28-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7c28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c28-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7c28-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b7c28-126">Versão</span><span class="sxs-lookup"><span data-stu-id="b7c28-126">Version</span></span><br/>                  | <span data-ttu-id="b7c28-127">Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b7c28-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="b7c28-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b7c28-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7c28-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7c28-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c28-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7c28-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c28-131">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="b7c28-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="b7c28-132">**DVD. topMenu**</span><span class="sxs-lookup"><span data-stu-id="b7c28-132">**DVD.topMenu**</span></span>](dvd-topmenu.md)
</dt> </dl>

 

 





