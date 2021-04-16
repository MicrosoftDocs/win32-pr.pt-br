---
title: ClosedCaption.SAMIStyleCount
description: A propriedade SAMIStyleCount recupera o número de estilos com suporte pelo arquivo SAMI atual.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- ClosedCaption. SAMIStyleCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761478"
---
# <a name="closedcaptionsamistylecount"></a><span data-ttu-id="aecad-104">ClosedCaption.SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="aecad-104">ClosedCaption.SAMIStyleCount</span></span>

<span data-ttu-id="aecad-105">A propriedade **SAMIStyleCount** recupera o número de estilos com suporte pelo arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="aecad-105">The **SAMIStyleCount** property retrieves the number of styles supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a><span data-ttu-id="aecad-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="aecad-106">Possible Values</span></span>

<span data-ttu-id="aecad-107">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="aecad-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="aecad-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="aecad-108">Remarks</span></span>

<span data-ttu-id="aecad-109">Esse método não pode ser usado até que um arquivo de mídia digital esteja aberto (*Player*.**OpenState** é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="aecad-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="aecad-110">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.</span><span class="sxs-lookup"><span data-stu-id="aecad-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="aecad-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aecad-111">Requirements</span></span>



| <span data-ttu-id="aecad-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aecad-112">Requirement</span></span> | <span data-ttu-id="aecad-113">Valor</span><span class="sxs-lookup"><span data-stu-id="aecad-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aecad-114">Versão</span><span class="sxs-lookup"><span data-stu-id="aecad-114">Version</span></span><br/> | <span data-ttu-id="aecad-115">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="aecad-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="aecad-116">DLL</span><span class="sxs-lookup"><span data-stu-id="aecad-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="aecad-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aecad-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aecad-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="aecad-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aecad-119">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="aecad-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="aecad-120">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="aecad-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="aecad-121">**ClosedCaption.getSAMIStyleName**</span><span class="sxs-lookup"><span data-stu-id="aecad-121">**ClosedCaption.getSAMIStyleName**</span></span>](closedcaption-getsamistylename.md)
</dt> <dt>

[<span data-ttu-id="aecad-122">**ClosedCaption. SAMIstyle**</span><span class="sxs-lookup"><span data-stu-id="aecad-122">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





