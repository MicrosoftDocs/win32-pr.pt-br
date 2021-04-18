---
title: BOTÃO de opção. Radio
description: O atributo Radio especifica ou recupera um valor que indica se o botão é composto por botões de opção.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- O Windows Media Player. Radio
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784907"
---
# <a name="buttongroupradio"></a><span data-ttu-id="94ce0-104">BOTÃO de opção. Radio</span><span class="sxs-lookup"><span data-stu-id="94ce0-104">BUTTONGROUP.radio</span></span>

<span data-ttu-id="94ce0-105">O atributo **Radio** especifica ou recupera um valor que indica se o **botão** é composto por botões de opção.</span><span class="sxs-lookup"><span data-stu-id="94ce0-105">The **radio** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>

``` syntax
        elementID.radio
```

## <a name="possible-values"></a><span data-ttu-id="94ce0-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="94ce0-106">Possible Values</span></span>

<span data-ttu-id="94ce0-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="94ce0-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="94ce0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="94ce0-108">Value</span></span> | <span data-ttu-id="94ce0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="94ce0-109">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="94ce0-110">true</span><span class="sxs-lookup"><span data-stu-id="94ce0-110">true</span></span>  | <span data-ttu-id="94ce0-111">O tipo de **botão** é estilo de rádio.</span><span class="sxs-lookup"><span data-stu-id="94ce0-111">The **BUTTONGROUP** is radio style.</span></span>              |
| <span data-ttu-id="94ce0-112">false</span><span class="sxs-lookup"><span data-stu-id="94ce0-112">false</span></span> | <span data-ttu-id="94ce0-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="94ce0-113">Default.</span></span> <span data-ttu-id="94ce0-114">O **botão** de opção não é estilo de rádio.</span><span class="sxs-lookup"><span data-stu-id="94ce0-114">The **BUTTONGROUP** is not radio style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="94ce0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="94ce0-115">Remarks</span></span>

<span data-ttu-id="94ce0-116">Se **Radio** for definido como true, todos os elementos **buttonelement** no grupo de **botões** serão adesivos, mas apenas um botão por vez estará no estado inoperante.</span><span class="sxs-lookup"><span data-stu-id="94ce0-116">If **radio** is set to true, all the **BUTTONELEMENT** elements in the **BUTTONGROUP** will be sticky, but only one button at a time will be in the down state.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ce0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94ce0-117">Requirements</span></span>



| <span data-ttu-id="94ce0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ce0-118">Requirement</span></span> | <span data-ttu-id="94ce0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="94ce0-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="94ce0-120">Versão</span><span class="sxs-lookup"><span data-stu-id="94ce0-120">Version</span></span><br/> | <span data-ttu-id="94ce0-121">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="94ce0-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94ce0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="94ce0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ce0-123">**BUTTONelement. adesivo**</span><span class="sxs-lookup"><span data-stu-id="94ce0-123">**BUTTONELEMENT.sticky**</span></span>](buttonelement-sticky.md)
</dt> <dt>

[<span data-ttu-id="94ce0-124">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="94ce0-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





