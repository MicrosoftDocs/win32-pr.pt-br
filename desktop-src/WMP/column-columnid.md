---
title: COLUNA. columnID
description: O atributo columnID especifica ou recupera uma ID de coluna no controle PLAYLIST.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- COLUNA. columnID Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810572"
---
# <a name="columncolumnid"></a><span data-ttu-id="e0127-104">COLUNA. columnID</span><span class="sxs-lookup"><span data-stu-id="e0127-104">COLUMN.columnID</span></span>

<span data-ttu-id="e0127-105">O atributo **columnid** especifica ou recupera uma ID de coluna no controle **playlist** .</span><span class="sxs-lookup"><span data-stu-id="e0127-105">The **columnID** attribute specifies or retrieves a column ID in the **PLAYLIST** control.</span></span>

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a><span data-ttu-id="e0127-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e0127-106">Possible Values</span></span>

<span data-ttu-id="e0127-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e0127-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0127-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0127-108">Remarks</span></span>

<span data-ttu-id="e0127-109">Os valores de **columnid** são os mesmos valores usados com o método **getItemInfo** em um objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="e0127-109">The **columnID** values are the same values used with the **getItemInfo** method on a **Media** object.</span></span> <span data-ttu-id="e0127-110">Uma lista pode ser obtida usando a *mídia*. Propriedade **attributeCount** para determinar o número de atributos disponíveis para um determinado objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="e0127-110">A list can be obtained by using the *Media*.**attributeCount** property to determine the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="e0127-111">Os números de índice podem ser usados com a *mídia*. método **GetAttributeName** para determinar os nomes dos atributos que, por sua vez, podem ser passados para a *mídia*. **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="e0127-111">Index numbers can then be used with the *Media*.**getAttributeName** method to determine the names of the attributes, which can in turn be passed to *Media*.**getItemInfo**.</span></span> <span data-ttu-id="e0127-112">A propriedade **columnid** só pode ser definida com esses valores, com exceção de alguns valores que podem não ser retornados pela *mídia*. **GetAttributeName**.</span><span class="sxs-lookup"><span data-stu-id="e0127-112">The **columnID** property can only be set to these values, with the exception of some values that may not be returned by *Media*.**getAttributeName**.</span></span> <span data-ttu-id="e0127-113">Esses valores estão listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="e0127-113">These values are listed below.</span></span>



| <span data-ttu-id="e0127-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e0127-114">Value</span></span>     | <span data-ttu-id="e0127-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0127-115">Description</span></span>                                                                        |
|-----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0127-116">name</span><span class="sxs-lookup"><span data-stu-id="e0127-116">name</span></span>      | <span data-ttu-id="e0127-117">Exibe o nome do objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="e0127-117">Displays the name of the **Media** object.</span></span>                                         |
| <span data-ttu-id="e0127-118">duration</span><span class="sxs-lookup"><span data-stu-id="e0127-118">duration</span></span>  | <span data-ttu-id="e0127-119">Exibe a duração do objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="e0127-119">Displays the duration of the **Media** object.</span></span>                                     |
| <span data-ttu-id="e0127-120">sourceURL</span><span class="sxs-lookup"><span data-stu-id="e0127-120">sourceURL</span></span> | <span data-ttu-id="e0127-121">Exibe a URL do objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="e0127-121">Displays the URL of the **Media** object.</span></span>                                          |
| <span data-ttu-id="e0127-122">status</span><span class="sxs-lookup"><span data-stu-id="e0127-122">status</span></span>    | <span data-ttu-id="e0127-123">Exibe o status da cópia de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e0127-123">Displays the status of copying files.</span></span>                                              |
| <span data-ttu-id="e0127-124">tamanho</span><span class="sxs-lookup"><span data-stu-id="e0127-124">size</span></span>      | <span data-ttu-id="e0127-125">Exibe o tamanho do arquivo que o objeto de **mídia** representa.</span><span class="sxs-lookup"><span data-stu-id="e0127-125">Displays the size of the file that the **Media** object represents.</span></span>                |
| <span data-ttu-id="e0127-126">extensão</span><span class="sxs-lookup"><span data-stu-id="e0127-126">extension</span></span> | <span data-ttu-id="e0127-127">Exibe a extensão de nome de arquivo do arquivo que o objeto de **mídia** representa.</span><span class="sxs-lookup"><span data-stu-id="e0127-127">Displays the file name extension of the file that the **Media** object represents.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e0127-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0127-128">Requirements</span></span>



| <span data-ttu-id="e0127-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0127-129">Requirement</span></span> | <span data-ttu-id="e0127-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e0127-130">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e0127-131">Versão</span><span class="sxs-lookup"><span data-stu-id="e0127-131">Version</span></span><br/> | <span data-ttu-id="e0127-132">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="e0127-132">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0127-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0127-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0127-134">**Elemento COLUMN**</span><span class="sxs-lookup"><span data-stu-id="e0127-134">**COLUMN Element**</span></span>](column-element.md)
</dt> <dt>

[<span data-ttu-id="e0127-135">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="e0127-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e0127-136">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="e0127-136">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="e0127-137">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="e0127-137">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="e0127-138">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="e0127-138">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> </dl>

 

 





