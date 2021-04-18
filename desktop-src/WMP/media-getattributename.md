---
title: Método Media. GetAttributeName
description: O método GetAttributeName recupera o nome do atributo correspondente ao índice especificado.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- método GetAttributeName do Windows Media Player
- método GetAttributeName do Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método GetAttributeName
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781553"
---
# <a name="mediagetattributename-method"></a><span data-ttu-id="25f21-106">Método Media. GetAttributeName</span><span class="sxs-lookup"><span data-stu-id="25f21-106">Media.getAttributeName method</span></span>

<span data-ttu-id="25f21-107">O método **GetAttributeName** recupera o nome do atributo correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="25f21-107">The **getAttributeName** method retrieves the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f21-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f21-108">Syntax</span></span>


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="25f21-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25f21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25f21-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="25f21-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25f21-111">**Número** (**longo**) que contém o índice do atributo.</span><span class="sxs-lookup"><span data-stu-id="25f21-111">**Number** (**long**) containing the index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25f21-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25f21-112">Return value</span></span>

<span data-ttu-id="25f21-113">Esse método retorna uma **cadeia de caracteres** especificando o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="25f21-113">This method returns a **String** specifying the name of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="25f21-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="25f21-114">Remarks</span></span>

<span data-ttu-id="25f21-115">O nome do atributo retornado pode ser usado em conjunto com **getItemInfo** para recuperar o valor de um atributo nomeado específico.</span><span class="sxs-lookup"><span data-stu-id="25f21-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="25f21-116">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="25f21-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="25f21-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="25f21-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="25f21-118">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player..</span><span class="sxs-lookup"><span data-stu-id="25f21-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="25f21-119">**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="25f21-119">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="25f21-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25f21-120">Examples</span></span>

<span data-ttu-id="25f21-121">O exemplo de JScript a seguir usa *mídia*. **GetAttributeName** para preencher uma área de texto HTML chamada MyText com o índice e o nome de cada atributo para o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="25f21-121">The following JScript example uses *Media*.**getAttributeName** to fill an HTML text area named myText with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="25f21-122">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="25f21-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="25f21-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f21-123">Requirements</span></span>



| <span data-ttu-id="25f21-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f21-124">Requirement</span></span> | <span data-ttu-id="25f21-125">Valor</span><span class="sxs-lookup"><span data-stu-id="25f21-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25f21-126">Versão</span><span class="sxs-lookup"><span data-stu-id="25f21-126">Version</span></span><br/> | <span data-ttu-id="25f21-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="25f21-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="25f21-128">DLL</span><span class="sxs-lookup"><span data-stu-id="25f21-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="25f21-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25f21-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f21-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="25f21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f21-131">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="25f21-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="25f21-132">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="25f21-132">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="25f21-133">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="25f21-133">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="25f21-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="25f21-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="25f21-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="25f21-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





