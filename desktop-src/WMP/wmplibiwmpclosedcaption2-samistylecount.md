---
title: Propriedade IWMPClosedCaption2 SAMIStyleCount
description: A propriedade SAMIStyleCount Obtém o número de estilos com suporte pelo arquivo SAMI atual.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Propriedade SAMIStyleCount Windows Media Player
- Propriedade SAMIStyleCount Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, Propriedade SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761927"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a><span data-ttu-id="9c3fd-106">Propriedade IWMPClosedCaption2:: SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="9c3fd-106">IWMPClosedCaption2::SAMIStyleCount property</span></span>

<span data-ttu-id="9c3fd-107">A propriedade **SAMIStyleCount** Obtém o número de estilos com suporte pelo arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="9c3fd-107">The **SAMIStyleCount** property gets the number of styles supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c3fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c3fd-108">Syntax</span></span>


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="9c3fd-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9c3fd-109">Property value</span></span>

<span data-ttu-id="9c3fd-110">Um **System. Int32** que é o número de estilos.</span><span class="sxs-lookup"><span data-stu-id="9c3fd-110">A **System.Int32** that is the number of styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c3fd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c3fd-111">Remarks</span></span>

<span data-ttu-id="9c3fd-112">Essa propriedade retorna 0, a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="9c3fd-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c3fd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c3fd-113">Requirements</span></span>



| <span data-ttu-id="9c3fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c3fd-114">Requirement</span></span> | <span data-ttu-id="9c3fd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9c3fd-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c3fd-116">Versão</span><span class="sxs-lookup"><span data-stu-id="9c3fd-116">Version</span></span><br/>   | <span data-ttu-id="9c3fd-117">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9c3fd-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9c3fd-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c3fd-118">Namespace</span></span><br/> | <span data-ttu-id="9c3fd-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9c3fd-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9c3fd-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="9c3fd-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9c3fd-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9c3fd-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c3fd-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c3fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c3fd-123">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="9c3fd-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="9c3fd-124">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9c3fd-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9c3fd-125">**IWMPClosedCaption. SAMIstyle (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9c3fd-125">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9c3fd-126">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9c3fd-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9c3fd-127">**IWMPClosedCaption2. getSAMIStyleName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9c3fd-127">**IWMPClosedCaption2.getSAMIStyleName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





