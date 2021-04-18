---
title: Interface IWMPControls2 (VB e C) (Wmp.h)
description: Fornece um método que complementa a interface IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB e C) interface do Windows Media Player
- IWMPControls2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760253"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a><span data-ttu-id="9601e-105">Interface IWMPControls2 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="9601e-105">IWMPControls2 (VB and C#) interface</span></span>

<span data-ttu-id="9601e-106">Fornece um método que complementa a interface [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .</span><span class="sxs-lookup"><span data-stu-id="9601e-106">Provides a method that supplements the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) interface.</span></span>

## <a name="members"></a><span data-ttu-id="9601e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9601e-107">Members</span></span>

<span data-ttu-id="9601e-108">A interface **IWMPControls2 (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9601e-108">The **IWMPControls2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="9601e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9601e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9601e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9601e-110">Methods</span></span>

<span data-ttu-id="9601e-111">A interface **IWMPControls2 (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9601e-111">The **IWMPControls2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="9601e-112">Método</span><span class="sxs-lookup"><span data-stu-id="9601e-112">Method</span></span>                                                           | <span data-ttu-id="9601e-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="9601e-113">Description</span></span>                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9601e-114">**etapa**</span><span class="sxs-lookup"><span data-stu-id="9601e-114">**step**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | <span data-ttu-id="9601e-115">Move o item de mídia de vídeo atual para o próximo quadro ou para o quadro anterior e congela a reprodução.</span><span class="sxs-lookup"><span data-stu-id="9601e-115">Moves the current video media item to the next frame or the previous frame and freezes playback.</span></span><br/> |



 

<span data-ttu-id="9601e-116">O código de exemplo a seguir mostra como acessar uma interface [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) .</span><span class="sxs-lookup"><span data-stu-id="9601e-116">The following example code shows how to access an [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) interface.</span></span> <span data-ttu-id="9601e-117">O código de exemplo converte o valor [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) que a propriedade [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) retorna a um valor **IWMPControls2** .</span><span class="sxs-lookup"><span data-stu-id="9601e-117">The example code casts the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) value that the [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) property returns to a **IWMPControls2** value.</span></span>

<span data-ttu-id="9601e-118">Para **C#**:</span><span class="sxs-lookup"><span data-stu-id="9601e-118">For **C#**:</span></span>


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



<span data-ttu-id="9601e-119">Para **VB**:</span><span class="sxs-lookup"><span data-stu-id="9601e-119">For **VB**:</span></span>


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a><span data-ttu-id="9601e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9601e-120">Requirements</span></span>



| <span data-ttu-id="9601e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9601e-121">Requirement</span></span> | <span data-ttu-id="9601e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9601e-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9601e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9601e-123">Header</span></span><br/> | <dl> <span data-ttu-id="9601e-124"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="9601e-124"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9601e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9601e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9601e-126">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="9601e-126">**IWMPControls**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[<span data-ttu-id="9601e-127">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="9601e-127">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="9601e-128">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9601e-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9601e-129">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9601e-129">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





