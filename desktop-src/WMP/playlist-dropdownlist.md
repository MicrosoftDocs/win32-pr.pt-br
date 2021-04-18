---
title: PLAYLIST. dropDownList
description: O atributo dropDownList especifica ou recupera um valor que indica quais elementos aparecem na caixa de listagem suspensa para uma determinada instância do elemento PLAYLIST.
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- Windows Media Player de PLAYLIST. dropDownList
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771580"
---
# <a name="playlistdropdownlist"></a><span data-ttu-id="41cc7-104">PLAYLIST. dropDownList</span><span class="sxs-lookup"><span data-stu-id="41cc7-104">PLAYLIST.dropDownList</span></span>

<span data-ttu-id="41cc7-105">O atributo **dropDownList** especifica ou recupera um valor que indica quais elementos aparecem na caixa de listagem suspensa para uma determinada instância do elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="41cc7-105">The **dropDownList** attribute specifies or retrieves a value indicating which elements show up in the drop-down list box for a given instance of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a><span data-ttu-id="41cc7-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="41cc7-106">Possible Values</span></span>

<span data-ttu-id="41cc7-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="41cc7-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="41cc7-108">Valor</span><span class="sxs-lookup"><span data-stu-id="41cc7-108">Value</span></span>       | <span data-ttu-id="41cc7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="41cc7-109">Description</span></span>                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41cc7-110">conálbums</span><span class="sxs-lookup"><span data-stu-id="41cc7-110">showAlbums</span></span>  | <span data-ttu-id="41cc7-111">Mostra álbuns.</span><span class="sxs-lookup"><span data-stu-id="41cc7-111">Shows albums.</span></span>                                                                                    |
| <span data-ttu-id="41cc7-112">showAll</span><span class="sxs-lookup"><span data-stu-id="41cc7-112">showAll</span></span>     | <span data-ttu-id="41cc7-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="41cc7-113">Default.</span></span> <span data-ttu-id="41cc7-114">Mostra todos os elementos disponíveis, incluindo listas de reprodução de CD, listas de reprodução de usuários e predefinições de rádio.</span><span class="sxs-lookup"><span data-stu-id="41cc7-114">Shows all available elements including CD playlists, user playlists, and radio presets.</span></span> |
| <span data-ttu-id="41cc7-115">showCD</span><span class="sxs-lookup"><span data-stu-id="41cc7-115">showCD</span></span>      | <span data-ttu-id="41cc7-116">Mostra a lista de reprodução de CD.</span><span class="sxs-lookup"><span data-stu-id="41cc7-116">Shows the CD playlist.</span></span>                                                                           |
| <span data-ttu-id="41cc7-117">exclipes</span><span class="sxs-lookup"><span data-stu-id="41cc7-117">showClips</span></span>   | <span data-ttu-id="41cc7-118">Mostra todos os clipes.</span><span class="sxs-lookup"><span data-stu-id="41cc7-118">Shows all clips.</span></span>                                                                                 |
| <span data-ttu-id="41cc7-119">Atual</span><span class="sxs-lookup"><span data-stu-id="41cc7-119">showCurrent</span></span> | <span data-ttu-id="41cc7-120">Mostra a lista de reprodução atual e não salva.</span><span class="sxs-lookup"><span data-stu-id="41cc7-120">Shows the current, unsaved playlist.</span></span>                                                             |
| <span data-ttu-id="41cc7-121">obter biblioteca</span><span class="sxs-lookup"><span data-stu-id="41cc7-121">showLibrary</span></span> | <span data-ttu-id="41cc7-122">Mostra somente listas de reprodução de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="41cc7-122">Shows only library playlists.</span></span>                                                                    |
| <span data-ttu-id="41cc7-123">Opção de</span><span class="sxs-lookup"><span data-stu-id="41cc7-123">showRadio</span></span>   | <span data-ttu-id="41cc7-124">Mostra as predefinições de rádio.</span><span class="sxs-lookup"><span data-stu-id="41cc7-124">Shows radio presets.</span></span>                                                                             |
| <span data-ttu-id="41cc7-125">todas as consultas</span><span class="sxs-lookup"><span data-stu-id="41cc7-125">showQueries</span></span> | <span data-ttu-id="41cc7-126">Mostra consultas.</span><span class="sxs-lookup"><span data-stu-id="41cc7-126">Shows queries.</span></span>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="41cc7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41cc7-127">Requirements</span></span>



| <span data-ttu-id="41cc7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="41cc7-128">Requirement</span></span> | <span data-ttu-id="41cc7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="41cc7-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="41cc7-130">Versão</span><span class="sxs-lookup"><span data-stu-id="41cc7-130">Version</span></span><br/> | <span data-ttu-id="41cc7-131">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="41cc7-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41cc7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="41cc7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cc7-133">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="41cc7-133">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





