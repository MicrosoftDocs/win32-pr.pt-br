---
title: Método de etapa IWMPControls2
description: O método Step faz com que o item de mídia de vídeo atual passe para o próximo quadro ou para o quadro anterior e congele a reprodução.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- método Step Windows Media Player
- método Step Windows Media Player, interface IWMPControls2
- Interface IWMPControls2 Windows Media Player, método Step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784053"
---
# <a name="iwmpcontrols2step-method"></a><span data-ttu-id="0ea5d-106">Método IWMPControls2:: Step</span><span class="sxs-lookup"><span data-stu-id="0ea5d-106">IWMPControls2::step method</span></span>

<span data-ttu-id="0ea5d-107">O método **Step** faz com que o item de mídia de vídeo atual passe para o próximo quadro ou para o quadro anterior e congele a reprodução.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-107">The **step** method causes the current video media item to step to the next frame or the previous frame and freeze playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea5d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ea5d-108">Syntax</span></span>


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a><span data-ttu-id="0ea5d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ea5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea5d-110">*lStep* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0ea5d-110">*lStep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea5d-111">Um valor **System. Int32** que indica quantos quadros depurar antes de congelar.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-111">A **System.Int32** value indicating how many frames to step before freezing.</span></span> <span data-ttu-id="0ea5d-112">Deve ser definido como 1 ou-1.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-112">Must be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea5d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ea5d-113">Return value</span></span>

<span data-ttu-id="0ea5d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea5d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ea5d-115">Remarks</span></span>

<span data-ttu-id="0ea5d-116">Esse método atualmente dá suporte apenas aos parâmetros 1 ou-1, de modo que você só pode passar um quadro por vez.</span><span class="sxs-lookup"><span data-stu-id="0ea5d-116">This method currently supports only the parameters 1 or -1, so you can only step one frame at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea5d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ea5d-117">Requirements</span></span>



| <span data-ttu-id="0ea5d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ea5d-118">Requirement</span></span> | <span data-ttu-id="0ea5d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0ea5d-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea5d-120">Versão</span><span class="sxs-lookup"><span data-stu-id="0ea5d-120">Version</span></span><br/>   | <span data-ttu-id="0ea5d-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0ea5d-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0ea5d-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ea5d-122">Namespace</span></span><br/> | <span data-ttu-id="0ea5d-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0ea5d-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ea5d-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="0ea5d-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ea5d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea5d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ea5d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea5d-127">**Interface IWMPControls2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0ea5d-127">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ea5d-128">**Interface IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0ea5d-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





