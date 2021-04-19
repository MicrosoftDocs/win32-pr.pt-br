---
title: Método Media. setItemInfo
description: O método setItemInfo define o valor do atributo especificado para o item de mídia atual.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- método setItemInfo Windows Media Player
- método setItemInfo Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770606"
---
# <a name="mediasetiteminfo-method"></a><span data-ttu-id="b1ed6-106">Método Media. setItemInfo</span><span class="sxs-lookup"><span data-stu-id="b1ed6-106">Media.setItemInfo method</span></span>

<span data-ttu-id="b1ed6-107">O método **setItemInfo** define o valor do atributo especificado para o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-107">The **setItemInfo** method sets the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ed6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1ed6-108">Syntax</span></span>


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="b1ed6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1ed6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ed6-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1ed6-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ed6-111">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-111">**String** containing the attribute name.</span></span> <span data-ttu-id="b1ed6-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ed6-113">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b1ed6-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1ed6-114">**Cadeia de caracteres** que contém o novo valor.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-114">**String** containing the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1ed6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1ed6-115">Return value</span></span>

<span data-ttu-id="b1ed6-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1ed6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1ed6-117">Remarks</span></span>

<span data-ttu-id="b1ed6-118">A propriedade **attributeCount** contém o número de atributos disponíveis para um determinado objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="b1ed6-118">The **attributeCount** property contains the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="b1ed6-119">Os números de índice podem ser usados com o método **GetAttributeName** para determinar os nomes dos atributos internos que podem ser usados com esse método.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-119">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="b1ed6-120">Antes de usar esse método, use o método **isReadOnlyItem** para determinar se um atributo específico pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-120">Before using this method, use the **isReadOnlyItem** method to determine whether a particular attribute can be set.</span></span>

<span data-ttu-id="b1ed6-121">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="b1ed6-122">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b1ed6-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b1ed6-123">**Observação**</span><span class="sxs-lookup"><span data-stu-id="b1ed6-123">**Note**</span></span>

<span data-ttu-id="b1ed6-124">Se você inserir o controle do Windows Media Player em seu aplicativo, os atributos de arquivo alterados não serão gravados no arquivo de mídia digital até que o usuário execute o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-124">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="b1ed6-125">Se você usar o controle em um aplicativo remoto escrito em C++, os atributos de arquivo alterados serão gravados no arquivo de mídia digital logo depois que você fizer as alterações.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-125">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="b1ed6-126">Em ambos os casos, as alterações ficam imediatamente disponíveis para seu código por meio da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-126">In either case, the changes are immediately available to your code through the library.</span></span>

<span data-ttu-id="b1ed6-127">**Windows Media Player 10 Mobile:** Este método não está implementado.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-127">**Windows Media Player 10 Mobile:** This method is not implemented.</span></span>

## <a name="examples"></a><span data-ttu-id="b1ed6-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1ed6-128">Examples</span></span>

<span data-ttu-id="b1ed6-129">O exemplo de JScript a seguir usa *mídia*. **setItemInfo** para alterar o valor do atributo gênero para o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-129">The following JScript example uses *Media*.**setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="b1ed6-130">Um elemento de entrada de texto HTML chamado genText permite que o usuário insira uma cadeia de texto, que é usada para alterar as informações de atributo.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-130">An HTML TEXT input element named genText allows the user to enter a text string, which is then used to change the attribute information.</span></span> <span data-ttu-id="b1ed6-131">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="b1ed6-131">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a><span data-ttu-id="b1ed6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1ed6-132">Requirements</span></span>



| <span data-ttu-id="b1ed6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1ed6-133">Requirement</span></span> | <span data-ttu-id="b1ed6-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b1ed6-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ed6-135">Versão</span><span class="sxs-lookup"><span data-stu-id="b1ed6-135">Version</span></span><br/> | <span data-ttu-id="b1ed6-136">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b1ed6-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b1ed6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ed6-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1ed6-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1ed6-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ed6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1ed6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ed6-140">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="b1ed6-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b1ed6-141">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b1ed6-141">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b1ed6-142">**Media. isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="b1ed6-142">**Media.isReadOnlyItem**</span></span>](media-isreadonlyitem.md)
</dt> <dt>

[<span data-ttu-id="b1ed6-143">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b1ed6-143">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b1ed6-144">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b1ed6-144">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





