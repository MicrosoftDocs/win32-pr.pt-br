---
title: Propriedade do rótulo IWMPCdromBurn
description: A propriedade Label Obtém a cadeia de caracteres do rótulo do volume do CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- Propriedade de rótulo Windows Media Player
- Propriedade de rótulo Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, Propriedade Label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780376"
---
# <a name="iwmpcdromburnlabel-property"></a><span data-ttu-id="4c54e-106">Propriedade IWMPCdromBurn:: Label</span><span class="sxs-lookup"><span data-stu-id="4c54e-106">IWMPCdromBurn::label property</span></span>

<span data-ttu-id="4c54e-107">A propriedade *Label* Obtém a cadeia de caracteres do rótulo do volume do CD.</span><span class="sxs-lookup"><span data-stu-id="4c54e-107">The *label* property gets the CD volume label string.</span></span>

<span data-ttu-id="4c54e-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4c54e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c54e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c54e-109">Syntax</span></span>


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a><span data-ttu-id="4c54e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4c54e-110">Property value</span></span>

<span data-ttu-id="4c54e-111">Um **System. String** que é a cadeia de caracteres do rótulo do volume.</span><span class="sxs-lookup"><span data-stu-id="4c54e-111">A **System.String** that is the volume label string.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c54e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c54e-112">Remarks</span></span>

<span data-ttu-id="4c54e-113">Devido à maneira como os rótulos de CD são armazenados, o rótulo do CD pode ser menor do que o comprimento da cadeia de caracteres do rótulo de volume especificado.</span><span class="sxs-lookup"><span data-stu-id="4c54e-113">Due to the way CD labels are stored, the label of the CD may be shorter than the length of the specified volume label string.</span></span> <span data-ttu-id="4c54e-114">Se a cadeia de caracteres for maior do que o comprimento máximo de um rótulo de CD, o texto será truncado.</span><span class="sxs-lookup"><span data-stu-id="4c54e-114">If the string is longer than the maximum length of a CD label, the text will be truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c54e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c54e-115">Requirements</span></span>



| <span data-ttu-id="4c54e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c54e-116">Requirement</span></span> | <span data-ttu-id="4c54e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4c54e-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c54e-118">Versão</span><span class="sxs-lookup"><span data-stu-id="4c54e-118">Version</span></span><br/>   | <span data-ttu-id="4c54e-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="4c54e-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="4c54e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c54e-120">Namespace</span></span><br/> | <span data-ttu-id="4c54e-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4c54e-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4c54e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="4c54e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c54e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4c54e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c54e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c54e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c54e-125">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4c54e-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





