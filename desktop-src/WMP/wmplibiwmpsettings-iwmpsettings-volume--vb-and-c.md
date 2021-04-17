---
title: Propriedade de volume IWMPSettings
description: A propriedade volume Obtém ou define o volume de reprodução atual.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Propriedade de volume Windows Media Player
- Propriedade de volume Windows Media Player, interface IWMPSettings
- Interface IWMPSettings do Windows Media Player, propriedade de volume
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782870"
---
# <a name="iwmpsettingsvolume-property"></a><span data-ttu-id="10ac0-106">Propriedade IWMPSettings:: volume</span><span class="sxs-lookup"><span data-stu-id="10ac0-106">IWMPSettings::volume property</span></span>

<span data-ttu-id="10ac0-107">A propriedade **volume** Obtém ou define o volume de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="10ac0-107">The **volume** property gets or sets the current playback volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ac0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="10ac0-108">Syntax</span></span>


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="10ac0-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="10ac0-109">Property value</span></span>

<span data-ttu-id="10ac0-110">Um **System. Int32** que é o nível de volume, variando de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="10ac0-110">A **System.Int32** that is the volume level, ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="10ac0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="10ac0-111">Remarks</span></span>

<span data-ttu-id="10ac0-112">Um valor de zero não especifica nenhum volume (mudo).</span><span class="sxs-lookup"><span data-stu-id="10ac0-112">A value of zero specifies no volume (muted).</span></span> <span data-ttu-id="10ac0-113">Um valor de 100 especifica o volume completo.</span><span class="sxs-lookup"><span data-stu-id="10ac0-113">A value of 100 specifies full volume.</span></span> <span data-ttu-id="10ac0-114">Se nenhum valor for especificado para essa propriedade, o padrão será a última configuração de volume estabelecida para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="10ac0-114">If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="10ac0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10ac0-115">Requirements</span></span>



| <span data-ttu-id="10ac0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ac0-116">Requirement</span></span> | <span data-ttu-id="10ac0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="10ac0-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ac0-118">Versão</span><span class="sxs-lookup"><span data-stu-id="10ac0-118">Version</span></span><br/>   | <span data-ttu-id="10ac0-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="10ac0-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="10ac0-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="10ac0-120">Namespace</span></span><br/> | <span data-ttu-id="10ac0-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="10ac0-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="10ac0-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="10ac0-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="10ac0-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="10ac0-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ac0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="10ac0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ac0-125">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="10ac0-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





