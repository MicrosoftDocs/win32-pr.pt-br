---
title: Playlist. attributeName
description: A propriedade attributeName recupera o nome de um atributo em um índice especificado.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Windows Media Player de playlist. attributeName
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784542"
---
# <a name="playlistattributename"></a><span data-ttu-id="b4a07-104">Playlist. attributeName</span><span class="sxs-lookup"><span data-stu-id="b4a07-104">Playlist.attributeName</span></span>

<span data-ttu-id="b4a07-105">A propriedade **AttributeName** recupera o nome de um atributo em um índice especificado.</span><span class="sxs-lookup"><span data-stu-id="b4a07-105">The **attributeName** property retrieves the name of an attribute at a specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a07-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4a07-106">Syntax</span></span>

<span data-ttu-id="b4a07-107">*Player*. *currentPlaylist*. **AttributeName**( *índice* )</span><span class="sxs-lookup"><span data-stu-id="b4a07-107">*player*.*currentPlaylist*.**attributeName**( *index* )</span></span>

## <a name="parameters"></a><span data-ttu-id="b4a07-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4a07-108">Parameters</span></span>

<span data-ttu-id="b4a07-109">*index*</span><span class="sxs-lookup"><span data-stu-id="b4a07-109">*index*</span></span>

<span data-ttu-id="b4a07-110">**Número** (**longo**) que contém o índice.</span><span class="sxs-lookup"><span data-stu-id="b4a07-110">**Number** (**long**) containing the index.</span></span>

## <a name="possible-values"></a><span data-ttu-id="b4a07-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b4a07-111">Possible Values</span></span>

<span data-ttu-id="b4a07-112">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b4a07-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a07-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4a07-113">Remarks</span></span>

<span data-ttu-id="b4a07-114">O número de atributos é recuperado pela propriedade **attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="b4a07-114">The number of attributes is retrieved by the **attributeCount** property.</span></span> <span data-ttu-id="b4a07-115">Dado um índice, **AttributeName** retorna uma **cadeia de caracteres** que pode ser usada em conjunto com **setItemInfo** ou **getItemInfo** para especificar ou recuperar um valor para o atributo.</span><span class="sxs-lookup"><span data-stu-id="b4a07-115">Given an index, **attributeName** returns a **String** that can be used in conjunction with **setItemInfo** or **getItemInfo** to specify or retrieve a value for the attribute.</span></span>

<span data-ttu-id="b4a07-116">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b4a07-116">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="b4a07-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b4a07-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b4a07-118">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b4a07-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="b4a07-119">Consulte a propriedade [attributeCount](playlist-attributecount.md) para obter o código de exemplo que usa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b4a07-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a07-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a07-120">Requirements</span></span>



| <span data-ttu-id="b4a07-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a07-121">Requirement</span></span> | <span data-ttu-id="b4a07-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b4a07-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a07-123">Versão</span><span class="sxs-lookup"><span data-stu-id="b4a07-123">Version</span></span><br/> | <span data-ttu-id="b4a07-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b4a07-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b4a07-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b4a07-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4a07-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4a07-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a07-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4a07-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a07-128">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="b4a07-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="b4a07-129">**Playlist. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="b4a07-129">**Playlist.attributeCount**</span></span>](playlist-attributecount.md)
</dt> <dt>

[<span data-ttu-id="b4a07-130">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b4a07-130">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b4a07-131">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b4a07-131">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b4a07-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b4a07-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b4a07-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b4a07-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





