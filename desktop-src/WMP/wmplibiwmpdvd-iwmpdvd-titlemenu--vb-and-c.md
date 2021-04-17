---
title: Método IWMPDVD titleMenu
description: O método titleMenu para a reprodução e exibe o menu título.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- método titleMenu Windows Media Player
- método titleMenu Windows Media Player, interface IWMPDVD
- Interface IWMPDVD Windows Media Player, método titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748307"
---
# <a name="iwmpdvdtitlemenu-method"></a><span data-ttu-id="f6d69-106">Método IWMPDVD:: titleMenu</span><span class="sxs-lookup"><span data-stu-id="f6d69-106">IWMPDVD::titleMenu method</span></span>

<span data-ttu-id="f6d69-107">O método **titleMenu** para a reprodução e exibe o menu título.</span><span class="sxs-lookup"><span data-stu-id="f6d69-107">The **titleMenu** method stops playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d69-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6d69-108">Syntax</span></span>


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a><span data-ttu-id="f6d69-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6d69-109">Parameters</span></span>

<span data-ttu-id="f6d69-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f6d69-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6d69-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6d69-111">Return value</span></span>

<span data-ttu-id="f6d69-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f6d69-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6d69-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6d69-113">Remarks</span></span>

<span data-ttu-id="f6d69-114">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="f6d69-114">Every DVD is authored differently.</span></span> <span data-ttu-id="f6d69-115">O DVD deve conter um menu para que esse método funcione.</span><span class="sxs-lookup"><span data-stu-id="f6d69-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="f6d69-116">Alguns DVDs são criados para que os métodos **IWMPDVD. topMenu** e **titleMenu** Abram o mesmo menu.</span><span class="sxs-lookup"><span data-stu-id="f6d69-116">Some DVDs are authored so that the **IWMPDVD.topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="f6d69-117">O método **titleMenu** geralmente invoca o menu title, mas ele pode invocar o menu superior se não houver nenhum menu de título disponível.</span><span class="sxs-lookup"><span data-stu-id="f6d69-117">The **titleMenu** method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d69-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6d69-118">Requirements</span></span>



| <span data-ttu-id="f6d69-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6d69-119">Requirement</span></span> | <span data-ttu-id="f6d69-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f6d69-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d69-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f6d69-121">Version</span></span><br/>   | <span data-ttu-id="f6d69-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f6d69-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f6d69-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6d69-123">Namespace</span></span><br/> | <span data-ttu-id="f6d69-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f6d69-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f6d69-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="f6d69-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f6d69-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f6d69-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d69-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6d69-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d69-128">**Interface IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f6d69-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f6d69-129">**IWMPDVD. topMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f6d69-129">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





