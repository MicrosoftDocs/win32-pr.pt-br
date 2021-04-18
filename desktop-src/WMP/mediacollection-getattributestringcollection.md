---
title: Método mediacollection. getAttributeStringCollection
description: O método getAttributeStringCollection recupera um objeto StringCollection que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia especificado.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- método getAttributeStringCollection Windows Media Player
- método getAttributeStringCollection Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782982"
---
# <a name="mediacollectiongetattributestringcollection-method"></a><span data-ttu-id="91c48-106">Método mediacollection. getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="91c48-106">MediaCollection.getAttributeStringCollection method</span></span>

<span data-ttu-id="91c48-107">O método **getAttributeStringCollection** recupera um objeto **StringCollection** que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="91c48-107">The **getAttributeStringCollection** method retrieves a **StringCollection** object representing the set of all values for a specified attribute within a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c48-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91c48-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="91c48-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91c48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c48-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91c48-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c48-111">**Cadeia de caracteres** que especifica o atributo.</span><span class="sxs-lookup"><span data-stu-id="91c48-111">**String** specifying the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="91c48-112">*MediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91c48-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91c48-113">**Cadeia de caracteres** que representa o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="91c48-113">**String** representing the media type.</span></span> <span data-ttu-id="91c48-114">Contém um dos seguintes valores: "áudio", "vídeo", "playlist" ou "outros".</span><span class="sxs-lookup"><span data-stu-id="91c48-114">Contains one of the following values: "Audio", "Video", "Playlist", or "Other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c48-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91c48-115">Return value</span></span>

<span data-ttu-id="91c48-116">Esse método retorna um objeto **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="91c48-116">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c48-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="91c48-117">Remarks</span></span>

<span data-ttu-id="91c48-118">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="91c48-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="91c48-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="91c48-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="91c48-120">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a seção [referência de atributo](attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="91c48-120">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md) section.</span></span>

## <a name="examples"></a><span data-ttu-id="91c48-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91c48-121">Examples</span></span>

<span data-ttu-id="91c48-122">O exemplo de JScript a seguir usa *mediacollection*. **getAttributeStringCollection** para exibir uma lista de valores que correspondem a um atributo específico para itens de áudio na coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="91c48-122">The following JScript example uses *MediaCollection*.**getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="91c48-123">Um elemento HTML SELECT, criado com ID = "Attribute", permite ao usuário selecionar um atributo, como artista, gênero ou álbum.</span><span class="sxs-lookup"><span data-stu-id="91c48-123">An HTML SELECT element, created with ID = "Attribute", allows the user to select an attribute, such as Artist, Genre, or Album.</span></span> <span data-ttu-id="91c48-124">Um elemento de TEXTAREA HTML, criado com ID = "AttributeVals", exibe o resultado.</span><span class="sxs-lookup"><span data-stu-id="91c48-124">An HTML TEXTAREA element, created with ID = "AttributeVals", displays the result.</span></span> <span data-ttu-id="91c48-125">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="91c48-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="91c48-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91c48-126">Requirements</span></span>



| <span data-ttu-id="91c48-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c48-127">Requirement</span></span> | <span data-ttu-id="91c48-128">Valor</span><span class="sxs-lookup"><span data-stu-id="91c48-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91c48-129">Versão</span><span class="sxs-lookup"><span data-stu-id="91c48-129">Version</span></span><br/> | <span data-ttu-id="91c48-130">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="91c48-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="91c48-131">DLL</span><span class="sxs-lookup"><span data-stu-id="91c48-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="91c48-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c48-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c48-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="91c48-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c48-134">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="91c48-134">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="91c48-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="91c48-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="91c48-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="91c48-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="91c48-137">**Objeto StringCollection**</span><span class="sxs-lookup"><span data-stu-id="91c48-137">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





