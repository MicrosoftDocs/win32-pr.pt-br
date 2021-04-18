---
title: Método mediacollection. getMediaAtom
description: O método getMediaAtom recupera o índice no qual um atributo especificado reside dentro do conjunto de atributos disponíveis.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- método getMediaAtom Windows Media Player
- método getMediaAtom Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788151"
---
# <a name="mediacollectiongetmediaatom-method"></a><span data-ttu-id="a0710-106">Método mediacollection. getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="a0710-106">MediaCollection.getMediaAtom method</span></span>

<span data-ttu-id="a0710-107">O método **getMediaAtom** recupera o índice no qual um atributo especificado reside dentro do conjunto de atributos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a0710-107">The **getMediaAtom** method retrieves the index at which a specified attribute resides within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0710-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0710-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="a0710-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0710-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0710-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0710-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0710-111">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="a0710-111">**String** containing the attribute name.</span></span> <span data-ttu-id="a0710-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a0710-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0710-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0710-113">Return value</span></span>

<span data-ttu-id="a0710-114">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="a0710-114">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0710-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0710-115">Remarks</span></span>

<span data-ttu-id="a0710-116">O número de índice recuperado com esse método pode ser passado para a *mídia*. método **getItemInfoByAtom** para acessar valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="a0710-116">The index number retrieved with this method can be passed to the *Media*.**getItemInfoByAtom** method to access attribute values.</span></span> <span data-ttu-id="a0710-117">Essa técnica é geralmente mais eficiente ao trabalhar com listas de reprodução grandes do que acessar um valor de atributo por nome por meio de *mídia*. **getItemInfo** ou *mídia*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="a0710-117">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span>

<span data-ttu-id="a0710-118">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a0710-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a0710-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a0710-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0710-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0710-120">Requirements</span></span>



| <span data-ttu-id="a0710-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0710-121">Requirement</span></span> | <span data-ttu-id="a0710-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a0710-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a0710-123">Versão</span><span class="sxs-lookup"><span data-stu-id="a0710-123">Version</span></span><br/> | <span data-ttu-id="a0710-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a0710-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a0710-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a0710-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a0710-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0710-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0710-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0710-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0710-128">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="a0710-128">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a0710-129">**Media. getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="a0710-129">**Media.getItemInfoByAtom**</span></span>](media-getiteminfobyatom.md)
</dt> <dt>

[<span data-ttu-id="a0710-130">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="a0710-130">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="a0710-131">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="a0710-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a0710-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a0710-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a0710-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a0710-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





