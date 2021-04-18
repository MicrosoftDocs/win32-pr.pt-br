---
title: Método Media. isReadOnlyItem
description: O método isReadOnlyItem retorna um valor que indica se o atributo especificado do item de mídia pode ser editado.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- método isReadOnlyItem Windows Media Player
- método isReadOnlyItem Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788888"
---
# <a name="mediaisreadonlyitem-method"></a><span data-ttu-id="a609b-106">Método Media. isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="a609b-106">Media.isReadOnlyItem method</span></span>

<span data-ttu-id="a609b-107">O método **isReadOnlyItem** retorna um valor que indica se o atributo especificado do item de mídia pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="a609b-107">The **isReadOnlyItem** method returns a value indicating whether the specified attribute of the media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="a609b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a609b-108">Syntax</span></span>


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="a609b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a609b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a609b-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a609b-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a609b-111">**Cadeia de caracteres** que indica o nome do atributo a ser testado.</span><span class="sxs-lookup"><span data-stu-id="a609b-111">**String** indicating the name of the attribute to test.</span></span> <span data-ttu-id="a609b-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player..</span><span class="sxs-lookup"><span data-stu-id="a609b-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a609b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a609b-113">Return value</span></span>

<span data-ttu-id="a609b-114">Esse método retorna um **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="a609b-114">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a609b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a609b-115">Remarks</span></span>

<span data-ttu-id="a609b-116">Se um atributo for somente leitura, ele não poderá ser definido com o método **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="a609b-116">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="a609b-117">Observe que esse método pode retornar valores diferentes para um atributo específico quando usado com versões diferentes do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a609b-117">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="a609b-118">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a609b-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a609b-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a609b-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a609b-120">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="a609b-120">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="a609b-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a609b-121">Examples</span></span>

<span data-ttu-id="a609b-122">O exemplo de JScript a seguir usa *mídia*. **isReadOnlyItem** para preencher um elemento de TextArea HTML chamado rwText com informações sobre o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="a609b-122">The following JScript example uses *Media*.**isReadOnlyItem** to fill an HTML TEXTAREA element named rwText with information about the current media item.</span></span> <span data-ttu-id="a609b-123">O código gera cada atributo do item de mídia atual, juntamente com o texto que indica se o atributo é somente leitura ou leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a609b-123">The code outputs each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="a609b-124">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a609b-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="a609b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a609b-125">Requirements</span></span>



| <span data-ttu-id="a609b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a609b-126">Requirement</span></span> | <span data-ttu-id="a609b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a609b-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a609b-128">Versão</span><span class="sxs-lookup"><span data-stu-id="a609b-128">Version</span></span><br/> | <span data-ttu-id="a609b-129">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a609b-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a609b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a609b-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="a609b-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a609b-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a609b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a609b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a609b-133">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="a609b-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="a609b-134">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="a609b-134">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a609b-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a609b-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a609b-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a609b-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





