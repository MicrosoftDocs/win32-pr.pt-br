---
title: Método IWMPDVD topMenu
description: O método topMenu para a reprodução e exibe o menu superior (ou raiz) do título atual.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- método topMenu Windows Media Player
- método topMenu Windows Media Player, interface IWMPDVD
- Interface IWMPDVD Windows Media Player, método topMenu
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762470"
---
# <a name="iwmpdvdtopmenu-method"></a><span data-ttu-id="7e161-106">Método IWMPDVD:: topMenu</span><span class="sxs-lookup"><span data-stu-id="7e161-106">IWMPDVD::topMenu method</span></span>

<span data-ttu-id="7e161-107">O método **topMenu** para a reprodução e exibe o menu superior (ou raiz) do título atual.</span><span class="sxs-lookup"><span data-stu-id="7e161-107">The **topMenu** method stops playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e161-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e161-108">Syntax</span></span>


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a><span data-ttu-id="7e161-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e161-109">Parameters</span></span>

<span data-ttu-id="7e161-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7e161-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e161-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e161-111">Return value</span></span>

<span data-ttu-id="7e161-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7e161-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e161-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e161-113">Remarks</span></span>

<span data-ttu-id="7e161-114">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="7e161-114">Every DVD is authored differently.</span></span> <span data-ttu-id="7e161-115">O DVD deve conter um menu para que esse método funcione.</span><span class="sxs-lookup"><span data-stu-id="7e161-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="7e161-116">Alguns DVDs são criados para que os métodos **topMenu** e **IWMPDVD. titleMenu** Abram o mesmo menu.</span><span class="sxs-lookup"><span data-stu-id="7e161-116">Some DVDs are authored so that the **topMenu** and **IWMPDVD.titleMenu** methods open the same menu.</span></span> <span data-ttu-id="7e161-117">O método **topMenu** geralmente invoca o menu superior (ou raiz), mas ele pode invocar o menu de título se não houver nenhum menu raiz disponível.</span><span class="sxs-lookup"><span data-stu-id="7e161-117">The **topMenu** method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e161-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e161-118">Requirements</span></span>



| <span data-ttu-id="7e161-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e161-119">Requirement</span></span> | <span data-ttu-id="7e161-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7e161-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e161-121">Versão</span><span class="sxs-lookup"><span data-stu-id="7e161-121">Version</span></span><br/>   | <span data-ttu-id="7e161-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7e161-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7e161-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e161-123">Namespace</span></span><br/> | <span data-ttu-id="7e161-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7e161-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7e161-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="7e161-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7e161-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7e161-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e161-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e161-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e161-128">**Interface IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7e161-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e161-129">**IWMPDVD. titleMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7e161-129">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





