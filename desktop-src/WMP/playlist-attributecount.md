---
title: Playlist. attributeCount
description: A propriedade attributeCount recupera o número de atributos associados à playlist.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Playlist. attributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782600"
---
# <a name="playlistattributecount"></a><span data-ttu-id="47716-104">Playlist. attributeCount</span><span class="sxs-lookup"><span data-stu-id="47716-104">Playlist.attributeCount</span></span>

<span data-ttu-id="47716-105">A propriedade **attributeCount** recupera o número de atributos associados à playlist.</span><span class="sxs-lookup"><span data-stu-id="47716-105">The **attributeCount** property retrieves the number of attributes associated with the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="47716-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="47716-106">Syntax</span></span>

<span data-ttu-id="47716-107">*Player*. *currentPlaylist*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="47716-107">*player*.*currentPlaylist*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="47716-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="47716-108">Possible Values</span></span>

<span data-ttu-id="47716-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="47716-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="47716-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="47716-110">Remarks</span></span>

<span data-ttu-id="47716-111">Como as listas de reprodução podem vir de várias fontes diferentes, elas podem ter vários conjuntos diferentes de propriedades.</span><span class="sxs-lookup"><span data-stu-id="47716-111">Because playlists can come from many different sources, they can have several different sets of properties.</span></span> <span data-ttu-id="47716-112">Esse método recupera o número total de propriedades disponíveis para que os outros métodos do objeto **playlist** possam acessá-las.</span><span class="sxs-lookup"><span data-stu-id="47716-112">This method retrieves the total number of properties available so that the other methods of the **Playlist** object can access them.</span></span>

<span data-ttu-id="47716-113">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="47716-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="47716-114">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="47716-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="47716-115">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="47716-115">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47716-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47716-116">Examples</span></span>

<span data-ttu-id="47716-117">O exemplo de JScript a seguir ilustra como várias propriedades e métodos da **playlist** e dos objetos de **mídia** são usados.</span><span class="sxs-lookup"><span data-stu-id="47716-117">The following JScript example illustrates how various properties and methods of the **Playlist** and **Media** objects are used.</span></span>


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a><span data-ttu-id="47716-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47716-118">Requirements</span></span>



| <span data-ttu-id="47716-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="47716-119">Requirement</span></span> | <span data-ttu-id="47716-120">Valor</span><span class="sxs-lookup"><span data-stu-id="47716-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47716-121">Versão</span><span class="sxs-lookup"><span data-stu-id="47716-121">Version</span></span><br/> | <span data-ttu-id="47716-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="47716-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="47716-123">DLL</span><span class="sxs-lookup"><span data-stu-id="47716-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="47716-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47716-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47716-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="47716-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47716-126">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="47716-126">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="47716-127">**Playlist. attributeName**</span><span class="sxs-lookup"><span data-stu-id="47716-127">**Playlist.attributeName**</span></span>](playlist-attributename.md)
</dt> <dt>

[<span data-ttu-id="47716-128">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="47716-128">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="47716-129">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="47716-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="47716-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="47716-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="47716-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="47716-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





