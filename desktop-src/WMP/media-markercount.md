---
title: Media. markerCount
description: A propriedade markerCount recupera o número de marcadores no item de mídia.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media. markerCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763470"
---
# <a name="mediamarkercount"></a><span data-ttu-id="73f02-104">Media. markerCount</span><span class="sxs-lookup"><span data-stu-id="73f02-104">Media.markerCount</span></span>

<span data-ttu-id="73f02-105">A propriedade **markerCount** recupera o número de marcadores no item de mídia.</span><span class="sxs-lookup"><span data-stu-id="73f02-105">The **markerCount** property retrieves the number of markers in the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f02-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73f02-106">Syntax</span></span>

<span data-ttu-id="73f02-107">*Player*. *currentMedia*. **markerCount**</span><span class="sxs-lookup"><span data-stu-id="73f02-107">*player*.*currentMedia*.**markerCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="73f02-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="73f02-108">Possible Values</span></span>

<span data-ttu-id="73f02-109">Essa propriedade é um **número** somente leitura (**Long**) que especifica o número de marcadores no arquivo.</span><span class="sxs-lookup"><span data-stu-id="73f02-109">This property is a read-only **Number** (**long**) specifying the number of markers in the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="73f02-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="73f02-110">Remarks</span></span>

<span data-ttu-id="73f02-111">Essa propriedade retornará zero se um arquivo não tiver marcadores ou se o item de mídia não for o mesmo que o *Player*. **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="73f02-111">This property returns zero if a file has no markers, or if the media item is not the same as *Player*.**currentMedia**.</span></span>

<span data-ttu-id="73f02-112">Os números de marcador começam em 1.</span><span class="sxs-lookup"><span data-stu-id="73f02-112">Marker numbers start at 1.</span></span>

<span data-ttu-id="73f02-113">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="73f02-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="73f02-114">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="73f02-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="73f02-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73f02-115">Examples</span></span>

<span data-ttu-id="73f02-116">O exemplo de JScript a seguir usa *mídia*. **markerCount** para recuperar o número de marcadores no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="73f02-116">The following JScript example uses *Media*.**markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="73f02-117">Esse valor é usado como o limite superior para uma estrutura de loop, que itera na lista de marcadores para recuperar cada nome de marcador.</span><span class="sxs-lookup"><span data-stu-id="73f02-117">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name.</span></span> <span data-ttu-id="73f02-118">Um elemento de TEXTAREA HTML chamado MNAMES exibe os nomes dos marcadores no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="73f02-118">An HTML TEXTAREA element named MNAMES displays the names of the markers in the current media item.</span></span> <span data-ttu-id="73f02-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="73f02-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="73f02-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73f02-120">Requirements</span></span>



| <span data-ttu-id="73f02-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="73f02-121">Requirement</span></span> | <span data-ttu-id="73f02-122">Valor</span><span class="sxs-lookup"><span data-stu-id="73f02-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73f02-123">Versão</span><span class="sxs-lookup"><span data-stu-id="73f02-123">Version</span></span><br/> | <span data-ttu-id="73f02-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="73f02-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="73f02-125">DLL</span><span class="sxs-lookup"><span data-stu-id="73f02-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="73f02-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73f02-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73f02-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="73f02-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f02-128">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="73f02-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="73f02-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="73f02-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="73f02-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="73f02-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="73f02-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="73f02-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





