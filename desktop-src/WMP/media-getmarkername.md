---
title: Método Media. GetMarkerName
description: O método getmarcadorname recupera o nome do marcador no índice especificado.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- método GetMarkerName do Windows Media Player
- método getmarcadorname do Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getmarcadorname
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763842"
---
# <a name="mediagetmarkername-method"></a><span data-ttu-id="257ab-106">Método Media. GetMarkerName</span><span class="sxs-lookup"><span data-stu-id="257ab-106">Media.getMarkerName method</span></span>

<span data-ttu-id="257ab-107">O método **Getmarcadorname** recupera o nome do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="257ab-107">The **getMarkerName** method retrieves the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="257ab-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="257ab-108">Syntax</span></span>


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="257ab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="257ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="257ab-110">*markerNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="257ab-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="257ab-111">**Número** (**longo**) que especifica um índice de marcador.</span><span class="sxs-lookup"><span data-stu-id="257ab-111">**Number** (**long**) specifying a marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="257ab-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="257ab-112">Return value</span></span>

<span data-ttu-id="257ab-113">Esse método retorna uma **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="257ab-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="257ab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="257ab-114">Remarks</span></span>

<span data-ttu-id="257ab-115">Esse método retornará **NULL** se o marcador especificado não existir.</span><span class="sxs-lookup"><span data-stu-id="257ab-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="257ab-116">Alguns itens de mídia digital não contêm marcadores.</span><span class="sxs-lookup"><span data-stu-id="257ab-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="257ab-117">Use **markerCount** para descobrir quantos marcadores estão no clipe atual.</span><span class="sxs-lookup"><span data-stu-id="257ab-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="257ab-118">Os números de índice de marcador começam em 1.</span><span class="sxs-lookup"><span data-stu-id="257ab-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="257ab-119">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="257ab-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="257ab-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="257ab-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="257ab-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="257ab-121">Examples</span></span>

<span data-ttu-id="257ab-122">O exemplo de JScript a seguir usa *mídia*. **Getmarcadorname** para preencher um elemento de TextArea HTML chamado MNAMES com os nomes dos marcadores no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="257ab-122">The following JScript example uses *Media*.**getMarkerName** to fill an HTML TEXTAREA element named MNAMES with the names of the markers in the current media item.</span></span> <span data-ttu-id="257ab-123">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="257ab-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="257ab-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="257ab-124">Requirements</span></span>



| <span data-ttu-id="257ab-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="257ab-125">Requirement</span></span> | <span data-ttu-id="257ab-126">Valor</span><span class="sxs-lookup"><span data-stu-id="257ab-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="257ab-127">Versão</span><span class="sxs-lookup"><span data-stu-id="257ab-127">Version</span></span><br/> | <span data-ttu-id="257ab-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="257ab-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="257ab-129">DLL</span><span class="sxs-lookup"><span data-stu-id="257ab-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="257ab-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="257ab-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="257ab-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="257ab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257ab-132">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="257ab-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="257ab-133">**Media. getmarcadortime**</span><span class="sxs-lookup"><span data-stu-id="257ab-133">**Media.getMarkerTime**</span></span>](media-getmarkertime.md)
</dt> <dt>

[<span data-ttu-id="257ab-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="257ab-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="257ab-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="257ab-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="257ab-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="257ab-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





