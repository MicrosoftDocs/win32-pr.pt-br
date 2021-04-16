---
title: Propriedade IWMPCdromBurn burnProgress
description: A propriedade burnProgress Obtém o progresso da gravação do CD como porcentagem concluída.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- Propriedade burnProgress Windows Media Player
- Propriedade burnProgress Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, Propriedade burnProgress
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761634"
---
# <a name="iwmpcdromburnburnprogress-property"></a><span data-ttu-id="186df-106">Propriedade IWMPCdromBurn:: burnProgress</span><span class="sxs-lookup"><span data-stu-id="186df-106">IWMPCdromBurn::burnProgress property</span></span>

<span data-ttu-id="186df-107">A propriedade **burnProgress** Obtém o progresso da gravação do CD como porcentagem concluída.</span><span class="sxs-lookup"><span data-stu-id="186df-107">The **burnProgress** property gets the CD burning progress as percent complete.</span></span>

<span data-ttu-id="186df-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="186df-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="186df-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="186df-109">Syntax</span></span>


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="186df-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="186df-110">Property value</span></span>

<span data-ttu-id="186df-111">Um **System. Int32** que é o valor de progresso.</span><span class="sxs-lookup"><span data-stu-id="186df-111">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="186df-112">Os valores de progresso variam de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="186df-112">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="186df-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="186df-113">Remarks</span></span>

<span data-ttu-id="186df-114">O valor de progresso representa a porcentagem completa de todo o processo de gravação, incluindo as operações de preparo.</span><span class="sxs-lookup"><span data-stu-id="186df-114">The progress value represents the completed percentage of the entire burning process, including any staging operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="186df-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="186df-115">Requirements</span></span>



| <span data-ttu-id="186df-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="186df-116">Requirement</span></span> | <span data-ttu-id="186df-117">Valor</span><span class="sxs-lookup"><span data-stu-id="186df-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186df-118">Versão</span><span class="sxs-lookup"><span data-stu-id="186df-118">Version</span></span><br/>   | <span data-ttu-id="186df-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="186df-119">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="186df-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="186df-120">Namespace</span></span><br/> | <span data-ttu-id="186df-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="186df-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="186df-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="186df-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="186df-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="186df-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186df-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="186df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186df-125">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="186df-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





