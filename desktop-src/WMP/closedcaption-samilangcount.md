---
title: ClosedCaption.SAMILangCount
description: A propriedade SAMILangCount recupera o número de idiomas com suporte pelo arquivo SAMI atual.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- ClosedCaption. SAMILangCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783622"
---
# <a name="closedcaptionsamilangcount"></a><span data-ttu-id="e09d9-104">ClosedCaption.SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="e09d9-104">ClosedCaption.SAMILangCount</span></span>

<span data-ttu-id="e09d9-105">A propriedade **SAMILangCount** recupera o número de idiomas com suporte pelo arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="e09d9-105">The **SAMILangCount** property retrieves the number of languages supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a><span data-ttu-id="e09d9-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e09d9-106">Possible Values</span></span>

<span data-ttu-id="e09d9-107">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e09d9-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e09d9-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e09d9-108">Remarks</span></span>

<span data-ttu-id="e09d9-109">Esse método não pode ser usado até que um arquivo de mídia digital esteja aberto (*Player*.**OpenState** é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="e09d9-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="e09d9-110">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.</span><span class="sxs-lookup"><span data-stu-id="e09d9-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e09d9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e09d9-111">Requirements</span></span>



| <span data-ttu-id="e09d9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e09d9-112">Requirement</span></span> | <span data-ttu-id="e09d9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e09d9-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e09d9-114">Versão</span><span class="sxs-lookup"><span data-stu-id="e09d9-114">Version</span></span><br/> | <span data-ttu-id="e09d9-115">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e09d9-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e09d9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e09d9-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="e09d9-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e09d9-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09d9-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e09d9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09d9-119">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="e09d9-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="e09d9-120">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="e09d9-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="e09d9-121">**ClosedCaption.getSAMILangName**</span><span class="sxs-lookup"><span data-stu-id="e09d9-121">**ClosedCaption.getSAMILangName**</span></span>](closedcaption-getsamilangname.md)
</dt> <dt>

[<span data-ttu-id="e09d9-122">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="e09d9-122">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





