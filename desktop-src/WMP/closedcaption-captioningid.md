---
title: ClosedCaption.captioningID
description: A propriedade captioningID especifica ou recupera o nome do elemento que exibe a legenda.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption. captioningID Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781269"
---
# <a name="closedcaptioncaptioningid"></a><span data-ttu-id="5eb92-104">ClosedCaption.captioningID</span><span class="sxs-lookup"><span data-stu-id="5eb92-104">ClosedCaption.captioningID</span></span>

<span data-ttu-id="5eb92-105">A propriedade **captioningID** especifica ou recupera o nome do elemento que exibe a legenda.</span><span class="sxs-lookup"><span data-stu-id="5eb92-105">The **captioningID** property specifies or retrieves the name of the element displaying the captioning.</span></span>

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a><span data-ttu-id="5eb92-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5eb92-106">Possible Values</span></span>

<span data-ttu-id="5eb92-107">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5eb92-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb92-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5eb92-108">Remarks</span></span>

<span data-ttu-id="5eb92-109">O nome do elemento especificado pode ser qualquer elemento HTML na página da Web, contanto que dê suporte ao atributo innerHTML.</span><span class="sxs-lookup"><span data-stu-id="5eb92-109">The element name specified can be any HTML element in the webpage as long as it supports the innerHTML attribute.</span></span> <span data-ttu-id="5eb92-110">Se a página da Web contiver vários quadros, o nome do elemento só poderá fazer referência a um elemento no mesmo quadro que o controle do jogador.</span><span class="sxs-lookup"><span data-stu-id="5eb92-110">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Player control.</span></span>

<span data-ttu-id="5eb92-111">**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="5eb92-111">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="5eb92-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5eb92-112">Examples</span></span>

<span data-ttu-id="5eb92-113">O exemplo do Microsoft JScript a seguir usa *ClosedCaption*. **captioningID** para escolher a área de uma página da Web usada para exibir legendas.</span><span class="sxs-lookup"><span data-stu-id="5eb92-113">The following Microsoft JScript example uses *ClosedCaption*.**captioningID** to choose the area of a webpage used to display captions.</span></span> <span data-ttu-id="5eb92-114">Dois elementos HTML DIV foram criados, com ID = CC1 e ID = CC2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5eb92-114">Two HTML DIV elements were created, with ID = CC1 and ID = CC2, respectively.</span></span> <span data-ttu-id="5eb92-115">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5eb92-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a><span data-ttu-id="5eb92-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eb92-116">Requirements</span></span>



| <span data-ttu-id="5eb92-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eb92-117">Requirement</span></span> | <span data-ttu-id="5eb92-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5eb92-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb92-119">Versão</span><span class="sxs-lookup"><span data-stu-id="5eb92-119">Version</span></span><br/> | <span data-ttu-id="5eb92-120">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5eb92-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5eb92-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5eb92-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="5eb92-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5eb92-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eb92-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5eb92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb92-124">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="5eb92-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="5eb92-125">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="5eb92-125">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





