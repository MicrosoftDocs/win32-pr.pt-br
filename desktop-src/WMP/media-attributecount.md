---
title: Media. attributeCount
description: A propriedade attributeCount recupera o número de atributos que podem ser consultados e/ou definidos para o item de mídia.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media. attributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763305"
---
# <a name="mediaattributecount"></a><span data-ttu-id="2a0d9-104">Media. attributeCount</span><span class="sxs-lookup"><span data-stu-id="2a0d9-104">Media.attributeCount</span></span>

<span data-ttu-id="2a0d9-105">A propriedade **attributeCount** recupera o número de atributos que podem ser consultados e/ou definidos para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2a0d9-105">The **attributeCount** property retrieves the number of attributes that can be queried and/or set for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a0d9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a0d9-106">Syntax</span></span>

<span data-ttu-id="2a0d9-107">*Player*. *currentMedia*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="2a0d9-107">*player*.*currentMedia*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="2a0d9-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2a0d9-108">Possible Values</span></span>

<span data-ttu-id="2a0d9-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="2a0d9-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a0d9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a0d9-110">Remarks</span></span>

<span data-ttu-id="2a0d9-111">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2a0d9-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="2a0d9-112">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2a0d9-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2a0d9-113">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2a0d9-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="2a0d9-114">**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="2a0d9-114">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="2a0d9-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a0d9-115">Examples</span></span>

<span data-ttu-id="2a0d9-116">O exemplo de JScript a seguir usa *mídia*. **attributeCount** para determinar o número de atributos disponíveis no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="2a0d9-116">The following JScript example uses *Media*.**attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="2a0d9-117">O código usa esse valor para imprimir uma lista de nomes e valores de atributos em uma área de texto HTML, chamada mytext.</span><span class="sxs-lookup"><span data-stu-id="2a0d9-117">The code uses that value to print a list of attribute names and values in an HTML text area, named myText.</span></span> <span data-ttu-id="2a0d9-118">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2a0d9-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="2a0d9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a0d9-119">Requirements</span></span>



| <span data-ttu-id="2a0d9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a0d9-120">Requirement</span></span> | <span data-ttu-id="2a0d9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2a0d9-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a0d9-122">Versão</span><span class="sxs-lookup"><span data-stu-id="2a0d9-122">Version</span></span><br/> | <span data-ttu-id="2a0d9-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2a0d9-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2a0d9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2a0d9-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a0d9-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a0d9-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a0d9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a0d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a0d9-127">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="2a0d9-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="2a0d9-128">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="2a0d9-128">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="2a0d9-129">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2a0d9-129">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2a0d9-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2a0d9-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2a0d9-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2a0d9-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





