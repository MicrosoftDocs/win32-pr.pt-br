---
title: Método mediacollection. getByAttribute
description: O método getByAttribute recupera uma lista de reprodução de itens de mídia que contêm um valor especificado para um atributo especificado.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- método getByAttribute Windows Media Player
- método getByAttribute Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796408"
---
# <a name="mediacollectiongetbyattribute-method"></a><span data-ttu-id="5e178-106">Método mediacollection. getByAttribute</span><span class="sxs-lookup"><span data-stu-id="5e178-106">MediaCollection.getByAttribute method</span></span>

<span data-ttu-id="5e178-107">O método **getByAttribute** recupera uma lista de reprodução de itens de mídia que contêm um valor especificado para um atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="5e178-107">The **getByAttribute** method retrieves a playlist of media items that contain a specified value for a specified attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e178-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e178-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="5e178-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e178-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e178-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e178-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e178-111">**Cadeia de caracteres** que indica o nome do atributo a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="5e178-111">**String** indicating the name of the attribute to search.</span></span> <span data-ttu-id="5e178-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5e178-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e178-113">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5e178-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e178-114">**Cadeia de caracteres** que indica o valor que o atributo deve ter.</span><span class="sxs-lookup"><span data-stu-id="5e178-114">**String** indicating the value that the attribute should have.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e178-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e178-115">Return value</span></span>

<span data-ttu-id="5e178-116">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="5e178-116">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e178-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e178-117">Remarks</span></span>

<span data-ttu-id="5e178-118">Esse método pode ser usado para criar uma consulta genérica para itens de mídia que correspondem a um valor para um atributo no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5e178-118">This method can be used to create a generic query for media items that match a value for an attribute in the database.</span></span> <span data-ttu-id="5e178-119">Isso é útil no caso de atributos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5e178-119">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="5e178-120">Se o atributo não existir, será resultado um erro.</span><span class="sxs-lookup"><span data-stu-id="5e178-120">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="5e178-121">Você pode usar esse método para recuperar todos os itens de mídia de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="5e178-121">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="5e178-122">Use o nome de atributo "MediaType" e um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5e178-122">Use the attribute name "MediaType" and one of the following values:</span></span>



| <span data-ttu-id="5e178-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5e178-123">Value</span></span>    | <span data-ttu-id="5e178-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e178-124">Description</span></span>                                                |
|----------|------------------------------------------------------------|
| <span data-ttu-id="5e178-125">áudio</span><span class="sxs-lookup"><span data-stu-id="5e178-125">audio</span></span>    | <span data-ttu-id="5e178-126">Músicas e outros itens somente de áudio.</span><span class="sxs-lookup"><span data-stu-id="5e178-126">Music and other audio-only items.</span></span>                          |
| <span data-ttu-id="5e178-127">playlist</span><span class="sxs-lookup"><span data-stu-id="5e178-127">playlist</span></span> | <span data-ttu-id="5e178-128">Listas de reprodução representadas como objetos de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="5e178-128">Playlists represented as **Media** objects.</span></span>                |
| <span data-ttu-id="5e178-129">radio</span><span class="sxs-lookup"><span data-stu-id="5e178-129">radio</span></span>    | <span data-ttu-id="5e178-130">Itens da estação de rádio.</span><span class="sxs-lookup"><span data-stu-id="5e178-130">Radio station items.</span></span> <span data-ttu-id="5e178-131">Não usado pelo Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="5e178-131">Not used by Windows Media Player 10.</span></span>  |
| <span data-ttu-id="5e178-132">video</span><span class="sxs-lookup"><span data-stu-id="5e178-132">video</span></span>    | <span data-ttu-id="5e178-133">Itens de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e178-133">Video items.</span></span>                                               |
| <span data-ttu-id="5e178-134">foto</span><span class="sxs-lookup"><span data-stu-id="5e178-134">photo</span></span>    | <span data-ttu-id="5e178-135">Itens de foto.</span><span class="sxs-lookup"><span data-stu-id="5e178-135">Photo items.</span></span> <span data-ttu-id="5e178-136">Requer o Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="5e178-136">Requires Windows Media Player 10.</span></span>             |
| <span data-ttu-id="5e178-137">outros</span><span class="sxs-lookup"><span data-stu-id="5e178-137">other</span></span>    | <span data-ttu-id="5e178-138">Outros itens, como arquivos ASF ou URLs para streaming de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e178-138">Other items, such as ASF files or URLs to streaming media.</span></span> |



 

<span data-ttu-id="5e178-139">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5e178-139">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5e178-140">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5e178-140">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5e178-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5e178-141">Examples</span></span>

<span data-ttu-id="5e178-142">O exemplo de JScript a seguir usa *mediacollection*. **getByAttribute** para reproduzir todo o conteúdo da biblioteca pelo artista chamado Triode 48.</span><span class="sxs-lookup"><span data-stu-id="5e178-142">The following JScript example uses *MediaCollection*.**getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="5e178-143">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5e178-143">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="5e178-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e178-144">Requirements</span></span>



| <span data-ttu-id="5e178-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e178-145">Requirement</span></span> | <span data-ttu-id="5e178-146">Valor</span><span class="sxs-lookup"><span data-stu-id="5e178-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e178-147">Versão</span><span class="sxs-lookup"><span data-stu-id="5e178-147">Version</span></span><br/> | <span data-ttu-id="5e178-148">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5e178-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5e178-149">DLL</span><span class="sxs-lookup"><span data-stu-id="5e178-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="5e178-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e178-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e178-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e178-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e178-152">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="5e178-152">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="5e178-153">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="5e178-153">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5e178-154">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5e178-154">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5e178-155">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5e178-155">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





