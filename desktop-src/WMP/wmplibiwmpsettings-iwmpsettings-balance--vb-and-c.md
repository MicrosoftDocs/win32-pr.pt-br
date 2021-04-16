---
title: Propriedade de saldo de IWMPSettings
description: A propriedade Balance Obtém ou define o saldo do estéreo atual.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Propriedade Balance Windows Media Player
- Propriedade Balance Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade Balance
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765031"
---
# <a name="iwmpsettingsbalance-property"></a><span data-ttu-id="6c334-106">Propriedade IWMPSettings:: Balance</span><span class="sxs-lookup"><span data-stu-id="6c334-106">IWMPSettings::balance property</span></span>

<span data-ttu-id="6c334-107">A propriedade **Balance** Obtém ou define o saldo do estéreo atual.</span><span class="sxs-lookup"><span data-stu-id="6c334-107">The **balance** property gets or sets the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c334-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c334-108">Syntax</span></span>


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6c334-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6c334-109">Property value</span></span>

<span data-ttu-id="6c334-110">Um **System. Int32** que é o valor de saldo.</span><span class="sxs-lookup"><span data-stu-id="6c334-110">A **System.Int32** that is the balance value.</span></span> <span data-ttu-id="6c334-111">Esse valor pode variar de 100 a 100.</span><span class="sxs-lookup"><span data-stu-id="6c334-111">This value can range from  100 to 100.</span></span> <span data-ttu-id="6c334-112">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="6c334-112">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c334-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c334-113">Remarks</span></span>

<span data-ttu-id="6c334-114">O valor zero indica que o áudio é reproduzido em um volume igual nos canais esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="6c334-114">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="6c334-115">Um valor de 100 indica que o áudio é reproduzido somente no canal à esquerda.</span><span class="sxs-lookup"><span data-stu-id="6c334-115">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="6c334-116">Um valor de 100 indica que o áudio é reproduzido somente no canal correto.</span><span class="sxs-lookup"><span data-stu-id="6c334-116">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c334-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c334-117">Requirements</span></span>



| <span data-ttu-id="6c334-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c334-118">Requirement</span></span> | <span data-ttu-id="6c334-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6c334-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c334-120">Versão</span><span class="sxs-lookup"><span data-stu-id="6c334-120">Version</span></span><br/>   | <span data-ttu-id="6c334-121">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6c334-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="6c334-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c334-122">Namespace</span></span><br/> | <span data-ttu-id="6c334-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6c334-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6c334-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="6c334-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6c334-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6c334-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c334-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c334-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c334-127">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6c334-127">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





